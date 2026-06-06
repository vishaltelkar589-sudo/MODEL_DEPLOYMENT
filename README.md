# Mall Customer Segmentation API

## Overview

This project is a Machine Learning-powered Customer Segmentation System that classifies mall customers into different segments based on their demographic and spending behavior.

The trained model is deployed using **FastAPI**, allowing users to send customer information through an API and receive the predicted customer segment instantly.

---

## Features

* Customer Segmentation using Machine Learning
* Data preprocessing and feature engineering
* Model training and evaluation
* Model serialization using Pickle
* FastAPI-based REST API deployment
* Interactive API documentation with Swagger UI
* Real-time customer segment prediction

---

## Project Structure

```text
MODEL_DEPLOYEMENT/
│
├── app.py
├── train_model.py
├── model.pkl
├── Mall_Customers.csv
├── requirements.txt
├── Dockerfile
├── outputs.png
├── outputs2.png
├── outputs3.png
├── outputs4.png
├── outputs5.png
├── outputs6.png
└── README.md
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* FastAPI
* Uvicorn
* Pickle
* Matplotlib

---

## Dataset

The project uses the **Mall Customers Dataset** containing:

* Gender
* Age
* Annual Income
* Spending Score

These features are used to identify customer groups and purchasing behavior.

---

## Machine Learning Workflow

### 1. Data Collection

Load customer data from:

```text
Mall_Customers.csv
```

### 2. Data Preprocessing

* Handle categorical values
* Feature selection
* Data transformation

### 3. Model Training

The customer segmentation model is trained using machine learning techniques and saved as:

```text
model.pkl
```

### 4. API Deployment

The trained model is deployed using FastAPI.

Endpoints:

#### Home Endpoint

```http
GET /
```

Response:

```json
{
  "message": "Mall Customer API Running"
}
```

#### Prediction Endpoint

```http
POST /predict
```

Request:

```json
{
  "gender": 1,
  "age": 25,
  "annual_income": 50,
  "spending_score": 80
}
```

Response:

```json
{
  "segment": 1,
  "segment_name": "High Value Customer"
}
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/mall-customer-segmentation-api.git
cd mall-customer-segmentation-api
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

### Train the Model

```bash
python train_model.py
```

### Start FastAPI Server

```bash
uvicorn app:app --reload
```

Server will start at:

```text
http://127.0.0.1:8000
```

---

## API Documentation

FastAPI automatically generates interactive API documentation.

Open:

```text
http://127.0.0.1:8000/docs
```

You can test all API endpoints directly from the browser.

---

## Sample Prediction

Input:

```json
{
  "gender": 1,
  "age": 25,
  "annual_income": 50,
  "spending_score": 80
}
```

Output:

```json
{
  "segment": 1,
  "segment_name": "High Value Customer"
}
```

---

## Future Improvements

* Web dashboard using Streamlit
* Cloud deployment using Render or Railway
* Customer analytics visualization
* Real-time prediction interface
* Model performance monitoring

---

## Author

Vishal Telkar H

Machine Learning Enthusiast | Python Developer | AI/ML Learner

---

## License

This project is licensed under the MIT License.
