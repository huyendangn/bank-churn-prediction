# 🛵 ABC Bank Churn Prediction

## 📌 1. Context & Problem Statement
- **Problem Statement**:
  - Banks always strive to retain their customers to sustain business operations — ABC Multinational Bank is no exception.
  - The Board of Directors is trying to understand why customer churn is occurring and whether customers will leave ABC's services (cancel their subscriptions) in the coming days.
- **Objective**: Build a model to predict whether a customer will churn or continue using the service. The output will be used by the Strategy team to estimate churn volume and develop improvement plans.

## 🔧 2. Tools & Technical Deep Dive
### 2.1 Tools
- Python (pandas, matplotlib, seaborn)
- scikit-learn (Logistic Regression, KNN, Decision Tree, Random Forest, XGBoost)
- Jupyter Notebook

### 2.2 Data Preprocessing
- Missing values are logically consistent — no action required.
- No incorrect data types detected.

### 2.3 EDA
- The dataset is imbalanced: only 20.4% of customers are churned.

### 2.4 Feature Engineering
- Create 3 new features based on EDA findings.
- **Encoding**: OneHotEncoder
- **Scaling**: StandardScaler
- Applied SMOTE to handle class imbalance.

### 2.5 Model & Optimization
- **Algorithm Benchmarking**: Evaluated and compared five classification algorithms — Logistic Regression, KNN, Decision Tree, Random Forest, and XGBoost
  — using 5-Fold Cross-Validation to ensure model stability and mitigate overfitting risk.
- **Hyperparameter Tuning**:  Used RandomizedSearchCV to optimize parameters and decision threshold for the best-performing baseline model: Random Forest.
- **Evaluation Metrics**: The model was fine-tuned to prioritize high _**Recall**_ in identifying churned customers, minimizing missed opportunities to address critical service issues.


## 📊 3. Results & Insights
### 3.1 Results
Based on the business context, the model is tuned to trade off Recall vs. Precision — this threshold can be adjusted to match leadership's actual priorities.

### 3.2 Key Findings 
- Number of products used is the strongest predictor of customer churn.
- Inactive customers (`active_member` = 0) are the clearest early warning signal.
- Germany has a churn rate roughly double that of France and Spain — a dedicated market strategy is needed.

## 💡 4. Recommendations & Limitations - Next Steps
- See in the report (Vietnamese ver): [Report](https://canva.link/pmscp1fdd686kk9)

## 📁 5. Dataset
Source: [Bank Customer Churn Prediction](https://drive.google.com/file/d/1Vmvsp_mxgDp1Wi1G64LQ9P9rCpFG70E8/view)
