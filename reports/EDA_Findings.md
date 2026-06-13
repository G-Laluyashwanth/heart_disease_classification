# 🫀 Exploratory Data Analysis — Heart Disease Dataset
### Findings, Insights & Feature Assessment

---

## 1. Dataset Overview

| Property | Value |
|---|---|
| Observations | 303 |
| Features | 14 |
| Target Variable | `target` — Binary (0 = No Disease, 1 = Disease) |
| Missing Values | None |
| Duplicate Records | None |

The dataset is clean, complete, and ready for modelling with no preprocessing overhead.

---

## 2. Target Variable Distribution

> **54% Heart Disease** · **46% No Heart Disease**

The classes are reasonably balanced. Standard classification models can be trained without aggressive resampling techniques (SMOTE, class weighting, etc.).

---

## 3. Key Feature-Level Findings

### 🔵 Age
- Heart disease is more frequent among **middle-aged to older** patients.
- No significant outliers detected.
- **Takeaway:** Age is a meaningful predictor and should be retained as-is.

### 🔵 Gender (`sex`)
- Males dominate the dataset and show **higher heart disease occurrence** than females.
- **Takeaway:** Gender contributes to predictive power — retain as a feature.

### 🔵 Chest Pain Type (`cp`)
- Strongest categorical signal in the dataset.
- Certain `cp` categories show a **disproportionately high** rate of disease.
- **Takeaway:** Likely one of the top features by importance.

### 🔵 Maximum Heart Rate (`thalach`)
- Decreases with age — the age vs. `thalach` relationship is clearly linear.
- Lower `thalach` correlates with higher disease risk.
- **Takeaway:** Strong continuous predictor.

---

## 4. Correlation Summary

| Direction | Features |
|---|---|
| ➕ Positive with Target | `cp` · `thalach` · `slope` |
| ➖ Negative with Target | `oldpeak` · `exang` · `ca` |

Several clinical features show **statistically meaningful relationships** with the target, indicating strong signal for ML models.

---

## 5. Outlier Detection (IQR Method + Boxplots)

| Feature | Outliers Detected |
|---|---|
| `age` | 0 |
| `trestbps` | 9 |
| `chol` | 5 |
| `thalach` | 1 |
| `oldpeak` | 5 |

> ⚠️ **Decision: Retained.** In a medical dataset, extreme values likely reflect genuine patient conditions rather than data-entry errors. Removing them risks discarding clinically relevant cases.

---

## 6. Top Predictive Features

Based on correlation analysis, visualisations, and domain context:

```
cp  ·  thalach  ·  oldpeak  ·  ca  ·  thal  ·  exang
```

These six features will receive priority attention during model evaluation and feature importance analysis.

---

## 7. Conclusion & Next Steps

The dataset is **clean, balanced, and structurally sound** — an ideal candidate for classification.

| Next Phase | Focus |
|---|---|
| Model Building | Logistic Regression · KNN · Random Forest |
| Tuning | Hyperparameter optimisation (GridSearchCV / RandomSearch) |
| Evaluation | Accuracy · Precision · Recall · ROC-AUC |

---