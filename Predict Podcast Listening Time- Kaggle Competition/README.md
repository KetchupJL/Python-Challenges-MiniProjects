# Predicting Podcast Listening Time with LightGBM
### *Kaggle Playground Series - Season 5, Episode 4 (S5E4)*

This machine learning project tackles the prediction of podcast listening time using metadata such as genre, popularity, episode structure, and sentiment. As part of the Kaggle Playground Series (S5E4), the task involves structured tabular regression with a rich and noisy real-world dataset.

> Kaggle Competition Link: [Playground Series S5E4](https://www.kaggle.com/competitions/playground-series-s5e4)

---

## Project Objectives
- Predict user **Listening Time (minutes)** from podcast episode features
- Apply **feature engineering** to encode user behaviour patterns
- Explore and compare **tree-based ML models** (LightGBM, Random Forest)
- Evaluate performance using RMSE and visual diagnostics
- Build a clean submission pipeline for Kaggle leaderboard evaluation

---

## Key Learning Outcomes
- Working with categorical and ordinal variables in LightGBM
- Feature engineering: binary flags, interactions, and density measures
- Model tuning with `RandomizedSearchCV`
- Residual analysis and feature importance interpretation
- Submission-ready ML pipelines

---

## Tools & Technologies
| Category           | Tools Used                                                  |
|--------------------|-------------------------------------------------------------|
| **Language**       | Python 3.10+                                                |
| **Modeling**       | LightGBM, RandomForestRegressor, XGBoost         |
| **Preprocessing**  | pandas, numpy, category handling, feature creation          |
| **Evaluation**     | scikit-learn (MAE, RMSE, R^2), matplotlib, seaborn          |
| **Notebook Type**  | Jupyter / Kaggle Notebooks                                  |

---

## Feature Engineering Highlights
- **Popularity Interaction**: Host × Guest popularity
- **Ad Density**: Number of ads divided by episode length
- **Has Guest**: Binary flag for presence of a guest
- **Is Weekend / Is Evening**: Time-based behavioural flags
- **Sentiment Score**: Encoded episode sentiment
- **Length Bin**: Categorised episode duration

These features helped the model better capture listening behaviour nuances and temporal context.

---

## Final Model: Tuned LightGBM
- Trained on full dataset with engineered features
- Tuned via `RandomizedSearchCV` across 50 iterations
- Evaluated with cross-validation and residual diagnostics

### Final Leaderboard Submission
| Metric | Value    |
|--------|----------|
| RMSE   | **18.5** |
| MAE    | 13.8     |
| R^2    | 0.85+    |

<p align="center"> <img src="https://raw.githubusercontent.com/KetchupJL/Python-Challenges-MiniProjects/refs/heads/main/Predict%20Podcast%20Listening%20Time-%20Kaggle%20Competition/Figures/Final%20Model%20-%20Feature%20Importance.png" alt="LightGBM Feature Importance" width="48%"/> <img src="https://raw.githubusercontent.com/KetchupJL/Python-Challenges-MiniProjects/refs/heads/main/Predict%20Podcast%20Listening%20Time-%20Kaggle%20Competition/Figures/Final%20Model%20-%20Residual%20Plot.png" alt="LightGBM Residual Plot" width="48%"/> </p>

<details> <summary>📉 <strong>Compare with Baseline Random Forest Model</strong></summary> <p align="center"> <img src="https://raw.githubusercontent.com/KetchupJL/Python-Challenges-MiniProjects/main/Predict%20Podcast%20Listening%20Time-%20Kaggle%20Competition/Figures/Random%20Forests%20-%20Feature%20Importance.png" alt="RF Feature Importance" width="48%"/> <img src="https://raw.githubusercontent.com/KetchupJL/Python-Challenges-MiniProjects/main/Predict%20Podcast%20Listening%20Time-%20Kaggle%20Competition/Figures/Random%20Forests%20-%20Residual%20Plot.png" alt="RF Residual Plot" width="48%"/> </p> </details>

---

## Repository Structure
```
├── notebooks/               # Development notebooks for EDA, modelling, tuning
│   ├── 01_eda.ipynb         # Initial exploration
│   ├── 02_baseline_models.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_lightgbm_tuning.ipynb
│   └── 05_submission_pipeline.ipynb
├── submission.csv           # Final predictions file
├── figures/                 # Optional: feature plots, residuals, importance
├── README.md                # This file
```

---

## View on Kaggle
📘 Notebook: [Final LightGBM Submission (Public)](https://www.kaggle.com/code/jameslewis066/predict-podcast-listening-time-ps-5-4)
📊 Competition Page: [Playground S5E4](https://www.kaggle.com/competitions/playground-series-s5e4)

---

## Contact
> James Lewis (2025)  
> MSc Applied Data Science & Statistics  
> [GitHub](https://github.com/KetchupJL) | [LinkedIn](https://www.linkedin.com/in/james-lewis3/)

<p align="center">
  <img src="https://img.shields.io/badge/Kaggle%20Competition-Podcast%20Listening%20Prediction-blue?style=for-the-badge"/>
</p>

