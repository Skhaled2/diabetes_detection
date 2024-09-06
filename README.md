# diabetes_detection

This project focuses on the classification of diabetes using various machine learning algorithms. Our dataset had a significant imbalance in the target class, which was addressed using SMOTE (Synthetic Minority Over-sampling Technique). To preprocess the data, we applied label encoding to convert categorical features to numerical and used StandardScaler for feature scaling. Additionally, Principal Component Analysis (PCA) was implemented to reduce dimensionality and compare performance with both built-in and custom PCA functions.

We evaluated the following machine learning models:

Random Forest
Decision Tree
Logistic Regression
Support Vector Machine (SVM)
K-Nearest Neighbors (KNN)
Additionally, Naive Bayes was explored, but it underperformed due to its limitations with complex data.

PCA Comparison:

We implemented two versions of PCA:

Built-in PCA function: This method showed a test accuracy of 97.4% with Random Forest and 97.2% with Decision Tree.

Custom PCA function: While we expected similar results, the custom function yielded significantly lower test accuracy for all models, with Random Forest achieving 82% and Decision Tree 77%. The reduced performance can be attributed to either suboptimal handling of variance or numerical stability issues in the custom function.
This demonstrates the importance of using robust, well-optimized libraries for high-dimensional datasets like this one.

Key Findings:

Random Forest achieved the highest test accuracy of 97.4%, followed closely by Decision Tree at 97.2%. The strong performance of Random Forest is due to its ensemble nature and ability to handle complex feature interactions.

Logistic Regression and SVM had lower accuracies (around 88%), which is reasonable for these models when handling complex data.
KNN performed well with 93% accuracy, while Naive Bayes had the lowest performance, likely due to its simplistic assumptions not holding well in this dataset.

Medical Dataset Considerations:

In medical applications, recall is a critical metric, as it measures the model’s ability to correctly identify positive cases. Both Random Forest and Decision Tree had the highest recall scores, making them ideal candidates for this classification task. Given that medical datasets often require identifying as many true positives as possible, these models are the most suitable.

Conclusion:

While the custom PCA function underperformed, the overall analysis shows that Random Forest and Decision Tree are the best models for this task, especially given the importance of recall in medical datasets. These models excel in identifying positive cases, making them invaluable tools in healthcare applications.
