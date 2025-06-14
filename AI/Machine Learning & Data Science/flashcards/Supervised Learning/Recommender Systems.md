#flashcards

What is a content-based recommender system?
?
A system that provides personalized recommendations by leveraging features of the items themselves and the interactions or preferences of users with those items.

How is a user's profile represented in content-based recommender systems?
?
Each user has a profile represented by a set of parameters denoted as \(\theta^j\).

What does \(r(i,j) = 1\) signify in the context of recommender systems?
?
It indicates that user \(j\) has rated item \(i\).

What is the prediction formula for a content-based recommender system?
?
The prediction can be made using the formula: \(p = (\theta^{j})^{T}(x^{i})\).

What is the objective of the cost function \(J(\theta^{j})\) in content-based recommender systems?
?
To minimize the error between predicted ratings and actual ratings for items that the user has rated.

What optimization method is commonly used to fit the parameters in content-based recommender systems?
?
Gradient Descent with regularization.

List one advantage and one disadvantage of content-based recommender systems.
?
Advantage: No Cold Start; Disadvantage: Limited Scope.

What is the main idea behind collaborative filtering?
?
The idea that users who have agreed in the past will likely agree again in the future.

What are the initial conditions for user parameters and item features in collaborative filtering?
?
They are initialized randomly.

Name an advantage and a disadvantage of collaborative filtering.
?
Advantage: Highly Personalized recommendations; Disadvantage: Cold Start issue.

Why doesn't collaborative filtering require feature engineering?
?
It focuses on user-item interactions instead of requiring item or user features.

What scalability issue does collaborative filtering face?
?
Calculating similarities can be computationally expensive for large datasets.

