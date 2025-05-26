#  Cloud-Based Credit Card Fraud Detection System

A real-time fraud detection system using a trained machine learning model served through a Flask API, with results stored in Firebase Firestore.

---

##  Features

-  Real-time credit card fraud prediction using machine learning
-  Random Forest classifier trained on highly imbalanced data
-  SMOTE oversampling to handle class imbalance
-  Flask API served with ngrok for easy testing
-  Firebase Firestore integration for storing transaction logs
-  Easily testable with Postman or Python

## Repository Structure

- model.pkl — Trained Random Forest model
- threshold.txt — Optimal classification threshold selected from F1-score
- firebase-key.json — Placeholder Firebase service account key (do not upload the real one)
- colab_training.ipynb — Google Colab notebook for training, threshold tuning, and testing
- README.md — Project description and setup instructions
  
## Getting Started

Follow these steps to run the project in Google Colab.

### 1. Upload the following files to Colab: 
- model.pkl
- threshold.txt
- firebase-key.json (your private key, do not upload to GitHub)

### 2. Install the required packages:
!pip install flask pyngrok firebase-admin

### 3. Run the Flask API:
- Load your model and threshold
- Connect to Firestore
- Start the Flask app using `pyngrok`
- A public URL will appear, such as: `https://xxxx.ngrok-free.app`

### 4. Send a test request:
- You can use either:
  - **Postman**: Send a `POST` request to `/predict` with JSON-formatted transaction data
  - **Python**: Use the `requests` library to call the API

