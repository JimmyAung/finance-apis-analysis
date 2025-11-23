# finance-apis-analysis
API-driven analysis of macro & market data (Alpha Vantage). Includes notebooks for acquisition/cleaning & simple visuals (indexed close, daily/monthly returns) plus Tableau screenshots. Keys/data excluded; see /data/README.md to reproduce.

![Tableau Overview](reports/Tableau_overview.png)

**TL;DR.** Pull macro & market series from **Alpha Vantage**, clean in pandas, and build tidy views: **indexed close (100 = first)**, **daily % returns**, and **monthly % returns**. Optional Tableau screenshots for presentation. Keys/data are excluded; see **/data/README.md** to reproduce.

## Project Summary
- Pulled GDP (quarterly) and daily market series (**VTI**, **VXX**, **BTC**) via Alpha Vantage.
- Cleaned/merged in pandas; created indexed (100=first) series and daily/monthly returns.
- Built quick visuals in notebooks; exported views/screenshots for presentation.


## Repository Structure
finance-apis-analysis/
├─ data/ # instructions only; no raw data or keys
├─ notebooks/ # 00_data_acquisition.ipynb, 01_clean_merge_views.ipynb
├─ reports/ # PDF write-up, Tableau screenshots (PNG), twbx (small)
├─ .gitignore
├─ LICENSE # MIT
└─ README.md


## Reproducibility
- Get a free **Alpha Vantage** key and **do not commit it** (store locally, e.g., `alpha.key`).
- See **/data/README.md** for where to place CSVs and how to re-run pulls.

## Data Source & Documentation

Data provider: **Alpha Vantage**  
- Get a free API key: https://www.alphavantage.co/support/#api-key  
- Docs home: https://www.alphavantage.co/documentation/

**Endpoints used in this project**
- Macro: `REAL_GDP` (Quarterly, USA)
- Equities: `TIME_SERIES_DAILY` (VTI, VXX)
- Crypto: `DIGITAL_CURRENCY_DAILY` (BTC, market = USD)

**Attribution & Terms**
This project uses the Alpha Vantage API. Please respect their rate limits and terms of service.


## Quick Start
1. Open the notebooks:  
   `notebooks/00_data_acquisition.ipynb` (pulls)  
   `notebooks/01_clean_merge_views.ipynb` (indexed series, returns, small charts)
2. See **reports/** for the PDF and **Tableau_overview.png**.

## Notes
- Keys and raw dumps are excluded for safety and to respect API terms.
- If `.twbx` files grow large, prefer screenshots or link to Tableau Public.


