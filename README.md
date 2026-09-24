<img width="969" height="532" alt="WhatsApp Image 2026-09-24 at 5 08 02 PM" src="https://github.com/user-attachments/assets/c79be7e4-00e4-4b57-adf6-6e61f8422c99" />
<img width="969" height="532" alt="WhatsApp Image 2026-09-24 at 5 08 02 PM" src="https://github.com/user-attachments/assets/ccb0cecf-9827-4ea6-a5bc-a7bcfa2b7c40" />
<img width="969" height="532" alt="WhatsApp Image 2026-09-24 at 5 08 02 PM" src="https://github.com/user-attachments/assets/5ed01244-ac25-41d1-8cee-e01fc2d55455" />
<img width="969" height="532" alt="WhatsApp Image 2026-09-24 at 5 08 02 PM" src="https://github.com/user-attachments/assets/c1d916cd-47ae-44db-9133-7ea264a209ba" />
# 🏡 California Housing Value Predictor

An end-to-end Machine Learning web application and regression pipeline designed to predict median district housing values across California based on demographic, structural, and geographical indicators.

---

## 📌 Project Introduction

Accurate real estate valuation is a critical challenge due to the complex, non-linear interplay between geographical positioning, socioeconomic factors, and neighborhood density. 

This project delivers a production-ready machine learning solution to estimate district-level median home values across California using census data. Starting from raw data ingestion and rigorous exploratory analysis, the pipeline implements automated statistical imputation, domain-specific ratio feature engineering, categorical encoding, and feature scaling. 

A baseline **Multiple Linear Regression** model was evaluated against an ensemble **Random Forest Regressor**[cite: 4]. The final optimized Random Forest model achieves an $R^2$ score of **~0.806** (outperforming the linear baseline's ~0.597) and reduces Root Mean Squared Error (RMSE) to **$50,368.16**[cite: 4]. The serialized pipeline is packaged into an interactive **Streamlit** dashboard for scenario modeling, real-time inference, and feature importance diagnostics.

---

## 🚀 Key Highlights & Features

- **Automated Data Cleaning:** Imputes missing values in `total_bedrooms` using training-set median statistics to prevent data leakage.
- **Domain Feature Engineering:** Computes structural indicators:
  - Rooms per Household ($\frac{\text{total\_rooms}}{\text{households}}$)
  - Bedrooms per Room ($\frac{\text{total\_bedrooms}}{\text{total\_rooms}}$)
  - Population per Household ($\frac{\text{population}}{\text{households}}$)
- **Robust Model Benchmarking:** Systematic empirical comparison between parametric (OLS Linear Regression) and ensemble non-parametric methods (Random Forest)[cite: 4].
- **Interactive UI (Streamlit):** Pre-configured geographical presets ("Urban / high income", "Inland family district", "Coastal community"), live input validation, feature scaling on inference, and dynamic top-8 feature importance charts.

---

## 🏗 Architecture & Machine Learning Pipelines
sent by praveen anna
