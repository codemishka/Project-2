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

