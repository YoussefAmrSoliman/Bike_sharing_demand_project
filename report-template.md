# Report: Predict Bike Sharing Demand with AutoGluon Solution
youssef amr

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
the output of the predictor was float and may have negative values that can't be submited so it must be changed

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
that season and weather are ints so we changed it to category and split datetime to month, day, hour to add more features

### How much better did your model preform after adding additional features and why do you think that is?
after adding features the score was 0.972113 and before was 0.914576

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
 after trying different hyper parameters the score was 0.970700 and before was 0.914576 
 
### If you were given more time with this dataset, where do you think you would spend more time?
no i think this scores are satisfaying

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
	model	        time_limit	presets	                auto_stack	score
1	initial	        600	        best_quality	        False	    1.80779
2	add_features	600	        best_quality	        False	    0.67326
3	hpo	            200	        optimize_for_deployment	True	    0.72248

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](cd0385-project-starter/project/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](cd0385-project-starter/project/model_test_score.png)

## Summary
the best score in evaluation was after adding features without changing hyperparameters
