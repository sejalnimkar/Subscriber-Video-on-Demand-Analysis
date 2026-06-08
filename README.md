# US SVOD Market Analysis: 2021–2022

An end-to-end analysis of the US subscription video-on-demand (SVOD) market covering 114 streaming services across 2021–2022, combining Python-based metric computation with an interactive Tableau dashboard.

---

## Overview

This project analyzes subscriber growth, market concentration, and competitive dynamics across the US streaming landscape. The analysis surfaces which platforms gained or lost subscribers, how market power shifted between incumbents and challengers, and which services launched or shut down during the period.

---

## Key Findings

- **15.3% overall market growth** from 2021 to 2022 (442M → 510M total subscribers)
- **93% of services grew** — only 8 of 114 platforms experienced subscriber decline
- **Market diversified**: top-3 concentration dropped 6.1 percentage points, from 49.7% to 43.6%
- **Paramount+** led absolute growth with +14.98M subscribers (Q4 YoY)
- **Netflix** was the largest decliner at −795K subscribers
- **9 services shut down** (including WWE Network, NHL.TV, Bleacher Report Live); **4 new services launched** (including NFL+, Vix Premium)

---

## Dashboard

Built in Tableau Public — two pages:

**Page 1 — US SVOD Market Performance: 2021–2022 Evolution**
- KPI cards: year-end market growth, platform expansion velocity, expansion breadth, attrition rate, new launches, closures
- Subscriber Acquisition Leaders (Q4 YoY) — horizontal bar chart
- Services with Audience Contraction — negative bar chart

**Page 2 — Competitive Landscape & Strategic Growth Trends**
- 8-quarter longitudinal subscriber trend line with per-service dropdown filter
- Top 10 services by subscription volume — donut chart with 2021/2022 toggle

🔗 [View Dashboard on Tableau Public](#) ← *replace with your link*

---

## Project Structure

```
├── svod_market_analysis.ipynb   # Python analysis & metric computation
├── Data.csv                     # Cleaned subscriber data
├── svod_timeline_continuous.csv # Exported timeline for Tableau
├── qoq_growth_rates.csv         # Quarter-over-quarter growth rates
└── README.md
```

---

## Methodology

- **Data source**: Dataxis SVOD subscriber dataset (monthly KPI values per platform, 2021–2022)
- **Metrics computed**: 8 core metrics (avg growth, gainer/decliner counts, service launches/closures) + advanced metrics (weighted market growth, market concentration, QoQ trends, top gainers/decliners)
- **Target encoding approach**: subscriber values aggregated at platform level for cross-platform comparisons
- **Dashboard data prep**: timeline CSV exported from Python, loaded into Tableau with a star-style relationship model

---

## Tech Stack

| Tool | Use |
|------|-----|
| Python (Pandas, NumPy) | Data cleaning, metric computation, CSV export |
| Tableau Public | Interactive dashboard, KPI cards, trend visualizations |

---

## How to Run

```bash
pip install pandas numpy
jupyter notebook svod_market_analysis.ipynb
```

Data CSVs are included. Tableau dashboard is published publicly — no local Tableau install needed to view it.
