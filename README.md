# 🚨 Insurance Fraud Detection Pipeline (n8n)

![n8n](https://img.shields.io/badge/n8n-workflow-orange)
![Python](https://img.shields.io/badge/Python-logic-blue)
![Outlook](https://img.shields.io/badge/Outlook-alerts-green)
![Google Sheets](https://img.shields.io/badge/GoogleSheets-storage-yellow)

---

## 📌 Overview

This project is a hands-on attempt to build a real-time fraud detection pipeline using n8n, focusing on how fraud detection systems work beyond just model building.  

This project focuses on building a complete data pipeline — from ingestion to alerting — rather than just developing a prediction model.

---

## 💡 Why I built this

While working on fraud analytics, I realized that building a model is only one part of the process.
In real scenarios, there’s always a pipeline around it.

This project helped me understand:

* how data flows in real time
* how fraud decisions are applied
* how alerts and reporting are handled

---

## ⚙️ What this pipeline does

* Accepts claim data via webhook
* Applies fraud logic using Python (inside n8n)
* Classifies risk as **HIGH / MEDIUM / LOW**
* Sends Outlook email alerts for **high-risk claims**
* Stores all records in Google Sheets
* Adds timestamps for tracking and analysis

---

## 🔄 Workflow

```plaintext
Webhook → Python Logic → Timestamp → Google Sheets → High Risk Alert (Outlook)
```

---

## 📸 Screenshots

### 🔹 Workflow

![Workflow](https://github.com/kristlingr/insurance-fraud-detection-n8n-/blob/main/Screeshorts/Fraud%20Detection%20Workflow%20.jpg)


### 🔹 Email Alert

![Email Alert](Screenshots/Email%20Alert%20.jpg)

### 🔹 Google Sheets Output

![Google Sheets](https://github.com/kristlingr/insurance-fraud-detection-n8n-/blob/main/Screeshorts/Fraud%20Data%20Tracker%20.jpg)

---

## 📊 Sample Input

```json
{
  "Claim_ID": "C101",
  "Fraud_Probability": 0.85,
  "Fraud_Label": 1
}
```

---

## 📈 Output Fields

* Predicted_Fraud
* Risk_Level
* Timestamp

---

## ⚠️ Challenges I faced

* Understanding data flow between nodes in n8n
* Handling type consistency for IF conditions
* Working around Python node limitations (no external imports allowed)
* Fixing Google Sheets column sync issues after schema updates

---
## ✅ Results

* Successfully simulated real-time fraud detection workflow  
* High-risk claims trigger automated email alerts  
* All transactions logged for analysis and reporting  
* Pipeline designed to be easily extended for real-world use cases
  
---
## 🛠 Tech Stack

* n8n
* Python (Code node)
* Microsoft Outlook
* Google Sheets

---

## 🚀 Future Improvements

* Integrate a trained ML model instead of rule-based logic
* Build a dashboard using Power BI / Tableau
* Automate ingestion from Outlook / SharePoint

---

## 📬 Feedback

Open to feedback and suggestions to improve this pipeline further.

---

## 👤 Author

Twinkle Grover
(Data Analyst | Fraud Analytics | Automation)
