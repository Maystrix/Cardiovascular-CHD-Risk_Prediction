# Cardiovascular-CHD-Risk_Prediction

![image](https://user-images.githubusercontent.com/102039796/216950415-62674817-5ad3-41b5-a9e7-8d4061238d73.png)

## Summary![rainbow](https://user-images.githubusercontent.com/102039796/216950551-0167dbfb-a34b-4938-9e4c-5baef30bab51.png)

The dataset contained information of over 3000 patients with different medical histories.For better interpretability of data ,age group was divided into 3 classes 'young, middle, old age' . Blood Pressure were classified based on their Hypertension severity into 'Normal, Elevated, Stage_1, Stage_2, Crisis, Isolated systolic , Isolated diastolic' on the basis systolic and diastolic Blood Pressures & Cholestrol levels were classified into 'Normal, Elevated, High risk'.Several features were interlinked to each other based on their usage and measures , which were further understood by visualizing their effect on CHD risk for patients. Null values were removed since we can't and should not make assumptions wrt medical conditions of patients . Some features were heavily influenced by outliers which can affect the model prediction hence they were handled using Inter-quartile Range (IQR) method. Further some categorical features were encoded using label encoding while rest were encoded using One-hot-df method as they contained multiple values , which are better understood when converted into dummies. For checking and handling multicollinearity Variance inflation factor(VIF) method was used to remove correlated independent variables. Since, the data was heavily imbalanced Synthetic Minority Oversampling Technique (SMOTE) was used to generate synthetic samples from the minority class. Before model implementation , dataset was Standardized using StandardScaler method since,the dataset is mostly normally distributed & it mantains information about outliers and makes model less sensitive. 6 models were implemented and some with below-par score underwent hypertuning for better results. Random Forest made the best predictions with an F1-score and test-accuracy of 90 %. Age , Heart rate  and  were the top features used by the model for data interpretation. 

## Conclusion ![rainbow](https://user-images.githubusercontent.com/102039796/216772334-4cecf546-71ae-4a0e-9755-0e879598b6ff.png)

* 6 different Machine Learning algorithms were trained on training dataset 
* Random forest provided best results and thus classifying the patients with  an F1-score and test accuracy of 90 %
* To provide immediate treatment to the patients at arisk of CHD. Type II error should be low, i.e. High Recall value is desired
* To avoid time consumption on providing patients with CHD treatment ,when actually they don't have any. Type I error should be low, i.e. High Precision is desired.
* To treat patients with actual risk of CHD, there should be a balance between precision & recall. i.e. High F1-score is desirable , since it punishes the extreme values more.
* The models which provide the above desired results are as follows :
1. **Recall :**  k-Nearest Neighbors
2. **Precision :**  Support Vector Machines
3. **F1-score :**  Random Forest
4. **Test Accuracy :**  Random Forest

* Age is the deciding factors for the patients mentioned in the dataset, followed by heart_rate, cigerettes per day and cholestrol level.
* More focus should be given on the above mentioned features of the patients attending for treatment.
* Though count of patients not suffering from CHD is more, count of patients with risk of CHD is high.
