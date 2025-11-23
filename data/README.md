# Data Folder

This repository does **not** ship raw data or API keys.

---

## How to reproduce

1) Get a free **Alpha Vantage** API key and store it locally as `alpha.key` (do **not** commit it).
   - Key signup: https://www.alphavantage.co/support/#api-key  
   - Docs: https://www.alphavantage.co/documentation/

2) Pull series with the acquisition notebook and save the CSVs using the exact filenames below.

### Exact API calls → expected files

- **Macro (Quarterly GDP)**
  - Endpoint: `REAL_GDP`
  - Save as: **`notebooks/data/gdp_quarterly.csv`**

- **Equity daily closes**
  - Endpoint: `TIME_SERIES_DAILY` (symbol **VTI**)
    - Save as: **`notebooks/data/vti_daily.csv`**
  - Endpoint: `TIME_SERIES_DAILY` (symbol **VXX**)
    - Save as: **`notebooks/data/vxx_daily.csv`**

- **Crypto daily series**
  - Endpoint: `DIGITAL_CURRENCY_DAILY` (symbol **BTC**, market **USD**)
    - Save as: **`notebooks/data/btc_daily.csv`**

> Keep these filenames exactly so the notebooks load paths without edits.

---

## Where to put files

Place all input CSVs under:

notebooks/data/
├─ gdp_quarterly.csv
├─ vti_daily.csv
├─ vxx_daily.csv
└─ btc_daily.csv

---

## Notes & safety

- Respect Alpha Vantage **rate limits** and **terms of service**.  
- **Never commit** your API key or raw dumps. (The repo’s `.gitignore` already ignores `alpha.key`, `.env`, and `notebooks/api/*.txt`.)
- If an endpoint changes or adds required parameters, update your acquisition notebook accordingly and keep the same output filenames.

