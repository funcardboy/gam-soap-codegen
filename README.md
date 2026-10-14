# GAM SOAP API Codegen Skill

A Hermes skill for generating Google Ad Manager (GAM) SOAP API v202608 Python code — service references, type definitions, and 162 official examples.

---

## 中文說明

### 這是什麼？

這是一個給 AI Agent 使用的 Hermes Skill，包含：

- **31 個 Service 參考文件**：每個 service 的方法（methods）、型別（types）、欄位定義（fields）
- **162 個官方 Python 範例**：可直接使用的程式碼範例

### 如何使用？

#### 方法 1：Hermes Agent 載入 Skill

```python
# 在 Hermes agent 中載入 skill
from hermes_tools import skill_view

# 載入特定 service 的參考
creative_ref = skill_view(name='gam-soap-codegen', file_path='references/services/CreativeService.md')

# 瀏覽範例索引
examples = skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')
```

#### 方法 2：直接 Clone Repo

```bash
git clone https://github.com/funcardboy/gam-soap-codegen.git
cd gam-soap-codegen

# 查看 service 參考
cat references/services/LineItemService.md

# 查看範例
cat references/examples/line_item_service/create_line_items.py
```

### 檔案結構

```
gam-soap-codegen/
├── SKILL.md                        # Skill 定義檔
├── README.md                       # 本說明文件
└── references/
    ├── examples-index.md           # 162 個範例的索引
    ├── examples/                   # Python 範例程式碼
    │   ├── adjustment_service/
    │   ├── creative_service/
    │   ├── line_item_service/
    │   └── ... (31 個 service)
    └── services/                   # Service 參考文件
        ├── CreativeService.md
        ├── LineItemService.md
        ├── OrderService.md
        └── ... (31 個 service)
```

### API 版本

- **Version**: v202608
- **Source**: https://developers.google.com/ad-manager/api/reference/v202608/
- **Generated**: 2026-10-14

---

## English

### What is this?

A Hermes skill for AI agents containing:

- **31 Service reference files**: Methods, types, and field definitions for each service
- **162 official Python examples**: Ready-to-use code samples

### How to use?

#### Method 1: Load as Hermes Skill

```python
# In Hermes agent, load the skill
from hermes_tools import skill_view

# Load specific service reference
creative_ref = skill_view(name='gam-soap-codegen', file_path='references/services/CreativeService.md')

# Browse examples index
examples = skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')
```

#### Method 2: Clone the Repo

```bash
git clone https://github.com/funcardboy/gam-soap-codegen.git
cd gam-soap-codegen

# Check service reference
cat references/services/LineItemService.md

# Check examples
cat references/examples/line_item_service/create_line_items.py
```

### File structure

```
gam-soap-codegen/
├── SKILL.md                        # Skill definition
├── README.md                       # This file
└── references/
    ├── examples-index.md           # Index of 162 examples
    ├── examples/                   # Python example code
    │   ├── adjustment_service/
    │   ├── creative_service/
    │   ├── line_item_service/
    │   └── ... (31 services)
    └── services/                   # Service reference files
        ├── CreativeService.md
        ├── LineItemService.md
        ├── OrderService.md
        └── ... (31 services)
```

### API version

- **Version**: v202608
- **Source**: https://developers.google.com/ad-manager/api/reference/v202608/
- **Generated**: 2026-10-14
