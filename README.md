# AntiFraud_Detection_AI
## Intro
This AI was a part of my second year Bachelor degree project.
The goal is to create an anti bank fraud system.
In the final project we will use a personal database so for the training we want a dataset without precomputed variables.
One advantage of a "blank" dataset is that it can be easily adapted with another dataset.
So we can create a new trainable and testable dataset with only basics transactions informations.

## Variables
Following some personnal research, we need to define some rules to detect a fraud, I selected 4 of them.
(N.B : it's a little bit simple, but the main goal is not to have a real bank anti fraud system)

- Moving Window/Average : It's the average number of transaction in a defined time period
- Standard deviation : Use to know waht are a "regular" transaction from a client
- Z-score : Evaluate the number of standard deviation average for a transaction
- Elapsed time : Time between the new transaction and the last one

## Models
After some sorting of all the columns in our dataset (new variables computed previously included), 4 models will be trained with those value.
The 4 models are :

- Random Forest Classifier
- K-nearest neighbors
- AdaBoost Classifier
- XGBoost
  
They are classifier models because we want to tell if a transaction is a fraud or not.
Some features engineering will be process to optimize each models and the last one will be selected.

## Sources
Datasheet : https://www.kaggle.com/datasets/dmirandaalves/predict-chargeback-frauds-payment

If you want some information about calculation and models :

- Moving window/average : https://en.wikipedia.org/wiki/Moving_average
- Standard deviation : https://www.mathsisfun.com/data/standard-deviation.html
- Z-score : https://datascience.eu/fr/mathematiques-et-statistiques/quest-ce-quun-z-score/

- Random Forest Classifier : https://en.wikipedia.org/wiki/Random_forest
- K-nearest neighbors : https://datascientest.com/knn
- Ada Boost : https://www.analyticsvidhya.com/blog/2021/09/adaboost-algorithm-a-complete-guide-for-beginners/
- XGBoost : https://www.datacorner.fr/xgboost/

For Information about how to use Models with python, I used this documentation :
- Classifiers from SciKit learn : https://scikit-learn.org/stable/modules/classes.html#module-sklearn.ensemble
- XGBoost : https://xgboost.readthedocs.io/en/stable/
