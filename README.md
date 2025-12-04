# 🧠 Predicting Customer Satisfaction Using MLOps  
[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  
![Build Passing](https://img.shields.io/badge/Build-Passing-brightgreen.svg)  
![MLflow](https://img.shields.io/badge/MLOps-MLflow-orange.svg)

> 🔮 **A Real-Time Sentiment Analysis & Automated Response System**

---

## 📌 Overview

Customer reviews reveal customer satisfaction trends but are hard to process manually at scale.  
This project implements an **end-to-end Real-Time Sentiment Analyzer with MLOps**, capable of:

✔ Classifying reviews into **Positive, Neutral, Negative**  
✔ Displaying **confidence score** for each prediction  
✔ Sending **automated email replies using Google Gemini AI**  
✔ Storing logs in **MongoDB**  
✔ Tracking & versioning models using **MLflow + CI/CD**

💡 **Goal:** Automate customer feedback handling & enhance user satisfaction with continuous ML improvement.

---

## 🎯 Objectives

### 🎯 Primary Goals
- Classify customer sentiment from text reviews
- Automate professional email responses
- Deploy model using MLOps best practices

### 🧠 Secondary Goals
- Log prediction history in MongoDB
- Use MLflow for versioning & retraining
- Provide intuitive UI for predictions & review management

---

## 🔑 Core Operations

### 1️⃣ Real-Time Sentiment Prediction
- Uses **TF-IDF + Random Forest**
- Returns **Sentiment + Confidence %**
---

### 2️⃣ Automated Reply Generation (Gemini AI)
- Generates a professional response
- Sends mail via SMTP (Gmail)

📌 **Gemini Popup Generation**  
![Gemini Reply](assets/images/gemini_reply_popup.png)

📌 **Gmail Response Output**  
![Mail](assets/images/gmail_reply.png)

---

### 3️⃣ MongoDB Logging
json
{ "email": "john@example.com", "review": "Good service", "sentiment": "positive", "confidence": "93%" }
📌 MongoDB Storage

4️⃣ CI/CD + MLOps Pipeline

Tracks models using MLflow

Logs metrics (Accuracy, Version, Artifacts)

Automated pipeline using GitHub Actions

📌 CI/CD Pipeline Output


📂 Folder Structure
📦 Sentiment-MLOPS
│── app.py                     # FastAPI Backend
│── pipeline.py                # MLflow Training Pipeline
│── requirements.txt           
│── .env                       # Secrets File
│
├── models/                    # Stored Models (TF-IDF, Pickle)
├── src/
│   ├── data_loader.py         # Loads dataset
│   ├── preprocessor.py        # Cleans text + TF-IDF
│   ├── trainer.py             # Trains model
│   ├── evaluator.py           # Model metrics
│   └── notifier.py            # (Optional) Email trigger
│
├── templates/                 # Frontend UI
│   ├── index.html
│   └── reviews.html
└── static/
    └── image/

🛠 Tech Stack
Component	Technology
Frontend	HTML, CSS, Bootstrap
Backend		FastAPI, Python
ML		Scikit-learn (RandomForest, TF-IDF)
MLOps		MLflow, GitHub Actions
Database	MongoDB
Email		Google Gemini API + SMTP
Deployment	Uvicorn Server

---

⚙️ Installation & Setup
1️⃣ Clone Repo
git clone https://github.com/yourusername/sentiment-mlops.git
cd sentiment-mlops

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Create .env File
MONGO_URI="your_mongodb_uri"
SENDER_PASS="your_gmail_app_password"
GEMINI_API_KEY="your_gemini_api_key"

4️⃣ Run Application
uvicorn app:app --reload

🚀 MLOps Pipeline
▶️ Train & Track Model
python pipeline.py

📊 Launch MLflow UI
mlflow ui

🔮 Future Enhancements
Feature	Purpose
🌐 Multilingual Support	Tamil, Hindi, etc.
🎭 Sarcasm Detection	Handle ironic feedback
🔎 Aspect-Based Sentiment	Category-wise insights
📊 Live Dashboard	Streamlit / PowerBI
🎙 Voice Input	Speech-to-text sentiment
👨‍💻 Contributors

👨‍🎓 Final Year B.E. CSE Students – Arunai Engineering College
🧑‍🏫 Guided by: Mrs. S. Lalitha, M.Tech.

---
