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
📌 MongoDB Stored Data

📍 4) CI/CD MLOps Pipeline
Tracks metrics, artifacts, and model versions via MLflow

Automates training and deployment using GitHub Actions

## 📌 CI/CD Pipeline Output

🏗️ System Architecture
┌─────────────┐     ┌──────────────┐     ┌──────────────┐
│   Web UI    │ --> │   FastAPI    │ --> │ ML Model (RF)│
└─────────────┘     └─────┬────────┘     └──────┬───────┘
                            │                    │
                            ▼                    ▼
                      MongoDB DB          Gemini AI (Email)
                            ▲                    │
                            └───── CI/CD + MLflow┘
## 📂 Folder Structure

📦 Sentiment-MLOPS
├── app.py                # FastAPI Backend
├── pipeline.py           # MLflow Training Pipeline
├── requirements.txt      
├── .env                  # Secret Credentials
│
├── models/               # Trained Model + TF-IDF Vectorizer
├── src/
│   ├── data_loader.py    # Load Dataset
│   ├── preprocessor.py   # Cleaning + Tokenization
│   ├── trainer.py        # Model Training
│   ├── evaluator.py      # Evaluation Metrics
│   └── notifier.py       # Email Trigger (Optional)
│
├── templates/            # Frontend UI
│   ├── index.html
│   └── reviews.html
└── static/
    └── image/            # Icons/Styling
## 🛠️ Tech Stack
Component	    Technology
Frontend	    HTML, CSS, Bootstrap
Backend	      FastAPI
ML Model	    Scikit-Learn (Random Forest + TF-IDF)
Database	    MongoDB
MLOps	        MLflow, GitHub Actions
Email	        Google Gemini API + SMTP
Deployment	  Uvicorn Server

## ⚙️ Installation & Setup
🔧 Step 1: Clone Repository

git clone https://github.com/yourusername/sentiment-mlops.git
cd sentiment-mlops
📦 Step 2: Install Dependencies

pip install -r requirements.txt
🔐 Step 3: Create .env File

MONGO_URI="your_mongodb_uri"
SENDER_PASS="your_gmail_app_password"
GEMINI_API_KEY="your_gemini_api_key"
🚀 Step 4: Run the Application

uvicorn app:app --reload
🎛️ MLOps Pipeline Usage
▶️ Train & Track Model

🔮 Future Enhancements
Feature	Description
🌐 Multi-Language Support	Tamil, Hindi, etc.
🎭 Sarcasm Detection	Improve accuracy
🔎 Aspect-Based Sentiment	Category-wise review
📊 Live Dashboard	Streamlit Analytics
🎙 Voice Feedback	Speech-to-text sentiment

👨‍💻 Contributors
👨‍🎓 Final Year B.E. CSE Students — Arunai Engineering College
🧑‍🏫 Project Guide: Mrs. S. Lalitha, M.Tech.

