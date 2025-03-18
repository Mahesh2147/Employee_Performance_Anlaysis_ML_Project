# Employee_Performance_Anlaysis_ML_Project

## PROJECT SUMMARY:
* BUSINESS CASE & GOAL OF PROJECT: BASED ON GIVEN FEATURE OF DATASET WE NEED TO PREDICT THE PERFOMANCE RATING OF EMPLOYEE
* The Data science project which is given here is an analysis of employee performance**

### THE GOAL AND INSIGHTS OF THE PROJECT ARE AS FOLLOWS:

### 1. Analysis
  * Data were analyzed by describing the features present in the data. the features play the bigger part in the analysis. The features tell the relation between the dependent and independent variables. Pandas also help to describe the datasets answering following           questions early in our project. The data present in the dataset are divided into numerical and categorical data.

### Categorical Features:
* EmpNumber

* Gender

* EducationBackground

* MaritalStatus

* EmpDepartment

* EmpJobRole

* BusinessTravelFrequency

* OverTime

* Attrition


### Numerical Features:

* Age

* DistanceFromHome

* EmpHourlyRate

* NumCompaniesWorked

* EmpLastSalaryHikePercent

* TotalWorkExperienceInYears

* TrainingTimesLastYear

* ExperienceYearsAtThisCompany

* ExperienceYearsInCurrentRole

* YearsSinceLastPromotion

* YearsWithCurrManager


### Ordinal Features:

* EmpEducationLevel

* EmpEnvironmentSatisfaction

* EmpJobInvolvement

* EmpJobLevel

* EmpJobSatisfaction

* EmpRelationshipSatisfaction

* EmpWorkLifeBalance

* PerformanceRating


### 2.Univariate, Bivariate & Multivariate Analysis:

**Library Used**: Matplotlib & Seaborn
 
**Plots Used**: Histplot, Lineplot, CountPlot, Barplot

**Tip**: All Observation or insights written below the plots

* Univariate Analysis: In univariate analysis we get the unique labels of categorical features, as well as get the range & density of numbers

* Bivariate Analysis: In bivariate analysis we check the feature relationship with target veriable.

* Multivariate Analysis: In multivariate Analysis check the relationship between two veriable with respect to the target veriable.

#### **CONCLUSION**
There are some features are positively correlated with performance rating( Target variable) 
(Emp Environment Satisfaction,Emp Last Salary Hike Percent,Emp Work Life Balance)


### 3.Explotary Data Analysis
**Basic Check & Statistical Measures:** Their is no constant column is present in Numerical as well as categoriacl data.


**Check Skewness of Numerical Features**
* Checking weather the data is Normally distributed or Not with Skewness.

**YearsSinceLastPromotion**, This column is skewed

* skewness for YearsSinceLastPromotion: 1.9724620367914252

## 4.Data Pre-Processing

1. Check Missing Value: Their is no missing value in data

2. Categorical Data Conversion: Handel categorical data with the help of frequency and mannual encoding, because feature is contain lot's of labels

    * Mannual Encoding: Mannual encoding is a best techinque to handel categorical feature with the help of map function,         map the labels based on frequency.
    
    * Frequency Encoding: Frequency encoding is an encoding technique to transform an original categorical variable to a          numerical variable by considering the frequency distribution of the data getting value counts.

3. Outlier Handling Some features are contain outliers so we are impute this outlier with the help of IQR because in all features data is not normally distributed

4. Feature Transformation: In YearsSinceLastPromotion some skewed is present, so we are use Square Root Transformation techinque

    * Square root transformation: Square root transformation is one of the many types of standard transformations.This            transformation is used for count data (data that follow a Poisson distribution) or small whole numbers. Each data           point is replaced by its square root. Negative data is converted to positive by adding a constant, and then                 transformed.
    * Q-Q Plot: Q–Q plot is a probability plot, a graphical method for comparing two probability distributions by plotting        their quantiles against each other.


5. Scaling The Data: scaling the data with the help of Standard scalar

    * Standard Scaling: Standardization is the process of scaling the feature, it assumes the feature follow normal               distribution and scale the feature between mean and standard deviation, here mean is 0 and standard deviation is            always 1.


## 5.Feature Selection

1.  Drop unique and constant feature: Dropping employee number because this is a constant column as well as drop Years Since Last Promotion because we create a new feaure using square root transformation

2. Checking Correlation: Checking correlation with the help of heat map, and get the their is no highly correlated feature is present.

     **Heatmap:** A heatmap is a graphical representation of data that uses a system of color-coding to represent                             different values.

3. Check Duplicates: In this data Their is no dupicates is present.

4. PCA: Use pca to reduce the dimension of data, Data is contain total 27 feature after dropping unique and constant column,from PCA it shows the 20 feature has less varaince loss, so we are going to select 20 feature.

      Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of          dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of         information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for          reducing the dimensionality of a dataset.

5. Saving Pre-Process Data: save the all preprocess data in new file and add target feature to it.

### 6.Machine learning Model Creation & Evaluation

1. Define Dependant and Independant Features:

2. Balancing the data: The data is imbalance, so we need to balance the data with the help of SMOTE

      **SMOTE:** SMOTE (synthetic minority oversampling technique) is one of the most commonly used oversampling methods to                  solve the imbalance problem. It aims to balance class distribution by randomly increasing minority class                    examples by replicating them. SMOTE synthesises new minority instances between existing minority instances.

 3.Splitting Training And Testing Data: 80% data use for training & 20% data used for testing

## Algorithms:

**HERE WE WILL BE EXPERIMENTING WITH 8 ALGORITHM**

1. Logistic Regression : 92.00% accuracy
2. Support Vector Classifier: 95.04% accuracy
3. KNN : 80.00% accuracy
4. Decision Tree : 80.38% accuracy
5. Decision Tree with HyperParameter Tunning : 83.05% accuracy
6. Random Forest : 95.05% accuracy
7. Random Forest with HyperParameter Tunning : 95.05% accuracy
8. Artifical Neural Network [Multilayer percepton]: 96.38%
   

## Tools and Library Used:
### Tools:
Jupyter


### Library Used:
* Pandas
* Numpy
* Matplotlib
* Seaborn
* pylab
* Scipy
* Sklearn


## Goal 1: Department Wise Performances

**PLOT USED**

1. Violinplot: It shows the distribution of quantitative data across several levels of one (or more) categorical variables such that those distributions can be compared.
2. CountPlot: countplot is used to Show the counts of observations in each categorical bin using bars.
Sales: The Performace rating level 3 is more in the sales department. The male performance rating the little bit higher compared to female.

      * From EmpDepartment, development department is showing high performance rating.
      * Male performance rating is slightly higher than female in sales dapertment. Performance rating of 3 is more in              sales department.
      * In Human Resources department most of the employees are having performance rating of 3. Female employees are                performing good.
      * In Development department, maximum of the employees are having performance rating of 3. The male and female                 performance is nearly same for both.
      * In Data Science department, Male employees are doing good. Most employees are having performance rating of 3.
      * In Research& development department, most of the employees are having level 3 performance rating. Both male and             female are doing nearly same.
      * In Finance department, Male employees are doing good. Maimum of employees are having 3 performance rating.

## Goal 2: Top 3 Important Factors effecting employee performance
The top three important features affecting the performance rating are ordered with their importance level as follows,

1. EmpEnvironmentSatisfaction
2. EmpLastSalaryHikePercent, 
3. EmpWorkLifeBalance.
      
      * By using Correlation function, we get the top 3 factor affecting to the employee performance are                            EmpEnvironmentSatisfaction, EmpLastSalaryHikePercent, EmpWorkLifeBalance.
      * EmpEnvironmentSatisfaction, EmpLastSalaryHikePercent, EmpWorkLifeBalance columns have high  correlation values as           compared to other columns.
      * High correlation values means that the columns have stong realtionship with the target features.
  
## Goal 3: A Trained model which can predict the employee performance
**The trained model is created using the machine learning algorithm as follows with the accuracy score**

1. Logistic Regression : 92.00% accuracy
2. Support Vector Classifier: 95.04% accuracy
3. KNN : 80.00% accuracy
4. Decision Tree : 80.38% accuracy
5. Decision Tree with HyperParameter Tunning : 83.05% accuracy
6. Random Forest : 95.05% accuracy
7.  Random Forest with HyperParameter Tunnin : 95.05% accuracy
8.  Artifical Neural Network [Multilayer percepton]: 65380%


## Goal 4: Recommendations to improve the employee performance

  * The overall employee performance can be achieved by employee environment satisfaction.
  * The company needs to focus more on the employee environment satisfaction.
  * The salary hike will give the boost to the employees to perform well.
  * Promote the employee every 6th month Improve Employee's work-life balance this affects the performance rating.
  * While recruiting for HR, consider the female candidates where they perform well compared to male
