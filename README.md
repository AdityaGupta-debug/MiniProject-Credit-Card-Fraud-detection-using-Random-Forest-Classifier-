# 💳 Credit Card Fraud Detection Dataset

## 📌 About the Dataset

This project uses a real-world dataset consisting of **credit card transactions made by European cardholders in September 2013**.  
It contains **284,807 transactions over two days**, of which only **492 are fraudulent** — making this a **highly imbalanced classification problem** (~0.17% fraud rate).

Due to confidentiality, most features have been anonymized using **Principal Component Analysis (PCA)**.  
Only `Time` and `Amount` retain their original values.

The target column is `Class`, where:
- `0` → Legitimate transaction  
- `1` → Fraudulent transaction

---

## 🧩 Features

- `Time`: Time in seconds since the first transaction  
- `V1` to `V28`: Principal components obtained via PCA  
- `Amount`: Transaction amount in Euros  
- `Class`: Target variable (0 = Non-fraud, 1 = Fraud)

---

## ⚙️ Algorithms Used

I experimented with multiple machine learning models to classify transactions as fraudulent or legitimate:

- 📈 Logistic Regression  
- 🔵 Support Vector Classifier (SVC)  
- 🌲 Decision Tree Classifier  
- 📍 K-Nearest Neighbors (KNN)  
- 🌳 Random Forest Classifier ✅

Out of all, **Random Forest** performed the best in terms of:
- **Precision**
- **Recall**
- **Overall accuracy**

Its **ensemble structure** made it robust to noise and well-suited for handling the **class imbalance**.

---

## 📈 Challenges & Techniques Used

### ⚠️ Class Imbalance
- Applied **resampling techniques** (e.g., undersampling)  
- Focused on **Recall**, **Precision**, and **F1-score** over plain Accuracy  
- Used **ROC-AUC** to assess model discrimination

### 📊 Feature Scaling
- Scaled `Time` and `Amount` for models sensitive to feature magnitude (e.g., Logistic Regression, SVC)

### ✅ Model Evaluation
- Accuracy was not the primary metric due to imbalance  
- **False negatives** were minimized as detecting fraud is more critical than false alarms

---

## 📚 Conclusion

The **Random Forest Classifier** delivered the **most reliable and balanced performance**, making it the best model for this fraud detection task.  
To further enhance detection:

- Consider **Balanced Random Forests**  
- Apply **SMOTE** or **ADASYN** for synthetic oversampling  
- Explore **anomaly detection methods** like Isolation Forest or Autoencoders

This project emphasizes the importance of **careful metric selection and model tuning** when working with imbalanced datasets in high-stakes domains like fraud detection.
