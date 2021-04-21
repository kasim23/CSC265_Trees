# CSC265_Trees
You will apply tree, bagging, random forests, and boosting methods to the `Caravan` data set with 5,822 observations on 86 variables with a binary response variable. This is a classification problem.

The data contains 5,822 real customer records. Each record consists of 86 variables, containing socio-demographic data (variables 1-43) and product ownership (variables 44-86). The socio-demographic data is derived from zip codes. All customers living in areas with the same zip code have the same socio-demographic attributes. Variable 86 (Purchase) is the target/response variable, indicating whether the customer purchased a caravan insurance policy. Further information on the individual variables can be obtained at http://www.liacs.nl/~putten/library/cc2000/data.html

Fit the models on the training set (as the split shown at the bottom codes) and to evaluate their performance on the test set. Use the R lab codes. Feel free to use other packs (caret) and k-fold methods if you like.

Q1)
a. Create a training set consisting from random 4,000 observations (shuffled and then split) with the seed with `set.seed(99)` and a test set consisting of the remaining observations (see the code at the bottom). Do a brief EDA on the target variable. Overall, describe the data. Do you think a small number of predictors suffice to get the good results?

b. Fit a `logistic regression` to the training set with `Purchase` as the response and all the other variables as predictors. Report the $Accuracy$ score on the train and test data sets. Discuss if any issues observed.

c. Fit a `classification tree` model to the training set with `Purchase` as the response and all the other variables as predictors. Use cross-validation `cv.tree()` in order to determine the optimal level of tree complexity and prune the tree. Then, report the $Accuracy$ score on the train and test data sets. If the R command gives errors, make necessary fixes to run the model. Discuss if any issues observed.

d. Use the `bagging approach` on the classification trees model to the training set with `Purchase` as the response and all the other variables as predictors. Report the $Accuracy$ score on the train and test data sets. Discuss if any issues observed.

e. Use the `random forests` on the classification trees model to the training set with `Purchase` as the response and all the other variables as predictors. Find the optimal `mtry` and `ntree` with a sophisticated choice (no mandatory to make cross-validation, just try some) and report these. Report the $Accuracy$ score on the train and test data sets. Discuss if any issues observed.


f. Perform `boosting` on the training set with `Purchase` as the response and all the other variables as predictors. Find the optimal `shrinkage` value and `ntree` with a sophisticated choice (no mandatory to make cross-validation, just try some) and report these. Report the $Accuracy$ score on the train and test data sets. Discuss if any issues observed.

Q2)
a. Overall, compare the five models (parts b-f) in Question#1. Which one is the best  in terms of $Accuracy$? Also, what fraction of the people predicted to make a purchase do in fact make one for on each model (use test data, what is called this score?)? Accuracy or this score: which one do you prefer to evaluate models? 


b. Determine which four features/predictors are the most important in the `random forests` and `boosting` models fitted. Include graphs and comments. Are they same features? Why? 


c. Joe claimed that his model accuracy on the prediction for the same problem is 94%. Do you think this is a good model? Explain.
