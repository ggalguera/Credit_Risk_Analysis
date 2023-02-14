# Credit Risk Analysis
## Analysis Overview
Using Python, we built and assessed multiple machine learning models to anticipate credit risk. Our procedure consisted of oversampling with RandomOverSampler and SMOTE, undersampling with ClusterCentroids, and a combination of both using SMOTEENN. We then compared two models, BalancedRandomForestClassifier and EasyEnsembleClassifier, that minimize bias. We will evaluate their performance and provide a recommendation on their suitability for credit risk prediction.
## Results
### Random Over Sampler Model
![RandomOversampler](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/RandomOversampler.png)

Balanced Accuracy Score was 64% for this model.
For the high-risk class, the precision is very low at 0.01, which means that out of all the instances predicted as high-risk, only 1% are actually true high-risk cases. However, the recall or sensitivity is relatively high at 0.73, which means that the model correctly identified 73% of the true high-risk cases.
For the low-risk class, the precision is very high at 1.00, which means that out of all the instances predicted as low-risk, all of them are true low-risk cases. The recall for the low-risk class is relatively low at 0.55, which means that the model correctly identified only 55% of the true low-risk cases.
### SMOTE Model
![SMOTE](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/SMOTE.png)

Balanced Accuracy Score was 66% for this model.
For the high-risk class, the precision is very low at 0.01, which means that out of all the instances predicted as high-risk, only 1% are actually true high-risk cases. The recall or sensitivity is 0.63, which means that the model correctly identified 63% of the true high-risk cases.
For the low-risk class, the precision is very high at 1.00, which means that out of all the instances predicted as low-risk, all of them are true low-risk cases. The recall for the low-risk class is 0.69, which means that the model correctly identified 69% of the true low-risk cases.
### Cluster Centroids Model
![ClusterCentroids](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/ClusterCentroids.png)

Balanced Accuracy Score was 66% for this model.
For the high-risk class, the precision is very low at 0.01, which means that out of all the instances predicted as high-risk, only 1% are actually true high-risk cases. The recall or sensitivity is 0.69, which means that the model correctly identified 69% of the true high-risk cases.
For the low-risk class, the precision is very high at 1.00, which means that out of all the instances predicted as low-risk, all of them are true low-risk cases. The recall for the low-risk class is 0.40, which means that the model correctly identified 40% of the true low-risk cases.
### SMOTEENN Model
![SMOTEENN](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/SMOTEENN.png)

Balanced Accuracy Score was 54% for this model, the lowest of the models reviewed so far.
In the given classification report, precision for the high-risk class is 0.01, which means that out of all the positive predictions made for the high-risk class, only 1% were actually correct. Recall for the high-risk class is 0.73, which means that out of all the actual high-risk instances, only 73% were correctly identified by the model.
For the low-risk class, precision is 1.00, indicating that all positive predictions for the low-risk class were true positives. Recall for the low-risk class is 0.57, which means that only 57% of actual low-risk instances were correctly identified by the model.
### Balanced Random Forest Classifier Model
![BalancedRandomForestClassifier](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/BalancedRandomForestClassifier.png)

Balanced Accuracy Score was 77% for this model, the second best of the models.
For the high-risk class, the precision is very low at 0.03, which means that out of all the instances predicted as high-risk, only 3% are actually true high-risk cases. However, the recall or sensitivity is relatively high at 0.67, which means that the model correctly identified 67% of the true high-risk cases.
For the low-risk class, the precision is very high at 1.00, which means that out of all the instances predicted as low-risk, all of them are true low-risk cases. The recall for the low-risk class is also relatively high at 0.87, which means that the model correctly identified 87% of the true low-risk cases.
### Easy Ensemble Classifier Model
![EasyEnsembleClassifier](https://github.com/ggalguera/Credit_Risk_Analysis/blob/main/EasyEnsembleClassifier.png)

Balanced Accuracy Score was 93% for this model, the highest of the models reviewed.
For the high_risk class, the precision is 0.09, meaning that 9% of the predicted high-risk loans are actually high-risk, it is low but it is the best of the results from all models reviewed. However, the recall is high at 0.92, which means that the model was able to identify 92% of the actual high-risk loans.
For the low_risk class, the precision is perfect at 1.00, indicating that all predicted low-risk loans are actually low-risk. The recall is 0.94, which means that the model was able to capture 94% of the actual low-risk loans.
## Summary
The Easy Ensemble Classifier Model outperformed other models in predicting credit risk with the highest precision and recall for high-risk and low-risk loans. Although its precision for high-risk loans was low at 9%, its recall was high at 92%, meaning it correctly identified 92% of high-risk loans while only granting 8% of total high-risk loans. Thus, it is the recommended model. However, the Bank should also consider the impact of the 91% of low-risk loans predicted as high risk on their finance compared to the 9% of high-risk loans identified by the model. A more detailed analysis is needed to determine how much the bank may lose on interest versus unpaid loans.
