# Project-2

## **Background**

Stroke is a critical health concern with profound implications for individuals and society. The application of data analysis techniques holds immense importance in predicting and preventing strokes. By scrutinizing extensive datasets encompassing medical records, genetics, lifestyle factors, and more, data analysis provides invaluable insights into stroke risk factors and early warning signs. 

These insights not only enable timely interventions and personalized treatment but also facilitate the development of preventive strategies, ultimately reducing the incidence and impact of stroke. Harnessing the power of data analysis is poised to revolutionize stroke research, clinical practice, and public health initiatives, offering the promise of saving lives and enhancing the well-being of individuals worldwide.

## **Business Understanding**

•	Objective: Predicting the likelihood of strokes in individuals based on existing signs and data.

•	Purpose of Machine Learning Model: Achieve a classification accuracy of more than 95% under specific conditions.

•	Solution Approach: Develop a machine learning model and evaluate model performance

•	Model Focus: The model's primary focus is to efficiently classify individuals who may be at risk of experiencing a stroke.

•	Revolutionizing Stroke Prediction: The model has the potential to revolutionize stroke prediction and contribute significantly to proactive healthcare interventions.

## **Features in Datasets:**

•	id : a unique identifier that distinguishes each data [int]

•	Gender: Patient's gender ('Male', 'Female', and 'Other') [str]

•	age : Age of the patient [int]

•	Hypertension: Hypertension or high blood pressure is a disease that puts a person at risk for stroke. 0 if the patient does not have hypertension, 1 if the patient has hypertension. [int]

•	heart_disease: Heart disease is a disease that puts a person at risk for stroke. 0 if the patient does not have heart disease, 1 if the patient has heart disease. [int]

•	ever_married : Describes whether the patient is married or not ('Yes' or 'No') [str]

•	work_type : Type of employment or status ('children' for children, 'Govt_job' for civil servants, 'Never_worked' for those who have never worked, 'Private' or 'Self-employed' for entrepreneurs or freelancers) [str]

•	Residence_type : Condition of residence ('Rural' for rural areas and 'Urban' for urban areas) [str]

•	avg_glucose_level : Average amount of glucose (sugar) in the blood [float]

•	bmi : Body Mass Index to measure the stability of body weight with height. [float]

•	smoking_status : Description of smoking ('formerly smoked' for those who have smoked, 'never smoked' for those who have never smoked, 'smokes' for those who smoke, and 'unknown' for those whose smoking status is unknown) [str]

•	Target: stroke : Prediction target if the patient has a stroke then 1, otherwise 0 [int]

## **Data Preparation:**

•	Eliminated the 'id' column as it did not provide valuable insights, reducing dimensionality.

•	Checked for NULL values in dataset attributes, finding only the 'BMI' attribute with missing values.

•	Imputed missing 'BMI' values with the median due to skewed distribution.

•	Retained records despite dataset skewness and the presence of missing 'BMI' values, as many of them correlated with positive stroke cases.

•	Deleted a single “Other” value in the 'gender' column 

•	Transformed numeric binary values in most attributes into string binary values for dummy encoding, introducing additional columns.

•	Executed random oversampling to address target attribute imbalance, increasing the number of records in the minority class for improved predictive accuracy.


The Random Forest model was best-performing one based on its accuracy. This is a common approach to model selection in machine learning.

Here's a breakdown of the accuracies and the chosen model:

Decision Tree: 97.68%
K-Nearest Neighbors (KNN): 97.73%
Random Forest: 99.33%

The Random Forest model achieved the highest accuracy at 99.48%, making it the chosen model. High accuracy is a good indicator of model performance, but it's important to consider other factors like the dataset's characteristics, model complexity, and the specific problem you're trying to solve.

## **Model Evaluation Summary**
We have developed a Random Forest Classifier for our project and evaluated its performance on a given dataset. Here's a summary of the evaluation results:

•	Precision: Our model achieved an impressive precision score of approximately 98.7%. This indicates that it excels in correctly identifying positive cases while maintaining a low rate of false positives.

•	Recall: The recall score is a perfect 100%, indicating that the model effectively captures all relevant instances of the positive class without missing any.

•	F1-Score: With an F1-Score of around 99.3%, our model demonstrates a balanced performance, effectively minimizing both false positives and false negatives.

•	Confusion Matrix: The confusion matrix reveals that our model produced 965 true positives and only 13 false positives, which is a strong performance.

•	Classification Report: The classification report confirms the model's consistency, with exceptional precision, recall, and F1-Score for both Class 0 and Class 1.

•	Accuracy: The overall accuracy of our Random Forest Classifier is 99%, indicating its capability to correctly classify instances in the dataset.

Summary: In summary, our Random Forest Classifier demonstrates exceptional performance, with high accuracy and reliability in correctly identifying both positive and negative cases. These results suggest that the model is promising for the intended task.

For detailed evaluation metrics and additional information, please refer to the documentation and codebase.

