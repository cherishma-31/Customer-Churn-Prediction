# Customer Churn Prediction

A machine learning project that predicts whether a telecom customer is likely to churn. The project includes data analysis, preprocessing, Logistic Regression modeling, model evaluation, and an interactive Streamlit web application.

## Project Overview

Customer churn refers to customers discontinuing a service. Predicting churn can help businesses identify customers who may leave and take preventive action.

In this project, a Telco Customer Churn dataset is analyzed and a Logistic Regression model is used to predict customer churn.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Streamlit
* Jupyter Notebook
* Git & GitHub

## Dataset

The dataset contains customer information such as:

* Gender
* Senior Citizen
* Partner
* Dependents
* Tenure
* Phone Service
* Internet Service
* Online Security
* Online Backup
* Device Protection
* Tech Support
* Streaming Services
* Contract
* Paperless Billing
* Payment Method
* Monthly Charges
* Total Charges
* Churn

The original dataset contains **7,043 customers**.

## Exploratory Data Analysis

Some important observations from the analysis:

* Month-to-month contract customers have considerably higher churn than one-year and two-year contract customers.
* Fiber optic customers show higher churn compared with DSL and customers without internet service.
* Electronic check users have relatively high churn.
* Customers with shorter tenure are more likely to churn.
* Customers who churn have higher average monthly charges.
* Customers with services such as Online Security and Tech Support generally show lower churn rates.

## Machine Learning

### Preprocessing

The data was prepared using:

* Categorical feature encoding with OneHotEncoder
* Numerical feature handling
* Feature preprocessing using Scikit-learn pipelines
* Train-test split

The `customerID` column was removed because it does not provide useful predictive information.

### Models Evaluated

The following models were tested:

* Logistic Regression
* Random Forest
* Balanced Logistic Regression

### Final Model

**Logistic Regression** was selected as the final model.

Normal Logistic Regression achieved:

* Accuracy: **80.55%**
* Churn Recall: **56%**
* Churn F1-score: **60%**

A balanced Logistic Regression model was also tested to improve detection of churn customers:

* Accuracy: **73.81%**
* Churn Recall: **78%**
* Churn F1-score: **61%**

The final application uses the selected Logistic Regression model and the saved preprocessing pipeline.

## Streamlit Web Application

The project includes an interactive Streamlit application where users can enter customer details and receive:

* Churn prediction
* Churn probability

Example predictions were tested successfully:

* Higher-risk customer → **90.82% churn probability**
* Lower-risk customer → **1.88% churn probability**

## Project Structure

```text
Customer-Churn-Prediction/
│
├── data/
│   └── dataset files
│
├── notebooks/
│   └── Customer_Churn_Prediction.ipynb
│
├── app.py
├── churn_model.pkl
├── preprocessor.pkl
├── requirements.txt
├── .gitignore
└── README.md
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/cherishma-31/Customer-Churn-Prediction.git
cd Customer-Churn-Prediction
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit application

```bash
streamlit run app.py
```

The application will open in your browser.

## Future Improvements

* Try additional classification algorithms
* Handle class imbalance using advanced techniques
* Add feature importance and model explainability
* Improve the Streamlit interface
* Deploy the application online

## Author

**Cherishma Penneru**

Machine Learning Project — Customer Churn Prediction
