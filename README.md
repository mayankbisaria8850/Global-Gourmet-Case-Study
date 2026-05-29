# Global-Gourmet-Case-Study
# 🍽️ Global Gourmet Challenge

### End-to-End AI Architecture for Last-Mile Delivery Optimization

An end-to-end **machine learning and analytics pipeline** developed for the **Global Gourmet Operational Excellence Challenge (Ingenium, IIT Indore)** to optimize food delivery logistics, customer retention, and revenue generation using predictive analytics, NLP, churn modeling, and economic optimization.

The project integrates **ETL pipelines, ETA prediction, sentiment analysis, topic modeling, churn propensity estimation, and dynamic surge pricing** into a unified decision-making system for large-scale food-tech operations.

---

## 📌 Problem Statement

Large-scale food delivery platforms face operational challenges including:

* Inaccurate **delivery time predictions (ETA)**
* Customer dissatisfaction from **late deliveries and poor service**
* Difficulty analyzing **large volumes of customer feedback**
* High **customer churn**
* Inefficient **surge pricing mechanisms**

The objective was to design a **production-inspired, multi-stage AI system** capable of improving delivery efficiency, customer experience, and platform revenue.

---

## 🚀 Key Features

### 1. Data Engineering & ETL Pipeline

* Built a robust **ETL pipeline** to integrate heterogeneous datasets:

  * Transactional order logs
  * Restaurant metadata
  * Courier telemetry data
* Implemented:

  * Duplicate handling
  * NULL value imputation
  * UTC timezone normalization
  * Spatio-temporal joins with **180-second timestamp tolerance**
* Generated a unified **Golden Table** for downstream ML workflows.

### 2. Spatio-Temporal ETA Prediction Engine

* Developed a high-fidelity **ETA regression system** using **XGBoost**.
* Performed advanced **feature engineering**, including:

  * Kitchen lag estimation
  * Peak-hour travel decay
  * Geospatial zone encoding
  * Weather integration
  * Holiday/event signals
  * Cuisine-specific encoding
* Designed a **custom asymmetric loss function** to penalize delivery lateness more heavily than early deliveries.

### 3. NLP-Based Customer Intelligence

* Built a **sentiment classification pipeline** using **VADER** to classify reviews into:

  * Satisfied
  * Neutral
  * Dissatisfied
* Applied **BERTopic** for grievance mining to identify major customer pain points:

  * Cold food
  * Missing items
  * Driver professionalism
  * Late delivery
* Quantified the relationship between ETA errors and negative reviews using **logistic regression**.

### 4. Customer Churn Prediction

* Developed a **Random Forest-based churn prediction model**.
* Engineered behavioral features including:

  * Historical delivery lateness
  * Negative review frequency
  * Changes in ordering patterns
* Optimized decision thresholds using **F2-score maximization** to prioritize recall and reduce missed churners.

### 5. Economic Optimization & Surge Pricing

* Designed a **dynamic surge pricing framework** using constrained optimization (**SLSQP**).
* Implemented:

  * Segment-wise elasticity modeling
  * Revenue maximization
  * Churn-aware pricing constraints
* Generated adaptive pricing strategies across customer segments.

---

## 🏗️ Project Architecture

```text
Raw Data Sources
│
├── Transaction Logs (SQL)
├── Restaurant Metadata (JSON)
└── Courier Telemetry (CSV/Parquet)
        │
        ▼
ETL Pipeline & Golden Table Generation
        │
        ▼
ETA Prediction Engine (XGBoost + Feature Engineering)
        │
        ▼
Customer Review Analysis (VADER + BERTopic)
        │
        ▼
Churn Prediction (Random Forest)
        │
        ▼
Dynamic Surge Optimization (SLSQP)
        │
        ▼
Business Insights & Decision Support
```

---

## 📊 Results

| Metric                     | Performance      |
| -------------------------- | ---------------- |
| ETA Prediction MAE         | **1.30 minutes** |
| Spatio-Temporal Match Rate | **95%+**         |
| Churn Recall               | **100%**         |
| Revenue Uplift             | **+27.6%**       |
| Extreme ETA Outliers       | **1.73%**        |

Key outcomes:

* Reduced ETA prediction errors significantly.
* Identified operational bottlenecks using NLP insights.
* Achieved **100% churn recall** through threshold optimization.
* Increased projected platform revenue through **adaptive surge pricing**.

---

## 🛠️ Tech Stack

### Languages & Libraries

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-Learn**
* **XGBoost**
* **BERTopic**
* **NLTK (VADER)**
* **SciPy**
* **SHAP**
* **Matplotlib**

### Data Sources

* NYC TLC Trip Data
* Yelp Academic Dataset
* Open-Meteo Weather API
* Holiday Calendar APIs

---

## 📂 Project Structure

```text
Global-Gourmet-Challenge/
│── data/
│── notebooks/
│   └── Ingenium.ipynb
│── reports/
│   └── Solution_Report.pdf
│── visualizations/
│── src/
│   ├── etl_pipeline.py
│   ├── eta_model.py
│   ├── sentiment_analysis.py
│   ├── churn_model.py
│   └── surge_optimizer.py
│── requirements.txt
│── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/global-gourmet-challenge.git
cd global-gourmet-challenge
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook Ingenium.ipynb
```

---

## 📈 Future Improvements

* Real-time ETA prediction using streaming telemetry.
* Deep learning-based sequence modeling for delivery forecasting.
* Multi-city deployment and scalable infrastructure.
* Reinforcement learning for adaptive pricing optimization.
* Explainable AI dashboards for business stakeholders.

---

## 👥 Contributors

**Mayank Bisaria**
Chemical Engineering + Data Science
Indian Institute of Technology (IIT) Indore

---

## 📜 Acknowledgements

Developed as part of the **Global Gourmet Operational Excellence Challenge** conducted during **Ingenium, IIT Indore**.
