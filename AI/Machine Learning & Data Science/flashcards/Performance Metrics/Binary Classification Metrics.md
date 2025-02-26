#flashcards

What is the definition of accuracy in the context of binary classification?
?
Accuracy = (TP + TN) / (TP + TN + FP + FN), which represents the proportion of correct predictions out of total predictions.

Why is accuracy not a good metric for skewed classes in binary classification?
?
Because if a model predicts everything as negative and the positive class is small, accuracy can still be high despite poor performance in identifying the minority class.

What does precision measure in binary classification?
?
Precision = TP / (TP + FP), it measures the proportion of true positive predictions among all positive predictions made by the model.

In which scenario is precision particularly important?
?
Precision is important when false positives are more critical than false negatives, as it indicates how reliable the positive predictions are.

What does recall measure in binary classification?
?
Recall = TP / (TP + FN), it measures the proportion of true positive predictions among all actual positive cases.

When is recall a critical metric?
?
Recall is critical in scenarios where false negatives are more detrimental than false positives, as it emphasizes capturing as many true positives as possible.

What is the formula for the F1 score?
?
F1 = 2 * (Recall * Precision) / (Recall + Precision), which is the harmonic mean of precision and recall.

What does a high recall value indicate about a model's predictions?
?
A high recall may indicate that the model is capturing most of the true positives, but it might also lead to over-prediction, including many false positives.

What is a potential downside of focusing solely on maximizing recall?
?
Focusing solely on recall may result in a model that over-predicts positive cases, which can significantly lower precision.

How do precision and recall complement each other in evaluating a model's performance?
?
Precision focuses on the accuracy of positive predictions, while recall focuses on the model's ability to identify all true positives, making a balance between them crucial for model evaluation.

