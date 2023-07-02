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
#### > Using the sample data set, we train the SVC model to predict the Trading signal 
#### > Then we test the model and run the Classification Report:
##### ![svc_report.txt](https://github.com/LUTOV001/14.AlgoTrading/blob/main/Results/svc_report.txt)
#### > And finally, we calculate the SVC Returns by multiplying the ML predicted signal times the Actual Return values and plot these 2, SVC Returns (Predicted) vs. the Actual returns:
##### ![svc_returns_plot.png](https://github.com/LUTOV001/14.AlgoTrading/blob/main/Results/svc_returns_plot.png)
#####
### ***ML Model 2 - LogReg Strategy***
#### > Using the sample data set, we train the LogReg model to predict the Trading signal 
#### > Then we test the model and run the Classification Report:
##### ![logreg_report.txt](https://github.com/LUTOV001/14.AlgoTrading/blob/main/Results/logreg_report.txt)
#### > And finally, we calculate the LogReg Returns by multiplying the ML predicted signal times the Actual Return values and plot these 2, LogReg Returns (Predicted) vs. the Actual returns:
##### ![logreg_returns_plot.png](https://github.com/LUTOV001/14.AlgoTrading/blob/main/Results/logreg_returns_plot.png)
#####
---
### **Conclussion and Summary**
### ***Questions and Answers from the Notebook***
#### *1. What impact resulted from increasing or decreasing either or both of the SMA windows?*
##### *Answer:* Changing the window sizes will change their SMA values, the longer the period, the more diluted the impact of the hourly changes in the data, hence impacting the Trade signal output occurrences (e.g. less 1s, more -1s) which in turn would make the sample data more unbalanced for 1s and thus making the training of the ML model and as a result its performance in testing less accurate.
#### *2. Did this new model (LogReg) perform better or worse than the provided baseline model?* 
##### *Answer:* The Testing Classification report showed improvements of the LogReg model over the SVC model as follows:
###### *Class (-1)* : Recall improved from 4% to 33%, making the F1 score improve from 7% to 38%
###### *Class ( 1)* : Recall decreased from 96% to 66%, making the F1 score decrease from 71% to 61%
###### *Overall Accuracy* : The LogReg model had a marginal improvement of 1 point, from 49% to 50% on overall precision and 8 points (43% to 51%) for the F1 score
#### *3. Did this new model perform better or worse than your tuned trading algorithm?*
##### *Answer:* Based on the Classifiction reports, the LogReg model overall performed better than the SVC model. The degradation in performance for class 1 (e.g. Buy), however, points to an opportunity to further improve the model by either getting a more balanced data set and/or changing the training parameters to better train the model
---
### **Credits**
#### Prepared by Luis Torres 
#### [LUTOV001](https://github.com/LUTOV001)
#### June 2023