Credit Card Fraud Detection Dataset
📌 About the Dataset
This project uses a credit card fraud detection dataset consisting of transactions made by European cardholders in September 2013. It contains 284,807 transactions over two days, out of which only 492 are fraudulent, making it a highly imbalanced dataset.

Due to confidentiality, most features have been anonymized using Principal Component Analysis (PCA). Only the Time and Amount columns retain their original meaning. The target column is Class, where:

0 → Legitimate transaction

1 → Fraudulent transaction

The major challenge with this dataset is detecting fraud with very few positive cases (~0.17%).

🧩 Features
Time: Seconds elapsed since the first transaction

V1 to V28: PCA components of original features

Amount: Transaction amount in Euros

Class: Target variable (0 → Non-fraud, 1 → Fraud)

⚙️ Algorithms Used
I experimented with several machine learning algorithms to solve this classification problem:

Logistic Regression

Support Vector Classifier (SVC)

Decision Tree Classifier

K-Nearest Neighbors (KNN)

Random Forest Classifier

After evaluating all models, Random Forest gave the best performance in terms of precision, recall, and overall accuracy. It handled the imbalanced dataset better due to its ensemble nature and robustness.

📈 Challenges & Techniques Used
Class Imbalance: Used resampling and evaluation metrics like ROC-AUC and F1-score to better assess model performance.

Feature Scaling: Scaled Amount and Time features for algorithms like Logistic Regression and SVC.

Model Evaluation: Focused on recall and precision over accuracy, given the importance of minimizing false negatives in fraud detection.

📚 Conclusion
The Random Forest Classifier achieved the most reliable results on this dataset, making it the best choice for this particular fraud detection problem. Further improvements could involve using ensemble methods like Balanced Random Forest or applying anomaly detection techniques.
