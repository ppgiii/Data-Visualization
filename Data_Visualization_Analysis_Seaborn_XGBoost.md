# Statistical Data Visualization

For this project, statistical data visualization uses Seaborn to create a model from a binary element response variable using feature selection.  It attempts to outline procedures for discovering the best model satisfying the objective.  

It covers the following groups:  
Objective  
EDA (Exploratory Data Analysis)  
Modeling

---
## Objective  
This exercise uses the dataset [Breast Cancer Diagnosis](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29) from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php).  The output variable, or response, is 'diagnosis' and a model will be constructed to predict the outcome for a given set of predictor variables.   

In this section, Python libraries will be imported and the dataset loaded using Pandas into a dataframe.  Another important aspect is to examine the dataset and its description.  Several information might be useful in helping prepare the data as well as gain insight on which model to use.

## EDA  
The majority of data science spends 80% just on the data itself, known as the [80/20 rule.](https://hbr.org/2018/08/what-data-scientists-really-do-according-to-35-data-scientists)  Exploratory Data Analysis examines the data in order to clean, manipulate and prepare for model evaluation.  Descriptive statistics that comes with Pandas provide details that can help in cleaning and identifying the state of the dataset.  Manipulation involves the adjustment of features or wrangling of data.  Finally, codes prepare the data for visualization to understand and inspect the behavior prior to modeling.

This notebook will use Seaborn as the tool for visual preparation.  Several examples include box plot, swarm plot, violin plot, & various correlation plots.

## Modeling  
Both the project objective and the type of datasets determine the steps for finding the highest probable model.  It is a binary classifier that estimates an outcome.  Feature selection develops the best available features that provides the highest probable prediction.

#### Classification  
The response variable only contains two elements so it is a nominal categorical variable and is a [binary classification](https://www.sciencedirect.com/topics/computer-science/binary-classification) problem.  This project uses the XGBClassifier from [XGBoost](https://xgboost.readthedocs.io/en/latest/).

#### Univariate Feature Selection
[Feature selection](https://machinelearningmastery.com/an-introduction-to-feature-selection/) aims to find the best combinations of features to create the best model based on the response variable.

#### [Recursive Feature Elimination](https://bookdown.org/max/FES/) with Cross-Validation  
This method is a greedy wrapper method in predictive modeling.  It ranks the feature in importance and removes a feature as it searches for the best model.

#### Plot CV Scores vs Number of Features Selected
This step evaluates the optimal model based on accuracy through plots.

#### Feature Extraction using Principal Component Analysis
Visualize the features based on model performance.
