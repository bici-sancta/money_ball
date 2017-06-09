# money_ball
example of ordinary logistic regression model building techniques


## 1. DATA EXPLORATION (40 points)

Describe the size and the variables in the MONEYBALL data set so that a manager can understand it. Consider that too much detail will cause a manager to lose interest while too little detail will make the manager consider that you aren’t doing your job. Some suggestions are given below. Please do NOT treat this as a check list of things to do to complete the assignment. You should have your own thoughts on what to tell the boss. These are just ideas.

a. Mean / Standard Deviation / Median
b. Bar Chart or Box Plot of the data
c. Is the data correlated to the target variable (or to other variables?)
d. Are any of the variables missing and need to be imputed “fixed”?


## 2. DATA PREPARATION (40 Points)

Describe how you have transformed the data by changing the original variables or creating new variables. If you did transform the data or create new variables, discuss why you did this. Here are some possible transformations.

a. Fix missing values (maybe with a Mean or Median value or use a decision tree)
b. Create flags to suggest if a variable was missing.
c. Transform data by putting it into buckets
d. Mathematical transforms such as log or square root
e. Combine variables (such as ratios or adding or multiplying) to create new variables

## 3. BUILD MODELS (40 Points)

Build at least three different LINEAR REGRESSION using different variables (or the same variables with different transformations). You may select the variables manually, use an approach such as Forward or Stepwise, use a different approach such as trees, or use a combination of techniques. Describe the techniques you used. If you manually selected a variable for inclusion into the model or exclusion into the model, indicate why this was done.

Discuss the coefficients in the model, do they make sense? For example, if a team hits a lot of Home Runs, it would be reasonably expected that such a team would win more games. However, if the coefficient is negative (suggesting that the team would lose more games), then that needs to be discussed. Are you keeping the model even though it is counter intuitive? Why? The boss needs to know.

## 4. SELECT MODELS (40 Points)

Decide on the criteria for selecting the “Best Model”. Will you use a metric such as Adjusted R-Square or AIC? Will you select a model with slightly worse performance if it makes more sense or is more parsimonious? Discuss why you selected your model.
STAND ALONE SCORING PROGRAM (40 POINTS)


### WRITE MODEL DEPLOYMENT CODE (40 Points)

Write a Stand Alone SAS data step that will score new data and predict the number of wins. The variable with the Predicted number of Wins should be named: 

P_TARGET_WINS

The SAS data step will need to include:

a. All the variable transformations such as fixing missing values
b. The regression formula

SCORED DATA FILE (50 POINTS)

SCORE THE MONEYBALL_TEST DATA SET (50 Points)

Use the stand alone program that you wrote in the previous section. Score the data file MONEYBALL_TEST. Create a file that has only TWO variables for each record: 

INDEX
P_TARGET_WINS

The first variable, INDEX, will allow me to match my grading key to your predicted value. If I cannot do this, you won’t get a grade. So please include this value. The second value, P_TARGET_WINS is the number of wins you believe the team will have in season based upon the data given to you.


Your values will be compared against …
A Perfect Model
Instructor’s Model
Performance of Other Students
Predict the Average value for everybody (MEAN)
Random Model
Worst Possible Model


If your model is not better than simply using an AVERAGE value, you will receive negative points
If your model is not better than generating a RANDOM value, you will receive a LOT of negative points
If your model is not better than the WORST model, then it will be a WHOLE LOT of negative points.

