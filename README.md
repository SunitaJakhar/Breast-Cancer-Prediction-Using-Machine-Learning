# Breast-Cancer-Prediction-Using-Machine-Learning

This analysis evaluated two powerful machine learning algorithms, Support Vector Machine (SVM) and XGBoost, for their effectiveness in classifying breast cancer as benign (0) or malignant (1) based on the provided dataset.


# Key Findings:

1. Overall Performance (Accuracy):
    * SVM: Achieved an accuracy of approximately 0.956 on the test set.
    * XGBoost: Also achieved a similar accuracy of approximately 0.956 on the test set after parameter tuning.

2. ROC Curve and AUC:
    * Both models demonstrated strong discriminative power, with high AUC values indicating their ability to distinguish between the two classes. The ROC curves visually confirmed their robust performance across various thresholds.

3. Importance of Confusion Matrix (False Negative Rate): The confusion matrix is particularly critical in medical diagnosis, as False Negatives (FN) (predicting benign when it's actually malignant) are generally more detrimental than False Positives (FP) (predicting malignant when it's benign). A high FN rate means a patient with cancer might be misdiagnosed as healthy, leading to delayed treatment.

    * SVM:
        * Confusion Matrix: [[70, 1], [4, 39]]
        * False Negatives (FN): 4 (out of 43 actual malignant cases)
        * False Negative Rate (FNR): 4 / (4 + 39) = 0.093 (approximately 9.3%)
    
    * XGBoost:
        * Confusion Matrix: [[69, 2], [3, 40]]
        * False Negatives (FN): 3 (out of 43 actual malignant cases)
        * False Negative Rate (FNR): 3 / (3 + 40) = 0.070 (approximately 7.0%)


# Implications for the Business/Social Problem:

* Minimizing False Negatives is Paramount: In breast cancer diagnosis, minimizing false negatives is a top priority. While both models showed high overall accuracy, XGBoost demonstrated a slightly lower False Negative Rate (7.0% vs. 9.3%) compared to SVM.
  
* XGBoost's Edge: The slightly better FNR of XGBoost suggests it might be marginally preferred in this specific medical context, as it would lead to fewer missed diagnoses of malignant cases, which is crucial for early intervention and patient outcomes.
  
* Balanced Performance: Both models provide a strong foundation for a diagnostic tool. The choice between them might also consider computational cost, interpretability, and ease of deployment.
  
In summary, both SVM and XGBoost are highly effective for this classification task. However, when considering the critical importance of minimizing false negatives in breast cancer diagnosis, XGBoost shows a slight advantage due to its lower False Negative Rate, making it a potentially more reliable model for this application.
