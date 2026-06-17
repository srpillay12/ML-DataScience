# ML-DataScience
# Indian Job Market Analysis & Salary Prediction Engine (2024–2026)
## 📌 Project Overview
This project delivers an end-to-end data pipeline that analyzes employment trends and predicts compensation models within the Indian job market using data spanning 2024 to 2026. By tackling high-dimensional categorical features and multi-label text strings (skills lists), this engine accurately maps salary expectations across different job roles, geographical hubs, experience tiers, and industry verticals.

### Key Objectives:
1. **Market Intelligence:** Extract data-driven insights regarding remote vs. hybrid work distributions, required education levels, and top-hiring industries.
2. **Salary Forecasting:** Develop a optimized machine learning framework capable of predicting compensation brackets based on multi-categorical job profiles.

### Key Objectives:
1. **Market Intelligence:** Extract data-driven insights regarding remote vs. hybrid work distributions, required education levels, and top-hiring industries.
2. **Salary Forecasting:** Develop a optimized machine learning framework capable of predicting compensation brackets based on multi-categorical job profiles.

## 🛠️ Feature Engineering & Preprocessing Pipeline
Real-world datasets contain structural complexities. The preprocessing architecture built for this project addresses those constraints seamlessly:

* **Categorical Encoding:** Deployed `OneHotEncoder` to handle sparse, high-cardinality nominal values such as Job Profiles and Cities.
* **Feature Scaling:** Applied `StandardScaler` across continuous features to minimize variance biases during linear modeling.
* **Multi-Label Parsing:** Resolved comma-separated strings inside the "Skills" column by implementing a custom `MultilabelBinarizer` routine, expanding multi-text inputs into clean binary vectors.

## 🤖 Modeling & Systematic Optimization
A rigorous model-selection process was used to compare basic linear models against advanced tree-based ensembles.

### Tested Architectures:
* **Baselines:** Linear Regression, Decision Trees
* **Tree-Boosted Variants:** XGBoost, Gradient Boosting
* **Ensemble Paradigms:** Random Forest, Bagging, Voting, and Stacking Regressors

### Optimization Workflow:
1. **Baseline Evaluation:** All 8 models were initially trained with default parameters to establish performance baselines.
2. **Hyperparameter Tuning:** The top-performing base model was selected for hyperparameter tuning using `GridSearchCV`.
3. **Validation Strategy:** Implemented a robust **5-fold cross-validation** layout to guarantee model stability, evaluating generalized performance against $R^2$ score and Root Mean Square Error (RMSE).

## 🏆 Final Results
| Model Architecture | R2score | 
| Linear Regression | 0.7952 |
| XGBoost | 0.9156 |
| GradientBoost | 0.9169 |
| Random forest| 0.9256 |
| Voting | 0.9260 |
| Bagging | 0.9276 |
| Stacking | 0.9066 |
| **Random Forest (Tuned)** | **0.9383** | **🏆 Selected Winner** |
