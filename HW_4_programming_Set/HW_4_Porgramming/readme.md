# Homework-4


In this assignment you will train logistic regression models using stochastic gradient descent to predict whether a human subject is viewing a picture or reading a sentence from their fMRI brain image data.


NOTE: It may take some time to run the experiments for this assignment, so we recommend that you start early. 

# Data

The data comes from the [starplus dataset](http://www.cs.cmu.edu/afs/cs.cmu.edu/project/theo-81/www/) (only the first subject). 

We provide starter code to read the provided matlab file into Python/Numpy arrays. 

The data for each trial consists of a sequence of brain images that we have flattened into a feature vector X. Your task is to train a classifier that outputs, y. The values of y are: {+1,-1}, which correspond to whether the subject was first shown a picture or a sentence during the trial. More details on the dataset are included in the comments of the starter code.

# Logistic Regression (10 points)

Recall the logistic regression algorithm that we have discussed in class. Your task will be to implement the logistic regression model with gradient descent by completing the associated sections in the starter code. You can run the provided code like so:

```
python linear_brain.py

```


(this assumes the data file is in the same directory)


First, implement the `SgdLogistic` function in the code. Notice the two helper functions that you should use: `LogisticGradient` and `LogisticLoss` 

`LogisticLoss` returns the total loss for a dataset given a specific set of weights. 
`LogisticGradient` returns the gradients for a given sample set.

Monitoring these two function will be useful for checking the convergence during gradient descent.

**You only need to add to the `SgdLogistic` function. The rest of the part is already done for you.** 


# Parameter Tuning (5 points)

After implementing the gradient update you are now ready to train your models. Your next task is to tune the learning rate. Try out several values of `lamda` including at least these: {0.1, 0.01, 0.001, 0.0001}. For each of these values report acccuracy on the development data and test data. Stop updating the gradient when the loss changes by less than 0.0001 or some number of maximum iterations is 100. Print out the loss at each iteration and turn in the output of your program in a separate file with your report.


# Bonus: Perceptron (5 points)

Modify the given Logistic Regression code and convert it to Perceptron learning. 



# Submission

Submit two file to Carmen: linear_brain.py and your report on parameter tuning.
Due: Friday, December 4, 11:59pm




