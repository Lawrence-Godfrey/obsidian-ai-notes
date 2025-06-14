#flashcards

What does the Mean Absolute Error (MAE) represent in linear regression?
?
MAE represents the average of the absolute differences between the predicted and actual values, giving a linear penalty to the prediction errors.

How is Mean Squared Error (MSE) calculated?
?
MSE is calculated as the average of the squared differences between the predicted and actual values: $$\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$$.

What is the formula for Root Mean Squared Error (RMSE)?
?
RMSE is calculated as the square root of the Mean Squared Error: $$\text{RMSE} = \sqrt{\text{MSE}} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}$$.

What does an R-squared value of 1 indicate?
?
An R-squared value of 1 indicates that the regression predictions perfectly fit the data.

What is the difference between MAE and MSE in terms of penalty to prediction errors?
?
MAE gives a linear penalty to prediction errors, while MSE gives a quadratic penalty.

What does R-squared measure in a linear regression model?
?
R-squared measures how well the regression predictions approximate the actual data points.

What are the components needed to calculate R-squared?
?
To calculate R-squared, you need the residual sum of squares (SS_res) and the total sum of squares (SS_tot).

Why might one choose RMSE over MSE or MAE as an evaluation metric?
?
RMSE is in the same units as the response variable, which can make it easier to interpret.

What disadvantage does MSE have compared to MAE?
?
MSE is more sensitive to outliers than MAE due to its quadratic penalty on errors.

When might you prefer to use MAE as a model evaluation metric?
?
You might prefer MAE when you want a metric that is less sensitive to outliers and provides a clear interpretation of average error.

