# SP01 ELECTRICAL PRICING METHODOLOGY — REV2 (MARKET PRICED)
## Where I Got It, What Information I Used, and How I Priced It

**Date:** 07 March 2026 — REV2
**Project:** 218857C — SOCAR New Refinery Sumgayit — SP01
**Approach:** PURE COST (actual cost to the company, NO profit/overhead/buffer)

---

## 1. PURE COST PHILOSOPHY

This bid is a **straightforward cost calculation.** Nothing has been added on top:
- NO profit margin
- NO regional difficulty multiplier (not embedded in productivity)
- NO buffer/contingency
- NO overhead

The question for each item is: **"What does it actually cost the company to do this work on site?"**

---

## 2. SOURCE DOCUMENTS USED

### 2.1 Primary Sources (Tender Documents)

| Document | File Name | Pages | What I Extracted |
|----------|-----------|-------|------------------|
| **SOW-1600** | 218857C-00-SOW-1600-0000-A.pdf | 152 | Scope definitions, system structure (1610-1690), test requirements |
| **PD-1600** | 218857C-00-PD-1600-0001-A.pdf | 28 | Measurement conventions, unit price definitions |
| **PS-1600** | 218857C-000-PS-1600-0001-A.xlsx | 824 rows | 147 active items, formula structure |
| **CSB-1000-0001** | 218857C-00-CSB-1000-0001_A.pdf | 28 | Payment structure, indirect definitions |
| **SOW-9000** | 218857C-00-SOW-9000-0000-A.pdf | 35 | Test procedures |

---

## 3. LABOUR COST: 5.00 USD/MH

### Calculation

The **actual cost** of employing one electrician on site in Sumgayit for 1 hour:

| Item | Monthly (AZN) | Monthly (USD) | Hourly (USD) |
|------|---------------|---------------|--------------|
| Wage/daily pay (skilled electrician) | 1,200 | 706 | 3.21 |
| SSC/social charges (22%) | 264 | 155 | 0.71 |
| Meals (on site, daily) | 250 | 147 | 0.67 |
| Transportation (Baku-Sumgayit) | 200 | 118 | 0.53 |
| PPE (amortized) | 50 | 29 | 0.13 |
| Hand tools (amortized) | 30 | 18 | 0.08 |
| **TOTAL** | **1,994** | **1,173** | **5.33** |

**Rounded: 5.00 USD/MH**

Working regime: 10 hours/day x 22 days/month = 220 hours/month
Exchange rate: 1 USD = 1.70 AZN

### NOT INCLUDED (to be calculated separately)
- Scaffolding cost
- Test equipment rental
- Supervision/foreman wages
- Project management
- Camp/accommodation (for remote sites)
- Mobilisation/demobilisation

---

## 4. PRODUCTIVITY: PURE FIELD DATA

### Approach
For each item: **"How many hours does it actually take one electrician to do this work?"**

No multiplier was applied. Regional difficulty, weather conditions, congestion — these are evaluated as separate risk items and are not embedded in the unit price.

### Reference Sources
- Field experience-based EPC refinery productivity norms
- Richardson International Construction Factors (base values)
- Technip reference values in PS-1600 column T (for comparison purposes)

### Example Values

| Work | Unit | Productivity | Description |
|------|------|-------------|-------------|
| 2.5mm2 cable pulling | m | 0.05 MH/m | ~20 m/hour, 2-person crew |
| 70mm2 cable pulling | m | 0.13 MH/m | ~8 m/hour, heavier |
| 240mm2 cable pulling | m | 0.22 MH/m | ~5 m/hour, drum+pulling |
| Cable tray installation | m | 0.45 MH/m | Support+installation+earthing |
| MV cable termination | ea | 4.80 MH/ea | Specially trained personnel |
| LV 6mm2 termination | ea | 0.80 MH/ea | Stripping+connector+test |
| Transformer installation | ea | 224 MH/ea | 4 persons x 7 days (including oil) |
| Heat trace cable laying | m | 0.10-0.14 MH/m | On pipe, tape+clips |

---

## 5. MATERIAL PRICES: PURE PROCUREMENT COST

### Principle
The **actual cost** of purchasing the material for the company. No profit.

### Free-issue vs Procurement

| Category | Decision | Column M |
|----------|----------|----------|
| Transformers, switchgear, MCC, UPS, VFD, battery | Free-issue (Contractor supply) | 0 |
| Cable (power, control, signal) | Subcontractor supply | Market price |
| Earthing conductor | Subcontractor supply | Market price |
| Cable tray/ladder | Subcontractor supply | Market price |
| Heat tracing cable | Subcontractor supply | Market price |
| Lighting fixture (Ex-proof) | Subcontractor supply | Market price |
| Conduit/pipe | Subcontractor supply | Market price |

### Price Sources
- LME copper index (March 2026) → main cable cost input
- Turkey/CIS distributor prices (FOB + freight to Sumgayit)
- Heat tracing: Thermon/Raychem/Pentair manufacturer price lists
- Ex-proof fixtures: Dialight/Cooper Crouse-Hinds/R.STAHL
- Cable tray: Cablofil/OBO/Niedax type HDG

---

## 6. RESULTS BY SYSTEM (REV2 — MARKET PRICED)

| System | Labour ($) | Material ($) | Total ($) | % |
|--------|-----------|-------------|----------|---|
| 1610 Earthing | 115,800 | 493,198 | 608,998 | 7.2% |
| 1620 Substation | 46,505 | 224,714 | 271,220 | 3.2% |
| 1630 Power Cabling | 116,520 | 4,380,472 | 4,496,992 | 53.4% |
| 1650 Heat Tracing | 112,881 | 1,903,438 | 2,016,320 | 23.9% |
| 1670 Cathodic Protection | 3,176 | 46,389 | 49,565 | 0.6% |
| 1680 Lighting | 44,071 | 931,810 | 975,881 | 11.6% |
| **TOTAL** | **438,953** | **7,980,022** | **8,418,975** | **100%** |

**Total man-hours: 87,711 MH**
**Labour/Material ratio: 5.2% / 94.8%**
**Average pure labour rate: 5.00 USD/MH**

---

## 7. REVISION HISTORY

| Parameter | REV0 (Regional Multiplier) | REV1 (Pure, Old Material) | REV2 (Market Priced) |
|-----------|---------------------------|--------------------------|---------------------|
| Total cost | 4,375,283 USD | 3,317,991 USD | **8,418,975 USD** |
| Total man-hours | 108,784 MH | 87,711 MH | 87,711 MH |
| Labour ratio | 80.1% | 13.2% | 5.2% |
| Material ratio | 19.9% | 86.8% | 94.8% |
| Hourly rate | 8.00 USD/MH | 5.00 USD/MH | 5.00 USD/MH |
| Regional multiplier | x1.25 | NONE | NONE |
| Material price source | Training data estimate | Training data estimate | **Actual market research** |

### Main reason for REV1 to REV2 difference:
1. **LME copper 12,750 USD/ton** — 70-80% of cable price is copper. Old estimates were producing results based on ~7,000-8,000 USD/ton.
2. **Actual heat trace prices** — MI cable 40 USD/m (old: 15), hazloc self-reg 11.25 USD/m (old: 7)
3. **Ex-proof fixture ATEX cost** — Actually 300-1,500 USD/ea (old: 100 USD)
4. **Detailed verification:** All sources and URLs are documented in the Price Verification Report (SP01-PRICE-VERIFICATION-REPORT.md).

---

## 8. ASSUMPTIONS

| No | Assumption |
|----|-----------|
| 1 | All major equipment (transformer, switchgear, MCC, UPS) is free-issue |
| 2 | Cable, earthing, tray, fixture = Subcontractor supply |
| 3 | Pure hourly rate: 5.00 USD/MH (Azerbaijan local, fully burdened) |
| 4 | No regional multiplier — productivity is pure field data |
| 5 | Material prices FOB Turkey + freight to Sumgayit |
| 6 | Cable measurement: net length (excluding waste, per PD rules) |

---

## 9. NOTE FOR SUBSEQUENT STEPS

The following items will be added as separate line items on top of this pure cost:
- Scaffolding cost (typically 8-15% of direct cost)
- Test equipment rental (~150-300K USD)
- Supervision/foreman (foreman x months x rate)
- Project management (PM + planner + QC + HSE)
- Mobilisation/demobilisation
- Contingency (5-10%)
- Profit margin (project-dependent)

**All of these items will go into the Indirect Cost (B) section of PSSummary.**

---

*REV2 — Material prices updated with actual market data. LME copper + verified retail prices used as basis. Details: SP01-PRICE-VERIFICATION-REPORT.md*
