# 📞 Telco Customer Churn Prediction using Deep Learning (Keras/TensorFlow)

This project predicts **customer churn** for a telecom company using the **Telco Customer Churn dataset**.  
It uses **data preprocessing, feature encoding, normalization, and an Artificial Neural Network (ANN)** built with **Keras/TensorFlow** to classify whether a customer is likely to leave the service.

---

## 📂 Dataset
The dataset used is **Telco Customer Churn**, which contains information such as:
- Demographic details (Gender, SeniorCitizen, Partner, Dependents)
- Service details (PhoneService, InternetService, Contract type, Payment method)
- Account details (Tenure, MonthlyCharges, TotalCharges)
- Target variable: **Churn** (`Yes` = customer left, `No` = customer stayed)

📌 You can download the dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) or use the provided `Telco_Customer_Churn.csv`.

---

## Project Workfolw
1️⃣ Data Loading & Cleaning:
  - Removed unnecessary columns (customerID)
  - Handled missing values in TotalCharges
  - Converted categorical variables to numeric
  - Replaced "No internet service" and "No phone service" with "No"
    
2️⃣ Exploratory Data Analysis (EDA):
  - Visualized tenure vs churn and monthly charges vs churn
  - Checked unique values for categorical features

3️⃣ Feature Engineering:
  - Converted Yes/No columns to binary values
  - Encoded categorical variables using pd.get_dummies
  - Scaled numerical columns using MinMaxScaler

4️⃣ Model Building:
  - Built an Artificial Neural Network using Keras:
      - Input layer: 26 features
      - Hidden layers: Dense(26, relu), Dense(13, relu)
      - Output layer: Dense(1, sigmoid)

5️⃣ Training & Evaluation:
  - Loss function: binary_crossentropy
  - Optimizer: Adam
  - Metrics: accuracy
  - Evaluated using:
      - Classification report
      - Confusion matrix heatmap

📈 Results:
  - Test Accuracy: ~76% (depends on training run)
  - Classification Report:
                    precision    recall  f1-score   support

           0       0.83      0.84      0.83       999
           1       0.60      0.56      0.58       408

    accuracy                           0.76      1407
   macro avg       0.71      0.70      0.71      1407
weighted avg       0.76      0.76      0.76      1407

🚀 How to Run:
  1. pip install pandas matplotlib numpy scikit-learn tensorflow seaborn
  2. Open the Jupyter Notebook or .py file.
  3. Run all cells to:
       - Preprocess data
       - Train the ANN
       - Evaluate results

