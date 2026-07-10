<div align="center">

# 🔍 Exercise 3: Clustering Algorithms Comparison — K-Means vs DBSCAN
# 🔍 تمرین سوم: مقایسه الگوریتم‌های خوشه‌بندی — K-Means در مقابل DBSCAN

</div>

---

## 📝 Overview | نمای کلی

**English:**
This exercise compares two popular clustering algorithms — **K-Means** and **DBSCAN** — on the `airport-codes.csv` dataset. Using geographic features (latitude, longitude, elevation), we evaluate clustering performance with the Silhouette Score and visualize the resulting clusters.

**فارسی:**
این تمرین دو الگوریتم محبوب خوشه‌بندی — **K-Means** و **DBSCAN** — را روی دیتاست `airport-codes.csv` مقایسه می‌کند. با استفاده از ویژگی‌های جغرافیایی (عرض جغرافیایی، طول جغرافیایی، ارتفاع)، عملکرد خوشه‌بندی را با Silhouette Score ارزیابی و خوشه‌های حاصل را مصورسازی می‌کند.

---

## 📂 Dataset | دیتاست

| Property | Value |
|----------|-------|
| **File** | `airport-codes.csv` |
| **Description** | Global airport codes with geographic and elevation data |
| **Used Features** | `latitude_deg`, `longitude_deg`, `elevation_ft` |
| **Preprocessing** | StandardScaler (Z-Score normalization) |

---

## 🔧 Technologies & Libraries | تکنولوژی‌ها و کتابخانه‌ها

| Library | Purpose | کاربرد |
|---------|---------|--------|
| `pandas` | Data handling | مدیریت داده |
| `numpy` | Numerical operations | عملیات عددی |
| `sklearn.preprocessing.StandardScaler` | Feature scaling | مقیاس‌دهی ویژگی‌ها |
| `sklearn.cluster.KMeans` | K-Means clustering | خوشه‌بندی K-Means |
| `sklearn.cluster.DBSCAN` | DBSCAN clustering | خوشه‌بندی DBSCAN |
| `sklearn.metrics.silhouette_score` | Clustering evaluation | ارزیابی خوشه‌بندی |
| `matplotlib` | Cluster visualization | مصورسازی خوشه‌ها |

---

## 🤖 Algorithms | الگوریتم‌ها

### K-Means Clustering

| Parameter | Value | توضیحات |
|-----------|-------|---------|
| `n_clusters` | 4 | تعداد خوشه‌ها |
| `random_state` | 42 | برای تکرارپذیری |
| `n_init` | 10 | تعداد دفعات مقداردهی اولیه |

**How it works:** Partitions data into K clusters by minimizing within-cluster sum of squares.

**نحوه کار:** داده‌ها را به K خوشه تقسیم می‌کند با حداقل کردن مجموع مربعات درون‌خوشه‌ای.

---

### DBSCAN Clustering

| Parameter | Value | توضیحات |
|-----------|-------|---------|
| `eps` | 0.3 | شعاع همسایگی |
| `min_samples` | 10 | حداقل نقاط برای تشکیل خوشه |

**How it works:** Groups together points that are closely packed together, marking points in low-density regions as outliers (-1).

**نحوه کار:** نقاطی که نزدیک به هم هستند را گروه‌بندی می‌کند و نقاط در مناطق کم‌چگالی را به عنوان نویز (-۱) علامت‌گذاری می‌کند.

---

## 📊 Evaluation Metric | معیار ارزیابی

| Metric | Description | توضیحات |
|--------|-------------|---------|
| **Silhouette Score** | Measures how similar an object is to its own cluster vs. other clusters | شباهت یک نمونه به خوشه خودش در مقابل خوشه‌های دیگر |

**Score range:** [-1, +1] | **بازه نمره:** [-۱، +۱]
- **+1** → Perfect clustering | خوشه‌بندی عالی
- **0** → Overlapping clusters | خوشه‌های هم‌پوشان
- **-1** → Incorrect clustering | خوشه‌بندی نادرست

---

## 📈 Outputs | خروجی‌ها

| Output | Description | توضیحات |
|--------|-------------|---------|
| Silhouette Score (K-Means) | Clustering quality score | نمره کیفیت خوشه‌بندی |
| Silhouette Score (DBSCAN) | Clustering quality score (excluding noise) | نمره کیفیت خوشه‌بندی (بدون نویز) |
| `K-Means Clusters` plot | 2D scatter of K-Means clusters | نمودار پراکندگی K-Means |
| `DBSCAN Clusters` plot | 2D scatter of DBSCAN clusters (noise = -1) | نمودار پراکندگی DBSCAN (نویز = -۱) |

---

## 🚀 How to Run | نحوه اجرا

```bash
# Install dependencies | نصب وابستگی‌ها
pip install pandas numpy matplotlib scikit-learn

# Run the script | اجرای اسکریپت
python exercise3.py
```

---

## 🏆 Comparison Criteria | معیارهای مقایسه

| Criteria | K-Means | DBSCAN |
|----------|---------|--------|
| Requires cluster count | ✅ Yes | ❌ No |
| Detects outliers | ❌ No | ✅ Yes |
| Cluster shape | Spherical only | Any shape |
| Works with large data | ✅ Yes | ⚠️ Moderate |
| Sensitive to initialization | ✅ Yes | ❌ No |

---

<div align="center">

**🎓 Part of Data Mining Course Exercises | بخشی از تمرینات درس داده‌کاوی**

</div>
