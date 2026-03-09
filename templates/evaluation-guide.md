# BID EVALUATION GUIDE
## Oil & Gas EPC Construction Tenders — General Framework

**Purpose:** Step-by-step guide for systematically evaluating bids received in any Oil & Gas EPC construction tender.
**Scope:** Onshore/Offshore — Electrical, Mechanical, Instrumentation, Civil disciplines
**Last Updated:** 2026-03-09

---

## 1. PRE-EVALUATION PREPARATION

The following must be ready before evaluating incoming bids:

| Preparation | Description |
|-------------|-------------|
| **Internal cost estimate** | Your own budget calculation (to be used as reference price) |
| **SOW analysis** | Complete list of scope items |
| **Tender documents** | CFB, TC, PS, PD, CSB — full understanding of bid requirements |
| **Reference productivity** | Discipline-based MH/unit reference values (under `references/`) |
| **Current market prices** | Material benchmarks (copper, cable, fittings, etc.) |

---

## 2. BID EVALUATION PROCESS — 5 STAGES

### STAGE 1: Completeness Check

First check for each incoming bid — if documents are missing, the bid is not accepted for evaluation.

**Commercial Bid — Check:**

| # | Document | Check |
|---|----------|-------|
| 1 | Bid letter (signed, sealed) | ☐ |
| 2 | Price summary table (PSSummary — Direct + Indirect) | ☐ |
| 3 | Discipline-based Price Schedule (Excel + PDF) | ☐ |
| 4 | Alternative prices (if any) | ☐ |
| 5 | Commercial deviations list | ☐ |
| 6 | Compliance Declaration | ☐ |

**Technical Bid — Check:**

| # | Document | Check |
|---|----------|-------|
| 1 | Execution Plan | ☐ |
| 2 | Direct workforce histogram | ☐ |
| 3 | Indirect workforce histogram | ☐ |
| 4 | Subcontractor list | ☐ |
| 5 | Work schedule and S-Curve | ☐ |
| 6 | Site equipment list | ☐ |
| 7 | Temporary facilities and infrastructure plan | ☐ |
| 8 | Camp/accommodation plan | ☐ |
| 9 | Technical deviations list | ☐ |
| 10 | HSE plan | ☐ |

> **Note:** The number and content of forms required in the tender documents varies by project. The above list is the typical minimum requirement for EPC construction tenders. Adapt according to each project's CFB document.

---

### STAGE 2: Price Consistency Check

Cross-verification between Price Schedule (PS) and Price Summary (PSSummary).

#### Typical EPC Price Structure

```
(A) DIRECT COSTS:
    a) Direct labour (hand tools, consumables, meals included)
    b) Direct labour for scaffolding
    c) Direct material (material to be integrated into the facility)
    d) Subcontracted works
    SUBTOTAL DIRECT COSTS (A)

(B) INDIRECT COSTS:
    1. Supervision and indirect labour
    2. Temporary site facilities
    3. General field expenses
    4. Construction equipment
    5. Heavy Lifting / Cranes
    6. Scaffolding cost
    7. HSE and Security
    8. Camp / Accommodation
    9. Design and engineering
    10. Local levies, duties, taxes
    11. Overheads and profit
    SUBTOTAL INDIRECT COSTS (B)

TOTAL = (A) + (B)
```

#### Check Points

| Check | Formula | Acceptance Criteria |
|-------|---------|---------------------|
| PS total = PSSummary Direct Cost | SUM(PS(discipline)) = A(discipline) | Exact match |
| Unit price x quantity = line total | UP x Q = Line Total | Correct on every line |
| MH total consistent | SUM(PS(MH)) = PSSummary(MH) | Exact match |
| Total = Direct + Indirect | A + B = Total | Exact match |

---

### STAGE 3: Technical Evaluation

#### 3.1 Labor (Man-Hour) Analysis

For each discipline, the proposed MH values are compared against reference productivity values.

**Reference Productivity Values (Electrical discipline examples):**

| Work Item | Unit | Reference MH | Acceptance Range |
|-----------|------|--------------|------------------|
| Small section cable pulling (<=6mm2) | m | 0.05 MH/m | 0.03-0.08 |
| Medium section cable pulling (~70mm2) | m | 0.13 MH/m | 0.08-0.18 |
| Large section cable pulling (~240mm2) | m | 0.22 MH/m | 0.15-0.30 |
| Cable tray installation | m | 0.45 MH/m | 0.30-0.65 |
| MV cable termination | ea | 4.80 MH/ea | 3.50-6.50 |
| LV termination | ea | 0.80 MH/ea | 0.50-1.20 |
| Transformer installation | ea | 224 MH/ea | 160-320 |
| Heat trace installation | m | 0.10-0.14 MH/m | 0.08-0.20 |

> Detailed reference values: `references/man-hour-rates.md`

**Evaluation rule:**
- Below the reference range: low bid risk, work quality should be questioned
- Above the reference range: high price, justification should be requested

#### 3.2 Material Price Analysis

Compare material prices against current market data. Each project's material procurement structure may differ:

| Procurement Type | Description | M Column in PS |
|-----------------|-------------|----------------|
| **Free-issue** | Supplied by the main Contractor | 0 |
| **Subcontractor supply** | Supplied by the bidding firm | Market price |

> Material price references: `references/electrical-material.md` and `references/mechanical-material.md`

#### 3.3 Hourly Rate Analysis

Calculate local labor cost based on project location:

| Item | Description |
|------|-------------|
| Wage/daily rate | Skilled worker gross wage |
| Social charges | Social security, taxes, etc. (15-25%, varies by country) |
| Meals | On-site meal cost |
| Transportation/shuttle | Worker transport |
| PPE | Personal protective equipment (amortized) |
| Hand tools | Amortized tool cost |

**Typical hourly rate ranges:**
- Caspian region (Azerbaijan/Turkmenistan) local: 4-7 USD/MH
- Middle East local: 3-6 USD/MH
- Expat personnel: 15-30 USD/MH
- Europe: 25-45 USD/MH

---

### STAGE 4: Commercial Evaluation

#### 4.1 Deviations Analysis

| Deviation Type | Risk Level | Typical Action |
|---------------|------------|----------------|
| Price escalation request | HIGH | Not acceptable if contract is fixed price |
| Payment term change | MEDIUM | Compare with standard terms |
| Scope reduction/exclusion | HIGH | Compare with SOW, identify missing items |
| Alternative material proposal | LOW | Acceptable if technical suitability is confirmed |
| Bond rate change | HIGH | Compare with tender requirements |
| LD penalty limit change | HIGH | Compare with tender requirements |

#### 4.2 Indirect Cost Ratios

| Item | Typical Rate | Acceptance Range |
|------|-------------|------------------|
| Supervision / Indirect labour | 8-12% | 5-15% |
| HSE and Security | 2-4% | 1-6% |
| QA/QC | 3-5% | 2-7% |
| Overheads and profit | 8-15% | 5-20% |
| Temporary facilities | Project-specific | — |
| Camp / Accommodation | Project-specific | — |
| Construction equipment | Project-specific | — |

#### 4.3 Financial Capacity Check

| Check | Question |
|-------|----------|
| Bank guarantee capacity | Can they cover the required total bond amount? |
| Payment terms | Can they work with the required payment terms? |
| Pre-financing | Can they start with their own capital until first payment? |
| Performance-based payments | Can they withstand HSE/Quality performance deduction risk? |

---

### STAGE 5: Comparative Analysis

#### 5.1 Bid Comparison Table

This table is filled for each incoming bid:

| Criterion | Company A | Company B | Company C | Internal Estimate |
|-----------|-----------|-----------|-----------|-------------------|
| Total price (USD) | | | | |
| Total MH | | | | |
| Avg. hourly rate (USD/MH) | | | | |
| Labor / Total (%) | | | | |
| Material / Total (%) | | | | |
| Indirect / Direct (%) | | | | |
| Commercial deviation count | | | | |
| Technical deviation count | | | | |
| Missing document count | | | | |
| Execution plan quality | ☆☆☆ | ☆☆☆ | ☆☆☆ | — |
| Reference project experience | | | | — |

#### 5.2 Scoring Matrix

| Criterion | Weight | Description |
|-----------|--------|-------------|
| **Price** | 40% | Lowest price = 100 points, others proportional |
| **Technical competence** | 25% | Execution plan, equipment, experience |
| **Commercial compliance** | 15% | Deviation count and severity |
| **MH consistency** | 10% | Alignment with reference values |
| **Organization** | 10% | Manpower histogram, camp plan, HSE |

> Weights can be adjusted per project. Increase technical weight for critical projects.

---

## 3. RISK ASSESSMENT

Typical risks that should be included in the bidder's price:

| Risk | Check Question |
|------|----------------|
| Concurrent subcontractor coordination | Has productivity loss been accounted for? |
| Brownfield/existing facility proximity | Are additional permit and safety costs included? |
| Weather conditions | Has seasonal efficiency factor been applied? |
| Precommissioning costs | Are temporary equipment and utilities included? |
| Procedure compliance (QCP, ITP, MS) | Is QA/QC team size adequate? |
| Scaffolding | Have height coefficients been calculated? |
| Hazardous area (ATEX/Ex-proof) | Is certified material cost differential included? |
| Currency risk | Is it USD-based, or is there other currency risk? |
| Transportation/logistics | Is FOB/CIF/DDP basis clear? |

---

## 4. TYPICAL PAYMENT AND BOND STRUCTURE (REFERENCE)

### Payment Structure (EPC Construction — Typical)

| Payment | Typical Rate | Condition |
|---------|-------------|-----------|
| Down Payment | 5-10% | Against bond |
| Mobilization | 3-5% | Mobilization plan approval |
| Work progress (Monthly) | 65-80% | Monthly progress certificate approval |
| Performance payment (HSE/Quality) | 3-7% | Subject to performance criteria |
| Work completion (Retention) | 5-10% | Completion Certificate |

### Bond Requirements (Typical)

| Bond | Typical Rate |
|------|-------------|
| Performance Bond | 5-10% |
| Down Payment Bond | Equal to down payment amount |
| Retention Bond | 5-10% |
| Parent Company Guarantee | Variable |

### Delay Penalty (LD — Typical)

| Penalty | Typical Rate | Typical Cap |
|---------|-------------|-------------|
| Milestone delay | 0.05-0.15%/day | Cumulative 5-10% |
| Completion delay | 0.10-0.20%/day | Cumulative 5-10% |

---

## 5. VARIATION (EXTRA WORK) MULTIPLIERS (REFERENCE)

| Working Condition | Typical Multiplier |
|-------------------|-------------------|
| Normal working hours | 1.00 |
| Overtime (daytime) | 1.10-1.25 |
| Night shift | 1.25-1.50 |
| Sunday/public holiday | 1.50-2.00 |
| Stand-by (labor) | 70-80% |
| Stand-by (equipment) | 50-60% |

### Scaffolding Height Coefficients (Typical)

| Height | Coefficient |
|--------|------------|
| 0-10m | 1.00 |
| 10-20m | 1.05-1.15 |
| 20-30m | 1.15-1.30 |
| 30-40m | 1.30-1.50 |
| 40m+ | 1.50-1.80 |
| Confined space/inside tank | 1.80-2.00 |

---

## 6. EPC TENDER DOCUMENT STRUCTURE (REFERENCE)

Typical document structure expected in an EPC construction tender:

```
1. Technical Information
   ├── 1.1 Scope of Work (SOW/CSA)
   ├── 1.2 Time Schedule (CSC)
   ├── 1.3 Drawings & Specifications (CSD)
   ├── 1.4 Construction Procedures (CSE)
   ├── 1.5 Quality Requirements (CSF)
   ├── 1.6 HSE Requirements (CSG)
   └── 1.7 Coordination Procedures (CSH)

2. Commercial Information
   ├── 2.1 Draft Contract (CS)
   ├── 2.2 Terms & Conditions (TC + Annexes)
   └── 2.3 Commercial Terms (CSB + PS + PSSummary + PD)

3. Forms for Bidders
   ├── 3.1 Call for Bid Letter (CFB)
   ├── 3.2 Clarification Log
   └── 3.3 Technical Bid Forms
```

| Prefix | Document Type |
|--------|--------------|
| CSA/SOW | Scope of Work |
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

---

*This guide provides a general framework for evaluating bids in any Oil & Gas EPC construction tender. It should be adapted to each project's specific conditions. Project-specific details can be found in the analysis documents within the relevant project folder.*
