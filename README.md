# Credit Card Fraud Detection Using Anomaly Detection and Classification Algorithms

## Aim
Detect fraudulent transactions in a credit card dataset by applying anomaly detection and classification algorithms.

## Description
This project focuses on identifying potentially fraudulent activities in credit card transactions. It provides an introduction to handling imbalanced datasets and implementing fraud detection techniques using various algorithms.

## Steps

### Step 1: Importing Necessary Libraries
Libraries such as NumPy, Pandas, Matplotlib, and Seaborn are used for data manipulation and visualization. Scikit-learn provides tools for model training and evaluation. The following anomaly detection algorithms are employed:
- Isolation Forest
- Local Outlier Factor
- One-Class SVM

### Step 2: Load the Dataset
The dataset contains 31 columns including anonymized features (V1 to V28), transaction time (Time), amount (Amount), and the target variable (Class). This comprehensive dataset offers insights into each transaction's characteristics.

### Step 3: Check for Missing Values
The dataset does not contain any missing values, which simplifies preprocessing and analysis.

### Step 4: Transaction Class Distribution
A bar plot illustrates a significant imbalance between non-fraudulent (Class 0) and fraudulent (Class 1) transactions. This imbalance highlights the need for techniques to handle class imbalance.

**Visualization Explanation:** 
The plot shows the majority of transactions are non-fraudulent, underscoring the importance of handling class imbalance effectively.

### Step 5: Analyze Transaction Amounts
Fraudulent transactions tend to involve higher amounts compared to normal transactions.

**Visualization Explanation:**
The histogram shows that fraudulent transactions often involve higher amounts and have a wider range compared to normal transactions.

### Step 6: Define Features and Target
A 10% sample of the dataset is used for faster processing. Features (X) and the target variable (Y) are defined for model training. X includes all features except for the target variable Class, while Y contains the target variable.

### Step 7: Apply Anomaly Detection Models
Three models are evaluated:
- **Isolation Forest**
- **Local Outlier Factor**
- **Support Vector Machine (SVM)**

**Model Performance Summary:**

- **Isolation Forest:**
  - Accuracy: 99.78%
  - Misclassified Points: 63
  - Insight: High accuracy overall but low precision for detecting fraudulent transactions, indicating that while most transactions are classified correctly, fraudulent transactions may not be detected effectively.

- **Local Outlier Factor:**
  - Accuracy: 99.68%
  - Misclassified Points: 91
  - Insight: High accuracy with low recall and precision for fraud detection, suggesting challenges in identifying fraud effectively.

- **Support Vector Machine (SVM):**
  - Insight: SVM's performance is typically evaluated based on its decision boundary and ability to distinguish between classes. Results indicate varied performance depending on model parameters.

### Step 8: Visualization

**Transaction Amount Distribution by Class**
- **Fraudulent Transactions (Red):** Higher concentration of larger transaction amounts, with the distribution skewed towards higher values.
- **Normal Transactions (Blue):** More even distribution with a higher number of lower-value transactions.

**Insights:**
- Fraudulent transactions generally involve higher amounts.
- There is some overlap, but fraudulent transactions tend to have higher peaks.

**Distribution of Transaction Amounts by Class**
- **Fraudulent Transactions (Red):** Generally involve higher amounts, with a concentration up to $20,000.
- **Normal Transactions (Blue):** More even distribution with a broader range, fewer high-value transactions.

**Insights:**
- Fraudulent transactions are typically of higher amounts.
- Normal transactions are more frequent overall, with a higher concentration in lower-value ranges.

**Time vs Amount for Fraud and Normal Transactions**
- **Fraudulent Transactions (Red):** Distributed across various times, but involve higher amounts.
- **Normal Transactions (Blue):** More evenly spread with lower amounts, showing no distinct temporal pattern.

**Insights:**
- Fraudulent transactions are associated with higher amounts, irrespective of time.
- No strong temporal pattern in fraudulent transactions, unlike normal ones.

### Sampled Data Overview
- **Sampled Data Shape:** (28,481, 31)
- **Outlier Fraction:** 0.0016
- **Fraud Cases in Sample:** 46
- **Valid Cases in Sample:** 28,435

**Correlation Heatmap:**
Visualizes relationships between features, highlighting strong correlations and potential multicollinearity.

**Heatmap Insights:**
- Identifies strong correlations between features.
- Helps in feature selection and engineering for better model performance.

## Key Insights
- All models demonstrated high accuracy, but their effectiveness in detecting fraudulent transactions varied.
- Isolation Forest and Local Outlier Factor both had high accuracy but struggled with low precision and recall for fraud detection.
- SVM results varied depending on the model parameters and feature scaling.

## Conclusion
The project provides foundational understanding of fraud detection using anomaly detection algorithms. The findings emphasize the importance of selecting appropriate models and fine-tuning their parameters to effectively handle imbalanced datasets and detect fraudulent activities. The visualizations and analysis offer insights into transaction patterns and highlight key differences between fraudulent and normal transactions.
