# Exercise 4 Classification of numbers and letters PART1:

For this exercise I chose a neural network with a fully connected hidden layer of 256 neurons and output layer equal to the 62 classes (alphanumeric).  The activation function for this multi-class classification task is softmax. The softmax function takes as input the rectified linear activation output from the hidden layer.  The required loss function was sparse_categorical_crossentropy. 

### Notes:
I was unable to figure out the display_metrics helper function for the full classification task. The multi-classification task required the use of a different sklearn function to generate the confusion matrices - multilabel_confusion_matrix.    


The second run of the neural network excluded six classes: 0, 1, O, I, 2, and Z.  Excluding these classes resulted in an increase in classification accuracy from 83.5% to 88%.  

### Notes:
Upon removal of the classes, I attempted to reduce the output layer to match the reduced number of classes.  However, this caused errors.  I was unable to discern why this occurred.

# Exercise 4 Classification of Numbers versus Letters using kf-crossvalidation PART2:

I used the sample code provided by Emily in the lecture 5 notes [lecture 4 cont'd](https://not.badmath.org/Lecture-5-Lecture-4-cont-d-6b685fdad4df4ec29f30c07f89597daf) to run the train-test-validate schema.  The models were RandomForest and XGBoost with hyperparameter tuning.  I used the test dataset from emnist with ~110k images to create the split.  Due to compute restrictions, I chose to perform the model showdown on 50% of the total images.  XGBoost with n-estimators = 150, max_depth = 7, and a learning rate of 0.2 was the strongest performer with an accuracy of ~87% on the validation holdout.  

[AlphaNumeric Classification](https://github.com/crapplersassistant/datasci_223/blob/exercise_4/exercises/4-classification/exercise.ipynb)