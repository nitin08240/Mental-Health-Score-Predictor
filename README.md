
# 🧠 Mental Health Score Predictor

A Machine Learning web application that predicts a student's **mental health score** based on social-media usage, academic habits, lifestyle, and stress level.

> **Note:** This project is for educational purposes and is not a clinical or medical diagnosis tool.

## 🚀 Features

* Predicts Mental Health Score on a **0–10 scale**
* Random Forest Regression model
* Data preprocessing using Scikit-learn Pipeline
* Hyperparameter tuning with `RandomizedSearchCV`
* FastAPI REST API
* Pydantic input validation
* Interactive HTML/CSS/JavaScript frontend
* Real-time prediction display with score gauge

## 🏗️ Architecture

```text
Student Input
     ↓
Pydantic Validation
     ↓
ML Preprocessing Pipeline
     ↓
Random Forest Regressor
     ↓
Mental Health Score
     ↓
Web Interface
```

## 🤖 Machine Learning

### Dataset

**Student Social Media And Mental Health Impact Dataset**

* 5,000 student records
* Demographic information
* Social-media usage
* Study hours
* Physical activity
* Sleep duration
* Stress level
* Mental health score

### Input Features

* Age
* Gender
* Country
* Academic Level
* Most Used Platform
* Purpose of Use
* Average Daily Usage Hours
* Daily Unlocks
* Study Hours
* Physical Activity Hours
* Sleep Hours
* Stress Level

### Model

The project compares Linear Regression and Random Forest models.

The final pipeline uses a **Random Forest Regressor** with hyperparameter tuning.

```text
n_estimators      = 200
max_depth         = 15
min_samples_split = 5
min_samples_leaf  = 2
random_state      = 42
```

### Model Performance

| Model               |     R² |    MAE |   RMSE |
| ------------------- | -----: | -----: | -----: |
| Linear Regression   | 0.7398 | 0.5362 | 0.6760 |
| Random Forest       | 0.8776 | 0.3472 | 0.4637 |
| Tuned Random Forest | 0.8650 | 0.3689 | 0.4869 |

## 🔌 FastAPI API

Backend: `main.py`

### Endpoints

**GET `/`**

Returns API welcome message.

**POST `/predict`**

Returns the predicted mental health score.

Example response:

```json
{
  "predicted_mental_health_score": 6.78
}
```

FastAPI uses **Pydantic** for request validation.

## 🖥️ Frontend

Built using:

* HTML5
* CSS3
* JavaScript

The frontend collects student information, sends it to the FastAPI backend, and displays the predicted score through an interactive gauge.

## 📁 Project Structure

```text
Mental-Health-Score-Predictor/
│
├── ML_Project.ipynb
├── ML Project.html
├── Student Social Media And Mental Health Impact.csv
├── Mental_Health_Model.pkl
│
├── main.py
├── requirements.txt
│
├── index.html
├── style.css
├── script.js
│
└── README.md
```

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/nitin08240/Mental-Health-Score-Predictor.git
cd Mental-Health-Score-Predictor
```

### Create Virtual Environment

```bash
python -m venv venv
```

Windows:

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run API

```bash
uvicorn main:app --reload
```

API:

```text
http://127.0.0.1:8000
```

Swagger documentation:

```text
http://127.0.0.1:8000/docs
```

## 🛠️ Tech Stack

```text
Python
Pandas
NumPy
Scikit-learn
Random Forest
Joblib
FastAPI
Pydantic
Uvicorn
HTML5
CSS3
JavaScript
```

## 🔮 Future Improvements

* SHAP-based model explainability
* Automated testing
* Model monitoring
* CI/CD with GitHub Actions
* Prediction confidence/uncertainty
* Improved deployment configuration

## 👨‍💻 Author

**Nitin Kumar**

GitHub: https://github.com/nitin08240

Repository: https://github.com/nitin08240/Mental-Health-Score-Predictor
