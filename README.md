# Customer-Analysis-Case-Study

## Scenario

You are working as an analyst for an auto insurance company. The company has collected some data about its customers including their demographics, education, employment, policy details, vehicle information on which insurance policy is, and claim amounts. You will help the senior management with some business questions that will help them to better understand their customers, improve their services, and improve profitability.

## Business Objectives

- Retain customers,
- analyze relevant customer data,
- develop focused customer retention programs.

Based on the analysis, take targeted actions to increase profitable customer response, retention, and growth.

## Activities

Refer to the [`Activities.md`](./Activities.md) file where you will find guidelines for some of the activities that you want to do.

## Data

The csv files is provided in the folder. The columns in the file are self-explanatory.

# Activites List
<b>Important: for Activity 1, Activity 2 and  Activity 3 , please use the files [file1.csv](./Data/file1.csv), [file2.csv](./Data/file2.csv) and [file3.csv](./Data/file3.csv) from the [Data](./Data) folder.</b>
### Activity 1 (Monday)

- Aggregate data into one Data Frame using Pandas. Pay attention that files may have different names for the same column. therefore, make sure that you unify the columns names before concating them. 
- Standardizing header names
- Deleting and rearranging columns – delete the column customer as it is only a unique identifier for each row of data
- Working with data types – Check the data types of all the columns and fix the incorrect ones (for ex. customer lifetime value and number of open complaints ). Hint: remove the percentage from the customer lifetime value and truncate it to an integer value.
- clean the number of open complaints and extract the middle number which is changing between records. pay attention that the number of open complaints is a categorical feature.
- Filtering data and Correcting typos – Filter the data in state and gender column to standardize the texts in those columns
- Removing duplicates

### Activity 2 (Tuesday)
- Replacing null values – Replace missing values with means of the column (for numerical columns). Pay attention that the Income feature for instance has 0s which is equivalent to null values. (We assume here that there is no such income with 0 as it refers to missing values)
Hint: numpy.nan is considered of float64 data type.
- Bucketing the data - Write a function to replace column "State" to different zones. California as West Region, Oregon as North West, and Washington as East, and Arizona and Nevada as Central
- (Optional) Standardizing the data – Use string functions to standardize the text data (lower case)

<b>Important: for Activity 3 and Activity 4 , please use the [file Data_Marketing_Customer_Analysis_Round3.csv](./Data/Data_Marketing_Customer_Analysis_Round3.csv) from the [Data](./Data) folder.</b>

### Activity 3 (Wednesday)

- Get the numeric data into dataframe called `numerical` and categorical columns in a dataframe called `categoricals`.
(You can use np.number and np.object to select the numerical data types and categorical data types respectively)
- Now we will try to check the normality of the numerical variables visually
  - Use seaborn library to construct distribution plots for the numerical variables
  - Use Matplotlib to construct histograms
  - Do the distributions for different numerical variables look like a normal distribution 
- For the numerical variables, check the multicollinearity between the features. Please note that we will use the column `total_claim_amount` later as the target variable.
- Optional: Drop one of the two features that show a high correlation between them (greater than 0.9). If there is no pair of features that have a high correlation, then do not drop any features.

### Activity 4 (Thursday)

- Show a plot of the total number of responses.
- Show a plot of the response by the sales channel.
- Show a plot of the response by the total claim amount.
- Show a plot of the response by income.
- (Optional) Don't limit your creativity!  plot any interesting findings/insights that describe some interesting facts about your data set and its variables.
- Plot the Correlation Heatmap.
- Clean your notebook and make it a readible and presentable with a good documentation that summarizes the Data Cleaning, Exploration(including plots) Steps that you have performed.
### Activity
(Wednesday)
#### Linear Regression
- Train-test split.
- Standardize the data (after the data split).
- Apply linear regression.
- Model Interpretation.

(Thursday)
#### Model Validation
- Model Evaluation:
  - MSE.
  - RMSE.
  - MAE.
  - R2.
  - Adjusted R2.
- Feature Importance.

#### Model Iteration (Thursday and Friday)
- Please rerun the model after adding the hot encoded categorical variables as well as other numeric categroical variables (e.g. number of open complaintes).
- Please rerun the model after removing the outliers and compare the results using R2 metric.
