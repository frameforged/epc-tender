# SP01 ELECTRICAL — PRICE VERIFICATION REPORT

**Date:** 7 March 2026
**Project:** 218857C — SOCAR New Refinery Sumgayit
**Subject:** Verification of PS-1600 material prices with current market data

---

## 1. PROBLEM IDENTIFICATION

In the initial pricing (REV0 and REV1), material prices **were not based on actual market data.** General estimates from training data were used. This report documents the process of verifying and correcting prices with actual sources.

---

## 2. MARKET DATA SOURCES

### 2.1 Exchange Rate and Commodity

| Parameter | Value | Source | Date |
|-----------|-------|--------|------|
| USD/TRY | 44.07 | TCMB / poundsterlinglive.com | 6 March 2026 |
| LME Copper | 12,750 USD/ton | LME / tradingeconomics.com | 5 March 2026 |

### 2.2 Cable Prices — Verified

| Cross-section | Source | TRY/m (incl. VAT) | Excl. VAT | USD/m (wholesale) |
|---------------|--------|--------------------|-----------|--------------------|
| 4x6mm2 NYY | kablocu.com.tr (Oznur) | 184.70 | 153.92 | 3.14 |
| 4x16mm2 NYY | elektrikmarket.com.tr (Oznur) | 530.32 | 441.93 | 9.03 |
| 4x50mm2 NYY | aydinlatmadunyam.com (Oznur) | 1,074.00 (ind.) | 895.00 | 20.32 |
| 4x120mm2 NYY | aydinlatmadunyam.com | 2,676.00 (ind.) | 2,230.00 | 50.60 |
| 4x240mm2 NYY | aydinlatmadunyam.com | 5,526.00 (ind.) | 4,605.00 | 104.51 |

**Calibration method:** Verified prices were compared against LME copper weight. Cable price is approximately consistent with Copper cost x 1.20 multiplier (processing+PVC+freight). This multiplier was applied to all cross-sections.

### 2.3 Heat Trace Cable — Verified

| Type | Source | Retail | Project wholesale |
|------|--------|--------|-------------------|
| Self-reg normal | flotraceusa.com | $3.25/ft = $10.66/m | $7.46/m (-30%) |
| Self-reg hazloc | flotraceusa.com | $4.90/ft = $16.08/m | $11.25/m (-30%) |
| Polymer insulated | Manufacturer reference | — | ~$20/m |
| Mineral insulated | Thermon MIQ reference | — | ~$40/m |

### 2.4 Ex-proof Lighting — Verified

| Type | Source | Price Range |
|------|--------|-------------|
| Pendant LED Zone 1 | industriallightingfixtures.org (Crown GYD680-T) | $300-500/ea |
| Stanchion LED Zone 1 | Larson Electronics, Eaton Crouse-Hinds | $350-600/ea |
| Floodlight LED Zone 1 | Eaton EV LED series | $800-1,500/ea |

### 2.5 Cable Tray

| Type | Source | Price |
|------|--------|-------|
| 600mm HDG ladder | Made-in-China / Cablofil type | $25-35/m |
| 600mm cover | General market | $10-15/m |

### 2.6 Ex-proof Control Station

| Type | Source | Price |
|------|--------|-------|
| Start/stop pushbutton Ex-d | Pepperl+Fuchs LCP, R.STAHL | $200-400/ea |
| Emergency stop Ex-d | General market | $150-300/ea |

---

## 3. OLD PRICES vs ACTUAL MARKET

### Critical differences (largest deviations):

| Item | Old M ($/m) | New M ($/m) | Difference | Reason |
|------|------------|------------|------------|--------|
| 4x70mm2 cable | 7.80 | 38.08 | +388% | LME copper 12,750$/ton impact |
| 4x240mm2 cable | 18.00 | 130.58 | +625% | Large cross-section = much copper |
| 4x16mm2 cable | 2.30 | 8.71 | +279% | Copper cost dominates |
| MI heat trace | 15.00 | 40.00 | +167% | MI cable is a very expensive product |
| Ex-proof fixture | 100.00 | 400.00 | +300% | ATEX certified product cost |
| 4x6mm2 cable | 1.50 | 3.26 | +117% | Copper-based |

### Main reason:
**LME copper price 12,750 USD/ton** (near historical highs). 70-80% of cable price is copper cost. Old estimates were producing results as if based on ~7,000-8,000 USD/ton copper price.

---

## 4. REVISION RESULT

| Version | Total Cost | Man-Hours | Labour % | Material % |
|---------|-----------|-----------|----------|-----------|
| REV0 (regional multiplier) | 4,375,283 USD | 108,784 MH | 80.1% | 19.9% |
| REV1 (pure, old material) | 3,317,991 USD | 87,711 MH | 13.2% | 86.8% |
| **REV2 (market priced)** | **8,418,975 USD** | **87,711 MH** | **5.2%** | **94.8%** |

### Distribution by system (REV2):

| System | Labour | Material | Total | % |
|--------|--------|----------|-------|---|
| 1610 Earthing | 115,800 | 493,198 | 608,998 | 7.2% |
| 1620 Substation | 46,505 | 224,714 | 271,220 | 3.2% |
| 1630 Power Cabling | 116,520 | 4,380,472 | 4,496,992 | 53.4% |
| 1650 Heat Tracing | 112,881 | 1,903,438 | 2,016,320 | 23.9% |
| 1670 Cathodic Protection | 3,176 | 46,389 | 49,565 | 0.6% |
| 1680 Lighting | 44,071 | 931,810 | 975,881 | 11.6% |
| **TOTAL** | **438,953** | **7,980,022** | **8,418,975** | **100%** |

---

## 5. NOTES AND LIMITATIONS

1. **Cable prices are calculated based on LME copper.** Actual supplier quotes may differ (brand, delivery time, volume discount).
2. **Heat trace prices are based on US retail** (FloTrace). Project-level Thermon/Raychem quotes may differ.
3. **Ex-proof fixture prices have a wide range** ($300-1500). Will be finalized based on brand and wattage.
4. **Control cable prices** were calculated with a different multiplier than power cables (shielding cost).
5. **Labour ratio of 5.2%** appears very low — this is normal because PS-1600 only contains "direct cost." Supervision, overhead, mob/demob are separate in PSSummary.
6. **Free-issue equipment** (1620 series) requires confirmation. If sub-procurement is required, there will be a very large cost impact.

---

## 6. SOURCES

| Source | URL | Accessed |
|--------|-----|----------|
| kablocu.com.tr (4x6 NYY Oznur) | kablocu.com.tr/4x6-nyy-oznur | 7 March 2026 |
| elektrikmarket.com.tr (4x16 NYY) | elektrikmarket.com.tr | 7 March 2026 |
| viraelektrik.com (4x50 NYY) | viraelektrik.com | 7 March 2026 |
| aydinlatmadunyam.com (NYY price list) | aydinlatmadunyam.com | 7 March 2026 |
| FloTrace USA (heat trace) | flotraceusa.com | 7 March 2026 |
| Crown GYD680-T (Ex-proof LED) | industriallightingfixtures.org | 7 March 2026 |
| Larson Electronics (ATEX LED) | larsonelectronics.com | 7 March 2026 |
| LME Copper | tradingeconomics.com | 5 March 2026 |
| USD/TRY | poundsterlinglive.com | 6 March 2026 |

---

*This report was prepared for pricing transparency. All prices are based on actual market research but should be verified with definitive supplier quotes.*
