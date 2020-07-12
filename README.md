#### __NOTE__ : 
I have identified few problems in my submitted notebook, and am going to work on those problems and implement the solutions in a new notebook. I will upload the new improved notebook once it gets completed. For this new notebook I will just use the train dataset and split it into training and testing set and compare the results of different classification algorithms.

# Novartis_Data_Science_Challenge

### Objective : To predict if the server will be hacked

#### Problem :
The problem is to predict the MULTIPLE_OFFENSE column which can take two values either 1 : Incident is a hack or 0 : Incident is not a hack.
The train data has 23,856 rows and 18 columns. The details of columns is as follows-
* __INCIDENT_ID__ : Unique identifier for a particular incident
* __DATE__ : Date on which the incident occured
* __X_1 - X_15__ : 15 parameters related to a particular incident
* __MULTIPLE_OFFENSE__ : *Target column (to be predicted) 

The dataset has a test set consisting of 15,903 different incidents and the related values for the columns INCIDENT_ID, DATE, X_1-X_15. We have to predict the MULTIPLE_OFFENSE column.

In order to achieve our objective we have to develop a machine learning model using appropriate algorithm.

#### __SOLUTION__ : 
Based on the problem and the data, it is clear that the problem is that of __CLASSIFICATION__ and we have to build a model using an appropriate classification algorithm. 

#### __server_hack_prediction.ipynb__ :
The .ipynb file contains the code used to achieve the objective. Different classification algorithms (Logistic Regression, SVC, K Nearest Neighbors, and Random Forest Classifier) have been used and the models have been trained on the complete train data to predict the outcome for MULTIPLE_OFFENSE column for the incidents of the test data. Grid Search CV has also been used to tune the Random Forest Classifier Model.

#### __pred_rand.csv__ : 
This is the submitted csv file containing two columns, INCIDENT_ID and MULTIPLE_OFFENSE(predicted). The predictions achieved using Random Forest Classifier was used for final submission.

#### __RESULT__ :
Based on the submission pred_rand.csv, a final score of __96.34747__ out of 100, was obtained.
