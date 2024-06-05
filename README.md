# Student Performance Evaluation ~Debasish Kumar


### Introduction About the Data

**The dataset** The goal is to predict the `math_score` of the Student.

There are 10 independent variables:

* `gender` : describing the gender of the student
* `race_ethnicity` : describing to which race_ethnicity the student belong
* `parental_level_of_education` : describing the highest level of parental education
* `lunch` : describing whether the student had lunch or not
* `test_preparation_course` : describing whether the student had purchased test preparation course or not
* `reading_score` : describing the reading score of the student 
* `writing_score` : describing the writing score of the student 


Target variable:

* `math_score` : the math score of the student


# Approach for the project 

1. Data Ingestion : 
    * In Data Ingestion phase the data is first read as csv. 
    * Then the data is split into training and testing and saved as csv file.

2. Data Transformation : 
    * In this phase a ColumnTransformer Pipeline is created.
    * For Numeric Variables first SimpleImputer is applied with strategy median , then Standard Scaling is performed on numeric data.
    * For Categorical Variables SimpleImputer is applied with most frequent strategy, then ordinal encoding performed , after this data is scaled with Standard Scaler.
    * This preprocessor is saved as pickle file.

3. Model Training : 
    * In this phase base model is tested . The best model found was catboost regressor.
    * After this hyperparameter tuning is performed on catboost and knn model.
    * This model is saved as pickle file.

4. Prediction Pipeline : 
    * This pipeline converts given data into dataframe and has various functions to load pickle files and predict the final results in python.

5. Flask App creation : 
    * Flask app is created with User Interface to predict the student performance inside a Web Application.


-----
-----





## --------Thanking You----------



