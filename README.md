#  Medical Insurance Cost Prediction (Multiple Linear Regression)

An end-to-end Machine Learning project built using Python, Pandas, Scikit-Learn, Matplotlib, and Seaborn. This repository predicts individual medical insurance costs based on demographic and lifestyle features using Multiple Linear Regression.

---

##  Project Overview
Healthcare costs can vary significantly based on individual risk factors. The goal of this project is to analyze individual health and demographic data to build an accurate predictive model for medical charges.

- **Target Variable:** `charges` (Medical cost in USD)
- **Algorithm Used:** Multiple Linear Regression
- **Frameworks:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib, IPyWidgets

---

## Dataset Features & Preprocessing
The dataset consists of **1,338 customer records** with 7 key variables:
1. `age`: Primary beneficiary's age
2. `sex`: Gender (`female`, `male`) -> Binary Encoded
3. `bmi`: Body Mass Index (kg/m²)
4. `children`: Number of dependents covered by health insurance
5. `smoker`: Smoking status (`yes`, `no`) -> Binary Encoded
6. `region`: Residential area in the US (`northeast`, `northwest`, `southeast`, `southwest`) -> One-Hot Encoded
7. `charges`: Individual medical costs billed by health insurance

### Data Cleaning Steps:
- Verified 0 missing values across all columns.
- Identified and removed 1 duplicate record, resulting in 1,337 clean entries.
- Applied One-Hot and Binary Encoding to categorical variables (`sex`, `smoker`, `region`).

---

##  Key EDA Insights
- **Smoking Impact:** Smoking is the single strongest factor driving up medical charges.
- **Age Factor:** Medical charges steadily increase as age increases for both smokers and non-smokers.
- **BMI & Smoking Combination:** High BMI (> 30) combined with smoking leads to the highest overall insurance costs.

---

##  Model Training & Performance

The dataset was split using an **80/20 train-test split** (`random_state=42`).

### Evaluation Metrics:
- **Mean Absolute Error (MAE):** ~$4,171.80
- **Root Mean Squared Error (RMSE):** ~$5,956.11
- **R² Score (Accuracy):** **80.69%**

---

##  How to Run the Prediction Application

1. Open the Jupyter Notebook / Google Colab file in this repository.
2. Run all cells sequentially.
3. Use the interactive form widgets at the end to input custom age, BMI, smoker status, gender, children, and region parameters to receive real-time medical cost predictions.

---

##  Limitations
- **Linearity Assumption:** Linear Regression assumes a straight-line relationship between features and target, which may underfit complex non-linear medical patterns.
- **Geographic Scope:** Data represents a US-based cohort and may not accurately reflect global healthcare pricing structures.
