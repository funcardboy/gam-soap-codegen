# AdRuleService Cheatsheet

## Methods

### createAdRules
Creates new [AdRule](/ad-manager/api/reference/v202608/AdRuleService.AdRule) objects.

### createAdSpots
Creates new [AdSpot](/ad-manager/api/reference/v202608/AdRuleService.AdSpot) objects.

### createBreakTemplates
Creates new `breakTemplate` objects.

### getAdRulesByStatement
Gets an [AdRulePage](/ad-manager/api/reference/v202608/AdRuleService.AdRulePage) of [AdRule](/ad-manager/api/reference/v202608/AdRuleService.AdRule) objects that satisfy the given
[Statement.query](/ad-manager/api/reference/v202608/AdRuleService.Statement#query). The following fields are supported for
filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [AdRule.id](/ad-manager/api/reference/v202608/AdRuleService.AdRule#id) ([AdRule.adRuleId](/ad-manager/api/reference/v202608/AdRuleService.AdRule#adRuleId) beginning in v201702) |
| `name` | [AdRule.name](/ad-manager/api/reference/v202608/AdRuleService.AdRule#name) |
| `priority` | [AdRule.priority](/ad-manager/api/reference/v202608/AdRuleService.AdRule#priority) |
| `status` | [AdRule.status](/ad-manager/api/reference/v202608/AdRuleService.AdRule#status) |

### getAdSpotsByStatement
Gets a [AdSpotPage](/ad-manager/api/reference/v202608/AdRuleService.AdSpotPage) of [AdSpot](/ad-manager/api/reference/v202608/AdRuleService.AdSpot) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/AdRuleService.Statement#query).

### getBreakTemplatesByStatement
Gets a [BreakTemplatePage](/ad-manager/api/reference/v202608/AdRuleService.BreakTemplatePage) of [BreakTemplate](/ad-manager/api/reference/v202608/AdRuleService.BreakTemplate) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/AdRuleService.Statement#query).

### performAdRuleAction
Performs actions on [AdRule](/ad-manager/api/reference/v202608/AdRuleService.AdRule) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/AdRuleService.Statement#query).

### updateAdRules
Updates the specified [AdRule](/ad-manager/api/reference/v202608/AdRuleService.AdRule) objects.

### updateAdSpots
Updates the specified [AdSpot](/ad-manager/api/reference/v202608/AdRuleService.AdSpot) objects.

### updateBreakTemplates
Updates the specified `breakTemplate` objects.
