### Content-Based Recommender Systems
Content-based recommender systems provide personalised recommendations by leveraging features of the items themselves, as well as the interactions or preferences of the users with those items.

Each user has a "profile", i.e., a set of parameters $\theta^j$ and each item has a feature vector $x^i$. Some users have rated some items. $r(i,j) = 1$ if user $j$ has rated item $i$. A prediction can then be made on item $i$ by user $j$: $$p = (\theta^{j})^{T}(x^{i})$$The intuition here is that $\theta^{j}$ has been learnt so that the features of the item which the user prefers are prioritised.

#### Optimisation Objective
To learn the parameters for each user, we want to minimise the cost function $$J(\theta^{j}) = \frac{1}{2}\sum\limits_{i:r(i,j)=1}((\theta^{j})^{T}(x^{i}) - y^{i,j})^2$$
I.e., go through all the items that the user has rated and sum the difference between our prediction and the actual rating. We would need to do this for each user. [[Gradient descent]] with regularisation can be used to fit the parameters for a particular user.

#### Advantages:
- **No Cold Start**: Content-based systems do not require other users to have interacted with an item to recommend it.
- **Personalised**: Recommendations are tailored to individual users based on their own behaviour.

#### Disadvantages:
- **Limited Scope**: Can only recommend items similar to those the user has already interacted with, potentially resulting in a lack of diversity.
- **Feature Engineering**: Requires meaningful feature representation of items, which can be challenging.

### Collaborative Filtering
Collaborative Filtering is one of the most commonly used techniques in recommender systems and focuses on finding patterns in user-item interactions rather than using feature-based representations of items or users. The main idea is that users who have agreed in the past tend to agree again in the future.

The idea is to initialise your user parameters and item features randomly, and then minimise the cost function with respect to both your parameters and features. The intuition behind this is that users who rate the same items similarly will probably continue to do so.

#### Advantages:
- **Highly Personalised**: Recommendations are tailored based on user interactions.
- **No Need for Feature Engineering**: Collaborative filtering doesn't require item or user features.

#### Disadvantages:
- **Cold Start**: Struggles to recommend items to new users or to recommend new items that have not been interacted with.
- **Scalability**: Calculating similarities can be computationally expensive for large datasets.
