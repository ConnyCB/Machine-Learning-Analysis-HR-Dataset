# Machine Learning 
## HR Analytics: Job Change of Data Scientists Data Set
<br>  <br> 

## Source dataset:
Link: https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists<br> 
Download date: 12.07.2022  <br> 
Collaborators: Möbius (Owner)<br> 
License: CC0: Public Domain<br> 
Original Source: https://datahack.analyticsvidhya.com/contest/janatahack-hr-analytics/True/#ProblemStatement<br> 
Collection Methodology: Changing data to imbalanced by augmentation<br> 
<br> <br> 

## Context and content:
A company which is active in Big Data and Data Science wants to hire data scientists among people who successfully pass some courses which conduct by the company. Many people signup for their training. Company wants to know which of these candidates are really wants to work for the company after training or looking for a new employment because it helps to reduce the cost and time as well as the quality of training or planning the courses and categorization of candidates. Information related to demographics, education, experience are in hands from candidates signup and enrollment.

This dataset designed to understand the factors that lead a person to leave current job for HR researches too. By model(s) that uses the current credentials,demographics,experience data you will predict the probability of a candidate to look for a new job or will work for the company, as well as interpreting affected factors on employee decision.

The whole data divided to train and test . Target isn't included in test but the test target values data file is in hands for related tasks. A sample submission correspond to enrollee_id of test set provided too with columns : enrollee _id , target

**Note:**

The dataset is imbalanced.<br> 
Most features are categorical (Nominal, Ordinal, Binary), some with high cardinality.<br> 
Missing imputation is part of the feature engineering.
<br> <br> 

## Research question:
**Predict the probability of a candidate looking for a new job.**<br> 
**What factors influence the candidate's decision?**
<br> <br> 

## Programs /libraries:
Python  
Statsmodels  
Sklearn 
Pandas, Numpy  
Matplotlib, Seaborn   
<br> <br> 

## Data Sets:
The data is split into training data (aug_train.csv) and test data (aug_test.csv). The target variables for the test data are stored in an additional file (sample_submission.csv).

The target size is a binary value of 1 or 0. However, all target sizes in the sample_submission.csv file have 0.5 as a target. Thus, the test file is not suitable for analysis and is discarded.

Only aug_test.csv is used for the analysis and splitted into:<br> 
80% training data (df_train) > 14368 rows, 14 columns<br> 
20% test data > 4790 rows, 14 columns (df_test) 
<br> <br> 

## Features (df_train):

Variable types:<br> 
Categorical: 10<br> 
Numerical: 4<br> 
Boolean: 1<br> 

Missing cells: 15608 (7,2%)<br> 
<br> 
### enrollee_id : Unique ID for candidate

> unique / high cardinality, no missing values

### city: City code

> probably large impact, no missing values

### city_development_index : Developement index of the city (scaled)

> probably large impact, no missing values

### gender: Gender of candidate

> 23.5% missing values, recoded to 'Other'

### relevent_experience: Relevant experience of candidate

> probably large impact, no missing values

### enrolled_university: Type of University course enrolled if any

> 2% missing values, KNNImputer(n_neighbors=3, weights="uniform")

### education_level: Education level of candidate

> 2,4% missing values, KNNImputer(n_neighbors=3, weights="uniform")

### major_discipline :Education major discipline of candidate

> imbalanced, 14,7% missing values, probably low impact

### experience: Candidate total experience in years

> 0.2% missing values, probably large impact

### company_size: No of employees in current employer's company

> 31% missing values KNNImputer(n_neighbors=3, weights="uniform")

### company_type : Type of current employer

> imbalanced, 32% missing values 

### lastnewjob: Difference in years between previous job and current job

> 2,2% missing values, KNNImputer(n_neighbors=3, weights="uniform")

### training_hours: training hours completed

> no missing values

### target: 0 – Not looking for job change, 1 – Looking for a job change

> no missing values

<br> <br>
## File location Pandas Profiling Report: "output" folder
hr-analysis-profile.html 
<br> <br>


## File location original data: "input" folder
**Files:**     
aug_train.csv<br>
aug_test.csv<br>
sample_submission.csv
<br> <br>

## File location Jupyter Notebooks: "main" folder
**Files:**  
EDA_HR_Analysis.ipynb   
ML_HR_Analysis.ipynb 
<br> <br>




