# WIJDAN — Student Mental Health Risk Prediction

A machine learning project designed to analyze student lifestyle, academic, and psychosocial factors to predict **mental health risk levels** (Low, Medium, High). The project covers the complete data science lifecycle, from exploratory data analysis to automated pipeline orchestration with Apache Airflow and an interactive Streamlit application.

---

## 🎯 Objectives
- **Risk Detection:** Identify students showing patterns associated with elevated psychological risk.
- **Factor Understanding:** Uncover key relationships between academic pressure, sleep, financial stress, and mental health.
- **End-to-End Pipeline:** Build a robust, leak-free machine learning workflow with automated retraining and interactive inference.

---

## 📊 Dataset
- **Source:** [Mental Health Risk Prediction Dataset (Students) - Kaggle](https://www.kaggle.com/datasets/maqdadali/mental-health-risk-prediction-dataset-students)
- **Size:** 2,000 records × 17 features
- **Target Variable:** `Mental_Health_Risk` (Low / Medium / High)
- **Key Indicators:** Sleep hours, GPA, study hours, financial stress, screen time, physical activity, family support, and prior mental health history.

---

## 🛠️ Tech Stack
- **Language:** Python 3.10
- **Data & ML:** Pandas, NumPy, Scikit-learn, Joblib, Matplotlib, Seaborn
- **Orchestration:** Apache Airflow (Docker)
- **Database:** PostgreSQL
- **UI & Visualization:** Streamlit

---

## 📚 Documentation & Quick Links
- ℹ️ **[Project Info & External Links](info.md)** — List of technologies and dataset / documentation links.
- 🚀 **[Bootstrap Guide](bootstrap.md)** — Guide outline for launching Docker, Airflow, and the Streamlit app.

---

## 📁 Repository Structure

```
WIJDAN/
├── data/                  # Raw dataset & data documentation
├── dags/                  # Apache Airflow DAGs
├── src/                   # Source code modules (preprocessing, training, evaluation)
├── models/                # Trained and serialized model pipelines (.joblib)
├── reports/               # Performance metrics and evaluation artifacts
├── notebook/              # Jupyter notebooks for exploration and experimentation
├── Dockerfile             # Custom Airflow container image
├── docker-compose.yaml    # Container orchestration (Airflow + Postgres)
├── requirements.txt       # Python dependencies
├── bootstrap.md           # [bootstrap.md](bootstrap.md) — Service startup outline
└── info.md                # [info.md](info.md) — Technologies and reference links
```

---

## ⚠️ Pedagogical Disclaimer
This project is strictly educational. The resulting model is a supervised learning prototype and must not be used as a clinical diagnostic tool, medical screening instrument, or for institutional disciplinary/admission decisions.
