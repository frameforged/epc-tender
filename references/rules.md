# BID AND TENDER PREPARATION RULES

**Version:** 1.0
**Date:** 2026-03-07
**Prepared by:** Bid & Tender Department
**Scope:** Turkmenistan, Azerbaijan — Onshore/Offshore Oil & Gas Electrical and Mechanical Construction Projects

---

## 1. GENERAL RULES

### 1.1 Fundamental Principles
- Every bid shall be prepared to cover **every clause** of the relevant tender document (ITB/RFQ/RFP).
- The SOW (Scope of Work) document and its attachments are the foundation of the bid; no clause may be skipped.
- All prices shall be standardized in **USD**. Local currency is shown separately if required.
- A **date stamp** and **source reference** shall be added to every budget item.
- Revision control is mandatory: every file must include a REV number and date.

### 1.2 Confidentiality
- Tender documents are confidential; they shall not be shared with third parties.
- Competitor price information shall never be referenced in the budget.
- Client-specific information shall be stored only in the relevant project folder.

---

## 2. SOW ANALYSIS RULES

### 2.1 Initial Reading
- Read the SOW document from beginning to end at least once.
- Number each section and clause.
- List and review all attachments and appendices.

### 2.2 Scope Determination
- List IN-SCOPE items separately.
- List OUT-OF-SCOPE (exclusion) items separately.
- Specifically flag "By Others" or "Not in Contractor's Scope" expressions.
- Add a "CLARIFICATION REQUIRED" note for ambiguous clauses.

### 2.3 Technical Standards
- List all standards referenced in the SOW (IEC, IEEE, API, NFPA, GOST, ASME, etc.).
- Note regional standard requirements (ATEX/IECEx, GOST-R certification).
- In case of standard conflicts, apply the stricter one (unless stated otherwise).

### 2.4 Output
- Prepare a SOW Analysis Report: clause-by-clause scope, technical requirements, ambiguities, risks.

---

## 3. BUDGET PREPARATION RULES

### 3.1 Material Pricing — PURE PROCUREMENT COST
- **Pricing philosophy:** The PURE cost to the company for procuring the material.
- Price = actual market/supplier price. No profit margin shall be added on top.
- Research **at least 2 different sources** for each material.
- Record the source URL and access date.
- Specify the FOB/CIF/DDP basis.
- Add freight and logistics cost (must be delivered-to-site price).
- Account for customs duties and import costs.
- Specify Ex-proof/certified product price difference separately.
- Estimate bulk purchase discount (if applicable).
- **Free-issue material = 0.** If the Client/Contractor supplies it, the M column is zero.

### 3.2 Man-Hour Calculation — PURE PRODUCTIVITY
- Separate each work item by discipline (electrical, mechanical, instrumentation, civil).
- Use **PURE productivity**: How many man-hours does a worker actually take to perform this task on site?
- Regional multiplier, difficulty factor, profit margin, buffer — **NONE** of these shall be added to productivity.
- Productivity = actual field data. Example: 2.5mm2 cable pulling = ~0.05 MH/m (20 m/hour/person)
- Offshore multiplier, brownfield multiplier, climate multiplier — these are calculated SEPARATELY as indirect cost or risk; they shall not be embedded in productivity.
- Account for overtime rate as a separate item (if applicable).

### 3.3 Labor Cost — PURE COST
- **Pricing philosophy:** PURE cost to the company. NO profit, overhead, buffer, or ANYTHING shall be added on top.
- Labor unit price = Productivity (MH) x Pure hourly rate (USD/MH)
- **Pure hourly rate:** The actual cost of employing a worker on site for 1 hour:
  - Salary/daily wage
  - Social security/social charges
  - Meals (on site)
  - Transportation/shuttle
  - PPE (personal protective equipment, amortized)
  - Hand tools (amortized)
  - **NOT INCLUDED:** scaffolding, test equipment, supervision, overhead, profit
- Scaffolding, test equipment, project management — calculated SEPARATELY as indirect costs.
- If expat personnel are involved, set a separate rate; do not mix.

### 3.4 Equipment
- Perform rental vs. purchase comparison.
- Include cranes, generators, welding machines, test instruments.
- For offshore projects, calculate barge/crane vessel cost separately.
- Add mobilization/demobilization costs.

### 3.5 Indirect Costs
| Item | Typical Rate |
|------|-------------|
| Project management | 8-12% |
| QA/QC | 3-5% |
| HSE | 2-4% |
| Insurance | 1-3% |
| Logistics/Freight | Project-specific |
| Camp/Accommodation | Project-specific |
| Mob/Demob | Project-specific |
| Administrative expenses | 2-4% |

### 3.6 Contingency and Profit — CALCULATED SEPARATELY
- **IMPORTANT:** Contingency and profit shall NEVER be embedded in unit prices.
- First calculate the pure cost, then add on top:
- Contingency: 5-15% (depending on risk level) — SEPARATE line item
- Profit margin: 8-15% (depending on competition) — SEPARATE line item
- Escalation: 3-5% per year for long-term projects — SEPARATE line item
- This keeps costs transparent and allows different margins to be applied to each project.

### 3.7 Verification
- Summary total = detail totals (cross-check)
- Unit price x quantity = total price (every line)
- Man-hours x rate = labor cost (every line)
- After completing the budget, benchmark the total amount on a per-m2 or per-ton basis.

---

## 4. FILE AND FOLDER RULES

### 4.1 Project Folder Structure
```
projects/
└── [PROJECT-NAME]/
    ├── (tender documents)       → PDF, ZIP, XLSX, DOCX
    └── (Claude's analyses)      → MD files
```

### 4.2 File Naming
Format: `[PROJECT-CODE]_[File-Type]_[REV-No]_[Date].[extension]`

Examples:
- `TKM-2026-001_BUDGET_REV0_20260307.xlsx`
- `AZE-2026-003_SOW-ANALYSIS_REV1_20260315.docx`
- `TKM-2026-001_BID_REV0_20260320.pdf`

### 4.3 Revision Control
- REV0: First draft
- REV1, REV2, ...: Revisions
- FINAL: Final approved version
- Include a brief description of each revision change in the file.

---

## 5. PRICE RESEARCH RULES

### 5.1 Accepted Sources
- Manufacturer official websites (ABB, Siemens, Schneider, Eaton, Prysmian, etc.)
- B2B platforms (Alibaba, Made-in-China, DirectIndustry, RS Components)
- Industry reports (IHS Markit, S&P Global, Wood Mackenzie)
- FRED (Federal Reserve Economic Data) — PPI indices
- Local distributor quotations (written offer/invoice)

### 5.2 Source Documentation
Mandatory information for each price:
- Source name and URL
- Access/research date
- Original currency and exchange rate
- FOB/CIF/DDP basis
- Product specification

### 5.3 Price Updates
- Prices older than 3 months shall be re-researched.
- Metal/copper/steel prices may fluctuate weekly — use LME/COMEX reference.
- Exchange rate shall be noted on a daily basis.

---

## 6. REGIONAL RULES

### 6.1 Turkmenistan
- Tender participation fee: ~575 USD/Lot (VAT inclusive)
- Bid period: 30 business days from publication date
- Document language: Turkmen/English/Russian
- Special permits may be required for offshore zones
- Turkmenneft / Turkmengaz standard specifications apply
- Bid envelope must be sealed and wax-sealed
- Technical and commercial bids in separate envelopes

### 6.2 Azerbaijan
- SOCAR/BP-Azerbaijan tender procedures
- Tender language: Azerbaijani/English
- Marination certificates for Caspian offshore projects
- AIOC standards (for BP operations)
- Tax exemptions may apply under PSA (Production Sharing Agreement)

### 6.3 Technip Energies Projects (Active)
- Bid platform: Technip Energies Digital Tool (online upload)
- Part A (commercial+technical) and Part B (technical) as separate ZIP files
- Bid Forms 2 and 3 → mandatory in .xls format
- Price structure: PSSummary (summary) + PS (detailed by discipline)
- Direct Costs (A) + Indirect Costs (B) structure
- Scaffolding MHR and direct cost → embedded in each item code's unit price
- Compliance Declaration mandatory (Sapin 2, FCPA, UK Bribery Act)
- Bid validity: 180 days
- Clarification questions: At least 7 days before bid closing
- Acknowledgement: Within 3 calendar days after receiving CFB
- Document coding: `[Project No]-[Unit]-[Code]-[Area]-[Serial]_[Rev]`
- Detailed format information: `references/technip-format.md`

---

## 7. QUALITY CONTROL RULES

### 7.1 Budget Verification Checklist
- [ ] Are all SOW clauses covered in the budget?
- [ ] Are all prices sourced?
- [ ] Have man-hour calculations been applied with productivity factors?
- [ ] Has the offshore multiplier been applied (if offshore project)?
- [ ] Has freight cost been added?
- [ ] Have customs/import costs been added?
- [ ] Has contingency been added?
- [ ] Has profit margin been added?
- [ ] Does the summary total = detail totals?
- [ ] Do all files have date and revision number?
- [ ] Has benchmark comparison been performed?

### 7.2 Bid Document Final Check
- [ ] Does it comply with client format?
- [ ] Are all requested documents present?
- [ ] Have technical and commercial bids been separated (if required)?
- [ ] Have signature and seal been added?
- [ ] Is the delivery date appropriate?

---

## 8. RISK MANAGEMENT

### 8.1 Typical Risks
| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Material price increase | High | Medium | Add escalation clause |
| Currency fluctuation | High | High | USD-based contract |
| Freight delay | Medium | High | Add buffer time |
| Local workforce quality | Medium | Medium | Add training budget |
| Weather conditions (winter) | Medium | Medium | Seasonal planning |
| Permit/visa issues | Medium | High | Early application |
| Scope change | High | High | Variation order procedure |

---

## 9. OUTPUT FORMATS

| File Type | Format | Usage |
|-----------|--------|-------|
| Main budget | .xlsx | Detailed cost analysis |
| SOW Analysis | .docx or .md | Scope assessment |
| Bid letter | .docx | Official bid |
| Technical approach | .docx or .pdf | Methodology document |
| Price references | .xlsx | Reference list |
| Risk analysis | .xlsx | Risk assessment |

---

*These rules are referenced during every bid preparation process and are updated on a project-specific basis.*
