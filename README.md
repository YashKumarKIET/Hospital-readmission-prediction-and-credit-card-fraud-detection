# Case Study 2: Credit Card Fraud Detection

## Objective
Detect fraudulent credit-card transactions in a heavily imbalanced dataset.

## Method
An **XGBoost** binary classifier is trained. **SMOTE** is applied only to the training data to reduce class imbalance without leaking information from the test set.

## Threshold Tuning
Instead of automatically using 0.50, multiple decision thresholds are tested. The demonstration selects the threshold with the highest F1 score. For a real deployment, the threshold should be selected using a validation set and business fraud-loss costs.

## Evaluation
The project reports:
- ROC-AUC
- PR-AUC
- Precision
- Recall
- F1-score
- Confusion matrix
- Feature importance

## Important Note
The feature-importance plot shows model contribution/importance, not causation.

## Running
```bash
pip install -r requirements.txt
python fraud_detection.py
```

For a dataset:
```bash
python fraud_detection.py --data your_transactions.csv
```

The target column should be `Class` or `is_fraud`.
