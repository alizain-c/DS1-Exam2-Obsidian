### What is a Confusion Matrix? 
A confusion matrix is a table that is often used to describe the performance of a classification model on a set of test data for which the true values are known.

| n = #    | Predicted: NO | Predicted: YES     |
| :----:      |    :----:   |   :---: |
| Actual: NO      | TN      | FP  |
| Actual: YES   | FN       | TP     |

![[True Positives (TP)]]

![[True Negatives (TN)]]

![[False Positives (FP)]]

![[False Negatives (FN)]]

### Precise:
Precise is used to determine the question, "when the model predicts yes, how often is it correct?" 

$$Precise = \frac{TP}{TP + FP}$$
### Recall:
Recall or Sensitivity is the ratio of <u>True Positives</u> to Total (Actual) Positives in the data. 

$$Recall = \frac{TP}{TP+FN}$$
### F1 Score: 
F1 Score is used when the classes are imbalanced and there is a serious downside to predicting False Negatives (FN). 

$$F1\;Score = \frac{2 * (Precision * Recall)}{(Precision + Recall)}$$
### Error Rate: 
Overall, how often is it wrong. This is also called Misclassification Rate.

$$Error Rate = \frac{FP+FN}{Total}$$
### Basic Example: 

![[Confusion Matrix Example.png]]