# Hermès Resale Index: open data

Monthly aggregates of **pre-owned Hermès handbag asking prices** (Birkin, Kelly, Constance), compiled by
[BirkinBagStock](https://birkinbagstock.com), an independent index of live listings from 70+ resellers worldwide, plus
Hermès auction results.

| File | What it is |
|---|---|
| `data/2026-10/asking_prices_by_model_size_leather.csv` | Live asking prices on 7 Oct 2026, by model, model and size, and model, size and leather: number of live listings, number of resellers, median, P25 and P75 in USD |
| `data/2026-10/report-summary.json` | Findings from the [Hermès Resale Report, October 2026](https://birkinbagstock.com/reports/hermes-resale-october-2026), with sample sizes and caveats |

## How to read it

- **Asking prices, not completed sales.** A listing is an offer at a reseller; it is not a transaction.
- Prices in other currencies are converted to USD with that day's reference rates.
- A cohort is published only if it has **10 or more live listings from 3 or more resellers**. Condition, colour, year and
  hardware are **not** held constant inside a cohort.
- Birkin 20 is dominated by limited Faubourg, Sellier and exotic pieces, so its median is far above the larger sizes.
- Not affiliated with Hermès. We do not authenticate bags.

Live numbers, methodology and per-model pages: https://birkinbagstock.com · API and MCP: https://birkinbagstock.com/developers ·
Embeddable live price widget: https://birkinbagstock.com/widgets

## License and citation

Data under **CC BY 4.0**. Please credit «BirkinBagStock (birkinbagstock.com)» with a link. See `CITATION.cff`.
New monthly snapshots are added as `data/YYYY-MM/`.
