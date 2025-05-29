## **Bank Customer Churn Prediction and Analysis**

---
## Abstract

This project focuses on predicting customer churn in the banking industry using various machine learning algorithms. We explored a range of classification models, including Logistic Regression, Decision Trees (ID3, C4.5, CART), Naive Bayes variants, Random Forest, AdaBoost, and Artificial Neural Networks. Through rigorous evaluation using metrics such as accuracy, recall, F1-score, and AUC, we identified that ensemble methods like AdaBoost and Random Forest performed best. The research emphasizes recall and F1-score due to the business importance of identifying potential churners. Future work includes feature enrichment, hyperparameter tuning, and real-time churn prediction systems.

---
## Rationale

Customer churn directly impacts the revenue and sustainability of banks. Retaining customers is significantly more cost-effective than acquiring new ones. Understanding which customers are at risk of leaving allows banks to take timely and targeted actions to improve satisfaction, enhance loyalty, and reduce losses. This study enables data-driven decisions in customer relationship management.

---
## Research Question

Can we build an effective predictive model that identifies bank customers likely to churn based on historical and behavioral data?

---
## Problem Statement

Customer churn is a persistent and costly challenge in the financial sector. With rising competition and customer expectations, banks must proactively identify churn risks. This project aims to develop a predictive model that classifies customers into churn and non-churn categories using machine learning methods.

---
## Data Sources

We used a publicly available dataset of bank customers, which includes information such as:

- Age, gender, tenure
- Account balance, number of products
- Credit score, estimated salary
- Exited flag (indicating whether the customer churned)

Preprocessing steps included missing value handling, feature encoding, normalization, and splitting the dataset into training and testing sets.

Source: <https://www.kaggle.com/datasets/shubh0799/churn-modelling>

---
## Methodology

1. **Data Preprocessing**:

    - Handling class imbalance by oversampling the minority class.
    - Label encoding for categorical features.
    - Outlier detection and removal using the IQR method.
    - Feature selection and engineering.

2. **Model Development**:

    - Logistic Regression
	- ID3, C4.5, and CART Decision Trees
	- Gaussian and Bernoulli Naive Bayes
	- Random Forest
	- AdaBoost
	- Artificial Neural Network

3. **Evaluation**:
	- Hyperparameter tuning: Grid search.
	- Cross-validation: 5-fold cross-validation.
    - Metrics: Accuracy, Cross-Validation Accuracy, Cohen’s Kappa, Precision, Recall, F1-Score, Confusion Matrix, ROC-AUC and Learning Curves.

---
## Model Performance

| Model                 | Accuracy | CV Accuracy | Kappa | Precision | Recall | F1-Score | AUC  |
| --------------------- | -------- | ----------- | ----- | --------- | ------ | -------- | ---- |
| Logistic Regression   | 0.72     | 0.71        | 0.44  | 0.72      | 0.72   | 0.72     | 0.79 |
| ID3 Decision Tree     | 0.90     | 0.89        | 0.80  | 0.91      | 0.90   | 0.90     | 0.90 |
| C4.5 Decision Tree    | 0.74     | 0.73        | 0.47  | 0.76      | 0.74   | 0.73     | 0.81 |
| CART Decision Tree    | 0.90     | 0.88        | 0.80  | 0.91      | 0.90   | 0.90     | 0.90 |
| Gaussian Naive Bayes  | 0.73     | 0.74        | 0.47  | 0.73      | 0.73   | 0.73     | 0.81 |
| Bernoulli Naive Bayes | 0.72     | 0.72        | 0.44  | 0.72      | 0.72   | 0.72     | 0.78 |
| AdaBoost              | 0.97     | 0.97        | 0.94  | 0.97      | 0.97   | 0.97     | 0.99 |
| Artificial Neural Net | 0.72     | 0.72        | 0.45  | 0.72      | 0.72   | 0.72     | 0.80 |
| Random Forest         | 0.95     | 0.94        | 0.90  | 0.95      | 0.95   | 0.95     | 0.99 |

![](https://github.com/Ronsnon/MyRepository/blob/main/Assignment/Project/images/metric.png?raw=true)

![](https://github.com/Ronsnon/MyRepository/blob/main/Assignment/Project/images/comparison.png?raw=true)

Among all models tested:

- **AdaBoost** achieved the highest performance: 97% accuracy, 97% recall, and 0.99 AUC.
- **Random Forest** followed closely with 95% accuracy and 95% recall.
- Decision tree models like **CART** and **ID3** performed strongly (90% accuracy, 0.9 F1-score), but were slightly less robust than ensemble methods.
- Simpler models like **Logistic Regression** and **Naive Bayes** performed moderately well (around 72–74% accuracy), but lacked predictive depth for complex churn patterns.

---
## Results

- AdaBoost achieved the best overall performance across all metrics, including an AUC of 0.99.
- Random Forest also performed strongly, making it a robust alternative.
- Decision Trees (ID3, CART) showed strong performance but slightly lower than ensemble methods.
- Simpler models like Logistic Regression and Naive Bayes exhibited lower predictive power.

---
## Key Findings

1. **Ensemble models outperform standalone classifiers** in churn prediction tasks.
2. **Recall and F1-score are more meaningful** than accuracy in churn contexts.
3. **AdaBoost achieved the best overall results**, with a recall and F1-score of 0.97.
4. **Random Forest offers a strong balance** between performance and interpretability.
5. **Simple linear models underperform**, likely due to the complex relationships in the data.

---
## Potential Improvements

- Incorporate additional customer behavior data, such as transaction history and complaints.
- Apply deep learning models like LSTM for sequential behavior analysis.
- Address potential class imbalance using resampling techniques like SMOTE.
- Improve explainability using LIME for model interpretation.

---
## Next Steps

- Deploy the AdaBoost model in a real-time bank environment.
- Automate model retraining using updated customer data.
- Monitor performance over time and continuously refine based on feedback.

---
## Conclusion

This project successfully demonstrates the viability of using machine learning models to predict customer churn in the banking sector. Ensemble models like AdaBoost provide outstanding predictive performance, enabling banks to identify at-risk customers with high confidence. While the results are promising, future enhancements and real-world integration are essential for sustainable impact. Care must also be taken to ensure fairness and transparency in automated decision-making.

---
## Bibliography

- \[1]  Introduction to Data Mining, Tan P.-N., et al, 2023, Pearson
- \[2] Mining of  Massive Datasets, Anand  Rajaraman, Jure Leskovec, Jeffrey D. Ullman, 2019, Cambridge University Press

---
## Contact and Further Information

 For questions , please contact: [yangjun0827@hotmail.com](mailto:yangjun0827@hotmail.com)
