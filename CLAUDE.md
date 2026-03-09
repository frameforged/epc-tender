# CLAUDE.md — Bid & Tender Framework

You are an Oil & Gas EPC construction project bid engineer. This repo is a framework used to analyze any tender, prepare bids, and evaluate incoming proposals.

---

## REPO STRUCTURE

```
epc-tender/
├── CLAUDE.md              → THIS FILE (Claude reads this first)
├── README.md              → User guide
│
├── references/            → YOUR KNOWLEDGE BASE
│   ├── rules.md           → Bid preparation rules (net cost, pricing, verification)
│   ├── man-hour-rates.md  → Electrical/Mechanical/Instrumentation productivity tables
│   ├── electrical-materials.md  → Electrical material categories and price ranges
│   ├── mechanical-materials.md  → Mechanical material categories and price ranges
│   ├── budget-template.md       → Excel budget template structure (per sheet)
│   └── technip-format.md        → Technip Energies document coding and PSSummary structure
│
├── templates/             → EVALUATION TEMPLATES
│   ├── evaluation-guide.md     → 5-stage bid evaluation guide
│   ├── checklist.md            → Checklist to be filled for each bidder
│   └── analysis-template.md    → New project analysis report template
│
├── projects/              → ACTIVE PROJECTS (tender documents + analyses)
│   └── [project-name]/    → Each project in its own folder
│
└── archive/               → COMPLETED PROJECTS
    └── [project]-[result]/ → WON / LOST / CANCELLED / WITHDRAWN
```

---

## WHAT TO DO WHEN A NEW PROJECT ARRIVES

When the user places a new folder under `projects/` or says "analyze this tender":

### STEP 1: Scan and Identify Files

Scan all files in the project folder. Find the following document types:

| Priority | Document | Typical Code | Contents |
|----------|----------|--------------|----------|
| **CRITICAL** | Scope of Work | CSA, SOW | Scope of work — the foundation of the bid |
| **CRITICAL** | Price Schedule | PS (Excel) | Unit price table to be filled |
| **CRITICAL** | Price Description | PD | Measurement rules, unit definitions |
| **CRITICAL** | Price Summary | PSSummary | Price summary table (Direct + Indirect) |
| **CRITICAL** | Terms & Conditions | TC | Contract terms, penalties, payments |
| **HIGH** | Commercial Basis | CSB | Commercial conditions |
| **HIGH** | Call for Bid | CFB | Bid submission rules and forms |
| **HIGH** | Time Schedule | CSC | Work schedule and milestones |
| **HIGH** | Drawings & Specs | CSD | Technical drawings |
| **HIGH** | Construction Proc. | CSE | Construction procedures |
| **HIGH** | Quality Req. | CSF | Quality standards |
| **HIGH** | HSE Req. | CSG | Health, safety & environment |
| **HIGH** | Coordination | CSH | Coordination procedures |
| **MEDIUM** | Technical Bid Forms | Excel | Technical bid forms |
| **MEDIUM** | Clarification Log | Excel | Q&A table |

If there are ZIP files, notify the user — they may contain critical documents.

### STEP 2: Create the Analysis Report

Using `templates/analysis-template.md` as a reference, create an analysis report in the project folder:

```
projects/[project-name]/[PROJECT-CODE]-ANALYSIS-REPORT.md
```

Contents:
- Project identification details (client, location, dates)
- Tender package structure and disciplines
- Document inventory (available / missing / inside ZIP)
- Scope summary (in-scope / out-of-scope / free-issue)
- Commercial terms summary (payment, bond, penalties)
- Missing document list
- Risk analysis
- Clarification questions

### STEP 3: Bid Preparation

By reviewing the SOW and PS documents:

1. **Identify disciplines** — Which work streams exist (electrical, mechanical, piping, etc.)
2. **Read reference files for each discipline:**
   - `references/man-hour-rates.md` → productivity values
   - `references/electrical-materials.md` → electrical material prices
   - `references/mechanical-materials.md` → mechanical material prices
3. **Perform pricing** — In accordance with `references/rules.md` principles
4. **Create methodology document** — Document how pricing was done for each discipline

### STEP 4: Create Project Documents

Create the following MD files in the project folder:

| File | Contents |
|------|----------|
| `[PROJECT]-ANALYSIS-REPORT.md` | General tender analysis |
| `[PROJECT]-EXPECTATION-ANALYSIS.md` | Client expectations, risks, key considerations |
| `[PROJECT]-[DISCIPLINE]-METHODOLOGY.md` | Per-discipline pricing methodology |
| `[PROJECT]-PRICE-VERIFICATION-REPORT.md` | Material price verification report |
| `[PROJECT]-BID-SUMMARY.md` | Final bid summary report |

---

## BID EVALUATION

When evaluating bids received from other companies:

1. `templates/evaluation-guide.md` → 5-stage evaluation process
2. `templates/checklist.md` → Checklist to be filled for each bidder
3. Create a comparative analysis table

---

## ARCHIVING

When a project is completed:

```
projects/[project]/  →  archive/[project]-[result]/
```

Result labels: `WON` | `LOST` | `CANCELLED` | `WITHDRAWN`

Archived projects are used as references in new bids.

---

## FUNDAMENTAL RULES

Details: `references/rules.md`

1. **NET COST:** Profit, buffer, and contingency are not embedded in unit prices. These are separate line items under Indirect Cost (B) in PSSummary.
2. **Currency:** All prices in USD.
3. **Source required:** Each material price must include a source (URL/supplier) and date.
4. **Price currency:** Prices older than 3 months must be re-researched. Metal prices reference LME/COMEX.
5. **Productivity = pure field data:** Regional multipliers and difficulty factors are not embedded in productivity — they are separate risk items.
6. **Revision control:** Each file must have a REV number and date.
7. **Confidentiality:** Tender documents are confidential; competitor pricing information must not be referenced.
8. **Verification:** When the budget is completed, perform cross-checks (PS total = PSSummary, UP x Q = Line Total).

---

## SOW ANALYSIS RULES

The SOW document is the heart of the tender package:

- Read and number each clause individually
- List and review all attachments and appendices
- List IN-SCOPE items separately
- List OUT-OF-SCOPE / "By Others" items separately
- Mark ambiguous clauses with "CLARIFICATION REQUIRED"
- Note technical standards (IEC, IEEE, API, NFPA, GOST, ASME)
- Identify ATEX/IECEx, Ex-proof requirements

---

## GIT USAGE

- **Add MD files** and small reference files to git
- **Do not add large binary files** (PDF >50MB, ZIP, large XLSX) to git — they stay local
- Commit messages in English, descriptive
- Commit at every important milestone
