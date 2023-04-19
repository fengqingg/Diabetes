# Diabetes Classification with R
This repository contains an R notebook (Diabetes_Classification.ipynb) that performs classification of diabetes using the Pima Indians Diabetes Dataset. The notebook utilizes machine learning algorithms to train a model to predict whether or not a person has diabetes based on certain medical predictor variables.


# Data Insights
To select features that are important for model prediction, NA values were dropped and multiple plots such as boxplot and barcharts were plotted of the different features. The aim is to determine if the feature are strong or weak in predicting the classification.
![image](https://user-images.githubusercontent.com/85885666/232962814-b8edb774-e2cc-492b-9e01-1e708e99b53b.png)
![image](https://user-images.githubusercontent.com/85885666/232963396-c50530bd-2869-4aa3-958d-58875766ed55.png)

The features are then categorized into different degree and only the medium and strong features are selected for classification.
| Degree of association |                  Variables                 |
|:---------------------:|:------------------------------------------:|
|          Weak         |                  Pressure                  |
|         Medium        | Pregnant, Triceps, Mass, Insulin, Pedigree |
|         Strong        |           Glucose, Age, G/I ratio          |

# Model Performance
|                | Logistic Regression | kNN Classification | Linear SVM | Polynomial SVM |
|:--------------:|:-------------------:|:------------------:|:----------:|:--------------:|
|    Accuracy    |         75%         |         77%        |     76%    |       76%      |
| False Positive |          86         |         94         |     87     |       90       |
|  True Positive |          16         |          9         |     15     |       12       |
| False Negative |          22         |         27         |     22     |       25       |
|  True Negative |          29         |         24         |     29     |       26       |

The final model selected is the Linear SVM model. This model is selected as the linear SVM has the lowest FN rate with the highest accuracy. FN classification will lead to undetected cases which defeats the purpose of the model to prevent future diabetes. As all the predictor variables are also quantitative, there is no categorical predictor affecting margin calculation. 

# Conclusion
There is a high class imbalance between positive and negative. Also, the small sample size causes high variance in accuracy which makes it difficult to evaluate the model. Finally, this findings can be extrapolated to the general population outside of Pima Indians.


# Requirements
To run the notebook, you will need to have R and the following packages installed:

<ol>
  <li>dplyr</li>
  <li>ggplot2</li>
  <li>tidyr</li>
  <li>caret</li>
</ol>
You can install these packages by running the following command in R:\
<code>
install.packages(c("dplyr", "ggplot2", "tidyr", "caret"))
</code>

# Usage
To use the notebook, you can simply open it in Jupyter and run each cell sequentially. The notebook is divided into several sections:

Introduction
Data Exploration
Data Cleaning and Preparation
Model Building and Training
Model Evaluation
The notebook contains detailed explanations of each step, as well as code snippets and visualizations to help you understand the process.

# Dataset
The Pima Indians Diabetes Dataset contains information on female patients at least 21 years old of Pima Indian heritage who live near Phoenix, Arizona. The dataset includes 768 instances with 8 medical predictor variables and 1 binary target variable (whether or not the patient has diabetes).

You can find the dataset at the following link: https://www.kaggle.com/uciml/pima-indians-diabetes-database

# License
The code in this repository is licensed under the MIT License. See LICENSE for more information.
