# Appliance Energy Forecasting

Forecasting household appliance electricity use 24 hours ahead, comparing five classical
benchmarks, SARIMAX, an XGBoost feature-based model, and the Chronos foundation model.

## Repository structure

```
appliance-energy-forecasting/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   └── raw/
│       └── energydata_complete.csv     # original 10-minute Appliances Energy Prediction dataset
├── notebooks/
│   └── Energy_Forecasting.ipynb        # full analysis: EDA, benchmarks, SARIMAX, XGBoost, Chronos
├── outputs/
│   └── figures/                        # figures exported from the notebook (Figures 1-16)
└── reports/
    └── Forecasting Household Appliance Energy Use.docx   # final written report
```

## Data

Source: [Appliances Energy Prediction dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/00374/),
Candanedo et al. (2017). 10-minute readings of appliance energy use, indoor temperature/humidity
across 9 sensors, and outdoor weather, resampled to hourly means for modelling.

## Running the analysis

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/Energy_Forecasting.ipynb
```

Run the notebook top to bottom. It is organized into 9 parts: data prep/EDA, forecasting
problem definition, benchmark models, SARIMAX, feature engineering, XGBoost, Chronos,
consolidated evaluation, and the analysis questions.

## Report

The full report, including methodology, results, and discussion, is in
`reports/Forecasting Household Appliance Energy Use.docx`.
