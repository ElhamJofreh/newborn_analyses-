# Newborn Case Count Prediction 📊

This project uses **scikit-learn** to train a linear regression model that predicts the number of genetic disorder cases based on newborn screening data from different regions of California.

## 📁 Files Included

- `sklearn_excel_model.ipynb` – Main Jupyter Notebook with data cleaning, dummy variable conversion, and model training.
- `newborn.xlsx` – Excel file with the screening data (make sure to include this manually).
- `README.md` – You are reading it :)

## 🔍 How to Use

1. Upload the `newborn.xlsx` file into the same directory.
2. Open the notebook `sklearn_excel_model.ipynb` in Jupyter.
3. Run the notebook step-by-step to train and evaluate the regression model.
4. Check the R² score, coefficients, and prediction plot for evaluation.

## 🎯 Target

The model predicts:
- `Case Count` (تعداد موارد بیماری‌ها)

Based on:
- `Number Screened` (تعداد افراد غربال شده)
- `Region` and `Disease` (منطقه و نوع بیماری) – converted to dummy variables

---

## 👩‍💻 Author

Created by **Elham Jofreh**

Inspired by real-world newborn screening data from California.

