Bagging and Boosting are both [[ensemble learning]] techniques used to improve the performance of weak models by combining a number of them together. 
## Bagging (Bootstrap Aggregating)
Bagging is a technique where multiple versions of the model are trained independently on different versions of the dataset, and the predictions are combined together. The versions of the dataset are created using [[bootstrapping]] (aka sampling with replacement). 

For regression tasks, the outputs are averages together, and for classification the majority vote is used. This essentially smooths out noise that would be present if a single model was used, and makes the ensemble model more robust. This works especially well for decision trees, which, when used by themselves, overfit easily. 
## Boosting
With boosting models are trained sequentially, where each model focuses on correcting errors made by the previous model in the chain. Each model is trained on the original data but puts emphasis on data points which had high residuals or were misclassified by previous models. 

This reduces bias by creating models that gradually improve as the correct each other's mistakes. [[AdaBoost]], [[Gradient Boosting]], and [[XGBoost]] are popular boosting algorithms.
