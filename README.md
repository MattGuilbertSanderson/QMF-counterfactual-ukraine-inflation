# Counterfactual Inflation Analysis: What If Ukraine Had Been Part of the Euro Area?

#Project

This repository contains my final project for the course Quantitative Methods in Finance, Master 2 Finance, Technology and Data, Université Paris 1 Panthéon-Sorbonne.

The project constructs a counterfactual inflation path for Ukraine under the hypothetical scenario in which Ukraine had been a member of the Euro Area.

The analysis is divided into two parts:

-Part A documents the evolution of Ukraine’s exchange-rate and monetary regime from 2000 to 2025.
-Part B estimates a counterfactual inflation path using an econometric framework that combines a Euro Area inflation anchor, exchange-rate pass-through, time-varying treatment intensity, local projections, and a Blanchard–Quah SVAR benchmark.

#Research question

What would Ukraine’s inflation trajectory have looked like had Ukraine been a member of the Euro Area?

#Main idea

The counterfactual is not treated as a constant treatment over time.  
Part A shows that Ukraine’s monetary sovereignty varied substantially across the sample:

- during peg periods, the National Bank of Ukraine had limited de facto monetary sovereignty;
- during devaluation episodes and the post-2016 inflation-targeting period, monetary sovereignty was more meaningful;
- during wartime, the exchange-rate regime and capital controls again strongly constrained monetary policy.

This motivates a time-varying treatment-intensity index used in the counterfactual model.

#Repository structure

```text
.
├── README.md
├── requirements.txt
├── QMF_Project_Matt_GUILBERT_SANDERSON.ipynb
├── data/
│   └── README_data.md
├── figures/
├── outputs/
└── docs/
    └── partA_monetary_regime_summary.md