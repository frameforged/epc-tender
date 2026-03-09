# Budget Template Structure (Excel / XLSX)

## General Structure

Every budget file uses the following sheet structure.

---

## Sheet 1: SUMMARY

| Column | Content |
|--------|---------|
| A | Item No |
| B | Main Category |
| C | Description |
| D | Total Cost (USD) |
| E | Percentage (%) |

Main categories:
1. Electrical Materials
2. Mechanical Materials
3. Instrumentation Materials
4. Civil/Structural Materials
5. Electrical Labor
6. Mechanical Labor
7. Instrumentation Labor
8. Civil/Structural Labor
9. Equipment Rental
10. Engineering and Project Management
11. HSE
12. Logistics and Freight
13. Insurance
14. Camp/Accommodation
15. Mobilization/Demobilization
16. Contingency
17. Profit Margin
18. **GRAND TOTAL**

Sub-section: Project information (project name, date, revision no, prepared by, client)

---

## Sheet 2: ELECTRICAL MATERIALS

| Column | Content |
|--------|---------|
| A | Seq No |
| B | SOW Reference No |
| C | Material Code |
| D | Material Description |
| E | Technical Specification |
| F | Unit |
| G | Quantity |
| H | Unit Price (USD) |
| I | Total Price (USD) = G x H |
| J | Brand / Origin |
| K | Price Source |
| L | Source Date |
| M | Notes |

---

## Sheet 3: MECHANICAL MATERIALS

Same column structure (same as Sheet 2)

---

## Sheet 4: INSTRUMENTATION MATERIALS

Same column structure

---

## Sheet 5: CIVIL/STRUCTURAL MATERIALS

Same column structure

---

## Sheet 6: MAN-HOURS CALCULATION

| Column | Content |
|--------|---------|
| A | Seq No |
| B | Work Item |
| C | Discipline (Electrical/Mechanical/Instrumentation/Civil) |
| D | Unit |
| E | Quantity |
| F | Base Man-Hour/Unit |
| G | Productivity Factor |
| H | Total Man-Hours = E x F x G |
| I | Personnel Type |
| J | Hourly Rate (USD/hour) |
| K | Total Labor Cost (USD) = H x J |
| L | Note |

Sub-section: Total man-hour summary (by discipline)

---

## Sheet 7: EQUIPMENT / TOOLS

| Column | Content |
|--------|---------|
| A | Seq No |
| B | Equipment Name |
| C | Capacity/Spec |
| D | Quantity |
| E | Usage Duration (days) |
| F | Unit Cost (USD/day or USD/month) |
| G | Total Cost (USD) |
| H | Rental/Purchase |
| I | Mobilization Cost (USD) |
| J | Note |

---

## Sheet 8: INDIRECT COSTS

| Column | Content |
|--------|---------|
| A | Item No |
| B | Description |
| C | Calculation Method |
| D | Rate (%) or Amount (USD) |
| E | Base Amount (USD) |
| F | Total (USD) |

Items: Project management, QA/QC, HSE, Insurance, Logistics, Camp, Mob/Demob, Administrative expenses

---

## Sheet 9: REFERENCES / SOURCES

| Column | Content |
|--------|---------|
| A | Seq No |
| B | Material / Item |
| C | Source Name |
| D | URL |
| E | Access Date |
| F | Price (USD) |
| G | Currency (Original) |
| H | Exchange Rate |
| I | Note |

---

## Sheet 10: RISK AND CONTINGENCY

| Column | Content |
|--------|---------|
| A | Risk Description |
| B | Probability (Low/Medium/High) |
| C | Impact (USD) |
| D | Risk Score |
| E | Mitigation Measure |
| F | Contingency Amount (USD) |

---

## Formatting Rules

1. **Currency**: All amounts in USD, right-aligned, thousands separator comma, 2 decimals
2. **Headers**: Bold, background color: dark blue (#1F4E79), white text
3. **Subtotals**: Light blue background (#D6E4F0), bold text
4. **Grand total**: Dark background (#1F4E79), white text, bold
5. **Borders**: Thin borders on all cells
6. **Column widths**: Auto-fit to content
7. **Page header**: Project name, date, revision number on every sheet
8. **Print setup**: Landscape orientation, A3 size, page numbers
9. **Formulas**: Total and subtotal cells must use SUM formulas
10. **Verification**: SUMMARY sheet total = detail sheet totals (cross-check)
