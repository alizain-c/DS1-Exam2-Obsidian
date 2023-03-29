Logistic Regression is used when the dependent variable (target) is #categorical. We use a given set of independent variables here. 

For example: 
-   To predict whether an email is spam (1) or (0)
-   Whether the tumor is malignant (1) or not (0)

### How does it differ from linear regression? 
**Linear Regression** is used to predict the continuous dependent variable using a given set of independent variables. 

**[[Logistic Regression]]** is used to predict the categorical dependent variable (Binary: 0 or 1) using a given set of independent variables.

![[Image LinLogReg.png]]

### The Logistic Function (Sigmoid Curve): 
Instead of trying to predict Y, predict _P(Y=1)_, i.e, the probability of Y occuring. 
So, we can model P(Y=1) using a function that gives outputs between 0 and 1, hence, using Logistic Regression. When you graph this function you will get a Sigmoid curve that looks similar to: 

![[Sigmoid Curve.png]]

![[LogicticReg Formula.png]]

### Odds: 
Given some event with probability `p` of being 1, the odds of that event are given by: 
$${odds = \frac{p}{1-p}}$$
### Odds Ratio: 

![[OddsRatio1.png]]
![[OddsRatio2.png]]

### Logit: 
The logit is the natural log of the odds

![[Logit.png]]

$$logit(p) = ln(odds) = ln(\frac{p}{1-p}) $$
![[LogitEx.png]]

The log odds (logit) is assumed to be linearly related to the independent variable X. 
$$logit(p) = \beta_0 + \beta_1 X $$
Now, you just need to focus on solving an ordinary linear regression equation.
