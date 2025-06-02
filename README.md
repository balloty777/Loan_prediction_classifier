# 🏦 Loan Approval Prediction App

A full-stack machine learning application that predicts whether a loan application should be approved or not based on applicant data. This project demonstrates end-to-end ML deployment using FastAPI (backend), Streamlit (frontend), and containerization via Docker.

---

## 🧠 Problem Statement

The goal is to automate loan eligibility predictions for a financial institution based on features like applicant income, credit history, marital status, etc. The system helps streamline the loan approval process.

---

## 📌 Features

- 🧠 ML Model: RandomForestClassifier for binary classification (approve/reject)
- 🔗 REST API using FastAPI for model predictions
- 🎛️ Streamlit UI for interactive user input and results
- 🧹 ML pipeline includes preprocessing (e.g., encoding, scaling)
- 🚀 Deployed on free cloud services (Render + Streamlit Cloud)
- 🐳 Docker-ready backend

---

## 🗂️ Project Structure

loan-approval-app/
├── backend/
│ ├── app.py # FastAPI app
│ ├── model.pkl # Trained model
│ ├── pipeline.pkl # Preprocessing pipeline
│ └── requirements.txt
│
├── frontend/
│ ├── streamlit_app.py # Streamlit frontend
│ └── requirements.txt
│
├── README.md


---

## 📊 Features Used

- Gender
- Married
- Dependents
- Education
- Self_Employed
- ApplicantIncome
- CoapplicantIncome
- LoanAmount
- Loan_Amount_Term
- Credit_History
- Property_Area

---

## 🔧 How to Run Locally

### ✅ Backend (FastAPI)
```bash
cd backend
pip install -r requirements.txt
uvicorn app:app --reload
Frontend (Streamlit)
bash
Copy
Edit
cd frontend
pip install -r requirements.txt
streamlit run streamlit_app.py
Update streamlit_app.py to point to http://localhost:8000/predict when running locally.

🌐 Deployment Steps
Backend on Render:
Push backend/ to GitHub

Create a new Web Service on Render

Set the Start Command:

bash
Copy
Edit
uvicorn app:app --host=0.0.0.0 --port=10000
Frontend on Streamlit Cloud:
Push frontend/ to GitHub

Go to Streamlit Cloud

Deploy using streamlit_app.py

📮 API Endpoint
POST /predict: Returns approval status

Swagger docs: /docs

Sample request:

json
Copy
Edit
{
  "Gender": "Male",
  "Married": "Yes",
  "Dependents": "1",
  "Education": "Graduate",
  "Self_Employed": "No",
  "ApplicantIncome": 5000,
  "CoapplicantIncome": 2000,
  "LoanAmount": 150,
  "Loan_Amount_Term": 360,
  "Credit_History": 1.0,
  "Property_Area": "Urban"
}
✍️ Author
Ayush Pandey
⭐️ Star the Repo
If this project helped you, consider giving it a ⭐️ to show support!
