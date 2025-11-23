# Data Folder

This repo does **not** ship raw data or API keys.

### How to reproduce

1) Get a free **Alpha Vantage** key and store it locally as `alpha.key` (do **not** commit).
   - Key signup: https://www.alphavantage.co/support/#api-key
   - Docs: https://www.alphavantage.co/documentation/

2) Pull series with the acquisition notebook using these endpoints:
   - **REAL_GDP (quarterly)** → saved as `gdp_quarterly.csv`
   - **TIME_SERIES_DAILY** for **VTI** and **VXX** → `vti_daily.csv`, `vxx_daily.csv`
   - **DIGITAL_CURRENCY_DAILY** for **BTC** → `btc_daily.csv`

3) Save intermediate CSVs under `notebooks/data/` (keep the same filenames used in notebooks).
