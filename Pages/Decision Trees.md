### What are Decision Trees?
In decision trees, the goal is to create a model that predicts the value of a target variable by learning simple decision rules inferred from the data features. Decision Trees have a hierarchical, tree structure, which consists of a root node, branches, internal nodes and leaf nodes.

![[Decision Tree Example.png]]

### How to build a Decision Tree? 

They are constructed using two kinds of elements: **nodes and branches**. At each node, one of the features of our data is evaluated in order to split the observations in the training process or to make an specific data point follow a certain path when making a prediction.
When they are being built decision trees are constructed by **_recursively_** evaluating different features and using at each node the feature that best splits the data. This will be explained in detail later.

![[Root Node]]

![[Internal Node]]

![[Leaf Node]]

### How are Decision Trees Pruned? 

To understand this, we need to first understand what is Pruning. Pruning is a data compression technique in Machine Learning Algorithms that reduces the size of decision trees by removing of the tree that are non-critical and redundant to classify instances.

### Advantages of Decision Trees: 
- Easy to construct/implement
- Extremely fast
- Models are easy to interpret for small sized trees
- Accuracy is comparable to other classification techniques for many simple data sets

### Disadvantages of Decision Trees:
- Computationally expensive to train
- Some decision trees can be overly complex
- Less expressivity: There may be concepts that are hard to learn with limited decision trees
- Easily prone to overfitting and hence low predictive accuracy

#### To avoid overfitting, we can use:  
* Pre-Pruning: 
	1. Minimum samples for leaf split - Determine minimum number of data points which need to be present at leaf nodes. If additional split at a leaf node would cause two branches where one branch would have less than minimum samples of nodes, then leaf cannot be split further.
	2. Maximum Depth - Setting maximum allows us to determine how shallow/deep a tree can be. Shallower trees generalize better but will be less accurate. Deeper trees will be more accurate on training data but will generalize worse (OVERFIT)
* Post-Pruning: Approach that corrects tree after it has been fitted to training dataset. Algorithm removes starts at leaf nodes and remove branches which after removal will not affect tree accuracy on dataset. Allows us to preserve high performance while lowering complexity (Less branches and splits).
* Ensemble Methods: Random forest. Ensemble methods combine multiple trees into an ensemble algorithm. The ensemble uses tree ‘voting’ as a mechanism to determine the true answer.
* Boosted Decision Trees: Boosted decision trees correct the overfitting by using the standard machine learning method of boosting. Build shallow decision trees and with each iteration, build a new decision tree onto the data partition that had the worst splitting metric.

As mentioned previously, decision trees are built by recursively splitting our training samples using the features from the data that work best for the specific task. This is done by evaluating certain metrics, like the **_Gini index_** or the **_Entropy_** for categorical decision trees, or the **_Residual or Mean Squared Error_** for regression trees. Since the focus of this exam is on Logistic Regression (Classification), we will focus on Entropy and Gini. 

### Entropy & Information Gain:
These are ways to measure impurity. 
$$Entropy = \Sigma{p_jlog{_2}(p_j)}$$
The higher the information gain, the better the split.
$$Information\;Gain = Initial\;Entropy - Split\; Entropy$$
Entropy is very similar to what we did for Exam 1: 
![[EntropyQEx1.png]]
![[EntropyQEx1_2.png]]

#### Solving the review question: 
![[Entropy Review Q.png]]

### Gini Index: 
This is used to minimize the probability of misclassification in a decision tree.

$$Gini = 1 - \Sigma p_j^2$$

#### Solving the review question: 
![[Gini Index Calculation Review Q.png]]

Calculating Impurity of a Leaf Node: 
![[Impurity Leaf Node Q.png]]

### Bias and Variance Tradeoff: 
There is usually a bias-variance tradeoff caused by model complexity. 

* Complex Models with many parameters usually have lower bias, but higher variance.
* On the other hand, simple models with few parameters have higher bias, but lower variance. 

The error caused is called the total expected error. 
$$Total\;Expected\;Error = (Bias)^2 + Variance$$

- If Variance strongly dominates, it means there is too much variation between models. This is called over-fitting.
- If Bias strongly dominates, then the models are not fitting the data well enough. This is called under-fitting.

![[Bias Var.png]]