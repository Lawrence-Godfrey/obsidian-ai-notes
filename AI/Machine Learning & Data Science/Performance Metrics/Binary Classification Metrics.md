For algorithms which produce binary classification outputs, like [[Logistic Regression]], creating a confusion matrix like the one below and calculating the precision, recall and F1 score can help evaluate the model.

![[Pasted image 20230828143833.png | center ]]

$$Accuracy = \frac{TP + TN}{TP + TN + FP + FN } = \frac{Correct Predictions}{Total Predictions}$$
$$Precision = \frac{TP}{TP + FP} = \frac{Correct Positive Predictions}{TotalPositivePredictions}$$
$$Recall = \frac{TP}{TP + FN} = \frac{CorrectPositivePredictions}{TotalPositiveLabels}$$
$$F1 = 2\frac{Recall \times Precision}{Recall + Precision}$$
