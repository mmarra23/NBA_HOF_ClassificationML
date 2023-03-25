# NBA_HOF_ClassificationML
NBA Hall of Fame Predictive Machine Learning Development

**Objective**

The goal of this project was to predict NBA players who will enter the Hall of Fame (HOF) Players from players who are currently playing or have Retired after 2018. The approach would try different classifiers and identify the most accurate models used in the prediction based on the Precision and ROC primarily. Note, the python code is attached above in this repository.

**Data Selection**

To conduct this project, a dataset from Kaggle was sourced and selected, NBA Hall of Fame Prediction Project: https://www.kaggle.com/code/iliaskydyraliev/nba-hall-of-fame-prediction-project/data

**Data Exploration & Analysis**

Conducted basic statistical analyses and reviews with the original data set such as:
* The dataset had 39 columns and 5023 rows.
* 36 numerical and 3 non-numerical variables.
* Distribution of Hall vs non-winners.
* Analysis of features like age, win share, and points scored of HOFer's vs non-HOFer's.

**Data Cleaning & Transformation**
* Add a binary column that would identify the Hall of Famer's in the dataset with a number 1.
* Used data from 1980 to 2018 as the model train/test.
* Feature Analysis and Final Input Data.
* Conducted Feature Analysis via the Univariate ANVOA method to find the top 20 features we should use within our machine learning model.
* Assessed those 18 features through Pair Plot and Correlation to find any collinearity. 
* Split the data into Train, Test, and Validation. 
* Further, split our training/test/validation into the target and predictor variables.
* Applied feature scaling using the StandardScaler function.

**Predictive Model Development & Analysis**

* Employed classification modelling to predict the probability of each player entering the HOF.
* Choose the top 3 classifiers for this predictive model: Random Forest, LGBM and XGBoost Boost. 
* Developed, Hyperparameter Tuned, and fitted the 3 models with the train/test/validation data sets.
* Reviewed the output of the predictions on the Test data. Along with the Precision and ROC values of each model.

**Conclusion**

The Random Forest Classifier with the following Hyperparameters: {'n_estimators': 200, 'max_features': 'auto', 'max_depth': 10, 'criterion': 'gini'} performed the best considering Precision and ROC performance KPIs.

Random Forest Classifier performance: 
* Precision: 0.9897
* ROC_AUC: 0.9678

![image](https://user-images.githubusercontent.com/89919659/227675210-81824ddc-da91-408f-99ff-fee951998af0.png)

Learning curve
* Plotted the learning curve for the training data based on Precision.
* Using the final selected ML model Random Forest with the hyperparameters stated above.
* The plot result shows the model performs well and does not show signs of over or underfitting.

![image](https://user-images.githubusercontent.com/89919659/227675275-6347dd0e-71d8-4b51-92f4-6c9135b47a7f.png)

The top 5 features that highly impacted the classification model were as follows:
* All-Star appearances
* Win Shares
* Points per game
* NBA 75 Team appearances
* All NBA appearances

![image](https://user-images.githubusercontent.com/89919659/227675332-c40c2f59-f136-48d6-83c0-c08e872cf84a.png)

Here is a sample of the ML classification output to predict the HOFers

![nbahof](https://user-images.githubusercontent.com/89919659/213784591-033f3ae8-241f-4c1f-a749-bc621bee7b41.PNG)
