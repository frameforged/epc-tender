# Tender & Bid Preparation Framework

Claude Code-powered tender preparation and evaluation system for Oil & Gas EPC construction projects.

---

## Quick Start

### 1. Clone the Repo

```bash
git clone https://github.com/[USER]/epc-tender.git
cd epc-tender
```

### 2. Open Claude Code

```bash
claude
```

When Claude opens this repo, it automatically reads the `CLAUDE.md` file and knows what to do. No extra configuration is needed.

---

## Step by Step: When a New Tender Arrives

### Scenario: A 6-package EPC tender package arrived from Technip Energies

#### Step 1: Place the tender folder into the project

```bash
cp -r ~/Downloads/ITB "projects/SOCAR-SUMGAYIT-2026"
```

Name the folder as you like:
- `projects/TURKMENGAZ-ONSHORE-2026`
- `projects/SOCAR-SUMGAYIT-SP01`
- `projects/BP-AZERI-OFFSHORE`
- `projects/STAR-REFINERY-TANK`

#### Step 2: Have Claude perform a general analysis

```
Analyze the tender in the projects/SOCAR-SUMGAYIT-2026 folder.
How many packages are there, summarize the scope and disciplines of each package.
Find missing documents, tell me which ZIPs are critical.
```

What Claude does:
- Scans all folders and subfolders
- Automatically identifies document codes (CSA, CSB, TC, PS etc.)
- Detects packages (SP01, SP02, SP04...)
- Warns if there are `missing.txt` files
- Lists missing critical documents
- Creates an analysis report: `SOCAR-SUMGAYIT-2026-ANALYSIS-REPORT.md`

#### Step 3: Extract ZIP files

Claude will tell you which ZIPs are critical. Priority order:

```bash
cd "projects/SOCAR-SUMGAYIT-2026/SP01/.../2.3 COMMERCIAL TERMS"
unzip "PS.zip" -d "PS-extracted"
unzip "PD.zip" -d "PD-extracted"
```

Then:

```
I extracted the ZIPs. Now do a detailed analysis for the SP01 package.
Extract the electrical scope (1600) from the SOW, compare the items in PS-1600 Excel with the SOW.
```

#### Step 4: Prepare discipline-based pricing

See the "Real Command Examples" section below — it is explained in detail there.

#### Step 5: Evaluate bids (optional)

If you want to evaluate a bid received from another company:

```
Evaluate the file projects/SOCAR-SUMGAYIT-2026/received-bids/ABC-company-bid.xlsx.
Compare unit prices with references/electrical-materials.md, create a benchmark table.
```

#### Step 6: Archive when done

```
Archive the SOCAR-SUMGAYIT-2026 project, bid was submitted and won
```

Claude moves the project to `archive/SOCAR-SUMGAYIT-2026-WON/`.

---

## Real Command Examples (Write Like an Electrical Engineer)

You can type the commands below to Claude as-is. Each one triggers a task that a real EPC bid engineer would perform.

### Tender Analysis Phase

```
Analyze the SOW document (CSA-1000-0001) for the SP01 package.
Extract the electrical scope (Section 1600) separately.
List IN-SCOPE, OUT-OF-SCOPE and BY OTHERS items.
If there are ambiguous clauses, write them as clarification questions.
```

```
Compare the SOWs of SP01 and SP02 packages.
Find the differing items in the electrical scope (1600, 1610-1690).
Same discipline but different area — extract things that will affect the price difference.
```

```
Read the TC (Terms & Conditions) document.
Summarize delay penalty rates, LD cap, retention percentage, bond requirements.
Extract payment terms (milestone-based, monthly, back-loaded).
```

```
Prepare clarification questions for all packages (SP01-SP06).
Create a question list for missing documents, ambiguous scope items, conflicting clauses.
Write in CLARIF Excel format.
```

### Pricing Phase

```
Prepare a budget for the SP01 electrical discipline (1600).
Price each item in the PS-1600 Excel one by one.
Use references/man-hour-rates.md for man-hour calculations.
Use references/electrical-materials.md for material prices.
Pure cost — do not add profit and buffer, show them separately.
```

```
Fill in the 147 active items in the PS-1600 Excel.
Calculate the unit price for each item:
- Cable pulling: MH x rate + material
- Cable tray installation: MH x rate + material
- Termination: MH x rate + material
- Testing & commissioning: MH x rate
Calculate according to the measurement rules in PD-1600.
```

```
Fill in the PSSummary for SP01.
Direct Cost (A) = take from PS-1600 totals.
Indirect Cost (B) = site establishment, mobilization, insurance, contingency as separate line items.
Total = A + B.
Write according to the references/technip-format.md structure.
```

```
Prepare a budget for the SP06 tank erection package.
Review tank data sheets (01-T-101, 01-T-201, 01-T-301...).
Price each tank based on tonnage, diameter, material type.
Erection + welding + testing + painting items separately.
```

### Material Price Research

```
Research cable prices for the SP01 electrical scope.
Find current market prices for XLPE, PVC, SWA, fire-resistant types.
Add source (URL or supplier) and date. Do not use prices older than 3 months.
```

```
Update lighting fixture prices.
Separate for ATEX Zone 1, Zone 2 and safe area.
In LED floodlight, bulkhead, fluorescent categories.
Check the LME copper price, reflect it in cable prices.
```

### Price Verification

```
Check my PS-1600 calculations.
Verify that UP x QTY = Line Total for each row.
Verify that the sum of Line Totals = PS total.
Verify that the PS total matches the PSSummary Direct Cost (A) total.
Report discrepancies.
```

```
Benchmark the SP01 electrical budget.
Compare with unit prices from similar projects (references/electrical-materials.md).
Flag items that are extremely cheap or extremely expensive.
Warn if cable pulling is below 2 USD per meter or above 8 USD.
```

### Bid Evaluation (For Received Bids)

```
Evaluate ABC company's SP01 electrical bid.
Perform the 5-stage evaluation per templates/evaluation-guide.md.
Fill in the templates/checklist.md checklist.
Compare unit prices with our references, show deviations.
```

```
Compare bids from 3 companies for SP01 side by side.
Tabulate PS-1600 prices from ABC, XYZ and DEF companies item by item.
Show the cheapest, most expensive and average for each item.
Compare total cost with Direct + Indirect breakdown.
```

---

## Folder Structure

```
epc-tender/
├── CLAUDE.md                ← Claude's framework instructions (first file read)
├── README.md                ← You are reading this now
│
├── references/              ← Claude's knowledge base
│   ├── rules.md             ← Bid preparation rules (pure cost, verification)
│   ├── man-hour-rates.md    ← Labor productivity (electrical/mechanical/instr.)
│   ├── electrical-materials.md   ← Electrical material prices and sources
│   ├── mechanical-materials.md   ← Mechanical material prices and sources
│   ├── budget-template.md        ← Excel budget template structure (sheet-based)
│   └── technip-format.md         ← Technip Energies document coding and PSSummary
│
├── templates/               ← Evaluation templates
│   ├── evaluation-guide.md  ← 5-stage bid evaluation
│   ├── checklist.md         ← Checklist to fill for each bidder
│   └── analysis-template.md ← New project analysis report template
│
├── projects/                ← YOUR ACTIVE PROJECTS GO HERE
│   └── [project-name]/
│       ├── (tender documents)     ← PDF, ZIP, XLSX, DOCX
│       └── (Claude's analyses)    ← Automatically generated MD files
│
└── archive/                 ← Completed projects are moved here
    └── [project]-[result]/  ← WON / LOST / CANCELLED / WITHDRAWN
```

---

## What to Expect Inside a Tender Package

Every project is different. Folder names, file names, and structure vary from project to project. But the **types of information** they contain are always similar. Claude looks at the type of information in the content, not the file name.

### A Tender Generally Contains 3 Main Sections

Folder names may differ but these 3 main information groups are always present:

| # | Information Group | What It Contains | Why It Matters |
|---|-------------------|------------------|----------------|
| 1 | **Technical Information** | Scope of Work, drawings, time schedule, construction/quality/HSE procedures | Defines what the work is |
| 2 | **Commercial Information** | Draft contract, conditions (penalties/payment/bond), price schedules | Determines the price and risks |
| 3 | **Bidder Forms** | Bid letter rules, Q&A table, technical bid form | Tells you how to submit the bid |

### Types of Information That Should Be in Every Tender Package

File names vary from project to project. For example, a scope of work may be called `CSA-1000-0001_A.pdf` in one project, `SOW-Rev2.pdf` in another, and `Scope_Document_Final.docx` in yet another. What matters is not the file name but the type of information it contains.

**On the technical side, these should be present:**

| Information Type | Example File Names | Purpose |
|------------------|-------------------|---------|
| **Scope of Work (scope)** | `CSA-xxxx.pdf`, `SOW-Rev2.pdf`, `Scope_Document.docx` | MOST CRITICAL — defines what the work is, determines disciplines |
| **Drawings and specifications** | `CSD-xxxx.pdf`, `Drawings.zip`, `Technical_Specs/` | Technical details, layout, single line diagram |
| **Time schedule** | `CSC-xxxx.pdf`, `Schedule.xlsx`, `Milestone_Plan.pdf` | Dates, milestones, durations |
| **Construction procedures** | `CSE-xxxx.pdf`, `Construction_Procedure.pdf` | How construction will be performed, test procedures |
| **Quality requirements** | `CSF-xxxx.pdf`, `Quality_Req.pdf`, `ITP/` folder | ITPs, welding, test standards |
| **HSE requirements** | `CSG-xxxx.pdf`, `HSE_Requirements.pdf` | Occupational safety, environmental rules |
| **Coordination procedures** | `CSH-xxxx.pdf`, `Coordination.pdf` | Reporting, meeting, communication rules |

**On the commercial side, these should be present:**

| Information Type | Example File Names | Purpose |
|------------------|-------------------|---------|
| **Draft contract** | `CS-xxxx.pdf`, `Draft_Contract.pdf` | Legal framework |
| **Terms & Conditions (T&C)** | `TC-xxxx.pdf`, `Terms_Conditions.pdf` | Penalties, LD, retention, bond, payment terms |
| **T&C Annexes** | `Annex1_Performance_Bond.pdf`, `Annex_PPP.pdf` | Bond templates, compliance declarations |
| **Commercial terms** | `CSB-xxxx.pdf`, `Commercial_Basis.pdf` | Payment structure, currency, escalation |
| **Price Schedule (PS)** | `PS-xxxx.xlsx`, `Price_Schedule.xlsx`, `BOQ.xlsx` | Unit price table TO BE FILLED |
| **Price Summary (PSSummary)** | `PSSummary-xxxx.xlsx`, `Summary.xlsx` | Direct + Indirect total table |
| **Price Description (PD)** | `PD-xxxx.pdf`, `Price_Description.pdf` | Measurement unit definitions, what is included |

**In bidder forms, these should be present:**

| Information Type | Example File Names | Purpose |
|------------------|-------------------|---------|
| **Bid letter** | `CFB-xxxx.pdf`, `Call_for_Bid.pdf` | Submission deadline, format, rules |
| **Q&A table** | `CLARIF-xxxx.xlsx`, `Clarification_Log.xlsx` | Questions to ask the client |
| **Technical bid form** | `Technical_Bid_Forms.xlsx` | Technical capacity and experience form |

### Package (Sub-Package) Structure

Large EPC projects are generally tendered as multiple sub-packages. Each package covers a different scope of work.

For example, a refinery project may have these packages:
- **SP01** — Process North area construction works
- **SP02** — Process South area construction works
- **SP04** — Building works (process buildings)
- **SP05** — Building works (non-process buildings)
- **SP06** — Tank erection works

Another project may have a single package, or may be divided by discipline (electrical package, mechanical package, etc.). The folder structure is always different — Claude understands what it is by analyzing the content.

### Things That May Vary From Project to Project

- **Folder names**: Instead of "1. Technical Information" it could be "Technical Documents" or just "Tech"
- **Subfolder numbering**: 1.1, 1.2... may not exist, files may be placed flat
- **File formats**: The same content may be in PDF, DOCX, or inside a ZIP
- **ZIP usage**: In some projects everything is zipped, in others files are uncompressed
- **Single package vs multiple packages**: Small projects may be a single folder, large ones 6+ packages
- **Discipline-based PS**: In some projects PS is in separate files per discipline (PS-1600, PS-1300...), in others all disciplines are sheets within a single PS file
- **PD (Price Description)**: In some projects it is a separate file, in others it is a sheet within the PS Excel

### PS (Price Schedule) File Structure

Regardless of the file name, the PS Excel contains these columns (order may vary):

- **Item No** — Item number
- **Description** — Work description (e.g., "Cable pulling, 1x95mm2 XLPE")
- **Unit** — Unit of measure (m, m2, ea, set, lot, kg, ton)
- **Quantity** — Quantity (sometimes left blank, may be "to be quoted")
- **Unit Price** — YOU WILL FILL THIS IN
- **Total Price** — UP x QTY (usually has a formula)

If there are discipline-based PS files, extract them from the ZIP:

| Discipline Code | Discipline | Example File Name |
|-----------------|------------|-------------------|
| 1300 | Piping | `PS-1300-xxxx.xlsx` |
| 1500 | Instrumentation | `PS-1500-xxxx.xlsx` |
| 1600 | Electrical | `PS-1600-xxxx.xlsx` |
| 2000 | Civil / Structural | `PS-2000-xxxx.xlsx` |
| 6800 | Mechanical / Equipment | `PS-6800-xxxx.xlsx` |

### PQ (Pre-Qualification) Process

In some tenders, there is a pre-qualification process before submitting a bid. PQ documents typically require the following:

- **Company profile catalog** — General information about the company
- **Facility and workshop list** — Owned facilities
- **Current workload** — Ongoing projects
- **Subcontractor list** — Which works are subcontracted
- **Certificates** — ISO, HSE, quality certificates
- **Licenses** — Country-specific operating licenses
- **Sanctions declaration** — Sanctions due diligence
- **Company information form** — Questionnaire to be filled (usually Excel)

---

## Technip Energies Document Coding System (Example)

The coding system below is used in Technip Energies projects. Other EPC companies (Bechtel, Fluor, Worley, Saipem, etc.) may have different coding systems but the logic is similar. Claude tries to understand the content by parsing the file name.

### Technip File Name Example

```
218857C-00-CSA-1000-0001_A.pdf
│       │  │   │    │    │
│       │  │   │    │    └── Revision (_A or -A = Rev A)
│       │  │   │    └────── Package no (0001=SP01, 0002=SP02...)
│       │  │   └─────────── Discipline code (1000=Process, 2000=Building, 2500=Tank)
│       │  └──────────────── Document type (CSA, CSB, TC, PS...)
│       └─────────────────── Level (00=project-wide)
└──────────────────────────── Project number
```

Because the document type, discipline and package information is embedded in the file name in this coding system, Claude identifies them automatically. In other projects, file names may not be this structured — in that case Claude identifies them by looking at the file content.

### Common Document Type Codes

These codes are used similarly across different EPC companies:

| Code | Meaning |
|------|---------|
| CSA / SOW | Scope of Work |
| CSB | Commercial Basis |
| CSC | Time Schedule |
| CSD | Drawings & Specifications |
| CSE | Construction Procedure |
| CSF | Quality Requirements |
| CSG | HSE Requirements |
| CSH | Coordination Procedure |
| TC | Terms & Conditions |
| PS | Price Schedule |
| PD | Price Description |
| CFB | Call for Bid |
| BOQ | Bill of Quantities (another name for PS) |

---

## Pre-Bid Preparation Checklist

Make sure the following are ready before telling Claude to "prepare a bid":

- [ ] Tender documents are under `projects/[PROJECT]/`
- [ ] ZIP files are extracted — especially **PS.zip** and **PD.zip** (required for pricing)
- [ ] **SOW** document is available — a bid cannot be prepared without it
- [ ] **Price Schedule (PS)** Excel file is available and extracted
- [ ] **Price Description (PD)** is available — provides measurement rules
- [ ] **PSSummary** Excel file is available
- [ ] **Terms & Conditions (TC)** has been read — for penalty, payment, bond information
- [ ] You noted the bid submission deadline
- [ ] You decided which package(s) and which discipline(s) to bid on

---

## Important Rules

### Pricing Philosophy
- **Pure cost:** Profit, buffer, contingency are not embedded in unit prices
- These are shown as separate line items under Indirect Cost (B) in the PSSummary
- The question for each item: "How much does it actually cost the company to perform this work on site?"

### Material Prices
- Every price must have a source (URL or supplier) and date next to it
- Prices older than 3 months must be updated
- Metal prices reference LME/COMEX
- Do not confuse ATEX/Ex-proof equipment with safe area prices

### Productivity (Man-Hours)
- Pure field data is used
- Regional multiplier, difficulty factor are not embedded in productivity — shown as a separate risk item
- Details: `references/man-hour-rates.md`

### Git
- Only MD files and small reference files are added to git
- Large binary files (PDF >50MB, ZIP) are not added to git — they stay local

---

## Existing Project Example

Under `projects/ITB/` there are files generated by Claude for a Technip Energies SOCAR Refinery project (X-package EPC tender). This is just an example — your project may come with a completely different client, different structure, different file names. Claude analyzes the content in any case and produces the same output structure.

| File | Content |
|------|---------|
| `ITB-ANALYSIS-REPORT.md` | General analysis of X packages, document inventory, gaps, risks |
| `EXPECTATION-ANALYSIS-DOCUMENT.md` | Client expectations, points to watch out for |
| `SP01-ELECTRICAL-1600-EXPECTATION-ANALYSIS.md` | Electrical discipline (1600) detailed expectation analysis |
| `SP01-ELECTRICAL-PRICING-METHODOLOGY.md` | Documentation of how each item was priced |
| `SP01-ELECTRICAL-BID-SUMMARY-REPORT.md` | Final bid summary (total cost, breakdowns) |
| `SP01-PRICE-VERIFICATION-REPORT.md` | Cross-check: PS total = PSSummary, UP x QTY = Line Total |
| `218857C-000-PS-1600-0001-A-BID-FILLED.xlsx` | Filled PS-1600 Excel file |

When a new project arrives, Claude automatically produces the same output structure. All you need to do is place the tender documents under `projects/` and tell Claude to "analyze it".
