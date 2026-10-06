# Store Operations Dashboard: Store Performance Insights

Hackathon project analysing 10 Noida dark stores (18 May – 28 Jun 2026).
**Lane 1 question:** *Which stores make money, and which lose?*

## Team

| Member | Lane | Slack |
|---|---|---|
| Triveni Chavhan | Lane 1: Store Performance | n/a |
| Rohit | Lane 2: Product & Cost Analysis | [Slack](https://7damwfaprilbatch.slack.com/archives/C0C4UF2TMQE/p1791263130121459) |
| Monika | Lane 3: Opreational Analysis| [Slack](https://7damwfaprilbatch.slack.com/archives/C0C4UF2TMQE/p1791263132835189) |

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
1. **Top earners:** S06, S01,
