# Algerian Forest Fire Prediction — End-to-End ML Pipeline & Web App

An end-to-end Machine Learning web application designed to predict the **Fire Weather Index (FWI)** based on meteorological observations and FWI system components. The pipeline is trained on the Kaggle Algerian Forest Fires dataset covering the **Bejaia** and **Sidi Bel-abbes** regions and is served via an interactive **Flask** web application.

---

## Project Overview

The Fire Weather Index (FWI) is a Canadian system adapted internationally to quantify wildfire danger based on weather observations. This project covers the full machine learning lifecycle:

1. **Dataset & Preprocessing:** Sourced from Kaggle, containing observations across two distinct Algerian zones:
   * **Bejaia Region:** Located in northeast Algeria.
   * **Sidi Bel-abbes Region:** Located in northwest Algeria.
2. **Exploratory Data Analysis (EDA) & Feature Engineering:** Cleaning raw data, handling missing values, encoding regional identifiers (`0` for Bejaia, `1` for Sidi Bel-abbes), dropping collinear variables (`BUI`, `DC`), and standardizing features.
3. **Model Selection & Regularization:** Comparing Linear, Lasso, Ridge, and ElasticNet models; Ridge Regression was selected to prevent overfitting and ensure consistent generalizability.
4. **Serialization:** Exporting the trained `StandardScaler` and `Ridge` models to `.pkl` artifacts.
5. **Web Deployment:** Serving predictions through a lightweight Flask backend with interactive Jinja2 HTML templates.

---

## Tech Stack

* **Language:** Python
* **Machine Learning:** Scikit-Learn, Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Web Framework:** Flask, Jinja2
* **Version Control:** Git, GitHub

---

## Project Structure

```text
Algerian_Forest_Fire_Prediction/
│
├── models/
│   ├── ridge.pkl               # Trained Ridge Regression model
│   └── scaler.pkl              # StandardScaler object
│
├── notebooks/
│   ├── Algerian_forest_fires_dataset.csv
│   ├── EDA and FE.ipynb        # Exploratory Data Analysis & Feature Engineering
│   └── Model_training.ipynb    # Model experimentation & hyperparameter tuning
│
├── templates/
│   ├── index.html              # Landing page
│   └── home.html               # Prediction input form and results display
│
├── application.py              # Flask server and routing logic
├── requirements.txt            # Project dependencies
└── README.md

## How to Clone and Setup

1. Open your terminal or Git Bash.
2. Clone the repository:
   ```bash
   git clone (https://github.com/Shrestha-Ain/Algerian_Forest_Fire_Prediction.git)