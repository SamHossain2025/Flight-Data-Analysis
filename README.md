# ✈️ Flight Delay & Cancellation Prediction (US Domestic)

A predictive analytics project focused on analyzing and modeling flight cancellations and delays in the US domestic aviation market. This was developed as part of the **MMA 867 - Predictive Modeling** course at Queen’s University.

## 📊 Project Objective

To build an interpretable machine learning model that predicts the likelihood of a flight being **canceled**, based on historical US domestic flight data. The objective is to extract insights that can help airlines and passengers **anticipate cancellations**, reduce uncertainty, and improve planning.

---

## 📁 Folder Structure

Flight-Data-Analysis/
│
├── 📂 Data/ # Raw and cleaned flight data (2021–2023)
├── 📂 Notebooks/ # Exploratory analysis and modeling in Jupyter
├── 📂 Visualizations/ # Charts and graphs for cancellation analysis
├── 📂 Dash_App/ # Interactive dashboard using Dash
├── 📂 Reports/ # Final project report, slides, and documentation
├── 📂 Models/ # Trained Random Forest and Logistic models
├── README.md # You're here

Flight-Data-Analysis/
│
├──  Final_Report.pdf
├──  README_template.md
├──  model_logistic.pkl
├──  model_rf.pkl
├──  project_notebook.ipynb
└──  requirements.txt


---

## 🔧 Tools & Technologies

- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly)
- **Dash by Plotly** – for interactive web app interface
- **Jupyter Notebook** – for exploration and modeling
- **Random Forest & Logistic Regression** – core predictive models

- **Python** with libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly
- **Jupyter Notebook** for exploratory analysis and modeling
- **Scikit-learn** for modeling:
  - Random Forest
  - Logistic Regression

---

## 📈 Key Analysis Areas

- Cancellation trends by **month**, **airline**, **origin**, and **weekday**
- Reasons for cancellation: **Carrier**, **Weather**, **NAS**, **Security**
- Feature engineering for **delay types**, **CRS times**, and **airport codes**
- Dashboard for real-time prediction based on flight inputs

---

## 🧠 Predictive Models

| Model               | Accuracy | ROC AUC | Precision (Cancel) | Recall (Cancel) |
|--------------------|----------|---------|---------------------|-----------------|
| Random Forest       | 97.7%    | 0.70    | 8%                  | 1%              |
| Logistic Regression | 97.9%    | 0.55    | 0%                  | 0%              |

> Random Forest outperformed Logistic Regression significantly on minority class prediction.

---
##  Key Findings & Model Insights

- **Random Forest** achieved ~97% accuracy with an ROC-AUC of ~0.70.
- **Logistic Regression** offered lower performance on cancel prediction (ROC-AUC ~0.55).
- Weather, airline, and origin airport proved to be key predictors of cancellation risk.

Refer to the `Final_Report.pdf` for detailed insights, visuals, and strategic recommendations.

---

## 🖥️ Dashboard

A user-facing **flight cancellation prediction dashboard** was built using Dash, allowing input of:
- Year, Month, Date
- Airline
- Origin and Destination

> The model returns a **live prediction** ("Canceled" / "Not Canceled") based on historical patterns.

---

## 📄 Final Report

A four-page **consulting-style report** includes:
- Project background
- Analytical strategy
- Flight cancellation patterns
- Model evaluation
- Strategic recommendations

📎 See `Reports/Final_Report.pdf` for full insights.

---

## 📌 Recommendations

- Add weather, aircraft, and booking features for richer context
- Balance data or tune thresholds to reduce bias against minority class
- Explore time-series forecasting or ensemble models
- Deploy dashboard with backend API for production

---

## 👥 Team

> This project was completed by Team Q&A (Queen’s MMA 2025)  
> All team members contributed to modeling, analysis, and dashboard development.

---

## 📬 Contact

**Sam Hossain**  
Data & AI × Finance | Queen’s MMA 2025  
🔗 [LinkedIn](https://www.linkedin.com/in/samhossain)  
📫 Email: sam.hossain@queensu.ca

---

_This project was developed as part of the Queen’s University MMA 867 Predictive Modeling course._


About & Contact

Team: MMA 867 (Predictive Modeling), Queen’s University, Class of 2025
Contact: Sam Hossain — sam.hossain@queensu.ca

Project developed as part of the Queen’s MMA 867 course requirements.
---


##  Getting Started

1. **Clone the repository**:
   ```bash
   git clone https://github.com/SamHossain2025/Flight-Data-Analysis.git
   cd Flight-Data-Analysis

2. Install dependencies:

pip install -r requirements.txt

3. Explore or re-run analyses:

Open project_notebook.ipynb for data exploration, model building, and evaluation

Load trained models using:

import joblib
rf_model = joblib.load("model_rf.pkl")











<p align="center">
  <img src="6 Assets/Banner.png" width="100%">
</p>

# ✈️ Flight Cancellation Prediction for US Airlines

*AI-powered prediction of domestic US flight cancellations using airline data from 2021-2023, modelled with machine learning and dashboarded via Dash.*

- Topics covered: **Airline Operations & Delay Analytics**  
- Models used: **Random Forest, Logistic Regression**  
- Skills demonstrated: **Data cleaning, feature engineering, ROC analysis, dashboarding**  
- Expected outcome:  
  - **Predict flight cancellations with ML**  
  - **Enable planning for passengers & airlines**

---

## 👥 Authors

**Sam Hossain, Zaheen Mahaey**

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
  <img src="5 Assets/Model2.png" width="80%">
  <img src="5 Assets/Model3.png" width="80%">
</p>

### 🛬 Cancellation Analysis & Dashboard Workflow
- Cleaned data and transformed categorical/time variables
- Explored cancellations by **month, day, year, airline, origin city**
- Built final prediction model using Random Forest
- Created interactive **Dash app** to predict based on inputs: `Year`, `Month`, `Date`, `Airline`, `Origin`, `Destination`
- Output = Canceled / Not Canceled

---

## 🧪 Key Findings

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

## 🧪 Key Recommendations

* Pre-warn passengers in **high-risk months** with alerts or flexible booking offers
* Reinforce operations staffing on **Mondays/Fridays**
* Prioritize contingency planning at **top 10 volatile airports**

<p align="center">
  <img src="6 Assets/Recommendation1.png" width="80%">
  <img src="6 Assets/Recommendation2.png" width="80%">
  <img src="6 Assets/Recommendation3.png" width="80%">
</p>

---

## 📊 Output Dashboard

<p align="center">
  <img src="6 Assets/Dashboard1.png" width="80%">
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

## 📊 Data Sources

* 📌 [US BTS Flight Delay Data](https://www.transtats.bts.gov/)  
* 📌 Public airline operation datasets (via Kaggle)

---

## 🔓 License

This project is licensed under the [MIT License](LICENSE)












