# Data Folder

This repo does **not** ship raw data or API keys.

**How to reproduce**
1) Get a free Alpha Vantage key (`alpha.key`) and store it locally (do **not** commit).
2) Pull series with the acquisition notebook:
   - `gdp_quarterly.csv`, `vti_daily.csv`, `vxx_daily.csv`, `btc_daily.csv`
3) Save intermediate CSVs under `notebooks/data/` (keep the same filenames used in notebooks).

> Respect API rate limits and terms; never commit keys or raw dumps.

