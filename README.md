# Warfarin Dose Prediction using Machine Learning

This project focuses on predicting the optimal Warfarin dose based on both **genetic factors** (CYP2C9, VKORC1) and **clinical features** (age, gender, height, weight). The goal is to explore how pharmacogenomics can improve dose accuracy using multiple machine learning models and feature importance techniques.

---

## 📌 Project Objectives

- To build and compare machine learning models for Warfarin dose prediction.
- To evaluate the contribution of genetic and clinical features using **Permutation Importance**.
- To demonstrate how pharmacogenomics can support personalized medicine.

---

## 🧬 Background

Warfarin is an anticoagulant with a narrow therapeutic index, where frequent INR (International Normalized ratio) monitoring is required to identify the therapeutic dose for the patients (Johnson, 2012). Small dosing errors can lead to bleeding or thrombosis (Teka *et al*., 2024), as the therapeutic INR value is typically between 2.0 to 3.0 (Shikdar *et al*., 2025). Genetic polymorphisms in **CYP2C9** and **VKORC1** significantly affect drug metabolism and sensitivity (Johnson, 2012), making Warfarin an ideal case for pharmacogenomic modeling.

---

## 🗂️ Dataset Description

| Feature Type  | Features Included                         |
|---------------|-------------------------------------------|
| Genetic       | `CYP2C9_code`, `VKORC1_code`              |
| Clinical      | `Age`, `Gender_code`, `Height (cm)`, `Weight (kg)` |
| Target        | `Warfarin Dose` (continuous variable)     |

---

## 🤖 Machine Learning Models Used

| Model | Description |
|-------|------------|
| Linear Regression | Baseline model for linear relationships |
| Ridge Regression  | Regularized linear model to handle collinearity |
| Decision Tree     | Non-linear model capturing interactions |
| Gradient Boosting | Ensemble method for improved accuracy |

---

## 📏 Evaluation Metrics

| Metric | Description |
|--------|------------|
| **R² Score** | Measures variance explained by the model |
| **MAE (Mean Absolute Error)** | Average absolute error |
| **RMSE (Root Mean Squared Error)** | Penalizes larger errors |

---

## 🔍 Feature Importance (Permutation Importance)

Permutation Importance was applied to understand how each genetic and clinical feature contributes to dose prediction.  
This analysis highlights whether genetics or clinical factors have stronger influence depending on the model.

✔ Stored in separate CSV files for each model  
✔ Compared using pivot tables and heatmaps

---

## 📊 Results Overview 

- **Best Model:** Ridge Regression (highest R², lowest MAE)
- **Most Influential Features:** VKORC1 (genetic factor)
- Clinical features such as Age and Weight showed moderate contribution

*Note: Exact numeric results can be found in `/results/` CSV files.*

---

## 🛠️ How to Run the Project

```bash
# Clone repository
git clone https://github.com/FarahYusri12/Warfarin_Dosing_Prediction-Model_Comparison.git
cd Warfarin_Dosing_Prediction-Model_Comparison

# Install dependencies
pip install -r requirements.txt

# Run notebooks or scripts
jupyter notebook
```

---

## 🗂️ Project Structure 

```
├── data/               # Preprocessed dataset 
├── notebooks/          # Model training & analysis (4 models)
├── results/            # CSV: metrics & permutation importance
├── visuals/            # Graphs & heatmaps
└── README.md           # Project documentation
```

---

## 🚀 Future Improvements

- Add more genetic markers (e.g., CYP4F2)
- Hyperparameter tuning & cross-validation
- Deploy as web app (Flask/Streamlit)
- External clinical validation dataset

---

## 🙌 Acknowledgements

This project is inspired by research in **pharmacogenomics** and aims to showcase the integration of machine learning in personalized medicine.

---

## References

Johnson J. A. (2012). Warfarin pharmacogenetics: a rising tide for its clinical value. *Circulation, 125*(16), 1964–1966. https://doi.org/10.1161/CIRCULATIONAHA.112.100628

Shikdar, S., Vashisht, R., Zubair, M., & Bhattacharya, P. T. (2025). *International normalized ratio: Assessment, monitoring, and clinical implications*. In StatPearls [Internet]. StatPearls Publishing. https://www.ncbi.nlm.nih.gov/books/NBK507707/

Teka, F. S., Korsa, A. T., Bayisa, H. G., Fida, H. Y., & Senbeta, B. S. (2024). Adverse clinical outcomes of warfarin therapy and predictors among adult outpatients at public hospitals in Nekemte town, western Ethiopia: A retrospective cross-sectional study. *Thrombosis Update, 15*, 100170. https://doi.org/10.1016/j.tru.2024.100170

---
**Author:** FarahYusri12  
**Field:** Biomedical Science / Pharmacogenomics  
**Contact:** [LinkedIn](http://www.linkedin.com/in/farah-yusri) | [Gmail](mailto:farahyusri12@gmail.com)



