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

