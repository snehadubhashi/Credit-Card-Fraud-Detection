# 💳 Credit Card Fraud Detection using Data Analysis & Random Forest

## 📌 Project Overview

Credit card fraud is one of the biggest challenges faced by financial institutions. Detecting fraudulent transactions quickly helps reduce financial losses and improve customer security.

In this project, I performed **Exploratory Data Analysis (EDA)** to understand the dataset and built a **Random Forest Classifier** to predict whether a transaction is fraudulent or legitimate.

---

# 🎯 Problem Statement

The objective of this project is to analyze credit card transaction data, identify fraud patterns, and build a machine learning model capable of detecting fraudulent transactions.

Since fraudulent transactions are very rare compared to legitimate transactions, the dataset is highly imbalanced, making fraud detection a challenging classification problem.

---

# 📂 Dataset

* **Dataset:** Credit Card Fraud Detection
* **Source:** Kaggle
* **Total Records:** 284,807 Transactions
* **Fraudulent Transactions:** 492
* **Legitimate Transactions:** 284,315

The dataset contains anonymized numerical features generated using Principal Component Analysis (PCA) along with:

* **Time**
* **Amount**
* **Class**

  * 0 → Legitimate Transaction
  * 1 → Fraudulent Transaction

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# 📊 Exploratory Data Analysis (EDA)

The following analyses were performed:

* Dataset overview
* Data type inspection
* Missing value analysis
* Statistical summary
* Class distribution analysis
* Count Plot
* Bar Plot
* Histogram
* Correlation Heatmap

---

# 📈 Data Visualizations

The project includes the following visualizations:

* Count Plot (Fraud vs Non-Fraud)
* Bar Plot
* Histogram
* Correlation Heatmap
* Confusion Matrix
* ROC Curve

---

# 🔍 Key Insights

* The dataset is highly imbalanced, with fraudulent transactions representing only a very small fraction of all transactions.
* Most transactions are legitimate, making fraud detection a challenging classification problem.
* Correlation analysis helps understand relationships between the anonymized features and the target variable.
* Since the dataset is imbalanced, evaluation metrics such as Precision, Recall, F1-score, and ROC-AUC are more meaningful than Accuracy alone.

---

# 🤖 Machine Learning Model

The following machine learning model was used:

* **Random Forest Classifier**

### Workflow

1. Data Loading
2. Data Exploration
3. Data Visualization
4. Feature Selection
5. Train-Test Split
6. Random Forest Model Training
7. Prediction
8. Model Evaluation

---

# 📊 Model Evaluation

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC-AUC Score
* ROC Curve

These metrics provide a better understanding of model performance on an imbalanced dataset.

---

# 📁 Project Structure

```text
Credit-Card-Fraud-Detection/
│   
│
├── notebook/
│   └── Credit_Card_Fraud_Detection.ipynb    
│   └── creditcard.csv
├── images/
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Credit-Card-Fraud-Detection.git
```

### 2. Navigate to the Project Folder

```bash
cd Credit-Card-Fraud-Detection
```

### 3. Install Required Libraries

```bash
pip install -r requirements.txt
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

### 5. Run the Notebook

Execute all cells in **Credit_Card_Fraud_Detection.ipynb**.

---

# 📌 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Data Visualization
* Feature Analysis
* Machine Learning
* Random Forest Classification
* Model Evaluation
* Business Insight Generation

---

# 📈 Future Improvements

* Handle class imbalance using SMOTE
* Compare multiple machine learning algorithms
* Perform hyperparameter tuning
* Analyze feature importance
* Deploy the model using Flask or FastAPI
* Build a real-time fraud detection system

---

# 👩‍💻 Author

**Sneha Dubhashi**

If you found this project helpful, consider giving it a ⭐ on GitHub.
