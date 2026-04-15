<div align="center">

<br/>

<h1>R E V S Y N C &nbsp; R C M</h1>
<sub>— &nbsp; E N G I N E &nbsp; —</sub>

<br/>

**Enterprise Revenue Cycle Intelligence · Dynamic Array Engineering · Zero-Touch Workflow Triage**

<br/>

![Status](https://img.shields.io/badge/STATUS-PRODUCTION_READY-217346?style=for-the-badge&labelColor=000000&logoColor=white)
![Scale](https://img.shields.io/badge/SCALE-200K%2B_RECORDS-217346?style=for-the-badge&labelColor=000000&logoColor=white)
![Engine](https://img.shields.io/badge/ENGINE-EXCEL_365-217346?style=for-the-badge&logo=microsoftexcel&labelColor=000000&logoColor=217346)
![Python](https://img.shields.io/badge/PYTHON-3.12-217346?style=for-the-badge&logo=python&labelColor=000000&logoColor=217346)
![Pipeline](https://img.shields.io/badge/PIPELINE-ETL_WORKFLOW-217346?style=for-the-badge&logo=apacheairflow&labelColor=000000&logoColor=217346)
![Data](https://img.shields.io/badge/DATA-PANDAS-217346?style=for-the-badge&logo=pandas&labelColor=000000&logoColor=217346)

<br/>

</div>
<br/>
  <div>
    <img src="https://raw.githubusercontent.com/Muntasirzx/RevSync-RCM-with-Excel/8874f09d8d709e3c70597784df63ea3cd59f91f5/DATA/15.04.2026_13.42.00_REC-Trim-ezgif.com-video-to-gif-converter.gif" width="49%"/>
    <img src="https://raw.githubusercontent.com/Muntasirzx/RevSync-RCM-with-Excel/refs/heads/main/DATA/%7B8B411BD9-F5CE-4952-81DF-462CEA515289%7D.png" width="49%"/>
  </div>
<br/>

---

## `〉` Overview

**RevSync RCM** is an enterprise-grade Revenue Cycle Management engine that ingests hundreds of thousands of Medicare remittance records, reconciles them against simulated bank feeds, and routes every broken claim to the correct internal department — automatically.

Built entirely on **modern Excel dynamic arrays** and a **Python 3.12 ETL pipeline**, RevSync eliminates manual triage bottlenecks and delivers root-cause financial intelligence through an interactive command-center dashboard.

---

## `〉` Core Features

<br/>

| | Feature | Description |
|---|---|---|
| `🔑` | **Composite Primary Keys** | Built on-the-fly inside `XLOOKUP` arrays to prevent cross-contamination across dozens of DRG service lines |
| `🛡️` | **Leading Zero Protection** | `TEXT()` functions enforced inside the calculation memory layer — defeats Excel's silent leading-zero truncation |
| `⚡` | **Zero-Touch Spill Arrays** | Engine auto-detects raw data footprint and processes every row in a single formula pass — no manual range updates |
| `📊` | **Executive Command Center** | Translates 200K+ rows of granular variance data into interactive PivotCharts for live root-cause analysis |
| `🔄` | **Automated Claim Routing** | `IFS` logic evaluates variance depth and assigns broken claims to the correct desk (Escalation, Billing, Write-Off) |
| `🧮` | **Floating-Point Sanitization** | `ROUND(..., 2)` enforced throughout to eliminate binary math ghost-variances |

<br/>

---

## `〉` Technology Stack

<br/>

<div align="center">

**— Presentation Layer —**

![Excel](https://img.shields.io/badge/Microsoft_Excel_365-217346?style=for-the-badge&logo=microsoftexcel&logoColor=217346&labelColor=000000)
![PivotCharts](https://img.shields.io/badge/PivotCharts_%26_Slicers-217346?style=for-the-badge&logo=databricks&logoColor=217346&labelColor=000000)

**— Logic & Processing Layer —**

![DynamicArrays](https://img.shields.io/badge/Dynamic_Arrays_%26_Spill-217346?style=for-the-badge&logo=lightning&logoColor=217346&labelColor=000000)
![XLOOKUP](https://img.shields.io/badge/XLOOKUP_%7C_IFS_%7C_TEXT-217346?style=for-the-badge&logo=github-actions&logoColor=217346&labelColor=000000)

**— Ingestion & Simulation Layer —**

![Python](https://img.shields.io/badge/Python_3.12-217346?style=for-the-badge&logo=python&logoColor=217346&labelColor=000000)
![Pandas](https://img.shields.io/badge/Pandas-217346?style=for-the-badge&logo=pandas&logoColor=217346&labelColor=000000)
![CMS](https://img.shields.io/badge/CMS_Public_Data-217346?style=for-the-badge&logo=databricks&logoColor=217346&labelColor=000000)

</div>

<br/>

---

## `〉` Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                      REVSYNC RCM PIPELINE                       │
├────────────────┬────────────────────────────────────────────────┤
│  INPUT LAYER   │  CMS Medicare Feed + Simulated Bank Remittance │
│                │  tbl_Remit.csv  ·  tbl_Bank.csv                │
├────────────────┼────────────────────────────────────────────────┤
│  ETL LAYER     │  Python 3.12 / Pandas                          │
│                │  generate_remit_data.py injects variance:      │
│                │    · Fee discrepancies   · Claim denials       │
│                │    · Partial payments    · Duplicate rows      │
├────────────────┼────────────────────────────────────────────────┤
│  ENGINE LAYER  │  Reconciliation_Engine (Excel)                 │
│                │  E2 master array → spills entire dataset       │
│                │    · Composite key: TEXT(ClaimID,9) & DRG      │
│                │    · XLOOKUP match → variance math             │
│                │    · ROUND(variance,2) → IFS routing           │
├────────────────┼────────────────────────────────────────────────┤
│  OUTPUT LAYER  │  Operations_Dashboard (Excel)                  │
│                │    · Aging A/R tracker                         │
│                │    · Root Cause PivotChart                     │
│                │    · Top Offending Service Lines               │
│                │    · Department Routing Queue                  │
└────────────────┴────────────────────────────────────────────────┘
```

---

## `〉` Reconciliation Workflow

```
 ① RAW INGEST          ② KEY GENERATION        ③ VARIANCE MATH
 ─────────────         ────────────────         ───────────────
 CMS + Bank CSV   →    TEXT() composite    →    Cross-ref deposit
 200K+ records         9-digit primary key       ROUND(..., 2)
                        built in-memory          sanitization

 ④ CLAIM ROUTING        ⑤ COMMAND CENTER
 ───────────────         ────────────────
 IFS(variance)   →      PivotCharts update
 → Escalation Desk       live Aging A/R
 → Billing Dept          Root Cause matrix
 → Write-Off Queue       Top Offenders view
```

---

## `〉` Prerequisites

![Excel](https://img.shields.io/badge/Excel_365_or_2021%2B-required-217346?style=flat-square&logo=microsoftexcel&logoColor=217346&labelColor=000000)
![Python](https://img.shields.io/badge/Python_3.12%2B-required-217346?style=flat-square&logo=python&logoColor=217346&labelColor=000000)
![Git](https://img.shields.io/badge/Git-latest-217346?style=flat-square&logo=git&logoColor=217346&labelColor=000000)
![CMS](https://img.shields.io/badge/CMS_Public_Data-optional-555555?style=flat-square&logo=database&logoColor=white&labelColor=000000)

> **Excel version matters.** Dynamic arrays (`XLOOKUP`, spill operators, `IFS`) require **Excel 365** or **Excel 2021+**. The engine will not function in Excel 2019 or earlier.

---

## `〉` Installation

### 1 · Clone the repository

```bash
git clone https://github.com/your-username/revsync-rcm.git
cd revsync-rcm
```

### 2 · Install Python dependencies

```bash
pip install -r requirements.txt
# pandas, numpy, faker — all pinned to stable releases
```

### 3 · Generate simulated bank remittance feed

```bash
python generate_remit_data.py
# Output → tbl_Bank.csv  (injected with fees, denials, partials)
```

### 4 · Initialize the Excel engine

```
1. Open  RevSync_Engine_Master.xlsx
2. Import tbl_Bank.csv and tbl_Remit.csv into the Data Model
3. Navigate to the  Reconciliation_Engine  tab
4. Verify Cell E2 — the master spill array should populate all rows
```

### 5 · Refresh dashboard connections

```
Operations_Dashboard tab → Data › Refresh All
```

---

## `〉` File Structure

```
revsync-rcm/
├── generate_remit_data.py        # Python ETL simulation script
├── requirements.txt              # Pinned dependencies
└── excel/
    └── RevSync_Engine_Master.xlsx
        ├── tbl_Remit.csv          # CMS remittance source
        └── tbl_Bank.csv           # Simulated bank deposit feed
        ├── Reconciliation_Engine  # Master dynamic array tab
        └── Operations_Dashboard   # Executive command center
```

---

## `〉` Key Formula Patterns

**Composite Primary Key (prevents DRG cross-contamination)**
```excel
= TEXT([ClaimID], "000000000") & "-" & TEXT([DRG], "000")
```

**Master Reconciliation Array (Cell E2 — spills entire dataset)**
```excel
= XLOOKUP(
    Remit[CompositeKey],
    Bank[CompositeKey],
    Bank[DepositAmt],
    "NO MATCH",
    0
  )
```

**Floating-Point Safe Variance**
```excel
= ROUND([RemitAmt] - [BankDeposit], 2)
```

**Automated Claim Routing**
```excel
= IFS(
    [Variance] = 0,         "MATCHED",
    ABS([Variance]) < 1,    "BILLING REVIEW",
    [BankAmt] = "NO MATCH", "ESCALATION DESK",
    [Variance] < 0,         "UNDERPAYMENT — BILLING",
    TRUE,                   "WRITE-OFF QUEUE"
  )
```

---

<div align="center">

<br/>

![Built](https://img.shields.io/badge/Engineered_to_eliminate_manual_triage_bottlenecks-000000?style=for-the-badge&labelColor=217346&logoColor=white)

<br/>

![Footer](https://img.shields.io/badge/RevSync_RCM-Revenue_Cycle_Intelligence_at_Scale-000000?style=flat-square&labelColor=000000&color=217346)

</div>
