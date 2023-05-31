# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Myat Hsu Khaing

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The output of the predictor can't be negative so I need to adjust the negative counts of the predictor to zero.

### What was the top ranked model that performed?
TODO: Add your explanation

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
For Exploratory Data Analysis, I split the given dataset's datetime feature into hour, day, and month features. And then, the season and weather features are dtype in the given train and test dataset, so I convert these to category type so that the model take these as categories.

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional fetures, the prediction result is improved.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
