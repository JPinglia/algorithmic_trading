# Overview of the Analysis

As a financial advisor working for a top financial advisory firm our goal is to help improve existing algorithms to help our firm maintain a competitive edge.

1) Test created algorithm with a support vector machine SVC model. 
2) Test and analyze model with a new machine learning classifier. 
3) Back test models and check for returns, model efficiency and effectiveness.

## Purpose of the analysis:
The purpose of this analysis is to help back test and improve an algorithm with machine learning models. 

We import a dataset containing data of OHLCV. Data is spliced, actual return analyzed and slow and long SMA's created. A trading signal is created with the SMA looking at crossover points and strategy returns determined. Data is split into a training and testing data sets. A three-month period is used as a training dataset. 

A SVM model is used to make signal predictions based on the training and testing data and a classification report is generated to evaluate model effectiveness. 

An alternative model is created with decision tree classifiers to improve model performance.

# Stage of modeling and analysis:
Original Model:
SVM - SVC model

![actual returns vs  the strategy returns - original](https://user-images.githubusercontent.com/95830866/161472493-5d9b4a81-6d42-49ec-b93a-fe67105dd99d.png)

Model Results:

![image_1_SVC_model](https://user-images.githubusercontent.com/95830866/161472514-c57aec9b-f334-49c5-88cb-1a607f368b16.PNG)

----------
Tweaked SMA

Short - 30 day,

Long - 200 day

![actual returns vs  the strategy returns - tweaked_SMA](https://user-images.githubusercontent.com/95830866/161475339-c25bbba7-12be-46d4-8b84-ac0bf2535f1f.png)
----------

Alternative Model:

Decision Tree Classifier

![actual returns vs  the strategy returns - Tree](https://user-images.githubusercontent.com/95830866/161472627-6f0f3b3e-ac36-4584-bc37-e906a0fafd7e.png)

Model Results:

![image_2_decision_tree](https://user-images.githubusercontent.com/95830866/161472639-c6e8f4f4-5d98-400a-9302-f8cbdfba99e5.PNG)


# Results
Result Analysis Model 1:
The strategy return was better with the SVM model up until 2016 and then diverged. The strategy return with the model was worse than the algorithms trading ability, without machine learning. We were more accurately able to predict the long side trades, with upwards of 96% accuracy. The short trades however were a dismal 4% correct prediction rate. The overall accuracy of the model was 55%. 

Tweaked SMA's did not change the outcome from the first analysis.

Result Analysis Model 2:
Using the decision tree classifier model, we find that our strategy returns increase greatly, vs the algorithm. Looking at the model classification report, we find the model is now bias towards predicting short trades with 89% with only 11% of long trades successfully predicted. The overall prediction accuracy is 45%. The mode however was able to perform better than the algorithm. 

# Summary
After using the decision tree classifier we were able to gain better trading result than the algorithm baseline strategy. That said however we found the SVC and the decision tree models to have a bias towards the long or short side. Both models were not good at determine both long and short trade directions/signals. 

Further steps need to be taken to improve modeling. 
1) use other models. 
2) increase the amount data provided to the models to train. 
3) tweak model SMA's to ones that maybe more fruitful.

