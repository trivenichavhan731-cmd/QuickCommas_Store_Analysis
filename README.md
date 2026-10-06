# Store Performance Insights – Lane 1

Analysis of 10 Noida dark stores, built from an Excel store-operations dashboard. It answers one business question: **which stores make money, and which lose?**

## Project Files

| File | Description |
|------|-------------|
| `insights.pptx` | 8-slide insights deck |
| `store_operations_zepto_style_dashboard.xlsm` | Excel dashboard (Store Operations Dashboard) |
| `orders.csv` | Order-level data (52,133 orders, 18 May – 28 Jun 2026) |
| `store_master.xlsm` (Lane 1 table 1) | Store details: rent, sqft, staff, cold storage, city |
| `store_hours.csv` (Lane 1 table 2) | Weekly operating hours per store |

## Business Question

Lane 1 – Store Performance: *Which stores make money, and which lose?*

## Dashboard Overview

The dashboard has KPI cards (Monthly Rent, Average Gross Revenue, Average Net Amount, Average Profit Margin) and four charts:

- Total Contribution by Store
- Total Discount by Store
- Total Revenue by Store
- Total Gross Amount by Store

A store filter (`store_id`) controls the whole dashboard.

## Key Insights

1. **Network average per store:** gross revenue ₹28.73L, net revenue ₹27.16L, contribution ₹4.42L.
2. **Top earners:** S06, S01, S02 and S04 each contribute ₹5.4–5.8L in six weeks.
3. **Discount problem:** S03 and S07 discount 9.1% of gross sales, against about 4.5% at the other stores.
4. **Root cause:** the `FRESH50` promo. About 11% of S03 and S07 orders use it, against under 1% elsewhere. It costs about ₹1.8L at each store, against about ₹0.2L at peers.
5. **Quality issues at S03 and S07:**
   - Return rate: 7.9% (S03) and 14.0% (S07), against about 3.2% elsewhere.
   - Late deliveries: 62%, against about 41% elsewhere.
6. **After rent:** S07 loses about ₹1.16L and S03 barely breaks even (₹0.31L). The other stores clear ₹1.9–3.6L.
7. **S09** opened on 15 June. It already earns about ₹12.5K a day, close to S01's ₹13.8K.
8. **Data gap:** the hours file has no Tuesday or Wednesday rows for S05 and no Sunday row for S10, yet both stores took orders on those days.

## Store Summary

| Store | Orders | Contribution (₹) | Discount % | After rent (₹) |
|-------|-------:|-----------------:|-----------:|---------------:|
| S06 | 6,153 | 5,81,602 | 4.1% | 3,60,402 |
| S01 | 6,091 | 5,79,937 | 4.6% | 3,30,737 |
| S02 | 5,877 | 5,63,371 | 4.6% | 3,36,571 |
| S04 | 5,622 | 5,39,231 | 4.5% | 3,26,431 |
| S10 | 5,327 | 5,13,787 | 4.6% | 2,82,787 |
| S08 | 5,309 | 5,12,031 | 4.3% | 3,07,631 |
| S05 | 4,688 | 4,49,633 | 4.5% | 1,96,233 |
| S03 | 5,564 | 3,05,530 | 9.1% | 31,130 |
| S07 | 5,687 | 2,02,788 | 9.1% | **−1,16,412** |
| S09 | 1,815 | 1,75,165 | 4.4% | 94,898 |

## Recommendations

1. Cap or end `FRESH50` at S03 and S07.
2. Investigate the return and late-delivery spike at those two stores.
3. Review S07's lease and cost base. It cannot cover ₹2.28L monthly rent.
4. Fix the hours file for S05 and S10.

## Metric Definitions

- **Gross amount:** order value before discount.
- **Net amount:** gross amount minus discount.
- **Contribution:** net amount − COGS − delivery cost.
- **Discount %:** total discount ÷ total gross amount.
- **After rent:** contribution − (monthly rent × days traded ÷ 30). Staff cost is not included.
- The dashboard's "Average Profit Margin" card is the average contribution per store.
- All figures include every order status (delivered, returned, cancelled), as on the dashboard.

## Tools Used

- Microsoft Excel (PivotTables and PivotCharts)
- Python (pandas) for analysis
- PowerPoint for the insights deck

## Author

Triveni Chavhan
