# Hermès Resale Index: open data

Monthly aggregates of **pre-owned Hermès handbag asking prices** (Birkin, Kelly, Constance), compiled by
[BirkinBagStock](https://birkinbagstock.com), an independent index of live listings from 130 resellers worldwide, plus
Hermès auction results.

| File | What it is |
|---|---|
| `data/black-friday-2026/baseline-2026-11-08.json` | Black Friday 2026 tracker, pre-season baseline (8 Nov 2026): median, P25 and P75 asking prices for Birkin 25/30/35, Kelly 25/28 and all Birkin, plus the share of listings with a price cut of 3 % or more in the previous 7 and 14 days (native currency). Article: [Birkin Black Friday 2026 price tracker](https://birkinbagstock.com/blog/birkin-black-friday-2026-price-tracker). A follow-up snapshot after Cyber Monday (30 Nov 2026) will be added in the same folder |
| `data/auctions/2026-11/hermes_auction_results_by_sale_and_model.csv` | Hermès handbag auction results by sale and model, as of 9 Nov 2026 (16 sales from 14 auction houses, July to November 2026): lots with a result, lots sold, sell-through, and median, P25, P75 and top price in each sale's own currency and price basis, with a link to each sale's results page. Updated daily on [Hermès auction results](https://birkinbagstock.com/auctions/results), with [Birkin](https://birkinbagstock.com/auctions/results/birkin) and [Kelly](https://birkinbagstock.com/auctions/results/kelly) results |
| `data/2026-11/asking_prices_by_model_size_leather.csv` | Live asking prices on 1 Nov 2026 (13,607 priced handbag listings, 126 resellers), by model and size, and model, size and leather: live listings, resellers, median, P25, P75, P10 and P90 in USD |
| `data/2026-11/report-summary.json` | Headline numbers from the [Hermès Resale Report, November 2026](https://birkinbagstock.com/reports/hermes-resale-november-2026), with sample sizes and caveats |
| `data/2026-10/asking_prices_by_model_size_leather.csv` | Live asking prices on 7 Oct 2026, by model, model and size, and model, size and leather: number of live listings, number of resellers, median, P25 and P75 in USD |
| `data/2026-10/report-summary.json` | Findings from the [Hermès Resale Report, October 2026](https://birkinbagstock.com/reports/hermes-resale-october-2026), with sample sizes and caveats |

## How to read it

- **Asking prices, not completed sales.** A listing is an offer at a reseller; it is not a transaction.
- Prices in other currencies are converted to USD with that day's reference rates.
- A cohort is published only if it has **10 or more live listings from 3 or more resellers**. Condition, colour, year and
  hardware are **not** held constant inside a cohort.
- The November file adds P10 and P90 and has no model-wide (all sizes) rows; size and size-plus-leather rows follow the same gate.
- Birkin 20 is dominated by limited Faubourg, Sellier and exotic pieces, so its median is far above the larger sizes.
- Not affiliated with Hermès. We do not authenticate bags.

Auction prices stay in the sale's currency (EUR, GBP or HKD) and on the basis the house publishes: `hammer` excludes the buyer's premium and `premium` includes it. They are never converted or mixed. A row needs 3 or more Hermès handbag lots with a result in that sale and model; unsold lots count toward sell-through. Source: results published by each auction house.

The Black Friday file measures **advertised asks before the shopping weekend**, not sales or Hermès promotions. Kelly cut rates are `null` in the baseline because the daily price recorder covered Birkin only until then (all-style capture is planned from 9 Nov 2026); a null rate is not evidence that prices held.

Also on Hugging Face: https://huggingface.co/datasets/birkinbagstock/hermes-resale-index

## Live data pages

The CSV is a monthly snapshot. The same data, updated daily:

- [Hermès Birkin and Kelly asking prices by country](https://birkinbagstock.com/market/by-country)
- [Today's market: live listings by model, size and leather](https://birkinbagstock.com/market/today)
- [Hermès auction results](https://birkinbagstock.com/auctions/results), with [Birkin](https://birkinbagstock.com/auctions/results/birkin) and [Kelly](https://birkinbagstock.com/auctions/results/kelly) results
- [Upcoming auctions with Hermès lots](https://birkinbagstock.com/auctions)

Live numbers, methodology and per-model pages: https://birkinbagstock.com · API and MCP: https://birkinbagstock.com/developers ·
Embeddable live price widget: https://birkinbagstock.com/widgets

## License and citation

Data under **CC BY 4.0**. Please credit «BirkinBagStock (birkinbagstock.com)» with a link. See `CITATION.cff`.
New monthly snapshots are added as `data/YYYY-MM/`.
