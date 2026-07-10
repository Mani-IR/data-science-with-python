<div align="center">

# 🌳 Exercise 4: Classification with Decision Tree & Naive Bayes
# 🌳 تمرین چهارم: طبقه‌بندی با درخت تصمیم و Naive Bayes

</div>

---

## 📝 Overview | نمای کلی

**English:**
This exercise implements and compares two classification algorithms — **Decision Tree** and **Naive Bayes** — on the `airport-codes.csv` dataset. Using geographic features, we predict the airport type and evaluate model performance using accuracy score and classification report.

**فارسی:**
این تمرین دو الگوریتم طبقه‌بندی — **درخت تصمیم** و **Naive Bayes** — را روی دیتاست `airport-codes.csv` پیاده‌سازی و مقایسه می‌کند. با استفاده از ویژگی‌های جغرافیایی، نوع فرودگاه را پیش‌بینی و عملکرد مدل را با accuracy score و گزارش طبقه‌بندی ارزیابی می‌کند.

---

## 📂 Dataset | دیتاست

| Property | Value |
|----------|-------|
| **File** | `airport-codes.csv` |
| **Description** | Global airport codes with geographic and elevation data |
| **Features (X)** | `latitude_deg`, `longitude_deg`, `elevation_ft` |
| **Target (y)** | `type` (airport type: small, medium, large, closed, etc.) |

---

## 🔧 Technologies & Libraries | تکنولوژی‌ها و کتابخانه‌ها

| Library | Purpose | کاربرد |
|---------|---------|--------|
| `pandas` | Data handling | مدیریت داده |
| `sklearn.model_selection.train_test_split` | Train-test split | تقسیم داده آموزش و تست |
| `sklearn.preprocessing.LabelEncoder` | Encode target labels | کدگذاری برچسب‌های هدف |
| `sklearn.tree.DecisionTreeClassifier` | Decision Tree classifier | طبقه‌بند درخت تصمیم |
| `sklearn.naive_bayes.GaussianNB` | Gaussian Naive Bayes | Naive Bayes گاوسی |
| `sklearn.metrics` | accuracy_score, classification_report | معیارهای ارزیابی |

---

## 🤖 Algorithms | الگوریتم‌ها

### Decision Tree Classifier | طبقه‌بند درخت تصمیم

| Parameter | Value | توضیحات |
|-----------|-------|---------|
| `random_state` | 42 | برای تکرارپذیری |
| `criterion` | default (`gini`) | معیار تقسیم: Gini Index |

**How it works:** Recursively splits data based on feature values to create a tree structure for classification decisions.

**نحوه کار:** به صورت بازگشتی داده‌ها را بر اساس مقادیر ویژگی‌ها تقسیم می‌کند تا ساختار درختی برای تصمیم‌گیری طبقه‌بندی ایجاد شود.

---

### Gaussian Naive Bayes | Naive Bayes گاوسی

| Parameter | Value | توضیحات |
|-----------|-------|---------|
| default | — | بدون پارامتر اجباری |

**How it works:** Applies Bayes' theorem with the assumption that features follow a Gaussian (normal) distribution and are independent.

**نحوه کار:** قضیه بیز را با فرض اینکه ویژگی‌ها از توزیع گاوسی (نرمال) پیروی می‌کنند و مستقل هستند، اعمال می‌کند.

---

## 📊 Model Evaluation | ارزیابی مدل

| Metric | Description | توضیحات |
|--------|-------------|---------|
| **Accuracy Score** | Ratio of correct predictions to total predictions | نسبت پیش‌بینی‌های صحیح به کل پیش‌بینی‌ها |
| **Classification Report** | Precision, Recall, F1-score per class | دقت، بازیابی، امتیاز F1 برای هر کلاس |

---

## 🔄 Workflow | گردش کار

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Load Dataset   │────▶│  Preprocessing  │────▶│  Label Encoding │
│  بارگذاری دیتاست │     │  پیش‌پردازش     │     │  کدگذاری برچسب  │
└─────────────────┘     └─────────────────┘     └────────┬────────┘
                                                         │
                              ┌──────────────────────────┘
                              ▼
                    ┌─────────────────┐
                    │ Train/Test Split│
                    │ تقسیم آموزش/تست │
                    │   (70% / 30%)   │
                    └────────┬────────┘
                             │
            ┌────────────────┼────────────────┐
            ▼                ▼                ▼
    ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
    │Decision Tree │  │  Gaussian    │  │   Compare    │
    │  Classifier  │  │ Naive Bayes  │  │  Results     │
    │درخت تصمیم    │  │  نیو بیز     │  │ مقایسه نتایج │
    └──────────────┘  └──────────────┘  └──────────────┘
```

---

## 📈 Outputs | خروجی‌ها

| Output | Description | توضیحات |
|--------|-------------|---------|
| `Accuracy Decision Tree` | Accuracy of Decision Tree model | دقت مدل درخت تصمیم |
| `Accuracy Naive Bayes` | Accuracy of Naive Bayes model | دقت مدل Naive Bayes |
| `Classification Report` | Detailed per-class metrics | معیارهای دقیق هر کلاس |
| `Final Comparison` | Which model performed better | کدام مدل بهتر عمل کرد |

---

## 🚀 How to Run | نحوه اجرا

```bash
# Install dependencies | نصب وابستگی‌ها
pip install pandas scikit-learn

# Run the script | اجرای اسکریپت
python exercise4.py
```

---

## 🏆 Algorithm Comparison | مقایسه الگوریتم‌ها

| Criteria | Decision Tree | Naive Bayes |
|----------|---------------|-------------|
| Interpretability | ✅ High (visualizable) | ⚠️ Moderate |
| Training speed | ✅ Fast | ✅ Very Fast |
| Handles non-linear data | ✅ Yes | ❌ Limited |
| Assumes feature independence | ❌ No | ✅ Yes |
| Handles continuous data | ✅ Yes | ✅ Yes (Gaussian) |
| Prone to overfitting | ⚠️ Yes (without pruning) | ❌ No |

---

<div align="center">

**🎓 Part of Data Mining Course Exercises | بخشی از تمرینات  داده‌کاوی**

</div>
