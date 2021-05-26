# Machine-Learning Model Selection for classification predictive modelling problem
I am a beginner in machine learning.This is a practice project  which is created for practising machine learning Model Selection for classification predictive modelling problem.
The dataset used is famous Pima Indians onset of diabetes dataset  which is used  to predict  class label for Diabetic disorder  from a given set of input observations.
The numerical data is standarized using standard  scaler
By Checking the counter of  output variable, data  seems to be slight imbalanced. So we have not applied imbalance corretion methods.
Now different algoritms(including some of the ensemble algorithms) are spot  checked  with test harness include KFold Cross Validation and model accuracy as the evaluation metric.
Evaluation is done by creation of three lists (models,results and names) using cross validation score  algorithm.
The algorithms to be spot checked  are appended to the models list and the results and model names are appended to results and names list respectively using for loop.
By seeing the results , it is evident to use Logistic regression algorithm as it has best accuracy.
Now  we would improve the accuracy of the Logistic regression algorithm using grid search and random search algorithm tuning methods.
Results  of the grid search shows  that best solver is newtom-cg  or saga.
Parameter C is sampled using uniform sampling method from scipy.stats.distributions for random search algorithm tuning method.
Morelver Solver Saga and newton-cg has similar results in grid search, we are using solver saga as it can be tested with both L1 and L2 penalty.
Now  we have checked  that  whether  accuracy  was increased using  tuning on ensemble algorithm but the results are not as good as results of logistic regression.
After Seeing the results, we conclude to use the model logistic regresssion as it shows  best accuracy with C': 2.195254015709299, 'penalty': 'l1', and solver='Saga'.
The model is saved using pickle library. We loaded the model on test dataset which is created using train_test_split algorithm.
