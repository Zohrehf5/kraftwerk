# Practical Application III- Comparing Classifiers

Our dataset comes from the UCI Machine Learning repository link  (dataset https://archive.ics.uci.edu/dataset/222/bank+marketing) . The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. The marketing campaigns were based on phone calls. The classification is to predict if the client will subscribe (yes/no) a term deposit (variable y). 

## Business Objective
The objective of this project is to compare different classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines) using the bank marketing dataset from the UCI Machine Learning Repository. The goal is to determine the most accurate and reliable model for predicting the success of a marketing campaign for a bank.

## Pre-requisite of Comparison
To compare the performance of classifiers, we can follow these steps:
1.	Data review: 
2.	Data Preprocessing: Convert categorical variables to numerical (one-hot encoding or label encoding).
3.	Train-test Split: Split the dataset into training and testing sets.
4.	Model Training: Train the following classifiers:
    o	Baseline
    o	Logistic Regression Basic
    o	K-Nearest Neighbors
    o	Logistic Regression
    o	Decision Trees
    o	Support Vector Machines
5.	Performance Comparison: Compare the performance of the classifiers using metrics such as Train Score, Test Score and Average Fit time. 
6.	Improve the Results:
  •	Scaling and Normalization
  •	More feature engineering and exploration: following features can be dropped due to their low correlation with the target variable: 
                 - Age, marital, housing, job, day_of_week, loan, month, campaign, default, contact
  •	Hyperparameter tuning and grid search. 

## Key Highlights
•	Logistic Regression and KNN models perform the best in terms of Test and Train accuracy. 
•	KNN model performs best in training time (0.003 Seconds).
•	SVM model (SVC classifier) has the highest training time and is computationally expensive.
•	Bank Marketing dataset is impbalanced because distribution is not similar within dataset.
•	The highest positive correlation between numerical independent variables is between "emp.var.rate" and "euribor3m" with a value of 0.97.
•	The highest negative correlation between numerical independent variables is between "pdays" and "previous" with a value of -0.59.
•	The "Day_of_Week" feature has a similar success rate among all categorical values, so it is not an important feature for the given model dataset.
•	The "nr.employed" & "euribor3m" are higher importance features since they have higher influence towards model predictions.
•	The "month", "cons.price.idx" and "duration" features have higher coefficient, and they contribute higher towards predicting the target variable.
•	Overall, the Logistic Regression model is the best performing model among all four models followed by KNN model.

## Next steps and Recommendations
•	Evaluate and identify non-important categorical features in a group (with other feature variable) rather than single to determine whether there exists combination of categorical features which can be discarded.
•	Continue to add samples from new marketing campaign and evaluate the different classifier models.
•	Imbalanced dataset: Since the bank marketing dataset is imbalanced, consider using techniques such as resampling, SMOTE, undersampling and class weighting are good strategies for improving performance on imbalanced datasets.
•	Training time and computational expense: Given that the SVM model (SVC classifier) has the highest training time and is computationally expensive, consider optimizing the model or exploring alternative models that can provide similar performance with lower training time. This can be mitigated by using more efficient kernels or simplifying the feature set.
•	Correlation analysis: Take note of the highest positive correlation between "emp.var.rate" and "euribor3m" and the highest negative correlation between "pdays" and "previous". These insights can help in understanding the relationships between variables and potentially identifying multicollinearity issues. We might consider using PCA to combine highly correlated features or regularization techniques like Lasso or Ridge.
•	For Decision Tree, trying ensemble methods like Random Forest or Gradient Boosting could yield even better results by reducing overfitting and improving generalization.
•	We can tune KNN n_neighbors in combination with other distance metrics (e.g., weights = 'distance') to improve performance.

## Repository Structure
1.	data/bank-additional-full.csv: Contains dataset used in the analysis.
   https://github.com/Zohrehf5/kraftwerk/blob/comparing_Classifiers/comparing_classifiers/data/bank-additional-full.csv
2.	data/bank-additional-names.txt: Contains the information about the dataset
   https://github.com/Zohrehf5/kraftwerk/blob/comparing_Classifiers/comparing_classifiers/data/bank-additional-names.txt
3.	Practical Application_III_Comparing Classifiers.ipynb: Contains the Jupyter Notebook with detailed code including comments and analysis.
   https://github.com/Zohrehf5/kraftwerk/blob/comparing_Classifiers/comparing_classifiers/prompt_III.ipynb
4.	README.md: Summary report of findings and next steps
   
5.	Practical Application 3.docx : Detail report of  Classifiers Comparison between different models and key highlights

