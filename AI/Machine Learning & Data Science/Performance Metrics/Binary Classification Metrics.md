For algorithms which produce binary classification outputs, like [[Logistic Regression]], creating a confusion matrix like the one below and calculating the precision, recall and F1 score can help evaluate the model.

![[Pasted image 20230828143833.png | center ]]

$$Accuracy = \frac{TP + TN}{TP + TN + FP + FN } = \frac{Correct Predictions}{Total Predictions}$$
Not good for skewed classes. If your model simply predicts everything as negative, and your positive class is small, your accuracy will still be high.

$$Precision = \frac{TP}{TP + FP} = \frac{Correct Positive Predictions}{TotalPositivePredictions}$$
Good for cases where false positives are more critical than false negatives. Basically, how good is your model at predicting positive cases.
Doesn't account for false negatives. I.e., doesn’t account for how many real positives the model is missing. So, even if the model misses a lot of actual positives, precision can still be high.

$$Recall = \frac{TP}{TP + FN} = \frac{CorrectPositivePredictions}{TotalPositiveLabels}$$
Useful in applications where false negatives are more critical than false positives. 
**Ignores false positives**: High recall can mean that the model is simply predicting a lot of positives, including many false positives, just to make sure it captures all true positives.
**Can lead to over-prediction**: Focusing on maximising recall might lead to a model that over-predicts positive cases, lowering precision.

$$F1 = 2\frac{Recall \times Precision}{Recall + Precision}$$
