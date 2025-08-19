

# Business Insights 360 — Power BI

A self-serve analytics dashboard that brings Finance, Sales, Marketing, Supply Chain and an Executive overview into one place. Built end-to-end with a clean star schema, robust DAX, thoughtful UX, and performance tuning—so decision-makers can get answers in minutes, not weeks.

## Live dashboard:
https://app.powerbi.com/view?r=eyJrIjoiMWFhNDk0MzgtZDRmZS00MzMxLTk1ZmMtZTk1YzZhY2U4Y2ZlIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9

## What’s Included

Subject Area Views

**Finance** — Revenue, Gross Margin %, Net Profit %, MTD/YTD vs LY, variance bars.

**Sales** — Product & customer leaders/laggards, dynamic Top-N, drillthrough to transaction detail

**Marketing** — Campaign ROI with % of selected and YoY deltas

**Supply Chain** — Stock cover, fill rate, delayed orders, simple forecast accuracy (MAPE/Bias)

**Executive** — One-page story: KPI cards, variance highlights, quick filters & dynamic titles

# UX Enhancements
1.Smart tooltips, guided navigation (bookmarks)

2.What-if parameters for pricing/discount scenarios

3.Data Quality page (missing keys, duplicates, late facts)

4.Anomaly flags (e.g., sudden margin dip > threshold) for fast triage

## Tech Stack

**Power BI Desktop, Power Query, DAX**

**Optional**: MySQL 8.x (for facts & dimensions), CSV/Excel for targets/market share

## Performance & Quality

1.Measure branching + VAR for readable, re-usable logic

2.Keep heavy transforms in Power Query, not calculated columns

3.Use Performance Analyzer to trim visuals & expensive interactions

4.Prefer filter arguments in CALCULATE over row-by-row FILTER() when possible

5.Validate relationships/cardinality; avoid unnecessary bidirectional filters

6.Run basic checks with DAX Studio (query plans, server timings) if you wish

## Run Locally

1.Clone/download this repository.

2.Open the .pbix in Power BI Desktop (latest).

3.If using your own data:

- Replace sample sources in Power Query (Home → Transform data).
- Ensure your Date table spans your data; Mark as Date table.
- Refresh (Home → Refresh).
- 
4.Use slicers/parameters:
- Adjust Top-N via the slicer.
- Try the What-if pricing/discount slider.

5.Explore pages in order: Executive → Finance → Sales → Marketing → Supply Chain → Data Quality.


## Data Sources

This build can work with either CSV/Excel or MySQL as back-end:

- Excel/CSV — Targets, Market Share, supporting lookups
- MySQL 8.x (optional) — Facts & Dimensions
    -Install the MySQL Connector (ODBC or .NET).
    -In Power BI: Get Data → MySQL database, enter Server (e.g., localhost or your host) and Database name, then provide credentials.
    -Map tables to the schema shown above; refresh.

Replace credentials/paths with your own. Do not commit secrets to the repo.




## Credits & Licence

-**Inspiration**: Codebasics “Business Insights 360” case by Dhaval Patel & Hemanand Vadivel (learning framework).
-**Build**: Data model, DAX, UX and performance patterns by Harpal Singh.
-This project is for educational/demonstration purposes.
-Licence: MIT (update if you prefer another licence).
