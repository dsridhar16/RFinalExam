# RFinalExam
1. For the entire dataset, please perform the data cleaning as instructed before; namely, delete observations with missing value(s). Please report how many cases (namely, data points) are left after this step. Then please use the random seed 123 to divide the cleaned data into 75% training and 25% testing. 

2. Next, Please use the neuralnet package in R to build the various neural network classifiers. For this question, we shall NOT perform data standardization (normalization). 

Please first build the best classifier to predict the class label using the training data and the Perceptron model with (i) no hidden layer, (ii) the default loss function of “sse”, and (iii) the default activation function of “logistic”. Please plot the perceptron model obtained using the training data. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the testing data.

Next we shall build the best classifier to predict the class label using the training data and the Perceptron model with (i) no hidden layer, (ii) the loss function of “ce” (namely, cross-entropy, or the negative log likelihood), and (iii) the default activation function of “logistic”. Please plot the perceptron model obtained using the training data. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the testing data.

Now we shall build the best classifier to predict the class label using the training data and the Logistic Regression model. Please report the fitted logistic regression model obtained using the training data – and compare to the Perceptron models obtained in the plots of Question 2 (a) and Question 2 (b). Which Perceptron model better resembles the logistic regression model, and why? Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the testing data.

Now we shall build the best classifier to predict the class label using the training data and the Perceptron model with (i) one hidden layer with 3 neurons, (ii) the default loss function of “sse”, and (iii) the default activation function of “logistic”. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the testing data. Please compare the performance in test data to that of Question 2 (a).

Next we shall build the best classifier to predict the class label using the training data and the Perceptron model with (i) one hidden layer with 3 neurons, (ii) the loss function of “ce” (namely, cross-entropy, or the negative log likelihood), and (iii) the default activation function of “logistic”. Please plot the perceptron model obtained using the training data. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the testing data. Please compare the performance in test data to that of Question 2 (b).

Now we shall use the randomforest function in R to build the random forest classifiers. For this question, we shall NOT perform data standardization (normalization). 
  
Please first build the best random forest to predict the class label using the training data. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy using the out of bag (OOB) samples. 

Next please use this random forest to predict the class label in the testing data. Please add the predicted label for every test data point. (Please do not print this data set out! It will be used in Question 5 below.) Please compute the Confusion matrix and report the sensitivity, specificity and the overall accuracy for the testing data. 

Please plot the variables importance measures using 

MeanDecreaseAccuracy, which is the average decrease of model accuracy in predicting the outcome of the out-of-bag samples when a specific variable is excluded from the model.
MeanDecreaseGini, which is the average decrease in node impurity that results from splits over that variable. The Gini impurity index is only used for classification problem.

Please show the importance of each variable in percentage based on MeanDecreaseAccuracy.  


For this question, we shall use rpart to build the classification tree and rattle to plot the tree. For this question, we shall NOT perform data standardization (normalization).   
  
Please first build a fully grown tree using the training data, and draw the tree plot using rattle. Next please use this tree to predict class label in the testing data. Please compute the Confusion matrix and report the sensitivity, specificity, and the overall accuracy for the testing data. 

To make the tree more robust, we shall prune the fully grown tree using the training data with 10-fold cross-validation. Please (1) show the complexity plot, (2) report the best CP value, and (3) draw the pruned tree using rattle.   

Please use this optimal pruned tree to predict the class label in the testing data. Please add the predicted label for every test data point. (Please do not print this data set out! It will be used in Question 5 below.) Please compute the Confusion matrix and report the sensitivity, specificity and the overall accuracy for the testing data. 

Now, (a) please compare the predicted labels between the random forest and the optimal pruned tree, to see what percentage of test data points were classified consistently with each other, regardless of whether the classification was right or wrong. (b) Please compute what percentage of test data points were classified correctly, by both classification methods.   

Part II. Regression Analyses & Variable Selections with the Mystery Data
The Mystery.csv data contain 14 predictors and one continuous response variable y.  
Our goal is to establish a regression model predicting the response variable using the predictors – and in particular, using various modern and classical techniques to perform variable selection.  
 
Please perform data cleaning by checking whether there are any missing values and if so, please delete observations with missing values. Please report how many observations with missing values we have in our dataset. Please use the random seed 123 to divide the data into 75% training and 25% testing.  

Now we shall perform penalized regression analysis with three different methods. 
  
Please first find the best Ridge Regression model using the training data. Please (a) find the best λ value through cross-validation and display this value; (b) display the coefficients of the fitted model; and (c) make prediction on the testing data, plot the observed response variable on the x-axis, and the estimated response variable on the Y-axis, and report the RMSE and the Coefficient of Determination R2. 

Please first find the best LASSO model using the training data. Please (a) find the best λ value through cross-validation and display this value; (b) display the coefficients of the fitted model; and (c) make prediction on the testing data, plot the observed response variable on the x-axis, and the estimated response variable on the Y-axis, and report the RMSE and the Coefficient of Determination R2. 

Please first find the best Elastic Net model using the training data. Please (a) find the best tuning parameter values through cross-validation and display these values; (b) display the coefficients of the fitted model; and (c) make prediction on the testing data, plot the observed response variable on the x-axis, and the estimated response variable on the Y-axis, and report the RMSE and the Coefficient of Determination R2. 

Please discuss which penalized regression method is the best for the Mystery data, and why.

Now we shall perform variable selection using the best subset method, and the stepwise variable selection method. Please identify the best models (either the best subset model, or the best stepwise regression model) using the same training data as in Question 2 above, only. 

We shall use ‘y’ as the response variables, and there are a total of 14 regressors to choose from. First, please use the R function regsubsets() [leaps package] for best-subset variable selection to identify different best models of different sizes ranging from 1 to 5.
Please use the 5-fold cross-validation to select the best overall model from all 5 best subset models identified in part (a) above. Please write down the equation of this best overall model.
Please use the R function stepAIC() [MASS package] to identify the best model using the stepwise variable selection method. Please write down the equation of this best overall model.
Compare to Question 2, the penalized regression methods above, which variable selection method is the overall best, based on what criterion (or criteria) of your choice? Please perform this comparison using the same testing data as in Question 2 above. 
