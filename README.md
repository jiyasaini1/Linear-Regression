# Linear-Regression

Linear regression is one of the easiest and most popular Machine Learning algorithms. It is a statistical method that is used for predictive analysis. Linear regression makes predictions for continuous/real or numeric variables such as sales, salary, age, product price, etc. Linear regression algorithm shows a linear relationship between a dependent (y) and one or more independent (y) variables, hence called as linear regression. Since linear regression shows the linear relationship, which means it finds how the value of the dependent variable is changing according to the value of the independent variable. The linear regression model provides a sloped straight line representing the relationship between the variables.

Simple Linear Regression:
If a single independent variable is used to predict the value of a numerical dependent variable, then such a Linear Regression algorithm is called Simple Linear Regression.
The following is the equation of a line of a simple linear regression model:

Y = mx + c

Y is the output feature (weight), m is the slope of the line, x is the input feature(height) and c is the intercept(weight is equal to c when height is 0 as shown below).

Y = m(0) + c = c

For different values of slope ‘m’ and constant ‘c’, we will get different lines as shown in the below graph.

Multiple Linear regression:
If more than one independent variable is used to predict the value of a numerical dependent variable, then such a Linear Regression algorithm is called Multiple Linear Regression.

Goal of Linear Regression: 
When working with linear regression, our main goal is to find the best fit line that means the error between predicted values and actual values should be minimized. The best fit line will have the least error.

The different values for weights or the coefficient of lines (a0, a1) gives a different line of regression, so we need to calculate the best values for a0 and a1 to find the best fit line, so to calculate this we use cost function.

A cost function is a mathematical function that is minimized to get the optimal values of slope ‘m’ and constant ‘c’. The cost function associated with linear regression is called the mean squared errors.
But There could be a huge number of combinations of ‘m’ and ‘c’, we cannot test them all.

Gradient Descent is the solution!

Gradient Descent is a technique to minimize the outcome of a function, which is the Mean squared error in the case of linear regression. Mathematically, the Gradient Descent works by calculating the partial derivative or slope corresponding to the current value of ‘m’ and ‘c’ as shown below. At each step, the value of both ‘m’ and ‘c’ get updated simultaneously. The values will keep on updating until we reach the value of ‘m’ and ‘c’ for which the cost function reaches the minimum value. 
If the slope is negative, then the value of ‘m’ increases by — learning rate * slope of ‘m’ and if the slope is positive, then the value of ‘m’ decreases by — learning rate * slope of ‘m’. The same is true for the value of c.


Assumptions we make in linear Reggression Model?
1. Linearity: The relationship between the dependent variable and the independent variables is assumed to be linear. This means that changes in the independent variables are associated with constant changes in the dependent variable.

2. Independence of errors: The errors, or residuals (the differences between observed and predicted values), are assumed to be independent of each other. This assumption implies that the error for one data point should not provide information about the error for another data point.

3. Homoscedasticity: The variance of the errors should be constant across all levels of the independent variables. In other words, the spread of residuals should be roughly the same across the entire range of predicted values.

4. Normality of errors: The errors are assumed to be normally distributed. This means that if you were to plot a histogram of the residuals, it should roughly resemble a bell-shaped curve.

5. No or little multicollinearity: In multiple linear regression (when there are multiple independent variables), the independent variables should not be highly correlated with each other. High multicollinearity can make it challenging to determine the individual effects of each independent variable.

6. No omitted variables bias: All relevant independent variables are included in the model. Omitting important variables can lead to biased parameter estimates.

I covered the basics of linear regression and gradient descent. To get hands-on linear regression I took an original dataset and apply the concepts that I have learned so far.

So, I have taken the Housing dataset which contains information about different houses in Boston. This data is accessible from the scikit-learn library. There are 506 samples and 13 feature variables present in this dataset. The objective is to predict the value of prices of the house using the given features.

First, I imported the Required Libraries.
Then I loaded the housing data from the scikit-learn library and read and understand the Data Description and Information.
Then I Converted the data from nd-array to data frame and added the feature names to the data.
Along with that, I added a price column to the Data.
Then I split the Data into Training and Testing Set and used scikit-learn’s LinearRegression to train our model on both the training and test sets.
After that I Plotted a Scatter graph to show the prediction results – ‘y_true’ value vs ‘y_pred’ value.
I evaluated the model using RMSE.
