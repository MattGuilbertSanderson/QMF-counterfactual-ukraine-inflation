#Counterfactual Inflation Analysis: What If Ukraine Had Been Part of the Euro Area?

#Key files for grading

* Main notebook: `QMF_Project_Matt_GUILBERT_SANDERSON.ipynb`
* Part A monetary-regime summary: `docs/partA_monetary_regime_summary.md`
* Part A regime / treatment-intensity table: `outputs/regime_table_partA.csv`
* Main counterfactual figure: `figures/main_required_actual_vs_counterfactual_only.png`
* Extended counterfactual figure with Euro Area factor: `figures/main_actual_vs_counterfactual_inflation.png`
* Main counterfactual time series: `outputs/main_counterfactual_series.csv`
* Local projection results: `outputs/local_projection_exchange_rate_passthrough.csv`
* Blanchard–Quah SVAR benchmark: `outputs/bq_svar_counterfactual_annual.csv`

#Project

This repository contains my final project for the course **Quantitative Methods in Finance**, Master 2 Finance, Technology and Data, Université Paris 1 Panthéon-Sorbonne.

The project constructs a counterfactual inflation path for Ukraine under the hypothetical scenario in which Ukraine had been a member of the Euro Area.

The analysis is divided into two parts:

* **Part A** documents the evolution of Ukraine’s exchange-rate and monetary regime from 2000 to 2025.
* **Part B** estimates a counterfactual inflation path using an econometric framework that combines a Euro Area inflation anchor, exchange-rate pass-through, time-varying treatment intensity, local projections, and a Blanchard–Quah SVAR benchmark.

#Research question

What would Ukraine’s inflation trajectory have looked like had Ukraine been a member of the Euro Area?

#Main idea

The counterfactual is not treated as a constant treatment over time.

Part A shows that Ukraine’s monetary sovereignty varied substantially across the sample:

* during peg periods, the National Bank of Ukraine had limited de facto monetary sovereignty;
* during devaluation episodes and the post-2016 inflation-targeting period, monetary sovereignty was more meaningful;
* during wartime, the exchange-rate regime and capital controls again strongly constrained monetary policy.

This motivates a time-varying treatment-intensity index used in the counterfactual model.

#Repository structure

```text
.
├── README.md
├── requirements.txt
├── QMF_Project_Matt_GUILBERT_SANDERSON.ipynb
├── data/
│   ├── README_data.md
│   ├── data_ecb_hicp_panel.csv
│   ├── data_ukraine_cpi_raw.csv
│   ├── nbu_usd_uah_daily.csv
│   ├── nbu_usd_uah_monthly.csv
│   ├── worldbank_emu_gdp_growth.csv
│   └── worldbank_ukr_gdp_growth.csv
├── figures/
├── outputs/
└── docs/
    └── partA_monetary_regime_summary.md
```

#Data

The project uses two types of data.

#Exam repository data

* `data_ecb_hicp_panel.csv`: monthly year-on-year HICP inflation for Euro Area countries.
* `data_ukraine_cpi_raw.csv`: Ukrainian CPI index, expressed as previous-month base.

The Ukrainian CPI series is transformed into year-on-year inflation in the notebook to make it comparable with the Euro Area HICP panel.

#External macroeconomic data

The project also uses external macroeconomic data:

* National Bank of Ukraine UAH/USD exchange-rate data;
* World Bank GDP growth data for Ukraine;
* World Bank GDP growth data for the Euro Area;
* Brent oil price data, downloaded programmatically in the notebook.

These variables are used to document the monetary-regime chronology, estimate the exchange-rate pass-through channel, control for global energy shocks, and construct the annual SVAR benchmark.

Additional details are provided in `data/README_data.md`.

#Methodology

The main monthly counterfactual model estimates Ukrainian year-on-year inflation as a function of:

* lagged Ukrainian inflation;
* exchange-rate depreciation;
* a Euro Area common inflation factor extracted from the Euro Area HICP panel;
* Brent oil price inflation;
* a time-varying treatment-intensity index derived from Part A.

The counterfactual removes or attenuates the exchange-rate depreciation channel depending on the degree of effective monetary sovereignty identified in Part A.

The analysis is complemented by:

* local projections measuring exchange-rate pass-through;
* a Blanchard–Quah SVAR benchmark based on output growth and inflation;
* robustness checks using an alternative Euro Area inflation anchor.

#Main outputs

The main figure required by the exam is:

```text
figures/main_required_actual_vs_counterfactual_only.png
```

It compares:

* actual Ukrainian year-on-year CPI inflation;
* counterfactual Ukrainian inflation under hypothetical Euro Area membership.

An extended version including the Euro Area common inflation factor is also available:

```text
figures/main_actual_vs_counterfactual_inflation.png
```

The corresponding time series is stored in:

```text
outputs/main_counterfactual_series.csv
```

The Part A regime and treatment-intensity table is stored in:

```text
outputs/regime_table_partA.csv
```


#Author

Matt Guilbert-Sanderson
Master 2 Finance, Technology and Data
Université Paris 1 Panthéon-Sorbonne
