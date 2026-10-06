# Store Operations Dashboard: Store Performance Insights

Hackathon project analysing 10 Noida dark stores (18 May – 28 Jun 2026).
**Lane 1 question:** *Which stores make money, and which lose?*

## Team

| Member | Lane |
|---|---|
| Triveni Chavhan | Lane 1: Store Performance |
| Rohit | Lane 2: Product & Cost Analysis |
| Monika | Lane 3: Operational Analysis |

## Lane 1: Store Performance

**Files owned:** `dark_stores_messy.csv`, `store_hours_messy.csv`, plus `orders.csv` for the metrics.

### Deliverables
- `store_operations_zepto_style_dashboard.xlsx`: Excel dashboard (KPI cards, contribution, discount, revenue and gross charts, store filter)
- `insights.pptx`: 8-slide insights deck

### Data used
| File | Contents |
|---|---|
| `orders.csv` | 52,133 orders: gross, discount, net, COGS, delivery cost, contribution, lateness, promo flags |
| Store master | store name, sqft, monthly rent, staff count, cold storage capacity, opened date |
| Store hours | open and close time per store per weekday |

### Key metrics
- **Contribution** = net amount − COGS − delivery cost
- **Contribution after rent** = contribution − (monthly rent × days traded ÷ 30). Staff cost is not included.
- Dashboard KPI cards are averages across all 10 stores. The "Average Profit Margin" card is average contribution (₹4.42L).

### Key findings
1. **Top earners:** S06, S01, S02 and S04 each contribute ₹5.4–5.8L.
2. **S07 loses money:** about −₹1.16L after rent (highest rent, ₹2.28L a month, and the lowest contribution).
3. **S03 is at risk:** only +₹0.31L after rent.
4. **Cause:** the FRESH50 promo. S03 and S07 give about ₹1.8L of FRESH50 discount each against ₹16–25K elsewhere, a 9.1% discount rate against about 4.5%. They also have higher returns (7.9% and 14.0%) and 62% late deliveries against about 41%.
5. **S09** opened on 15 June and already earns ₹12.5K a day, close to the network average.
6. **Data gap:** the hours file has no Tuesday or Wednesday rows for S05 and no Sunday row for S10, yet both stores took orders on those days.

### Recommendations
1. Cap or end FRESH50 at S03 and S07.
2. Investigate the return and late-delivery spike at those stores.
3. Review S07's lease and cost base.
4. Fix the hours file for S05 and S10.

## How to open
1. Download the repo.
2. Open the `.xlsx` in Excel. Use the **store_id** slicer to switch stores.
3. Open `insights.pptx` in PowerPoint.

## Notes
- All figures include every order status (delivered, returned and cancelled), as the dashboard does.
- S09 has only 14 days of data, so compare it per day rather than in total.
