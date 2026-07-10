<div align="center">

# 📊 Exercise 1: Statistical Analysis & Data Visualization
# 📊 تمرین اول: تحلیل آماری و مصورسازی داده

</div>

---

## 📝 Overview | نمای کلی

**English:**
This exercise performs comprehensive statistical analysis and data visualization on the `airport-codes.csv` dataset. It includes descriptive statistics, distribution analysis, correlation analysis, and various types of plots to understand the data structure.

**فارسی:**
این تمرین تحلیل آماری جامع و مصورسازی داده‌ها را روی دیتاست `airport-codes.csv` انجام می‌دهد. شامل آمار توصیفی، تحلیل توزیع، تحلیل همبستگی و انواع نمودارها برای درک ساختار داده‌هاست.

---

## 📂 Dataset | دیتاست

| Property | Value |
|----------|-------|
| **File** | `airport-codes.csv` |
| **Description** | Global airport codes with geographic and elevation data |
| **Features** | `latitude_deg`, `longitude_deg`, `elevation_ft`, `type`, `name`, `iso_country`, etc. |

---

## 🔧 Technologies & Libraries | تکنولوژی‌ها و کتابخانه‌ها

- `pandas` — Data manipulation and analysis | دستکاری و تحلیل داده
- `numpy` — Numerical computing | محاسبات عددی
- `matplotlib` — Data visualization | مصورسازی داده
- `seaborn` — Statistical data visualization | مصورسازی آماری داده
- `scipy` — Scientific computing | محاسبات علمی

---

## 📈 Analysis Steps | مراحل تحلیل

| Step | English | فارسی |
|------|---------|-------|
| 1 | Load and inspect dataset | بارگذاری و بررسی دیتاست |
| 2 | Descriptive statistics (mean, median, mode, variance, std, skewness, kurtosis) | آمار توصیفی (میانگین، میانه، مد، واریانس، انحراف معیار، چولگی، کشیدگی) |
| 3 | Five-number summary & Box plots | خلاصه پنج عددی و نمودار جعبه‌ای |
| 4 | Histograms & Density plots | هیستوگرام و نمودار چگالی |
| 5 | Scatter plots & Line plots | نمودار پراکندگی و نمودار خطی |
| 6 | Bar charts & Pie charts | نمودار میله‌ای و نمودار دایره‌ای |
| 7 | Correlation heatmap | نقشه گرمایی همبستگی |
| 8 | Pair plots & Violin plots | نمودارهای جفتی و ویولن |
| 9 | Missing data analysis | تحلیل داده‌های گمشده |

---

## 🖼️ Generated Outputs | خروجی‌های تولید شده

| File | Description | توضیحات |
|------|-------------|---------|
| `boxplots.png` | Box plots for numeric columns | نمودارهای جعبه‌ای ستون‌های عددی |
| `histograms.png` | Distribution histograms | هیستوگرام‌های توزیع |
| `density_plots.png` | KDE density plots | نمودارهای چگالی KDE |
| `scatter_plots.png` | Scatter plot pairs | نمودارهای پراکندگی جفتی |
| `line_plot.png` | Trend line plot | نمودار خطی روند |
| `bar_plot.png` | Mean value bar chart | نمودار میله‌ای میانگین‌ها |
| `pie_chart.png` | Category distribution pie chart | نمودار دایره‌ای توزیع دسته‌ها |
| `correlation_heatmap.png` | Correlation matrix heatmap | نقشه گرمایی ماتریس همبستگی |
| `pair_plot.png` | Pairwise relationship plots | نمودارهای روابط جفتی |
| `violin_plots.png` | Violin distribution plots | نمودارهای ویولن |
| `missing_data.png` | Missing data analysis chart | نمودار تحلیل داده‌های گمشده |

---

## 🚀 How to Run | نحوه اجرا

```bash
# Install dependencies | نصب وابستگی‌ها
pip install pandas numpy matplotlib seaborn scipy

# Run the script | اجرای اسکریپت
python exercise1.py
```

---

## 📊 Key Statistical Metrics | معیارهای آماری کلیدی

The script computes: | اسکریپت محاسبه می‌کند:
- **Mean** (میانگین)
- **Median** (میانه)
- **Mode** (مد)
- **Variance** (واریانس)
- **Standard Deviation** (انحراف معیار)
- **Skewness** (چولگی)
- **Kurtosis** (کشیدگی)
- **Five-number Summary** (خلاصه پنج عددی: Min, Q1, Q2, Q3, Max)
- **IQR** (دامنه میان‌چارکی)

---

<div align="center">

**🎓 Part of Data Mining Course Exercises | بخشی از تمرینات  داده‌کاوی**

</div>
