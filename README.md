<h1><p align = "center"> Medical Insurance Cost Prediction</p></h1>

# Project Overview
• Seek insight from the dataset with Exploratory Data Analysis <br>
• Performed Data Processing, Data Engineering and Feature Transformation to prepare data before modeling <br>
• Built a model to predict Insurance Cost based on the features <br>
• Evaluated the model using various Performance Metrics like RMSE, R2, Testing Accuracy, Training Accuracy and MAE <br>
<br>
Data source : https://www.kaggle.com/mirichoi0218/insurance

# Data Definition
1. age: age of primary beneficiary
2. sex: insurance contractor gender, female, male
3. bmi: Body mass index, providing an understanding of body, weights that are relatively high or low relative to height,
objective index of body weight (kg / m ^ 2) using the ratio of height to weight, ideally 18.5 to 24.9
4. children: Number of children covered by health insurance / Number of dependents
5. smoker: Smoking
6. region: the beneficiary's residential area in the US, northeast, southeast, southwest, northwest
7. charges: Individual medical costs billed by health insurance

# Exploratory Data Analysis
• Feature sex, region has an almost balanced amount, meanwhile most people are non smoker & obese <br>
![image](https://github.com/mohan-kartik/Health_Insurance_Cost_Prediction/blob/main/images/bar_chart1.png)

• A person who smoke and have BMI above 30 tends to have a higher medical cost <br>
![image](https://github.com/mohan-kartik/Health_Insurance_Cost_Prediction/blob/main/images/scatter1.png)

• Older people who smoke have more expensive charges <br>
![image](https://github.com/mohan-kartik/Health_Insurance_Cost_Prediction/blob/main/images/scatter2.png)

• People who smoke and obese have the highest average charges compared to others <br>
![image](https://github.com/mohan-kartik/Health_Insurance_Cost_Prediction/blob/main/images/bar2.png)

# Data Processing 
1. Check missing value - there are none <br>
2. Check duplicate value - there are 1 duplicate, will be remove <br>
3. Feature engineering - make a new column `weight_status` based on BMI score <br>
4. Feature transformation: <br>
 A) Encoding `sex`, `region`, & `weight_status` attributes <br>
 B) Ordinal encoding `smoker` attribute <br>
5. Modeling: <br>
 A) Separating target & features <br>
 B) Splitting train & test data <br>
 C) Modeling using Linear Regression, Random Forest, Decision Tree, Ridge, & Lasso algorithm <br>
 D) Find the best algorithm <br>
 E) Tuning Hyperparameter <br>
 
 # Model Evaluation 
| Score | LinearRegression | DecisionTree | RandomForest | Ridge |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| R2 | 0.77 | 0.78 | 0.78 | 0.86 |
| Train Accuracy | 0.74 | 1.0 | 0.97 | 0.74 |
| MAE | 4305.20 | 2798.83 | 2608.55 | 4311.10 |
| Test Accuracy | 0.77 | 0.78 | 0.86 | 0.77 | 
| RMSE | 6209.88 | 6067.50 | 4841.88 | 6238.13 |
 
 # Conclusion
Based on the predictive modeling, Linear Regression algorithm has the best score compared to the others, with MAE Score 4305.20, RMSE Score 6209.88, & R2 Score 0.77. <br>
Therefore, Linear Regression algorithm is the best fitted model based on the training and testing accuracy.
