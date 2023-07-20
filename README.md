# DataScience_ProjectSteps
#Data Science project pipeline:
1)Problem Statement Understanding
2)Data Gathering
3)Exploratory Data Analysis(EDA)
4)Feature Engineering
5)Feature Selection
6)Model Building
7)Model Evaluation
8)Model Deployment

# Project Explanation:
This project was started as a motivation for learning Data Science project basic steps and to learn the different data preprocessing techniques such as Exploratory Data Analysis, Feature Engineering, Feature Selection, Feature Scaling,Encoding etc.

# Exploratory Data Analysis(EDA):
EDA stands for Exploratory Data Analysis. where we do analysis and summary of our data by applying some statistical techniques and 
graphical representation.

i)With the help of head() and tail() pandas function we can do basic analysis 
ii)Check shape of the dataset with shape pandas function
iii)Check the features data types with dtype pandas function
iv)Check features data types of each feature as well as non null count with the help of info() function
v)Describe() pandas function can give quick statistical summary
vi)Detecting missing values 
vii)Detecting outliers: boxplot,Z score,IQR
viii)Checking Data balancing

# Feature Engineering :
Feture Engineering include the steps below steps:

a)Droping duplicates values
b)Missing value handling
c)Outliers handling
d)Encoding
e)Data Balancing
f)Feature scalling

a)Droping Duplicates values: With the help of drop_duplicates() pandas function we can drop duplicates entries from the dataset.

b)Missing value handling:
It's impotant to handle missing values before feeding that data to model building.
In real life datasets have many missing values due to a problem in the data collection or extraction process that could be a human error.
and we can not give missing value data for model training so we have to work on that data.if we pass data with missing value or NAN value then it will provide and error. and if we fill those missing value with 0 then it will affect on our accuracy and this process is called as data cleaning.
Below are the steps to handle missing values:
i)Droping all NAN values from the dataset with dropna() pandas function
ii)We can drop the features whose having more than 25% or 30% NAN values
(But we never follow to drop anything from dataset,which cause data lose)
iii)Imputation Techniques:We can impute the NAN values with its mean,median or mode with fillna() pandas function.

c)Outlier handling:
What is outlier?
The datapoints which are out of the range from given or observied data points.That means an outlier is vastly larger or smaller than the remaining values in the dataset.
when outlier present in a system it can negative affect on statistical analysis and trainign process .
and resulting in lower accuracy.
Below are the steps to handle outliers:
i)Droping the outliers value from dataset
ii)Imputation techniques:We can impute the outliers value with median,mode,upper_tail or lower_tail with fillna() pandas function.
iii)Transformation techniques:log transform, square root transform,cube root transform,reciprocol transform etc

d)Encoding :
The performance of a machine learning model not only depends on which algorithm we are using and the hyperparameter tunning 
which we do but also on how we do data pre processing. data can be a number or categorical. most machine learning models only 
accept numerical data, that is the reason it is neccesary to convert catagorical valuesof relevent feature into numbers.
preprocessing the categorical variables becomes a necessary step. We need to convert these categorical variables to numbers 
And this process is called feature encoding.
there are two type of categorical data:
1)ordinal data eg.high,medium,low  true false  approved declined
2)nominal data:city name,department name
If the data is ordinal data we use labled encoding. For the we use replace() pandas function.
And if the data is nomianl data then we use one hot encoding. Where no. of columns get increase by no. of unique value present in feature.

e)Data Balancing:
Data balancing is most important otherwise there are more chances of model get baised towards majority of class.
There are two ways of data balancing:
i)DownSampling: Here we are deleting some data points from majority class to make it balance with minority class. But mostly we are not prefered this as it comes under data loss.
ii)UpSampling: Here we are creating synthetic data points in minority class to make it balance. Or also we can create duplicate copies of our data points or also we can increase the weightage of the data points in minority class.

f)Feature Scalling:
feature scalling is a technique of normalising or standertize the independant features present in dataset in fixed range.
scaling the data makes it easy for a model to learn and understand the problem.
i) Normalization: 
    Minimum and maximum value of features are used for scaling.
    used when we don't know about data distribution.
    it is really affected by outliers.
    scikit learn provide transformer minmaxscaler for normalization.
    value scale down between 0-1
    
ii)Standerdization:
    mean and std devation is used for scaling.
    when we know distribution of data normal or guassion
    it is less affected by outliers.
    it is not bounded to certain range.
    scikit learn provide transformer StandardScaler for standerdization.

# Feature Selection :
In rare case all given features are useful for model building. and if feature are not helping us to predict the output then why unneccesary use them.
If we train our model with all given feature then curseof dimentaionality get increase ,result in model complexity will get 
increase and accuracy will reduce at the end.Hence goal of feature selection is to find the set of best features which helps us to build good model.

Benifits of feature selection: 
1.it help to avoid curse of dimentionality
2.reduce overfitting
3.reduce training and testing time

The techniques used in feature selection:
1)Filter method
2)Wrapper method
3)Embedded method
