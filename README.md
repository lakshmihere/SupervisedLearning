# SupervisedLearning



## 1. Red Wine Quality Prediction Dataset Description: 

- Red Wine Quality Prediction: Used machine learning to determine which physiochemical properties make a wine 'good'!. This dataset is available from the UCI machine learning repository, https://archive.ics.uci.edu/ml/datasets/wine+quality
-  The wine data used in this study comes from the north-west region, named Minho, of Portugal, and we have used only the data w.r.t. red wine
- Relevant publication: P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physico-chemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

## 2. Overview of Data: 

- The dataset of red wine contains 1599 rows and 12 columns. The following are the variables in the dataset
- **Input variables - “features” :** They are based on physicochemical tests namely fixed acidity, volatile acidity, 
citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, 
alcohol 
- **Output variables - “target” :** It is based on sensory data namely quality (score between 0 and 10)

## 3. Part I: Data Preprocessing 

*Summary:*

- All the relevant libraries for the project were imported and the data was read into the file
- A basic exploratory data analysis reveals the summary of the data along with the data types and the descriptive statistics
- There are no missing values in the dataset
- All the variable columns were analyzed for outliers with Tukey’s method
- The data was subjected to winsorization to eliminate outliers
- Univariate analysis and Bivariate analysis were conducted to understand the distribution of various attributes. Bivariate analysis reveals the following. (a). Quality decreases with volatile acidity (b). Quality increases with citric acid (c). Quality increases with sulphates (d). Quality increases with alcohol content
- Obtained Correlation Heat Map to understand correlation of variables and also to extract some important features. It revealed that alcohol has strongest positive correlation with quality. Also, there is a negative correlation between pH and fixed scidity of wine as it is mostly acidic with pH between 3 and 4
- **Review (Target):** Quality is represented by scores ranging from 0 to 10, 0 being the “worst” and 10 being the “best”
- **Review (Target):** Created a new target column “Review”
- **Label Encoding in Review:** Quality < = 5 as “0”, Quality > 5 as “1” 

## 4. Part II: Machine Learning

*Models:*

(A). LOGISTIC REGRESSION

(B). DECISION TREES

(C). RANDOM FORESTS

(D). SVM

(E). STOCHASTIC GRADIENT DESCENT

(F). KNN

*Top 3 Models for dataset:*

**1. SVM**
   - Hyperparameters were tuned, and these are the parameters used in the model are Kernel = ‘poly’, Degree = 3, Gamma = 'auto'
   - Accuracy was 82.5% for this model

**2. Random Forest**
   - Hyperparameters were tuned, and these are the parameters used in the model are criterion = 'entropy’, n_estimators = 100, 
   max_features = ‘sqrt’, min_samples_leaf = 1
   - Accuracy was 82.5% for this model
   
**3. Decision Trees**
   - Hyperparameters were tuned, and these are the parameters used in the model are criterion = ‘entropy’, max_depth = None, 
   min_samples_split = 3
   - Accuracy was 78% for this model

*Variable Importance Plot indicates that **alcohol** is the most important variable*

## 5. Conclusions:
 
- The red wine data was analyzed for quality 
- It was found that quality of the wine is mostly correlated to alcohol 
- Data was split into training and test set. Machine learning models were trained in training set and tested for accuracy on the test   set.
- SVM model does the best with an accuracy of 82.5%
- Machine learning also conclude that “alcohol” is the most important variable that determines the quality of wine

## 6. Future Scope:

- ML models accuracy is not high. The low prevalence of quality levels 3, 4 and 8 and the large distribution overlapping area stratified by quality is a reason.
- We do not have information about the composition of grape varieties in each wine, the mix of experts that evaluated wine quality, or the production year.
- Lack of information about how the dataset was created may impact the prediction of quality using the physicochemical properties as predictors. 