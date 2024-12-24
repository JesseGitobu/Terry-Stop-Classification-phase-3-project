# Terry-Stop-Classification-phase-3-project - README

## Project Overview
This project analyzes data from Terry Stops to predict specific outcomes, such as arrests, based on various features like demographics, officer characteristics, and stop context. The goal is to identify patterns and insights to support decision-making and improve fairness in law enforcement practices.

## Dataset Information
- **File Name:** `Terry_Stops_20241220.csv`
- **Rows:** 62,191
- **Columns:** 23
- **Key Features:**
  - Demographics (age group, gender, perceived race)
  - Officer attributes (gender, race, year of birth)
  - Stop context (call type, weapon type, arrest and frisk flags)

### Target Variable:
- **Arrest Flag** (Binary): 'Y' (Yes) or 'N' (No)
- Class Distribution:
  - No Arrest (N): 89.01%
  - Arrest (Y): 10.99%

## Exploratory Data Analysis (EDA)
- Feature Engineering was conducted to drop irrelevant features like 'Initial Call Type' and 'Final Call Type'.
- Key Findings:
  - **Age Groups:** Majority aged 26–35 and 36–45.
  - **Officer Demographics:** Predominantly male (88.5%) and White (71.3%).
  - **Call Types:** 47% were 911 calls; 21% were officer-initiated (on-view).

## Data Preprocessing
1. **Missing Values:**
   - Handled missing data for features such as 'Weapon Type'.
2. **Feature Encoding:**
   - Categorical features encoded for modeling.
3. **Class Imbalance Handling:**
   - Used **SMOTE** (Synthetic Minority Oversampling Technique) to balance classes.

## Modeling Process
### Algorithms Used:
1. **Logistic Regression**
2. **Random Forest Classifier**

### Evaluation Metrics:
- **Accuracy**
- **Precision, Recall, and F1-Score**
- **ROC-AUC Score**

### Results Overview:
- **Baseline Accuracy:** Models performed better than random guessing due to effective preprocessing and class balancing.
- **Random Forest Feature Importance:** Provided insights into key predictors of arrests.

## Limitations
- **Data Bias:** High imbalance in arrests may reflect biases in data collection.
- **Model Generalization:** Further validation required to ensure real-world applicability.
- **Feature Exclusions:** Dropping columns may overlook subtle influences.

## Recommendations for Stakeholders
1. **Focus Areas:**
   - Use results to address fairness in Terry Stops, particularly addressing race and gender biases.
2. **Deployment Considerations:**
   - Test model robustness with unseen data before implementation.
3. **Policy Implications:**
   - Develop interventions based on identified predictors (e.g., targeted training for officers).

## Next Steps
- Evaluate additional algorithms (e.g., XGBoost, Neural Networks) for performance improvements.
- Perform interpretability analysis to make the model outputs more transparent.
- Expand EDA with time-series analysis to capture trends over time.

---

For detailed code and results, refer to the Jupyter Notebook file (`project.ipynb`).

