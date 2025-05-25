# 🧠 Customer Churn Prediction

This project predicts whether a customer is likely to churn from a bank using a machine learning model built with TensorFlow and deployed via Streamlit. The model is trained on customer profile data and financial metrics.

---

## 📊 Dataset

The dataset used is `Churn_Modelling.csv` and contains the following features:

- `CreditScore`
- `Geography`
- `Gender`
- `Age`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`

The target variable is `Exited`, indicating whether a customer has churned.

---

## 📁 Project Structure

```

.
├── app.py                        # Streamlit app for churn prediction
├── streamlit\_regression.py      # Streamlit app for salary regression (optional)
├── model.h5                     # Trained churn prediction model
├── regression\_model.h5          # Trained regression model
├── scaler.pkl                   # StandardScaler for numerical features
├── lable\_encoder\_gender.pkl     # LabelEncoder for Gender
├── one\_hot\_encoder\_geo.pkl      # OneHotEncoder for Geography
├── requirements.txt             # Python dependencies
├── runtime.txt                  # Runtime environment (for deployment)
├── hyperparameter\_tuning.ipynb  # Notebook for tuning hyperparameters
├── predictions.ipynb            # Model prediction and evaluation
├── salaryregression.ipynb       # Regression model training
├── experiments.ipynb            # Initial exploratory analysis
├── Churn\_Modelling.csv          # Dataset
├── README.md                    # Project documentation

````

---

## 🚀 How to Run

1. **Install dependencies:**

```bash
pip install -r requirements.txt
````

2. **Run the Streamlit app:**

```bash
streamlit run app.py
```

The app will launch in your browser where you can input customer details and see churn predictions.

---

## 🧩 Model Workflow

1. **Preprocessing**

   * Encode categorical features:

     * `Gender` → LabelEncoded
     * `Geography` → OneHotEncoded
   * Scale numerical features with `StandardScaler`.

2. **Model**

   * A deep learning classification model built using Keras.
   * Output is a churn probability (between 0 and 1).

3. **Prediction**

   * If the probability > 0.5 → Customer is likely to churn.
   * Else → Customer is likely to stay.

---

## 📈 Experimentation

* Hyperparameter tuning notebooks are available for training custom models.
* You can find:

  * `hyperparameter_tuning.ipynb` — tuning classification model
  * `salaryregression.ipynb` — regression analysis
  * `predictions.ipynb` — model inference and evaluation

---

## 🛠 Deployment

* `requirements.txt` and `runtime.txt` are included for deployment on platforms like **Heroku** or **Streamlit Cloud**.
* For containerized deployment, a Dockerfile can be added if needed.

---
