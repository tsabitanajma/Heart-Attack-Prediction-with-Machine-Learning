# Heart-Attack-Prediction-with-Machine-Learning

## About Dataset
This dataset describes the contents of the heart-disease directory. It contains 76 attributes, but all published experiments
refer to using a subset of 14 of them. The "goal" field refers to the presence of heart disease
in the patient. It is integer valued from 0 (no presence) to 4. (Resource: https://www.kaggle.com/datasets/imnikhilanand/heart-attack-prediction).

Columns:
*   age : age in years
*   sex : sex (1 = male; 0 = female)
*   cp : chest pain type (1 = typical angina; 2 = atypical angina; 3 = non-anginal pain; 4 = asymptomatic)
*   trestbps : resting blood pressure (in mm Hg on admission to the
hospital)
*   chol : serum cholestoral in mg/dl
*   fbs : fasting blood sugar > 120 mg/dl (1 = true; 0 = false)
*   restecg : resting electrocardiographic results (0 = normal; 1 = having ST-T wave abnormality)
*   thalach : maximum heart rate achieved
*   exang : exercise induced angina (1 = yes; 0 = no)
*   oldpeak : ST depression induced by exercise relative to rest
*   slope : the slope of the peak exercise ST segment (1 = upsloping; 2 = flat; 3 = downsloping)
*   ca = number of major vessels (0-3) colored by flourosopy
*   thal : 3 = normal; 6 = fixed defect; 7 = reversable defect
*   num : diagnosis of heart disease (0 = <50% diameter narrowing; 1 = >50% diameter narrowing)

## Conclusion
1. The dataset contains missing values of less than 75% in the columns "trestbps", "restecg", "exang", "fbs", "chol", and "slope". These were handled using KNN Imputer. Columns "ca" and "thal" had more than 75% missing values and were removed to avoid irrelevant imputation results.

2. The dataset contains outliers in the columns "trestbps", "chol", and "oldpeak". These were handled using winsorizing.

3. Categorical data were converted into numerical data using LabelEncoder.

4. The data were split into training and testing sets with an 80:20 ratio.

5. Data imbalance was addressed using SMOTE.

6. Standardized X variables data using StandardScaler.

7. After the data clean, modeling was carried out using several methods:

  * Naive Bayes: achieved an accuracy of 83%
  * Decision Tree: achieved an accuracy of 73%
  * KNN: achieved an accuracy of 85%
  * Random Forest: achieved an accuracy of 85%
  * SVM: achieved an accuracy of 83%

8. Overfitting checks were performed on the two models with the highest F1 scores and it was found that the KNN model had more balanced training and testing accuracy.

9. The best classification model based on the F1 score and balanced train-test accuracy is the **KNN model** with **F-1 score accuracy is 85%**.
