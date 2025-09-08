<p align="center">
  <img src="5 Assets/Banner.png" width="100%">
</p>

# ✈️ Flight Cancellation Prediction for US Airlines

*AI-powered prediction of domestic US flight cancellations using airline data from 2021-2023, modelled with machine learning and dashboarded via Dash.*

- Topics covered: **Airline Operations Analytics**  
- Models used: **Random Forest, Logistic Regression**  
- Skills demonstrated: **Feature Engineering, ROC analysis, Dashboarding**  
- Expected outcome:  
  - **Predict flight cancellations with ML**  
  - **Enable planning for passengers & airlines**

---

## 👥 Authors

**Sam Hossain** and MMA Team Gordon Members (Alisha Sahota, Anthony Ramelo, Chris Wu, Elizabeth Zhang, Emily Zhao)

---

## 🔍 Problem Statement

**Goal:**  

Forecast whether a US domestic flight is likely to be cancelled, using historical flight, delay, and airline data.

**Challenges Addressed:**
- Low cancellation rate (2.1%) created class imbalance
- Categorical variables with high cardinality (Airlines, Airports)
- Incorporating temporal variables (year, month, day)
- Interpreting model output for operational insight

---

## 🔧 Workflow

### ✅ Data Preparation
- Loaded ~600K domestic flight records (2021-2023)
- Extracted `Year`, `Month`, `Day` from `Flight_Date`
- Cast key identifiers (`Airline`, `Origin`, `Destination`) as categorical
- Created binary targets for cancellation and reason-based cancellations
- Removed columns with high multicollinearity or limited predictive value

### 🤖 Models Built

| Model | Type | Target | Handling | Evaluation |
|-------|------|--------|----------|-------------|
| Logistic Regression | Linear Classifier | Cancelled (0/1) | Balanced weights | ROC AUC = 0.70  |
| Random Forest | Tree Ensemble | Cancelled (0/1) | Class-balanced, grid-tuned | ROC AUC = 0.72  |

**🔹 Verdict:** Random Forest provided better class separation and was selected for the dashboard.

<p align="center">
  <img src="5 Assets/Model1.png" width="80%">
</p>

### 🛬 Cancellation Analysis & Dashboard Workflow
- Cleaned data and transformed categorical/time variables
- Explored cancellations by **month, day, year, airline, origin city**
- Built final prediction model using Random Forest
- Created interactive **Dash app** to predict based on inputs: `Year`, `Month`, `Date`, `Airline`, `Origin`, `Destination`
- Output = Canceled / Not Canceled

---

## 🎯 Key Findings

* Monthly cancellation spikes in **January, July, December**  
* Highest cancellations on **Mondays & Fridays**  
* Disproportionate cancellations concentrated in **specific airports** (e.g., ATL, ORD, DFW)

<p align="center">
  <img src="5 Assets/Findings1.png" width="80%">
  <img src="5 Assets/Findings2.png" width="80%">
  <img src="5 Assets/Findings3.png" width="80%">
  <img src="5 Assets/Findings4.png" width="80%">
</p>

---

## 💡 Key Recommendations

* Pre-warn passengers in **high-risk months** with alerts or flexible booking offers
* Reinforce operations staffing on **Mondays/Fridays**
* Prioritize contingency planning at **top 10 volatile airports**

<p align="center">
  <img src="5 Assets/Recommendation1.png" width="80%">
  <img src="5 Assets/Recommendation2.png" width="80%">
  <img src="5 Assets/Recommendation3.png" width="80%">
</p>

---

## 📊 Output Dashboard

<p align="center">
  <img src="5 Assets/Dashboard1.png" width="80%">
</p>

---

## 🚀 How to Run This Project

1. **Clone the repository**
```bash
git clone https://github.com/SamHossain2025/Flight-Data-Analysis.git
cd Flight-Data-Analysis
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

4. **Open and execute notebooks**
* `01_data_cleaning.ipynb` → Clean & export CSV
* `02_eda_visualizations.ipynb` → Cancellation visuals
* `03_model_training_evaluation.ipynb` → Model training + ROC
* `04_dashboard_demo.ipynb` → Run Dash App

---

## 🧬 Data Sources

* 📌 [US BTS Flight Delay Data](https://www.transtats.bts.gov/)  
* 📌 Public airline operation datasets (via Kaggle)

---

## 🔓 License

This project is licensed under the [MIT License](LICENSE)












