# Signal Classification using Machine Learning

This project aims to classify physiological signals (EDA & ECG) into **stress** and **non-stress** states using classical machine learning techniques, mainly Random Forest and XGBoost.

---

## Objective

To build a binary classification model that detects stress from physiological signal windows, and improve accuracy through advanced feature engineering.

---

## Dataset Description

- Signals: Electrodermal Activity (EDA) and ECG
- Labels: Originally 0–7  
  - Filtered for relevant classes: 1 (baseline), 2 (stress), 3 (amusement), 4 (meditation)
  - Converted to binary:
    - Stress = 1 (label 2)
    - Non-stress = 0 (labels 1, 3, 4)

---

## Preprocessing

- Removed irrelevant and undefined labels (0, 5, 6, 7)
- Applied windowing (60s with 50% overlap)
- Normalized signal windows
- Converted to binary labels

---

## Feature Engineering

- Extracted statistical features:
  - Mean, std, min, max
  - **Skewness**
  - **Kurtosis**
- This helped improve the signal representation significantly.

---

## Models Used

1. **Random Forest**  
   - Baseline model  
   - Accuracy: ~0.77

2. **XGBoost (After feature engineering)**  
   - Accuracy: **~0.95**  
   - Significantly better performance on minority class

---

## Results

| Model          | Accuracy |
|----------------|----------|
| Random Forest  | 0.77     |
| XGBoost        | 0.95     |

---

## Visual Results

- Classification report screenshots (before and after) are available in the `assets/` folder.

---

## Conclusion

- Feature engineering (skewness, kurtosis) improved model performance.
- XGBoost was superior to Random Forest for this task.
- A solid baseline for stress detection using simple physiological signals.

---

## Files

- `signal_classification_notebook.ipynb` — Full notebook with code and results.
- `Signal_Classification_Presentation.pptx` — Final presentation.
- `Signal_Classification_Presentation.md` — Markdown version for GitHub preview.
- `README.md` — This file.

---

## Author Team

- taha mohamed   
- abdelRahman mohamed 
- ahmed esmail  

---
