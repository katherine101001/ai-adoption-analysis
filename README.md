# 📊 AI Adoption Frontier — PySpark Big Data Analytics

> **150,000 company records · Full ML pipeline on distributed Apache Spark · 12-stage analysis**

---

## 📸 Screenshots

<!-- TODO: Add screenshots from the notebook outputs -->
<!-- Recommended: KMeans cluster plot, correlation heatmap, ROC curve, feature importance chart -->

---

## 🧱 Pipeline Architecture

```
┌──────────────────────────────────────────────────────────────────────┐
│                     ML Pipeline (12 Stages)                           │
├──────────┬──────────┬──────────┬──────────┬───────────┬─────────────┤
│ 1. Data  │ 2. Data  │ 3. DF    │ 4. Pre-  │ 5. EDA    │ 6. Spark    │
│ Ingestion│ Profiling│ API Ops  │ process  │           │ SQL         │
├──────────┼──────────┼──────────┼──────────┼───────────┼─────────────┤
│ 7. CUBE  │ 8. Window│ 9. KMeans│10. Stats │11. Binary │12. Random   │
│ Rollups  │ Functions│ Cluster  │ Testing  │ Classify  │ Forest Regr │
└──────────┴──────────┴──────────┴──────────┴───────────┴─────────────┘
```

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Distributed Engine** | Apache Spark 4.0 (PySpark) |
| **Query Language** | Spark SQL (temp views, JOINs, subqueries, CUBE, Window functions) |
| **ML Library** | Spark MLlib (KMeans, Logistic Regression, GBT, RandomForest) |
| **Statistical Testing** | Chi-Square test for categorical feature significance |
| **Visualization** | Matplotlib · Seaborn |
| **Data Size** | 150,000 company records · 20+ features |
| **Environment** | Jupyter Notebook |

---

## ✨ Analytical Stages

### 1. Data Ingestion & Quality Checks
- CSV ingestion of 150K company records via PySpark DataFrame API
- Schema inference and type validation
- Initial row count, column enumeration, basic descriptive stats

### 2. Data Profiling
- Missing value detection (`isnan` / `isnull` checks)
- Statistical summary: min, max, mean, stddev, countDistinct per column
- Data quality report generation

### 3. DataFrame API — Core Transformations
- Filter, groupBy, aggregate operations across company size, industry, revenue tiers
- Derived metrics: AI tool count per company, adoption density
- Multi-level aggregation with custom expressions

### 4. Data Preprocessing Pipeline
- Type correction (DoubleType, IntegerType casting)
- Null handling strategies per column
- Feature scaling and normalization for ML readiness

### 5. Exploratory Data Analysis (EDA)
- Distribution plots for key metrics (company size, revenue, AI spend)
- Industry-wise adoption patterns
- Correlation exploration between organizational attributes and AI maturity

### 6. Spark SQL — Temp Views, JOINs & Subqueries
- Registered DataFrames as temporary SQL views
- Complex multi-table JOIN queries
- Subquery-based filtering for targeted analysis segments

### 7. Advanced Spark SQL — CUBE Rollups & Window Functions
- **CUBE aggregations** — multi-dimensional rollups across industry x size x region
- **Window functions** — RANK, LAG, rolling averages for trend detection
- Hierarchical summarization at every dimension level

### 8. KMeans Clustering — Company Segmentation
- **4 company archetypes** identified via unsupervised clustering
- Optimal K determination using elbow method
- Cluster profiling: AI Leaders, Fast Followers, Cautious Adopters, Laggards
- Feature importance analysis per cluster

### 9. Correlation & Statistical Testing
- **Chi-Square testing** for categorical feature significance against AI adoption
- Correlation matrix heatmap for numerical feature relationships
- Feature selection informed by statistical rigor

### 10. Binary Classification — High Adopter Prediction
- **Logistic Regression** vs **Gradient Boosted Trees (GBT)** head-to-head
- Train/test split with stratified sampling
- Model evaluation: accuracy, precision, recall, F1, ROC-AUC
- Threshold tuning for business-relevant precision/recall trade-off

### 11. MLlib Pipeline — RandomForest Regression
- **AI Maturity Score prediction** using RandomForest regression
- Feature engineering: 9 custom metrics from raw company attributes
- Feature importance ranking — what drives AI adoption most?
- Cross-validation for model stability

### 12. Pandas API on Spark
- Bridge between PySpark and Pandas workflows
- Leveraged for final reporting and export
- Comparison of Spark-native vs Pandas-on-Spark performance

---

## 📡 Key Results

| Analysis | Method | Outcome |
|----------|--------|---------|
| Company Segmentation | KMeans (K=4) | 4 distinct AI adoption archetypes |
| Feature Significance | Chi-Square Test | Identified top predictors of AI adoption |
| Adopter Classification | Logistic Regression vs GBT | Binary classifier for high-adopter prediction |
| AI Maturity Prediction | RandomForest Regression | Feature-ranked maturity scoring model |

---

## 🗂️ Project Files

| File | Description |
|------|------------|
| `Group_1.ipynb` | Complete 12-stage Jupyter notebook (all code + outputs) |
| `Group_1.html` | Exported HTML snapshot with rendered charts and tables |

---

## 🚀 Getting Started

```bash
pip install pyspark matplotlib seaborn
jupyter notebook Group_1.ipynb
```

---

<p align="center">
  <i>PySpark 4.0 · Spark SQL · MLlib · 150K Records · 12-Stage Pipeline</i>
</p>
