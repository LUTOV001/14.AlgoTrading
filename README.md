# **UCB FinTech Bootcamp Module 14 Challenge**
# *Algorithmic Trading with Machine Learning*
## **Introduction**
### The Bootcamp Module 14 Challenge - Algorithmic Trading with Machine Learning (ML) requires the preparation of an ML model to automate trading of assets (e.g. stocks) based on the data provided in the sample file. The file provide trading data/features for an unnamed investment: Opening Price, High, Low, Closing Price and Volume, all date and time stamped over a period that goes from January 2015 to January 2021. The purpose of the challenge is to create, train and test an ML model to predict the returns from investment in this asset and then compare the model predictions vs. the actual returns. Two ML models are to be prepared and evaluated for performance: the first model uses the [Support Vector Classifier (SVC)](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html) from SKLearn Support Vector Machine (SVM) and the second uses the [Logistic Regression (LogReg)](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html), also from SKLearn. A report comparing the models' predictions vs the actual returns is provided in the last section of this README file.
---
## **Goals and Objectives**
### *Part I.*  : Establish a baseline performance: Load the sample file from the Resource Folder (emerging_markets_ohlcv.csv) and calculate the trading Actual Returns (e.g. from the Close Price figures). Next, using the statistical mean metric (SMA) on the closing price, determine the 'Trading Signal' (1: Buy, 0: Hold, -1:Sell) if the returns are greater than zero( then Signal = -1, sell), if they are equal to zero ( then signal = 0, hold) or less than zero (then signal = 1, buy) for 2 analysis time frames/windows: short (4 days) and long (100 days). Lastly, match all the data - Close price, Actual Returns, SMA for the Short and Long Windows and Trading Signal - by date/time stamp in a data frame. 
### Then, verify how balanced the sample data is for the Trading Signal values; since this is the feature the ML models will predict, we want to make sure there is enough examples of each possible outcome in the sample data, so the model can be properly trained.

### *Part III.*  : Tune the baseline trading algorithm : Set the data for the ML models and then train, test and evaluate the perfprmance of the first ML model, using the Support Vector Classifier strategy from SKLearn Support Vector Machine (SVM). Plot the ML model predicted returns vs. the Actual Returns to evaluate the model's performance.
### *Part IV.* : Evaluate a new ML classifier model/strategy : Using the same sample data, create a second ML model based on the Logistic Regression Strategy from SKLearn. Train, test and evaluate the model's performance by plotting it's predicted returns vs the Actual Returns from the sample data
### *Part V.* : Create an evaluation report for the two ML models
---
## **Technologies and Tools**
### The following list includes the main technologies and tools using during the preparation and deployment of the solution:
### 1. *Python* - Programming language used to code the solution. Version 3.7.13 was used. Required libraries and frames listed in the Installation section below
### 2. *GitHub* - Reposotory for code deployment, version management and documentation of the presented solution
### 3. *Jupyter Labs* - IDE tool for coding, code testing/debugging and solution documentation. Version V3.4.4 was used
### 4. *Git Bash console* - Local console used to test the coded solution and sync wiht GitHub Version 2.40.0.windows.1 was utilized
### 5. *Slack* - Collaboration tool to communicate and brainstorm with other FinTech Bootcamp participants
### 6. *Operative System* - This solution was prepared in a PC running Windows 11 v H22
###
### *For additional details, please refer to the watermark output at the bottom of the ***machine_learning_trading_bot.ipynb*** Jupyter Notebook*
---
## **Installation Guide**

### 1. [sklearn](https://scikit-learn.org/) : scikit-learn, also known as sklearn, is a popular open-source machine learning library for Python. It provides a wide range of machine learning algorithms, tools, and utilities for tasks such as classification, regression, clustering, dimensionality reduction, model selection, and preprocessing of data. To install, follow these steps:
#### 1.1. Open the GitBash terminal
#### 1.2 Type the following command and press Enter:
```python 
pip install scitkit-learn
```
---
## **Solution Structure**

### The **[14.AlgoTrading](https://github.com/LUTOV001/14.AlgoTrading)** repository in GitHub contains the solution components. The repository consists of the following folders and contents as described below:
 
###   *1. Resources :* Contains the .csv file with the asset trading sample data used as the basis for the ML model training and predictions testing.
###   *2. Results :* Contains the plots for the 2 ML models comparing their Predicted Returns vs the Actual Results (.png files) and the Classification Reports for each of the ML models (.txt files) used in the evaluation report at the end of this README file
###   *2. gitignore :* Instructions for which files/file types to exclude from the sync process between GitHub and the local environment.
###   *3. README.md :* The present file containing this outline of the challenge and its components and results.
###   *4. machine_learning_trading_bot.ipynb :* This is the Jupyter Notebook with the code for the core challenge solution, analysis and ML models.
###  
---
## **User Instructions**
### 1. Launch the Jupyter Lab from the GitBash terminal using the following command line:
```python 
jupyter lab
```
### 2. From the Jupyter Lab terminal, navigate to the location of the ***machine_learning_trading_bot.ipynb*** notebook and open it
### 3. Reset the Kernel and
### 4. Run the steps from the top and in sequence verifying the results as per the comments in the notebook, including outputs on the screen such as dataframe listing/on screen printing and other on screen outputs such as model summaries and evaluation statistics.
####
---
## **Results Analysis Report**
#### Below are the key results and analysis of the two ML models 
### ***ML Model 1 - SVC Strategy***
#### > Using the original data set as-is (e.g. unbalanced), create a Logistics Regression model to predict the Loan Status classifiction for future loans by:
#### > Creating the model and fitting it to the original data set
#### > Training the model (*Note: We are using the default Training/Test split of 75/25)* 
#### > Test the model by generating the class predictions
#### > Qualify the prediction results by measuring/generating and analyzing accuracy, Confussion Matrix and the Classification Report
### ***Model 2 - Resampling/Balanced Classification***
#### > Using the [RandomOversampler module from the imbalanced-learn library](https://imbalanced-learn.org/stable/generated/imblearn.over_sampling.RandomOverSampler.html) resample the loan data and create a Logistics Regression model to predict the Loan Status classifiction for future loans by:
#### > Creating the model
#### > Run Resampling and ensure the classes are now balanced - e.g. Class 0 and Class 1 counts are equal
#### > Fit the model to the resampled data set
#### > Training the model (*Note: We will continue to use the default Training/Test split of 75/25)* 
#### > Test the model by generating the class predictions
#### > Qualify the prediction results by measuring/generating and analyzing accuracy, Confussion Matrix and the Classification Report
---
## **Results**
#### Below are the key results and analysis of the two ML models 

#### ***Machine Learning Model 1 (Original Data):***
#### *Confusion Matrix*
#### [[18663  , 102]
#### [   56   , 563]]

#### The first row of the matrix shows that 18,663 instances were correctly classified as positive, and 102 instances were incorrectly classified as negative. 
#### The second row of the matrix shows that 56 instances were incorrectly classified as positive, and 563 instances were correctly classified as negative.
#### We can see that due to the imbalance in the original data set, Class 1 metrics are not as good as Class 0, as shown by the 102 'False Negatives'.

#### *Classification Imbalanced Report*  
#### ![ML1 Classification Report](https://github.com/LUTOV001/12.ML_Credit_Risk/blob/main/Resources/ML_Model_1.jpg) 

#### While the overall model accuracy is 95%, we need to look at the detailed results by class: 
#### *1. Healthy Loan (Class 0):* Precision and F1 are both 100% and recall is almost as good (99%). While the SPE at 91% indicates good performance identifying 'positives' (e.g. correctly predicting 0s as such) there could be improvements in identifying 'false positives', which could be accomplished by increasing the training data rate (we used the default 75% for this model) and/or changing the evaluation model (Logistic Regression was used).
#### *2. High Risk Loan (Class 1):* Precision is 85% and f1 is 88%. While the spe at 99% indicates good performance identifying 'negatives' (e.g. correctly predicting 1s as such) there could be improvements in identifying 'false negatives'. This could be accomplished by increasing the training data rate (we used the default 75% for the original data set) and using a balanced data set
#### The IBA rate - which measures the model's accuracy taking into account class imbalance - looks good at 91% and 90% for class 0 and class 1 respectively, aligning with the other good ratios for Class 0, however, as discussed above, there is room for improvement for Class 1, therefore I recommend a resampling and balancing of the data to run an improved model.

#### ***Machine Learning Model 2 (Re-sampled/Balanced Data):***

#### *Confusion Matrix*
#### [[18649   , 116]
#### [    4   , 615]]

#### The first row of the matrix shows that 18,649 instances were correctly classified as positive, and 116 instances were incorrectly classified as negative. 
#### The second row of the matrix shows that 4 instances were incorrectly classified as positive, and 615 instances were correctly classified as negative.
#### We can see the impact of a balanced data set: 
#### The 'True negative' rate remained high, improving from 563 to 615 (9% improvement). On the down side, for 'False Negatives', there was a 13% increase in cases (from 102 to 116)
  
#### ![ML2 Classification Report](https://github.com/LUTOV001/12.ML_Credit_Risk/blob/main/Resources/ML_Model%20_2.jpg) 

#### While the overall model accuracy is now 99% after resampling, let's look at the detailed results by class: 
#### *1. Healthy Loan (Class 0):* Precision and F1 remained at 100% and recall also remained at 99%. Looking at the Confusion Matrix, there continued to be a high percentage of 'True Negatives' and a low percentage of False Positives, so the re-sampling did not impact the great rates we had for Class 0 and in fact, improved the "False positive" count, as explained above.
#### *2. High Risk Loan (Class 1):* While precision fell 1 point to 84%, F1 improved 3 points to 91% and recall jumped 14 points to 99%. Interpretation of metrics and conclusions follow below.
---
## **Summary**

#### In conclusion, looking at the models from both the ***Risk*** and ***Revenue*** perspectives, the resampling and rebalancing of the model proved benefitial on both areas: 

#### *Risk :* Besides improving the overall accuracy of the model by 4 points, the resampling improved the counts on risk relevant categories by improving the "True Negative" counts by 9% with very low impact (-1%) on 'True Positive" counts and a reduction of 96% on "False Positives".

#### *Revenue :* As mentioned above, minimal impact on the main revenue driver "True Positives" (-1%) and while it increased the case of cases driving revenue loss - e.g.'False Negatives' this comes as the downside of operating with a lower risk profile with the 96% reduction on  "False Positive" counts.

#### For the reasons listed above, ***we recommend using the Resample/Balance model which prioritizes operations with a lower risk profile without significant revenue impacts.***
---
### **Credits**
#### Prepared by Luis Torres 
#### [LUTOV001](https://github.com/LUTOV001)
#### June 2023