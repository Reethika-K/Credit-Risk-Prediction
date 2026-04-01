# Credit Risk Prediction
## About
This project builds an end-to-end machine learning pipeline to predict whether a client will face payment difficulties (loan default risk) using the Home Credit dataset.
The solution leverages advanced feature engineering across multiple relational tables and a LightGBM model optimized for imbalanced tabular data.
## Dataset
Source: Kaggle - https://www.kaggle.com/competitions/home-credit-default-risk/data
## Project Structure
Home-Credit/
<br>
├── dataset/
<br>
│   └── (datasets from link above)
<br>
│
<br>
├── models/
<br>
│   ├── bureau_preprocessing_final.ipynb
<br>
│   ├── pos_inst_cc_preprocessing_final.ipynb
<br>
│   ├── prev_appl_preprocessing_final.ipynb
<br>
│   └── Model_training.ipynb
<br>
│
<br>
├── processed_data/
<br>
│   ├── bureau_final.csv 
<br>
│   ├── pos_inst_cc_final.csv
<br>
│   └── prev_final.csv
<br>
│
<br>
└── README.md
- **bureau_preprocessing_final.ipynb** - Preprocessing of bureau_balance.csv & bureau.csv dataset
- **pos_inst_cc_preprocessing_final.ipynb** - Preprocessing of POS_CASH_balance.csv, installments_payments.csv & credit_card_balance.csv
- **prev_appl_preprocessing_final.ipynb** - Preprocessing of previous_application.csv
- **Model_training.ipynb** - Preprocessing of application_test/test.csv & Model training
- **bureau_final.csv** - Output of bureau_preprocessing_final.ipynb 
- **pos_inst_cc_final.csv** - Output of pos_inst_cc_preprocessing_final.ipynb
- **prev_final.csv** - Output of prev_appl_preprocessing_final.ipynb
- **Note:** Due to file size limitations, this repository includes only the model-related files. The original project contained additional raw data and intermediate processing files which are not uploaded.
## Data Preprocessing 
- Replaced anomalous values (e.g., DAYS_EMPLOYED = 365243)
- Handled missing values using sentinel values (-999)
- One-hot encoded categorical features
- Ensured consistency between train and test datasets
- Feature Engineering
- Feature Aggregation (Mean, Max, Sum, Count)
## Model Training
- Model: LightGBM Classifier
- Evaluation Metric: ROC-AUC
- Early stopping used to prevent overfitting
## Result
Validation ROC-AUC - **0.78**
## Key Learnings 
- Importance of feature engineering in tabular ML
- Handling multi-table relational datasets





