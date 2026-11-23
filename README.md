# Calibrating Low-Cost Ozone Sensors with Machine Learning

Coursework 1 – 6COSC017C Machine Learning and Data Analytics (2026–2027)

## Project summary

Low-cost air-quality sensors are cheap but inaccurate. This project trains machine-learning
regression models that use readings from a low-cost sensor to predict the ozone (O3) value
measured by an official monitoring station placed next to it.

- **Task:** supervised regression
- **Target:** ozone measured by the official reference station (µg/m³)
- **Inputs:** low-cost sensor readings (temperature, humidity, particles, gases, raw ozone) and time features

## Dataset

Montalbán Faet, G. et al. (2025) *Air Quality Data from Regulatory AQMS and Low-Cost Sensors
in Molí del Sol, Valencia (May 31 2024 – January 23, 2025)*. Zenodo.
https://doi.org/10.5281/zenodo.17044034 — licence: CC BY 4.0.

Files used (in `data/raw/`):

| File | Source |
|---|---|
| `gva_10.csv` | Official reference station |
| `n1_10.csv` | Low-cost sensor node 1 |
| `n2_10.csv` | Low-cost sensor node 2 |

## Project structure

```
ozone-calibration/
├── data/raw/          # original data files (unchanged)
├── notebooks/         # Jupyter notebook with the full analysis
├── app/               # Streamlit multi-page app
├── models/            # saved trained model
├── requirements.txt   # list of required Python libraries
├── LICENSE            # MIT licence (code only)
└── README.md
```

## How to run

Requires **Python 3.11 or newer**.

```bash
# 1. Download the project
git clone <repository-url>
cd ozone-calibration

# 2. Install the required libraries
pip install -r requirements.txt

# 3. Open the notebook and run all cells
jupyter notebook notebooks/coursework.ipynb

# 4. Run the Streamlit app
streamlit run app/Home.py
```

## Licence

Code: MIT (see `LICENSE`). Data: CC BY 4.0, © the dataset authors.