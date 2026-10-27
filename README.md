**Credit Card Fraud Detection using EDA and Random Forest**

Detecting rare fraudulent transactions in a highly imbalanced dataset using Python, SMOTE, and a Random Forest classifier.

**Results at a Glance**

**Metric (held-out test set)**	**Value**

Transactions analyzed	        284,807

Fraud rate	                    0.17% (492 fraud cases)

Precision	                    86.3%

Recall	                        83.7%

F1 Score	                    0.85

Accuracy	                    99.95%

                     

On the test set (56,962 transactions, 98 of them fraud), the model caught 82 of 98 fraud cases, missed 16, and wrongly flagged 13 legitimate transactions.

Accuracy alone is misleading here, because a model that predicts "not fraud" every time would still be 99.8% accurate. That is why precision, recall, and F1 are the main metrics in this project.

**Business Problem**


Banks lose money when fraudulent transactions go undetected, but blocking too many genuine transactions frustrates customers. The goal is to flag as many fraud cases as possible (high recall) while keeping false alarms low (high precision).

**Dataset**

Source: Credit Card Fraud Detection dataset on Kaggle

Records: 284,807 transactions (284,315 legitimate, 492 fraudulent)

Features: Time, Amount, and 28 anonymized numerical features (V1 to V28) produced by PCA

Target: Class (0 = legitimate, 1 = fraud)

Data quality: no missing values


The dataset file (creditcard.csv) is too large for GitHub. Download it from the Kaggle link above and place it in the project folder.

**Tools Used**


Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, imbalanced-learn (SMOTE), Jupyter Notebook

**Approach**

**Explored the data:** checked shape, data types, missing values, and class distribution.

**Visualized patterns:** class balance, transaction amount and time distributions, and a correlation heatmap.

**Split the data:** 80% train and 20% test, stratified so both sets keep the same fraud ratio.

**Scaled Time and Amount with StandardScaler** (fit on the training set only).

**Handled class imbalance with SMOTE on the training set only,** balancing 394 fraud cases against 227,451 legitimate ones. The test set was left untouched to avoid data leakage.

**Trained a Random Forest** (200 trees) and evaluated it on the untouched test set.


**Key Findings**

**Fraud is extremely rare:** only 0.17% of transactions are fraudulent, so the data needed rebalancing.

**Strongest correlations with fraud** are with the anonymized features V17 (-0.33), V14 (-0.30), V12 (-0.26), and V10 (-0.22).

**Transaction amount has almost no linear relationship with fraud **(correlation 0.006), so amount alone cannot identify fraud.

**Most important model features:** V14, V10, V4, V12, and V17. Because these features are anonymized, they cannot be explained in business terms.


**Top 10 Features**

**Model Performance**

Confusion Matrix

ROC Curve

**Did SMOTE help?**

Model	Precision	Recall	F1

Random Forest with SMOTE	86.3%	83.7%	0.85

**Limitations**

Features are anonymized, so the model's decisions cannot be tied to real transaction details such as merchant or location.

98 fraud cases in the test set is small, so results may vary with a different split.

The model was not tuned and was not compared against other algorithms.


**Next Steps**

Compare Random Forest with Logistic Regression and XGBoost

Tune hyperparameters and adjust the decision threshold to balance precision and recall

Add a cost-based view: the money saved by catching fraud versus the cost of false alarms

**Project Structure**
Credit-Card-Fraud-Detection/

├── Credit_Card_Fraud_Detection.ipynb

├── README.md

├── requirements.txt

└── images/

    ├── feature_importance.png
    
    ├── confusion_matrix.png
    
    └── roc_curve.png
    

creditcard.csv is not included. Download it from Kaggle as described above.

**How to Run**

bash
git clone https://github.com/snehadubhashi/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection
pip install -r requirements.txt
jupyter notebook

Place creditcard.csv in the folder, then run all cells in Credit_Card_Fraud_Detection.ipynb.

**Author**

Sneha Dubhashi 
