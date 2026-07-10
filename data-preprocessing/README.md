<div align="center">

# 🧹 Exercise 2: Data Preprocessing
# 🧹 تمرین دوم: پیش‌پردازش داده

</div>

---

## 📝 Overview | نمای کلی

**English:**
This exercise covers complete data preprocessing pipeline on the `airport-codes.csv` dataset. It includes data cleaning (handling missing values, removing duplicates, outlier detection), data transformation (normalization, standardization, label encoding, discretization), and saving processed datasets.

**فارسی:**
این تمرین pipeline کامل پیش‌پردازش داده را روی دیتاست `airport-codes.csv` پوشش می‌دهد. شامل پاکسازی داده (مدیریت مقادیر گمشده، حذف تکراری‌ها، تشخیص داده‌های پرت)، تبدیل داده (نرمال‌سازی، استانداردسازی، کدگذاری برچسب، گسسته‌سازی) و ذخیره دیتاست‌های پردازش شده.

---

## 📂 Dataset | دیتاست

| Property | Value |
|----------|-------|
| **File** | `airport-codes.csv` |
| **Description** | Global airport codes with geographic and elevation data |
| **Features** | `latitude_deg`, `longitude_deg`, `elevation_ft`, `type`, `name`, `iso_country`, etc. |

---

## 🔧 Technologies & Libraries | تکنولوژی‌ها و کتابخانه‌ها

| Library | Purpose | کاربرد |
|---------|---------|--------|
| `pandas` | Data manipulation | دستکاری داده |
| `numpy` | Numerical operations | عملیات عددی |
| `matplotlib` | Visualization | مصورسازی |
| `seaborn` | Statistical plots | نمودارهای آماری |
| `sklearn.preprocessing` | StandardScaler, MinMaxScaler, LabelEncoder | پیش‌پردازش |
| `sklearn.impute` | SimpleImputer | پر کردن مقادیر گمشده |

---

## 🔄 Preprocessing Pipeline | Pipeline پیش‌پردازش

### 1️⃣ Data Cleaning | پاکسازی داده

| Task | Method | روش |
|------|--------|-----|
| Missing Values (Numeric) | Fill with Median | پر کردن با میانه |
| Missing Values (Categorical) | Fill with Mode | پر کردن با مد |
| Duplicate Records | Remove duplicates | حذف رکوردهای تکراری |
| Outlier Detection | IQR Method (Q1 - 1.5×IQR, Q3 + 1.5×IQR) | روش IQR |

### 2️⃣ Data Transformation | تبدیل داده

| Transformation | Method | Description | توضیحات |
|----------------|--------|-------------|---------|
| Normalization | Min-Max Scaler | Scales to [0, 1] range | مقیاس‌دهی به بازه [۰، ۱] |
| Standardization | Z-Score (StandardScaler) | Mean=0, Std=1 | میانگین=۰، انحراف معیار=۱ |
| Label Encoding | LabelEncoder | Categorical → Numeric | دسته‌ای → عددی |
| Discretization | pd.cut | Continuous → 5 Bins | پیوسته → ۵ بازه |

---

## 📤 Output Files | فایل‌های خروجی

### Processed Datasets | دیتاست‌های پردازش شده

| File | Description | توضیحات |
|------|-------------|---------|
| `cleaned_dataset.csv` | Dataset after cleaning | دیتاست پس از پاکسازی |
| `normalized_dataset.csv` | Min-Max normalized data | داده‌های نرمال‌سازی شده |
| `standardized_dataset.csv` | Z-Score standardized data | داده‌های استانداردسازی شده |

### Visualization Outputs | خروجی‌های مصورسازی

| File | Description | توضیحات |
|------|-------------|---------|
| `data_cleaning_comparison.png` | Before/After missing data comparison | مقایسه داده‌های گمشده قبل و بعد |
| `outlier_detection.png` | Box plots with outlier bounds | نمودار جعبه‌ای با محدوده پرت |
| `normalization_comparison.png` | Before/After normalization histograms | هیستوگرام‌های قبل و بعد نرمال‌سازی |

---

## 🚀 How to Run | نحوه اجرا

```bash
# Install dependencies | نصب وابستگی‌ها
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the script | اجرای اسکریپت
python exercise2.py
```

---

## 📊 Preprocessing Summary Report | گزارش خلاصه پیش‌پردازش

The script performs: | اسکریپت این کارها را انجام می‌دهد:

1. ✅ **Data Cleaning | پاکسازی داده**
   - Fills all missing values | پر کردن تمام مقادیر گمشده
   - Removes duplicate records | حذف رکوردهای تکراری
   - Identifies outliers using IQR | شناسایی داده‌های پرت با IQR

2. ✅ **Data Transformation | تبدیل داده**
   - Min-Max normalization on numeric columns | نرمال‌سازی Min-Max روی ستون‌های عددی
   - Z-Score standardization | استانداردسازی Z-Score
   - Label encoding for categorical features | کدگذاری برچسب برای ویژگی‌های دسته‌ای
   - Discretization into 5 bins | گسسته‌سازی به ۵ بازه

---

<div align="center">

**🎓 Part of Data Mining Course Exercises | بخشی از تمرینات درس داده‌کاوی**

</div>
