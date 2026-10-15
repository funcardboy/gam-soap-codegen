# GAM SOAP API Codegen Skill (v3.1.0)

A Hermes / AI Agent skill for translating natural language data requests into working Google Ad Manager (GAM) SOAP API `v202608` Python code (`googleads` library) — complete with **43 Service Reference Cheatsheets**, **Enumerations**, **PQL Table Schemas**, and **162 Official Examples**.

## 中文說明

### 這是什麼？

這是一個專為「用自然語言拎 GAM Data（Data Extraction & Automation）」而設計的 AI Agent Skill，包含：

- **完整 43 個 Service 參考文件（`references/services/*.md`）**：涵蓋 `v202608` 全部 43 個 Services（包括 `LineItemService`、`OrderService`、`ReportService`、`PublisherQueryLanguageService`、`InventoryService`、`PlacementService`、`ForecastService`、`AdjustmentService`、`ProposalService`、`UserService`、`YieldGroupService` 等），每個檔案均包含：
  - **Methods**：方法簽名、Request 參數與 Response 型別
  - **Types**：完整資料結構與欄位定義（已過濾無用嘅 `*Error` / `*Exception` 雜訊，大幅節省 Context Token）
  - **Enumerations**：所有合法 Enum 字串值（如 `LineItemType`、`ComputedStatus`、`Dimension`、`Column`）
- **162 個官方 Python 範例索引（`references/examples-index.md`）**：按 Service 分類嘅範例對照表
- **三大標準拎數模板（載於 `SKILL.md`）**：
  1. **Template A (`get*ByStatement`)**：拉取 Entity 設定與即時狀態（內置安全解包 `DateTime`、`Money.microAmount`、自動翻頁）
  2. **Template B (`ReportService` + `DataDownloader.WaitForReport`)**：拉取跨維度報表並自動處理 binary gzip CSV 解壓轉 `pandas.DataFrame`
  3. **Template C (`PublisherQueryLanguageService.select`)**：查詢 PQL 系統對照表（如 `Geo_Target`、`Browser`、`Device_Category`）

### 檔案結構

```
gam-soap-codegen/
├── SKILL.md                        # Skill 核心路由、3 大 Code Templates 與防呆規則 (v3.1.0)
├── README.md                       # 說明文件（中英對照）
├── scripts/
│   └── build_service_cheatsheets.py # 從 GAM v202608 官方文檔生成全部 43 個 Service Cheatsheets 的腳本
└── references/
    ├── examples-index.md           # 162 個官方 Python 範例索引
    ├── examples/                   # 官方 Python 範例程式碼
    └── services/                   # 完整 43 個 GAM v202608 Service 參考文件
        ├── AdjustmentService.md
        ├── AdRuleService.md
        ├── CreativeService.md
        ├── ForecastService.md
        ├── InventoryService.md
        ├── LineItemService.md
        ├── OrderService.md
        ├── PlacementService.md
        ├── ProposalLineItemService.md
        ├── ProposalService.md
        ├── PublisherQueryLanguageService.md
        ├── ReportService.md
        ├── UserService.md
        ├── YieldGroupService.md
        └── ... (共 43 個 Services)
```

### API 版本

- **Version**: `v202608`
- **Reference Source**: https://developers.google.com/ad-manager/api/reference/v202608/
- **Updated**: 2026-10-15 (v3.1.0)

## English

### What is this?

An AI Agent skill that translates plain-language data requests into production-ready Google Ad Manager (GAM) SOAP API `v202608` Python code using `googleads.ad_manager`:

- **All 43 Service Reference Cheatsheets (`references/services/*.md`)**: Methods, clean non-error Types, and Enumerations for every service in GAM `v202608`.
- **3-Way Data Extraction Routing (`SKILL.md`)**: Automatically routes requests between `*Service.get*ByStatement`, `ReportService` (`DataDownloader.WaitForReport`), and `PublisherQueryLanguageService.select` (`StatementBuilder`), always outputting a clean `pandas.DataFrame`.
- **162 Official Python Examples (`references/examples-index.md`)**: Indexed by service for rapid adaptation.
