This folder is used for local data files and cached external datasets.

#Exam repository data

The project relies on the datasets provided in the exam repository:

- data_ecb_hicp_panel.csv: monthly year-on-year HICP inflation for Euro Area countries.
- data_ukraine_cpi_raw.csv: Ukrainian CPI index, expressed as previous-month base.

The Ukrainian CPI series is transformed into year-on-year inflation in the notebook.

#External data

The project also uses external macroeconomic data.

#National Bank of Ukraine

Used variable:

- UAH/USD exchange rate.

Purpose:

- document the exchange-rate regime in Part A;
- compute exchange-rate depreciation;
- proxy the exchange-rate pass-through channel in Part B.

#Brent oil price

Used variable:

- Brent oil price series.

Purpose:

- control for global energy-price shocks affecting Ukrainian inflation.

#World Bank

Used variables:

- real GDP growth for Ukraine;
- real GDP growth for the Euro Area.

Purpose:

- construct the annual Blanchard–Quah SVAR benchmark using output growth and inflation.

#Reproducibility

Whenever possible, the notebook downloads external data programmatically.

If an external source is temporarily unavailable, cached files may be stored in this folder.