# 🧬 Newborn Screening Data Analysis | تحلیل داده‌های غربالگری نوزادان

This project contains a full pipeline for cleaning, exploring, visualizing, and modeling newborn screening data from California.  
این پروژه شامل یک روند کامل برای پاک‌سازی، بررسی، تصویرسازی و مدل‌سازی داده‌های غربالگری نوزادان در ایالت کالیفرنیا است.

---

## 📁 Contents | محتوای پروژه
- `newborn.xlsx`: Raw dataset (from California newborn screening)
- `newborn_analysis_notebook.ipynb`: Full Jupyter notebook with all code and visualizations
- `newborn_analysis_report.md`: Full markdown report
- `README.md`: This description file

---

## 🧼 Steps Covered | مراحل انجام‌شده

1. **Primary Cleaning**: Column renaming, trimming, formatting  
   پاک‌سازی اولیه شامل اصلاح نام ستون‌ها و حذف نویز

2. **Missing & Type Checking**: Ensuring data integrity  
   بررسی مقادیر گمشده و نوع داده‌ها

3. **Outlier Detection**: Using IQR method  
   شناسایی مقادیر پرت با روش فاصله بین چارکی (IQR)

4. **Unique Value Analysis**  
   بررسی تعداد مقادیر یکتا و طبقه‌بندی ناحیه‌ها و بیماری‌ها

5. **Descriptive Statistics**  
   تحلیل آماری توصیفی شامل میانگین، میانه و ...

6. **Visualization**  
   نمودارهای ستونی، پراکندگی و مقایسه‌ای

7. **Linear Regression**  
   رگرسیون ساده و چندمتغیره برای بررسی پیش‌بینی‌پذیری داده‌ها

---

## ❓ What Questions Does This Project Answer?  
## ❓ این پروژه به چه سوالاتی پاسخ داده است؟

1. How many different disorders are detected in each region?  
   در هر ناحیه چند نوع اختلال ژنتیکی متفاوت شناسایی شده است؟

2. Which disorders are more prevalent across multiple regions?  
   کدام بیماری‌ها در چند ناحیه مختلف دیده شده‌اند و بیشتر گسترش دارند؟

3. Is there a relationship between the number of screened newborns and detected cases?  
   آیا بین تعداد نوزادان غربال‌شده و تعداد موارد شناسایی‌شده بیماری رابطه‌ای وجود دارد؟

4. Which regions report higher case counts or higher disorder percentages?  
   کدام نواحی تعداد بیشتری از بیماری‌ها یا درصد بالاتری از اختلالات را گزارش می‌دهند؟

5. Can we predict the number of disease cases using variables like screening size or disorder percent?  
   آیا می‌توان تعداد بیماری‌ها را بر اساس متغیرهایی مثل تعداد غربالگری یا درصد اختلال پیش‌بینی کرد؟

6. Are certain regions significantly associated with higher or lower disease detection rates?  
   آیا بعضی از نواحی به‌طور معناداری با نرخ بالاتر یا پایین‌تر شناسایی بیماری‌ها مرتبط هستند؟

---

## 📊 Regression Interpretation | تفسیر خروجی مدل‌های رگرسیون

### 🔹 Simple Linear Regression
- **R² = 0.042**: Very weak predictive power.
- **Conclusion**: Screening size alone is not a strong predictor.
  
📌 قدرت پیش‌بینی مدل خیلی ضعیف است. تعداد غربالگری به‌تنهایی برای پیش‌بینی تعداد بیماری‌ها کافی نیست.

---

### 🔹 Multiple Linear Regression (With Percent and Region)
- **R² = 0.866**: Very strong predictive model.
- **Significant predictors**: 
  - `percent_of_all_disorders_in_region` (very significant)
  - `california_region_Los Angeles` (significant positive effect)
- **number_screened**: Not significant anymore

📌 درصد اختلالات در منطقه و برخی نواحی مثل لس‌آنجلس نقش کلیدی دارند. مدل بسیار دقیق‌تر از حالت ساده است.

---

### 🔹 Categorical Region Effects
- Certain regions have no significant impact (e.g., Bay Area, Northern Inland)
- Only **Los Angeles** shows strong influence

📌 برخی نواحی تفاوت معناداری ندارند، اما لس‌آنجلس به‌طور مشخص با افزایش تعداد بیماری‌ها مرتبط است.

---

## 📈 Tools Used | ابزارهای استفاده‌شده
- Python 🐍
- Pandas / Matplotlib / Seaborn 📊
- Statsmodels for regression analysis 📉
- Jupyter Notebook 📒

---

**Feel free to fork or extend the project!**  
**برای توسعه یا استفاده از پروژه، آزاد هستید!**
---

## 👩‍💻 Author | نویسنده

**Elham Jofreh**  
GitHub: [github.com/elham-jofreh](https://github.com/elham-jofreh)

This project is part of Elham’s work on healthcare data analysis and modeling using real-world newborn screening data.
