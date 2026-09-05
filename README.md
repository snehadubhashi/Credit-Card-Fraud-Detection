# 💳 Credit Card Fraud Detection

A machine learning project focused on identifying fraudulent credit card transactions using **Exploratory Data Analysis (EDA), data preprocessing, SMOTE, and Random Forest classification**.

The project focuses not only on building a classification model, but also on understanding the challenges of **highly imbalanced financial transaction data** and selecting appropriate evaluation metrics.

---

## 📌 Project Overview

Credit card fraud detection is a challenging classification problem because fraudulent transactions represent only a very small proportion of all transactions.

This project uses a dataset containing **284,807 transactions**, of which only **492 transactions are fraudulent**.

The objective is to analyze transaction patterns and develop a machine learning model capable of identifying potentially fraudulent transactions.

### 🎯 Objective

- Analyze transaction data and identify patterns associated with fraud
- Perform Exploratory Data Analysis
- Handle the severe class imbalance
- Prepare the data for machine learning
- Build a Random Forest classification model
- Evaluate the model using multiple performance metrics
- Identify important features contributing to model predictions

---

## 📊 Dataset

The dataset contains **284,807 credit card transactions**.

| Category | Count |
|---|---:|
| Total Transactions | 284,807 |
| Legitimate Transactions | 284,315 |
| Fraudulent Transactions | 492 |

The dataset is highly imbalanced, making fraud detection more challenging.

Because fraudulent transactions are rare, simply predicting most transactions as legitimate can result in high accuracy while still failing to detect fraud effectively.

---

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand:

- Transaction distribution
- Class imbalance
- Feature relationships
- Statistical characteristics of the data
- Differences between legitimate and fraudulent transactions

Visualizations were used to better understand the structure and patterns within the dataset.

---

## ⚠️ Key Challenges

### 1. Severe Class Imbalance

Only **492 out of 284,807 transactions** are fraudulent.

This creates a significant imbalance between the two classes.

### 2. Accuracy Can Be Misleading

For an imbalanced dataset, a model can achieve very high accuracy while still failing to identify a significant number of fraudulent transactions.

Therefore, model performance cannot be judged using accuracy alone.

### 3. Choosing the Right Evaluation Metrics

Precision, Recall and F1-Score are particularly important for evaluating fraud detection performance.

- **Precision:** How many transactions predicted as fraud were actually fraudulent?
- **Recall:** How many actual fraudulent transactions were successfully identified?
- **F1-Score:** Balance between Precision and Recall.

---

## 🛠️ Technologies & Tools

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **SMOTE**
- **Random Forest**
- **Jupyter Notebook**

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Exploratory Data Analysis
   ↓
Data Preprocessing
   ↓
Class Imbalance Handling
   ↓
Feature Preparation
   ↓
Random Forest Classification
   ↓
Model Evaluation
   ↓
Feature Importance Analysis
⚙️ Methodology
1. Data Understanding

Inspected the dataset structure, features, data types and class distribution.

2. Exploratory Data Analysis

Analyzed transaction patterns and visualized the distribution of legitimate and fraudulent transactions.

3. Data Preprocessing

Prepared the dataset for machine learning and performed feature scaling where required.

4. Handling Class Imbalance

Applied SMOTE (Synthetic Minority Oversampling Technique) to address the imbalance between legitimate and fraudulent transactions.

SMOTE generates synthetic examples of the minority class to provide the model with a more balanced training dataset.

5. Model Building

A Random Forest Classifier was used for fraud classification.

The model was configured with 200 estimators.

6. Model Evaluation

The model was evaluated using:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
ROC-AUC
📈 Model Performance

The Random Forest model achieved the following results on the test set:

Metric	Score
Accuracy	99.95%
Precision	86.32%
Recall	83.67%
F1-Score	84.97%
Why Recall Matters

For fraud detection, Recall is an important metric because it measures how many actual fraudulent transactions the model successfully identifies.

The model achieved a Recall of 83.67%, meaning it identified a substantial proportion of the fraudulent transactions in the test data.

However, the model should not be evaluated based on Recall alone. Precision and F1-Score were also considered to understand the balance between detecting fraud and generating false alerts.

🔎 Feature Importance

Feature importance analysis was performed using the Random Forest model to understand which features contributed most to the model's predictions.

This provides additional interpretability beyond simply predicting whether a transaction is fraudulent.

💡 Key Learnings

Through this project, I strengthened my understanding of:

Exploratory Data Analysis
Data preprocessing
Highly imbalanced datasets
SMOTE and minority-class handling
Classification algorithms
Random Forest
Precision, Recall and F1-Score
Confusion Matrix
ROC-AUC
Feature importance
Interpreting machine learning results
Most Important Takeaway

A key lesson from this project was that a high accuracy score does not necessarily mean a model is effective.

The evaluation metric should be selected according to the actual problem and its business impact.

For fraud detection, identifying fraudulent transactions effectively is more important than simply maximizing overall accuracy.

🎯 Business Relevance

Credit card fraud can result in financial losses for customers and financial institutions.

A fraud detection system can help organizations:

Identify suspicious transactions
Detect potential fraudulent activity
Reduce financial losses
Improve transaction monitoring
Support faster investigation of suspicious activity

Machine learning can help analyze large volumes of transactions and identify patterns that may be difficult to detect manually.

🚀 Future Improvements

Possible improvements to this project include:

Comparing Random Forest with other classification algorithms
Hyperparameter tuning
Additional feature engineering
Experimenting with alternative approaches for imbalanced classification
Improving model interpretability
Deploying the model as an API or application
📁 Project Structure
Credit-Card-Fraud-Detection/
│
├── Credit_Card_Fraud_Detection.ipynb
├── README.md
├── requirements.txt
└── creditcard.csv
▶️ How to Run
1. Clone the repository
git clone https://github.com/snehadubhashi/Credit-Card-Fraud-Detection.git
2. Navigate to the project directory
cd Credit-Card-Fraud-Detection
3. Install dependencies
pip install -r requirements.txt
4. Open the notebook
jupyter notebook Credit_Card_Fraud_Detection.ipynb

Run the notebook cells sequentially to reproduce the analysis and model evaluation.

📓 Notebook

The complete implementation, including:

Data exploration
Visualizations
Preprocessing
SMOTE
Random Forest
Model evaluation
Feature importance

is available in:

Credit_Card_Fraud_Detection.ipynb

🔗 Connect & Explore More

🌐 Data Analytics Portfolio:
https://snehadubhashi.github.io/

💻 GitHub:
https://github.com/snehadubhashi/

⭐ Project Focus

Problem → Data → Analysis → Challenge → Solution → Evaluation → Insight

This project reflects my approach to learning through practical problem-solving rather than focusing only on model accuracy.

If you find this project useful, feel free to ⭐ the repository.
