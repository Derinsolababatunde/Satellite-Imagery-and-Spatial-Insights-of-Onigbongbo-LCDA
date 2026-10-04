# Sprint 4: Satellite Imagery to Spatial Intelligence

Development Change Analysis: Onigbongbo LCDA (2016–2026)

---

## Key Finding

**All five wards show NEGATIVE development change** — built-up area decreased from 2016 to 2026.

---

## Development Change Results

| Ward | 2016 Built-up (%) | 2026 Built-up (%) | Change (%) | Indicator |
|------|---|---|---|---|
| **GRA** | 72.11 | 44.66 | **-27.45** | Low |
| **Onigbongbo** | 82.62 | 64.44 | **-18.18** | Low |
| **Opebi** | 74.13 | 71.79 | **-2.34** | Low |
| **Oregun** | 88.60 | 87.66 | **-0.94** | Low |
| **Wasimi** | 41.47 | 41.04 | **-0.43** | Low |

---

## What This Means

**Unexpected Result:** Despite high land prices in Sprint 2 (₦3.5M/sqm in GRA, ₦2M in Opebi), satellite imagery shows a *decrease* in built-up area, not an increase.

### Possible Explanations

1. **Data artifact:** NDBI threshold (0.0) may classify developed areas differently in different years
2. **Vegetation growth:** Green areas expanding (deforestation reversal)
3. **Imagery timing:** Seasonal differences between 2016 and 2026 composites
4. **Market vs. reality:** High prices don't translate to visible construction
5. **Shadow effect:** Tall buildings casting shadows that reduce NDBI values

---

## Key Observations

**Largest decrease:** GRA (-27.45%)
- Highest market value (₦3.5M/sqm) but largest apparent decrease in built-up
- Suggests market signals may not correlate with visible development

**Smallest decrease:** Wasimi (-0.43%)
- Lowest market value (₦260K/sqm) but stable built-up area
- Most stable ward across decade

**Moderate decreases:** Opebi, Oregun (-2.34%, -0.94%)
- Mid-range market prices
- Relatively stable built-up signatures

---

## Comparison: Market vs. Development

**Sprint 2 (Market Prices):**
- GRA: ₦3,500,000/sqm (highest)
- Opebi: ₦2,000,000/sqm
- Onigbongbo: ₦1,550,000/sqm
- Oregun: ₦1,200,000/sqm
- Wasimi: ₦260,000/sqm (lowest)

**Sprint 4 (Development Change):**
- All wards: Negative development change
- GRA & Onigbongbo: Largest decreases (-27.45%, -18.18%)
- Wasimi: Smallest decrease (-0.43%)

**Finding:** Market value does NOT predict visible development growth. This divergence is significant for urban planning.

---

## Important Notes

1. **Negative values are unusual** — typically expect positive development change in growing cities
2. **Recommend further investigation:**
   - Visual inspection of satellite tiles
   - Check if NDBI threshold (0.0) is appropriate for Lagos built-up
   - Compare 2026 satellite composite dates
   - Validate against ground-truth data

3. **Possible next steps:**
   - Lower NDBI threshold to -0.05 or -0.1 (more sensitive)
   - Compare individual years (not annual composites)
   - Inspect raw Landsat bands for anomalies

---

## Methodology

**Data Source:** Landsat 8 (30-meter resolution)
**Index:** Normalized Difference Built-up Index (NDBI)
**Years:** 2016 baseline vs 2026 recent
**Threshold:** NDBI > 0.0 = built-up
**Classification:** All changes <5% = Low

---

## Output Files

- `Development_Change_Dataset.csv` - This results table
- `development_change_bar.png` - Chart visualization
- `development_change.json` - Machine-readable version

---

## Conclusion

Sprint 4 reveals a **critical insight:** market prices in Onigbongbo do not reflect visible physical development in satellite imagery. Either:
- Development is below-ground or not visible to satellites
- Market prices are speculative (not based on built assets)
- Satellite data needs recalibration for Lagos context

There is a disconnect between Sprint 2 (market) and Sprint 4 (satellite) and it is worth looking into
