# Technip Energies ITB Format Reference

## Table of Contents
1. Document Coding System
2. Price Summary Structure
3. Bid Form Requirements
4. SOW Reference System
5. Pre-commissioning/Commissioning Responsibility Matrix

---

## 1. Document Coding System

Technip Energies documents are coded in the following format:

```
[Project No]-[Unit]-[Document Code]-[Area]-[Serial No]_[Rev].pdf
```

Example: `218857C-00-CSA-1000-0001_A.pdf`

### Document Codes (Exhibit Codes):
| Code | Full Name | Content |
|------|-----------|---------|
| CS | Contract/Subcontract | Draft contract |
| CSA | Exhibit A - Scope of Work | Scope definition |
| CSB | Exhibit B - Commercial Terms | Commercial terms |
| CSC | Exhibit C - Time Schedule | Time schedule |
| CSD | Exhibit D - Drawings & Specs | Drawings and specifications (free issue) |
| CSE | Exhibit E - Construction Procedures | Construction procedures |
| CSF | Exhibit F - Quality Requirements | Quality requirements (ITP, JSC, PP) |
| CSG | Exhibit G - HSE Requirements | Occupational health, safety and environmental requirements |
| CSH | Exhibit H - Coordination Procedure | Coordination procedure |
| CFB | Call for Bid Letter | Invitation to bid letter |
| TC | Terms and Conditions | Terms and conditions |
| PS | Price Schedule | Price schedule (detail) |
| PSSummary | Price Summary | Price summary |
| PD | Price Details | Price details |
| CLARIF | Clarification Log | Clarification requests |
| SOW | Scope of Work | Detailed scope of work (by discipline) |

### SOW Discipline Codes:
| Works Code | Discipline |
|-----------|----------|
| 0001 | General Activities |
| 0002 | Indirect Works |
| 1300 | Aboveground Piping |
| 1500 | Instrumentation |
| 1600 | Electricity |
| 1700 | Site Prep, Piling, Roads, UG Networks, Civil |
| 1801 | Structural Steel Erection |
| 2000 | Buildings |
| 2200 | Insulation |
| 2300 | Painting |
| 2500 | Storage Facilities (Tanks) |
| 6800 | Hoisting, Mechanical Assembly |
| 9000 | Pre-commissioning / Commissioning |

---

## 2. Price Summary (PSSummary) Structure

### Discipline Columns:
1. CIVIL WORKS
2. PIPING PREFABRICATION WORKS
3. PIPING ERECTION
4. STEEL STRUCTURE ERECTION
5. MECHANICAL ERECTION
6. PAINTING WORKS
7. INSULATION WORKS
8. ELECTRICAL WORKS
9. INSTRUMENT WORKS
10. TELECOM WORKS
11. PRECOMMISSIONING
12. TOTAL

### (A) DIRECT COSTS Rows:
| Row | Description | Unit |
|-----|-------------|------|
| a) | Direct labour (hand tools, consumables, meals included) | USD |
| b) | Direct labour for scaffolding | USD |
| c) | Direct material (to be incorporated into the facility) | USD |
| d) | Subcontracted works | USD |
| **SUBTOTAL** | **Direct Costs (A)** | **USD** |

### (B) INDIRECT COSTS Rows:
| No | Description | Unit |
|----|-------------|------|
| 1 | Supervision and indirect labour cost | USD |
| 2 | Temporary SITE facilities cost | USD |
| 3 | General field expenses of TSF | USD |
| 4 | Construction equipment cost (excluding Heavy Lifting) | USD |
| 5 | Heavy Lifting Cranes cost | USD |
| 6 | Scaffolding cost | USD |
| 7 | HSE and Security cost | USD |
| 8 | Camp/Accommodation cost (catering, O&M included) | USD |
| 9 | Design and engineering cost | USD |
| 10 | All local levies, duties, taxes | USD |
| 11 | Overheads and profit | USD |
| **SUBTOTAL** | **Indirect Costs (B)** | **USD** |

### Man-Hours Section:
- DIRECT MANHOURS EXCLUDING SCAFFOLDING (NDT, PWHT, Handling included)
- MANHOURS FOR SCAFFOLDING
- DIRECT MANHOURS INCLUDING SCAFFOLDING

### Important Rules:
- Scaffolding MHR and direct cost shall be embedded in each item code's productivity and unit price
- Indirect scaffolding cost is a separate item (B-6)
- Yellow cells are to be filled by the bidder
- Direct costs total = Price List totals (cross-verification mandatory)

---

## 3. Bid Form Requirements

### Part A — Commercial Bid:
| Form | Content |
|------|---------|
| Form 1 | Form of Tender (on company letterhead, signed, with power of attorney) |
| Form 2 | Bid Price Summary (PSSummary file, pdf + xls) |
| Form 3 | Price Schedules (PS files, pdf + xls) |
| Form 4 | Prices of Alternatives |
| Form 5 | Commercial and Contractual Deviations |
| Form 6 | Declaration of Compliance (anti-corruption, Sapin 2, FCPA, UK Bribery Act) |

### Part B — Technical Bid:
| Form | Content |
|------|---------|
| Form 7 | Execution Plan |
| Form 8 | Direct Manpower Schedule Summary |
| Form 9 | Indirect Manpower Schedule Summary |
| Form 10 | Proposed Sub-subcontractors |
| Form 11 | Outline Schedule, Manpower Histogram, "S" Curves |
| Form 12 | Major Field Equipment List and Schedule |
| Form 13 | List of Proposed Temporary Site Facilities and Utilities |
| Form 14 | Housing and Camp Facilities |
| Form 15 | Alternatives |
| Form 16 | Technical Exceptions and Deviations |
| Form 17 | National Content and Local Communities Development Plan |
| Form 18 | ESG Requirements |

### Submission Format:
- Two separate ZIP files: "Part A" (commercial + technical) and "Part B" (technical)
- Microsoft Word and Excel compatible
- Bid Forms 2 and 3 are mandatory in .xls format

---

## 4. SOW Reference System

SOW documents for each package have two tiers:

**Tier 1 — General (applicable to all disciplines):**
- SOW-X000-0001: General Activities
- SOW-X000-0002: Indirect Works

**Tier 2 — Discipline-specific:**
- SOW-1300-0000: Aboveground Piping
- SOW-1500-0000: Instrumentation
- SOW-1600-0000: Electricity
- SOW-1700-0000: Civil Works
- SOW-1801-0000: Structural Steel
- SOW-2000-0000: Buildings
- SOW-2200-0000: Insulation
- SOW-2300-0000: Painting
- SOW-2500-0000: Storage Facilities
- SOW-6800-0000: Hoisting, Mechanical Assembly
- SOW-9000-0000: Pre-commissioning/Commissioning

**Key Principle:** EVERYTHING not within the Contractor's scope is automatically within the Subcontractor's scope and is included in the SUBCONTRACT PRICE.

---

## 5. Pre-commissioning/Commissioning (SOW-9000) Responsibility Codes

- **X** = Perform the Work
- **A** = Provide Assistance on reimbursable basis

### Subcontractor's Pre-commissioning Responsibilities (main items):
- Facility inspection (P&ID, GA, hook-up, isometric compliance check)
- Cold alignment and adjustment checks
- Circuit cleaning
- Reinstatement & tightness
- Energization tests (loop check, electrical settings)
- Building functional tests
- Punch list close-out
- Preservation and maintenance
- Temporary spool fabrication
- Temporary equipment supply (compressor, pump, dryer, etc.)
- Utilities supply (water, air, nitrogen)
- Scaffolding erection/maintenance/dismantling
- Method statement and working folder preparation
- Red-line mark-up (as-built)
- Daily report (before 10:00 AM)
- Job Hazard Analysis
- Permit to Work preparation
- LOTO personnel
- Temporary fire suppression
- Waste disposal

### Commissioning Pricing:
- Pre-commissioning is included in the SUBCONTRACT PRICE (lump sum)
- Commissioning assistance is paid via VARIATION (reimbursable)
