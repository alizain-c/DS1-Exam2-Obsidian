Ridge and Lasso Regression are ML Techniques used when the data suffers from multicollinearity. It is a neat little way to ensure you don't overfit your training data. 

In simpler terms, its linear regression with an error term added to it. 
$$y = a + bx + e$$
$e$ = error term to regulate the variance
error term is the value needed to correct for a prediction error between the observed and predicted value

The assumptions of this regression is same as least squared regression except normality is not to be assumed. 
So, taking that into consideraion, we can remember that as LIE: 
- L: Linearity 
- I: Independent Variables
- E: Equal Variance or Homoscedasticity

It shrinks the value of coefficients but doesn’t reaches zero, which suggests no feature selection feature. 

#### What is the difference between Ridge and Lasso Regression? 

Both serve similar purpose, but a regression model using the **L1 regularization technique** is called Lasso Regression, while a model using **L2 regularization technique** is called Ridge Regression. The difference between these two is the term penalty.



