# 🧠 Predicting Customer Satisfaction Using MLOps  
[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  
![Build Passing](https://img.shields.io/badge/Build-Passing-brightgreen.svg)  
![MLflow](https://img.shields.io/badge/MLOps-MLflow-orange.svg)

> 🔮 **A Real-Time Sentiment Analysis & Automated Business Email Response System**

---

## 📌 Project Overview

Traditional customer feedback analysis is slow and inefficient. This project introduces an **automated real-time sentiment analysis system with MLOps**, capable of:

✔ Classifying reviews as **Positive, Neutral, or Negative**  
✔ Providing **Confidence score** of predictions  
✔ Generating **Professional auto-email replies using Google Gemini AI**  
✔ Logging customer reviews in **MongoDB Database**  
✔ Tracking and versioning ML models using **MLflow + CI/CD (GitHub Actions)**  

🎯 **Goal:** Automate customer-feedback handling, reduce manual work, and improve business decision-making with continuous ML improvements.

---

## 🎯 Objectives

### 🔵 Primary Objectives
- Identify customer sentiment from feedback text
- Automate dynamic email responses using AI
- Deploy model with MLOps pipeline

### 🟢 Secondary Objectives
- Log customer prediction data into MongoDB
- Track, version, and retrain models using MLflow
- Provide intuitive UI for real-time predictions

---

## 🔑 System Features & Workflow

### 📍 1) Real-Time Sentiment Classification  
- Built using **TF-IDF + Random Forest Classifier**
- UI takes customer review and returns prediction + confidence

📌 **Prediction UI Output**
![Prediction UI](https://github.com/baskaran2003/FinalYearProject/blob/main/Outputs/PredictionUI.png)

---

### 📍 2) AI-Based Email Auto-Generation (Google Gemini API)  
- Creates personalized mail content based on sentiment  
- Uses **SMTP + Gmail Send Mail API**

📌 **Gemini AI Popup Generation**
![Mail Popup](https://github.com/baskaran2003/FinalYearProject/blob/main/Outputs/MailPopUp.png)

📌 **Auto-Generated Customer Email**
![Mail Response](https://github.com/baskaran2003/FinalYearProject/blob/main/Outputs/MailResponse.png)

---

### 📍 3) MongoDB Review Logging  
All customer feedback with sentiment and confidence is stored in MongoDB:
{ 
  "email": "john@example.com", 
  "review": "Good service", 
  "sentiment": "positive", 
  "confidence": "93%" 
}


