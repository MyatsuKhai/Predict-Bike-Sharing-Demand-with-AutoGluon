# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Myat Hsu Khaing

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The output of the predictor can't be negative so I need to adjust the negative counts of the predictor to zero.

### What was the top ranked model that performed?
The top ranked model is Weighted_Ensemble L_3 with -50.872112 score_val.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
For Exploratory Data Analysis, I split the given dataset's datetime feature into hour, day, and month features. And then, the season and weather features are dtype in the given train and test dataset, so I convert these to category type so that the model take these as categories.

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional fetures, the prediction result is improved since the root_mean_square_error (RMSE) in Kaggle competition was decreased from 1.79095 to 0.61633. I think that is the power of EDA: adding more features and the categorized data make the model to learn better the relation between features and target.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After trying to modify the hyperparameter configuration on the LightGBM model, the model's RMSE is increased but the score regarding with the Kaggle is improved. I still need to fix the model to reduce RMSE.

### If you were given more time with this dataset, where do you think you would spend more time?
If I were given more time with this dataset, I would spend more time in EDA to give the model more important features and I will explore more about hyperparameter tuning with customized different models, on the model which is advanced with more features.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|time_limit|Preset|num_trials|num_folds||score|
|--|--|--|--|--|--|
|initial|600|best_quality|default|default||1.79095|
|add_features|800|best_quality|default|default||0.61633|
|hpo-LightGBM Model|900|best_quality|8|14||0.56658|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
To summarize the project, the prediction model is trained with AutoGluon on AmazonSageMaker to predict the bike sharing demand. The dataset is taken from Kaggle and the results are submitted to kaggle competition to improve the scores. Firstly, model training take place with the original dataset's features and got a first raw result. And then, exploratory data analysis (EDA) is performed on the raw given dataset. After training with the optimized features, the result improved drastically. Finally, Hyperparameter tuning is implemented after EDA. Tuning some parameters of LightGBM Model, improve the model performance. But, I will have to explore more about hyperparameter tuning on many models because, the RMSE score is increased compared with the result of training after EDA. 
