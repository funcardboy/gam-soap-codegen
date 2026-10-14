---
name: gam-soap-codegen
description: "Use when writing GAM SOAP API v202608 Python code."
version: 1.0.0
author: sam
license: MIT
metadata:
  hermes:
    tags: [gam, soap-api, codegen, googleads, v202608]
    related_skills: [gam-api-reference]
---

# GAM SOAP API v202608 — Python Codegen

## Overview

Grounded code generation for the Google Ad Manager SOAP API (v202608) using the
`googleads` Python library. Backed by two local corpora:

- **Scrapped official reference** (every type/method page under
  `developers.google.com/ad-manager/api/reference/v202608/`):
  `~/Projects/gam-api/data/v202608/docs/*.md` + `index.json`
- **Official example scripts** (Apache-2.0, vendored):
  `~/Projects/gam-api/data/v202608/examples/<service>/...`

Distilled quick references live in this skill: `references/services/<Service>.md`
(method tables + type lists) and `references/examples-index.md` (task → example path).

For older-version doc searches (v202602, ChromaDB RAG) use the sibling skill
`gam-api-reference`. If the user's code pins a different version than v202608,
say so explicitly — field sets change between versions.

## Regenerating service cheatsheets

The `references/services/<Service>.md` files are generated from the raw docs. To regenerate when docs change:

```bash
python3 ~/Projects/gam-api/scripts/build_service_cheatsheets.py
```

This reads `data/v202608/docs/*.md` and extracts:
- Service overview + method signatures
- All type definitions with field tables (name, type, description only — no narrative)

The output is compact: each service file contains everything needed for codegen without requiring agents to grep through 1999 individual markdown files.

**Design principle**: Keep service cheatsheets per-service (31 files), not merged into one monolithic file. This balances completeness (all types included) with token efficiency (agents load only the service they need).

## Codegen workflow (follow in order)

1. **Identify the service + operation** (e.g. "create VAST creative" → CreativeService.createCreatives).
2. **Load the cheatsheet**: `skill_view(name='gam-soap-codegen', file_path='references/services/CreativeService.md')`.
3. **Get exact field names/types** — never invent fields. If the cheatsheet is not enough:
   ```bash
   grep -ril "VastRedirectCreative" ~/Projects/gam-api/data/v202608/docs | head
   read_file <matched doc>        # full field table incl. required/read-only flags
   ```
4. **Find a matching official example**: check `references/examples-index.md`, then read the example file. Adapt it; don't rewrite from scratch.
5. **Emit code** using the standard client bootstrap (below), with required fields
   marked, read-only fields omitted, and enums quoted exactly as in the docs.

## Standard client bootstrap

```python
from googleads import ad_manager

client = ad_manager.AdManagerClient.LoadFromStorage()  # ~/googleads.yaml
client.api_version = "v202608"  # only if not the library default
service = client.GetService("CreativeService")
```

`~/googleads.yaml` (OAuth2 service-account or refresh-token flow):

```yaml
ad_manager:
  application_name: sam-gam-tools
  network_code: "<Sam's network code>"
  path_to_private_key_file: <service account json>   # OR:
  # refresh_token: <oauth refresh token>
  # client_id: ...
  # client_secret: ...
```

Install: `pip install googleads`. Never print/commit credentials.

## Query patterns

- **get*ByStatement** (SOAP filter):
  ```python
  stmt = {"query": "WHERE name LIKE 'test%' ORDER BY id LIMIT 500"}
  resp = service.getCreativesByStatement(stmt)
  results = resp.get("results", [])
  ```
- **PQL** (reporting/ad-hoc, via PublisherQueryLanguageService): see
  `references/examples-index.md` → `publisher_query_language_service/`.
- **Reports**: runReportJob → poll getReportJobStatus == 'COMPLETED' →
  getReportDownloadUrlWithOptions → download CSV. Example in `report_service/`.

## Pitfalls

1. **Required vs read-only**: docs mark fields like `id` read-only-on-create and
   `advertiserId` required. Sending read-only fields on create → SOAP ApiError.
   Always check the field table in `data/v202608/docs/<Type>.md` first.
2. **Enum strings are exact** — e.g. `vastRedirectType: 'LINEAR'`, not `'linear'`.
3. **Version drift**: `LoadFromStorage()` defaults to the library's newest version;
   pin `v202608` explicitly in generated code.
4. **Dates are dicts**: `{'date': {'year': 2026, 'month': 10, 'day': 14}}`, and
   DateTime adds `'hour'/'minute'/'second'` + `'timeZoneId': 'Asia/Hong_Kong'`.
5. **Statement LIMIT max is 500** — page with OFFSET/`startIndex` for more.
6. **Sandbox first**: for mutating calls (create/update/perform*Action), suggest a
   dry-run against a test network; `perform*Action` needs the action dict with
   `xsi_type` (e.g. `{'xsi_type': 'PauseLineItems'}`).
7. Don't confuse with Google Ads API — this is Ad Manager (DFP), `googleads.ad_manager`.

## Verification checklist (before handing code to Sam)

- [ ] Every field name grep-verified against `data/v202608/docs/`
- [ ] Code matches an official example's structure (cite the example path)
- [ ] `python3 -m py_compile <generated file>` passes
- [ ] Mutating operations flagged + rollback action noted (e.g. perform*Action can pause/archive)
