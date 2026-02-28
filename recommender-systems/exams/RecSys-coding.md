# RECOMMENDER SYSTEMS - Coding  

## Example (officially released sample)

### Question 1 (2 points) 

Given the following snippet of the gradient descent training function for an **Asymmetric SVD recommendation model**, answer the questions concisely in the available space.

**The source code relies on the following variables:**

- *n users*: Number of users  
- *n items*: Number of items  
- *n factors*: Number of latent factors  
- *n samples*: Number of samples drawn for each epoch  
- *learning rate*, *alpha*: Scalar values  
- *URM*: CSR matrix of shape *(n users, n items)* containing explicit user-item ratings  

**Parameters that are used by the model and should be learned:**

- *X*, *Y*: Randomly initialized matrices of shape *(n items, n factors)*  

The implementation contains **two missing parts marked with `TODO`**: the first one requires computing the model prediction, the second one requires computing the model update. Fill them in a way that is consistent with the rest of the source code.

```python
for _ in range(n_samples):
    # Randomly pick sample
    user_id, item_id, true_rating = get_MSE_train_sample(URM_train)

    # Compute prediction
    user_profile = URM_train[user_id]

    # TODO: Complete this part to compute the predicted_rating for the given sample
    predicted_rating = 

    delta = true_rating - predicted_rating

    # Copy original value to avoid messing up the updates
    Y_copy = Y.copy()
    X_copy = X.copy()

    # TODO: Complete this part with the updates to the model parameters including the regularization
    X = 
    Y =
```
### Question 2 (3 points) 

Given a URM of shape (*n_users*, *n_items*) containing **implicit ratings** and two recommendation models: 

- A **similarity matrix** `S` of shape (*n_items*, *n_items*) 

- Matrices *U,* Σ*, V* obtained with **PureSVD**

(a) Write a function to compute the personalized recommendation list for a given *user_id* based on a hybrid of the two recommendation models computed as a linear combination. The recommendation list should be of length 10 and should not contain items the user has already interacted with. 

(b) Write two functions to compute **precision** and **recall** given a recommendation list, the test data and any other information you deem necessary. 

---

From here the questions are student-collected/ crowdsourced.

## 16/01/2026

### Question 1 (2 points) GF-CF

Given the following snippet of the `fit` function for a **Graph Filter Collaborative Filtering recommendation model**, answer the questions concisely in the available space.

**The implementation is based on graph-based normalization** and relies on the following data and parameters:

- **URM_train**: sparse matrix of shape *(n users, n items)* containing implicit user–item interactions  
- **num_factors**: number of latent factors  
- **alpha**: scalar hyperparameter controlling the normalization 

The implementation contains **three missing parts marked with `TODO`**. Fill them in a way that is consistent with the rest of the source code.

```python
def fit(self, alpha, num_factors):

    D_I =  # TODO
    D_U =  # TODO

    D_I_inv = 1 / (self.D_I + 1e-6)
    D_U_inv = 1 / np.sqrt(np.array(URM_train.sum(axis=1))).squeeze() + 1e-6

    D_I = sp.diags(self.D_I)
    D_I_inv = sp.diags(D_I_inv)
    D_U_inv = sp.diags(D_U_inv)

    R_tilde =  # TODO

    _, _, V = randomized_svd(
        R_tilde,
        n_components=num_factors,
        random_state=random_seed
    )

    D_I = sp.csr_matrix(D_I)
    D_I_inv = sp.csr_matrix(D_I_inv)
```
### Question 2 (3 points)

Given a URM of shape *(n_users, n_items)* containing **implicit ratings** and two recommendation models:

- a **SLIM item–item similarity matrix** `S` of shape *(n_items, n_items)*  
- the weight matrices `W` and `H` obtained from a **Two-Tower recommendation model**  
- any additional information you deem necessary

**Tasks:**

(a) Write a function `recommend()` that computes a **personalized recommendation list** for a given `user_id` by combining the predictions of the SLIM model and the Two-Tower model using a **linear hybrid strategy**.

- The hybrid score should be computed as a **linear combination controlled by the parameter `alpha`**, which determines the relative contribution of the two models.  
- The recommendation list must:  
  - Contain **10 items**  
  - **Exclude items the user has already interacted with**

(b) Write a function `evaluate()` that evaluates the recommender system defined in point (a) using the **Mean Average Precision (MAP)** metric given the test data and any other information you deem necessary.

- Generate recommendations using the `recommend()` function  
- Use a test set for evaluation  
- Compute and return the MAP score

(c) Write a function `optimize()` that, given the previously defined `recommend()` and `evaluate()` functions, searches over a **finite set of values of `alpha`** and returns the value of `alpha` that produces the **highest MAP score**


## 17/02/2026
### Question 1 (2 points)

Given the following snippet of the `fit` function for a **Matrix Factorization recommendation model trained with Bayesian Personalized Ranking (BPR) loss**, answer the questions concisely in the available space.

**The implementation is based on implicit feedback** and relies on the following data and parameters:

- **URM_train**: sparse matrix of shape *(n_users, n_items)* containing implicit user–item interactions  
- **num_factors**: number of latent factors  
- **learning_rate**: learning rate used for optimization  
- **regularization**: regularization coefficient  

The implementation contains **missing parts marked with `TODO`**.  
Fill them in a way that is consistent with the rest of the source code.

```python
def fit(self, URM_train, num_factors, learning_rate, regularization):

    self.n_users, self.n_items = URM_train.shape

    # Initialize latent factors
    self.U =  # TODO
    self.V =  # TODO

    for epoch in range(self.epochs):

        user_id, pos_item_id, neg_item_id =  # TODO

        x_uij = (
            np.dot(self.U[user_id], self.V[pos_item_id]) -
            np.dot(self.U[user_id], self.V[neg_item_id])
        )

        sigmoid = 1 / (1 + np.exp(-x_uij))

        # Gradient updates
        self.U[user_id] +=  # TODO
        self.V[pos_item_id] +=  # TODO
        self.V[neg_item_id] +=  # TODO
```
 
### Question 2 (3 points)

Given a URM of shape (n_users, n_items) containing implicit ratings and an **Elastic SLIM** recommendation model:

- an item–item similarity matrix S of shape (n_items, n_items)
- Elastic Net regularization with L1 and L2 penalties
- any additional information you deem necessary

(a) Write a function `recommend()` that computes a **personalized recommendation list** for a given user_id using the learned similarity matrix S.

- The recommendation list must:
    - contain **10 items**
    - exclude items the user has already interacted with

(b) Write a function `recall()` that evaluates the recommender system defined in point (a) using the **Recall** metric given the test data.
