# **UCB FinTech Bootcamp Module 14 Challenge**
# *Algorithmic Trading with Machine Learning*
## **Introduction**
### The Bootcamp Module 14 Challenge - Algorithmic Trading with Machine Learning (ML) requires the preparation of a model to predict the performance (successful/unsuccessful) of venture capital applicants. The data set contains  non-numerical features which need to be transformed to numerical values for proper analysis. The prediction Machine Learning model will use Neural Networks and their metrics for the evaluation of the model effectiveness (e.g. loss and accuracy). After evaluation of the first model is completed (e.g. data prepared, model defined, trained and tested) and saved for later use, 3 additional alternative models are to be prepared and saved for comparison purposes
---
## **Goals and Objectives**
### *Part I.*  : Load and prepare the data for the model ensuring value types are set as per ML modeling standards (e.g.numerical, scaled values) based on the provided data source file in the Resources folder (applicants_data.csv)
### *Part II.*  : Compile and evaluate the perormance of the model in predicting the applicant Status (e.g 'Is_Successful' column).
### *Part III.* : Save the model as an h5 file in the Resources folder for future use/reference.
### *Part IV.* : Optimize the model: Repeat steps above for Alternative models 1-3 with the goal of improving the model's performance (e.g. reduce loss, increase accuracy)
---
## **Technologies and Tools**
### The following list includes the main technologies and tools using during the preparation and deployment of the solution:
### 1. *Python* - Programming language used to code the solution. Version 3.7.13 was used. Required libraries and frames listed in the Installation section below
### 2. *GitHub* - Reposotory for code deployment, version management and documentation of the presented solution
### 3. *Jupyter Labs* - IDE tool for coding, code testing/debugging and solution documentation. Version V3.4.4 was used
### 4. *Git Bash console* - Local console used to test the coded solution and sync wiht GitHub Version 2.40.0.windows.1 was utilized
### 5. *Slack* - Collaboration tool to communicate and brainstorm with other FinTech Bootcamp participants
### 6. *Operative System* - This solution was prepared in a PC running Windows 11 v H22
### For additional details, please refer to the watermark output at the bottom of the ***venture_funding_with_deep_learning-V2.ipynb*** Jupyter Notebook
---
## **Installation Guide**

### 1. [tensorflow](https://www.tensorflow.org/install) : TensorFlow is an open-source machine learning framework developed by Google. It provides a comprehensive set of tools, libraries, and resources for building and deploying machine learning models. To install, follow these steps:
#### 1.1. Open the GitBash terminal
#### 1.2 Type the following command and press Enter:
```python 
pip install tensorflow==<version>
```
##### *Note* : Replace 'version' with the desired version number, such as 2.6.0.
### 2. [keras](https://keras.io//) : Keras is an open-source deep learning library written in Python. It provides a user-friendly and modular interface for building and training deep neural networks. Keras is also tightly integrated with TensorFlow, which provides additional resources and capabilities. To install the library, follow these instructions:
#### 2.1. Open the GitBash terminal
#### 2.2 Type the following command and press Enter:
```python 
pip install keras
```
##### *Note* : Starting from TensorFlow version 2.4, Keras is included as part of the TensorFlow library, so installing TensorFlow automatically installs Keras as well.
### 3. [sklearn](https://scikit-learn.org/) : scikit-learn, also known as sklearn, is a popular open-source machine learning library for Python. It provides a wide range of machine learning algorithms, tools, and utilities for tasks such as classification, regression, clustering, dimensionality reduction, model selection, and preprocessing of data. To install, follow these steps:
#### 3.1. Open the GitBash terminal
#### 3.2 Type the following command and press Enter:
```python 
pip install scitkit-learn
```
---
## **Solution Structure**

### The **[13.NNetworks4Funding](https://github.com/LUTOV001/13.NNetworks4Funding)** repository in GitHub contains the solution components. The repository consists of the following folders and contents as described below:
 
###   *1. Resources :* Contains the .csv file with the venture capital applicant data which serve as the basis for the analysis and predictions. Additionally, it is in this folder that the Neural network models are saved as .h5 files for future reference/use
###   *2. gitignore :* Instructions for which files/file types to exclude from the sync process between GitHub and the local environment.
###   *3. README.md :* The present file containing this outline of the challenge and its components.
###   *4. venture_funding_with_deep_learning-V2.ipynb :* This is the Jupyter Notebook with the code for the core challenge solution, analysis and neural netwokr models.
###  
---
## **User Instructions**
### 1. Launch the Jupyter Lab from the GitBash terminal using the following command line:
```python 
jupyter lab
```
### 2. From the Jupyter Lab terminal, navigate to the location of the ***venture_funding_with_deep_learning-V2.ipynb*** notebook and open it
### 3. Reset the Kernel and
### 4. Run the steps from the top and in sequence verifying the results as per the comments in the notebook, including outputs on the screen such as dataframe listing/on screen printing and other on screen outputs such as model summaries and evaluation statistics. Also review the Resources folder to verify the .h5 files for each model have been saved.
####
---
## **Credits**

### Prepared by Luis Torres 
### [LUTOV001](https://github.com/LUTOV001)
### June 2023
