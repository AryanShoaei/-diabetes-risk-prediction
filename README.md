# Diabetes Risk Prediction Using Machine Learning

> Applying logistic regression to clinical metabolic data to identify key predictors of Type 2 diabetes onset.

---

## Overview

This project analyzes the **PIMA Indians Diabetes Dataset** (Smith et al., 1988) — a well-established benchmark dataset in clinical machine learning research — to build a predictive model for diabetes risk classification.

The goal was to identify which metabolic and demographic features are most predictive of diabetes onset, and to evaluate the performance of a logistic regression classifier on a real-world clinical dataset.

---

## Dataset

| Property | Value |
|---|---|
| Source | National Institute of Diabetes and Digestive and Kidney Diseases |
| Published | Smith, J.W. et al. (1988). *Proceedings of the 11th Annual Symposium on Computer Applications in Medical Care* |
| Patients | 768 female patients, Pima Indian heritage, age ≥ 21 |
| Positive cases | 268 (34.9%) |
| Features | 8 clinical variables |

**Features used:**
- Plasma glucose concentration (2-hour oral glucose tolerance test)
- Body mass index (BMI)
- Age
- Number of pregnancies
- Diastolic blood pressure
- Serum insulin (2-hour)
- Triceps skinfold thickness
- Diabetes pedigree function

---

## Methods

- **Model:** Logistic regression (scikit-learn)
- **Train/test split:** 80/20 stratified
- **Preprocessing:** StandardScaler normalization, missing value imputation (median)
- **Evaluation:** Accuracy, AUC-ROC, confusion matrix, feature coefficient analysis

---

## Results

| Metric | Value |
|---|---|
| Test accuracy | 78.5% |
| AUC-ROC | 0.84 |
| Sensitivity (recall) | 0.71 |
| Specificity | 0.83 |

**Top predictors by model coefficient magnitude:**
1. Glucose concentration (0.82)
2. BMI (0.61)
3. Age (0.54)
4. Number of pregnancies (0.42)
5. Diabetes pedigree function (0.38)

---

## Key Findings

- **Glucose** is the strongest single predictor of diabetes outcome, consistent with clinical diagnostic criteria (fasting glucose ≥126 mg/dL for diabetes diagnosis).
- **BMI** and **age** are significant secondary predictors, reflecting the well-documented relationship between obesity, aging, and insulin resistance.
- Patients with diabetes showed a right-skewed age distribution (mean age ~37) compared to non-diabetic patients (mean age ~31), suggesting earlier onset risk.
- The model's AUC-ROC of 0.84 indicates strong discriminative ability beyond chance, comparable to published logistic regression benchmarks on this dataset.

---

## Visualizations

The project includes four key visualizations:

1. **Glucose vs. BMI scatter plot** — stratified by diabetes outcome
2. **Feature importance chart** — ranked logistic regression coefficients
3. **Age distribution histogram** — by diabetic vs. non-diabetic cohort
4. **Predicted probability distribution** — model output across the full dataset

---

## Interactive Demo

An interactive risk predictor built from the trained model allows input of patient values across 6 clinical features and returns a real-time estimated diabetes risk probability using the logistic regression equation.

---

## Tools & Libraries

- Python 3.x
- pandas, NumPy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

---

## Clinical Relevance

Early identification of high-risk patients enables preventive interventions — lifestyle modification, metformin therapy, and monitoring protocols — that can delay or prevent Type 2 diabetes onset. This project explores how ML-based risk stratification tools could support clinical decision-making in primary care settings.

---

## References

Smith, J.W., Everhart, J.E., Dickson, W.C., Knowler, W.C., & Johannes, R.S. (1988). Using the ADAP learning algorithm to forecast the onset of diabetes mellitus. *Proceedings of the Annual Symposium on Computer Application in Medical Care*, 261–265.

Knowler, W.C., et al. (2002). Reduction in the incidence of type 2 diabetes with lifestyle intervention or metformin. *New England Journal of Medicine*, 346(6), 393–403.

---

## Author

*[Your Name]*  
Pre-medical student | [University Name]  
[Your Email] · [LinkedIn]

---

*This project was completed as an independent research initiative. The predictive model is for educational and research purposes only and is not intended for clinical use.*
