# credit-card-fraud-sql
This project explores a credit card transactions dataset using SQL to identify patterns and risk factors associated with fraudulent activity. The goal is to simulate a real-world fraud analysis scenario and extract actionable insights that could support fraud detection strategies in banking.

Objectives
Understand the structure and composition of transaction data
Measure the overall fraud rate
Identify high-risk transaction characteristics
Detect behavioral patterns associated with fraud
Generate insights that could inform fraud prevention strategies

Tools Used
SQL
DB Browser for SQLite
CSV dataset (Kaggle)

Dataset Description

The dataset contains transactional and behavioral features, including:

amount – Transaction value
transaction_hour – Time of transaction
merchant_category – Type of merchant
foreign_transaction – Whether the transaction occurred internationally
location_mismatch – Whether the transaction location differs from expected
device_trust_score – Trust score of the device used
velocity_last_24h – Number of transactions in the last 24 hours
cardholder_age – Age of the customer
is_fraud – Target variable (1 = fraud, 0 = legitimate)

Analysis Performed
Dataset Overview

A summary of total transactions, number of fraudulent cases, and overall fraud rate was calculated.

<img width="1361" height="693" alt="image" src="https://github.com/user-attachments/assets/20e58e91-598d-4610-9d5f-abb39277f82e" />

It was noted that only 151 cases of fraud could be identified

Fraud Rate Analysis

The percentage of fraudulent transactions was calculated using the average of the fraud indicator.

<img width="1365" height="695" alt="image" src="https://github.com/user-attachments/assets/5c534716-237f-4d5a-a5ce-e17840376ca2" />

1.51 percent of transactions were noted as fraudulent 

Fraud by Merchant Category

Fraud rates were analysed across different merchant categories to identify high-risk sectors.

<img width="1364" height="692" alt="image" src="https://github.com/user-attachments/assets/527bdbc3-6d62-475c-bf69-49b3b06ae00a" />

The food merchant category was noted to have the highest rate of fruad. This could be due to factors such as declining economic activity forcing people to use less honest means to feed themselves.

Foreign Transaction Risk

Fraud rates were compared between domestic and international transactions.

<img width="1365" height="694" alt="image" src="https://github.com/user-attachments/assets/3d694ae6-5624-4b9e-a84e-9a942af03573" />

Foreign transactions have a higher rate of fruad, likely due to poor relationships between international law enforecment which may impact how individuals percieve the likelyhood of facing consequences.

Device Trust Score Analysis

Transactions were grouped into trust levels (Low, Medium, High) to assess fraud risk based on device credibility.

<img width="1365" height="690" alt="image" src="https://github.com/user-attachments/assets/c9f6671b-99a7-4835-a1b2-570c4a011cf6" />

Transactions originating from low-trust devices exhibit a significantly higher fraud rate (3.84%) compared to medium (0.37%) and high-trust devices (0.27%). This indicates that device trust score is a strong predictor of fraudulent activity,

Transaction Velocity Analysis

The relationship between transaction frequency (last 24 hours) and fraud likelihood was explored.

<img width="1365" height="692" alt="image" src="https://github.com/user-attachments/assets/3e0e3a4b-d909-427e-93d8-de080723f504" />

Fraud risk increases significantly with higher transaction velocity. This suggests that rapid transaction bursts are a strong indicator of fraudulent behavior and should trigger additional monitoring or intervention.

High-Value Fraud Cases

The largest fraudulent transactions were examined to understand extreme risk scenarios.

<img width="1365" height="691" alt="image" src="https://github.com/user-attachments/assets/c028ee3f-7521-491e-9d7d-9b5c2a966a99" />

Analysis of the highest-value fraudulent transactions reveals that fraud is not driven by a single factor but rather a combination of risk indicators. Many high-value fraud cases involve foreign transactions and location mismatches, suggesting geographic anomalies play a role.
