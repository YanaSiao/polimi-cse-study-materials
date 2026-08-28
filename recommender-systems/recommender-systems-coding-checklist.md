# Recommender Systems - Coding Implementation Exercises & Practice Problems

> ⚠️ **Notice:** This document is an open-source collection of python implementation exercises, code completion tasks, and evaluation challenges covering core recommender system algorithms. It is designed strictly for hands-on practice and skill verification.

---

# 📌 SECTION 1: Model Implementations & Fit Functions

## Matrix Factorization & Latent Factor Models

### Implementation Exercise: Asymmetric SVD Training Step
Complete the missing parts in the gradient descent optimization step for an **Asymmetric SVD recommendation model**.

**Context & Variables:**
- `n_users`, `n_items`: Dimensions of the User-Rating Matrix  
- `n_factors`: Rank of the latent representation space  
- `n_samples`: Number of training pairs sampled per epoch  
- `learning_rate`, `alpha`: Scalar optimization hyperparameters  
- `URM`: Sparse matrix in CSR format `(n_users, n_items)` containing explicit ratings  
- `X`, `Y`: Latent item factor matrices `(n_items, n_factors)` to be learned  

Complete the missing logic marked with `# TODO`:
1. Compute the model rating prediction for the selected user-item pair.
2. Apply the gradient updates for parameters `X` and `Y` including $L_2$ regularization.

```
for _ in range(nsamples):
    # Randomly pick sample
    user_id, item_id, true_rating = get_MSE_train_sample(URM_train)
    
    # Compute prediction
    user_profile = URM_train[user_id]
    
    # Calculate the predicted_rating for the sampled user and item
    predicted_rating = # TODO
    
    delta = true_rating - predicted_rating
    
    # Copy original value to avoid messing up simultaneous parameter updates
    Y_copy = Y.copy()
    X_copy = X.copy()
    
    # Perform gradient update step on model parameters including regularization
    X = # TODO 
    Y = # TODO
```

---

### Implementation Exercise: Matrix Factorization with BPR Loss
Complete the missing logic in the `fit()` method for a **Matrix Factorization model trained via Bayesian Personalized Ranking (BPR)** on implicit interaction logs.

**Context & Parameters:**
- `URM_train`: Sparse matrix `(n_users, n_items)` containing binary interactions  
- `num_factors`: Number of latent components  
- `learning_rate`: Step size for SGD updates  
- `regularization`: Penalty parameter for factor matrices  

Complete the missing assignments and gradient calculations marked with `# TODO`:

```
def fit(self, URM_train, num_factors, learning_rate, regularization):
    self.n_users, self.n_items = URM_train.shape
    
    # Initialize latent factors
    self.U =  # TODO: Initialize user latent factors matrix
    self.V =  # TODO: Initialize item latent factors matrix
    
    for epoch in range(self.epochs):
        user_id, pos_item_id, neg_item_id =  # TODO: Sample a (user, positive_item, negative_item) triplet
        
        x_uij = (
            np.dot(self.U[user_id], self.V[pos_item_id]) -
            np.dot(self.U[user_id], self.V[neg_item_id])
        )
        sigmoid = 1 / (1 + np.exp(-x_uij))
        
        # Gradient updates
        self.U[user_id] +=  # TODO: Update user vector
        self.V[pos_item_id] +=  # TODO: Update positive item vector
        self.V[neg_item_id] +=  # TODO: Update negative item vector
```

---

## Graph-Based & Linear Models

### Implementation Exercise: Graph Filter Collaborative Filtering (GF-CF)
Complete the matrix normalization and SVD steps within the training routine for **Graph Filter Collaborative Filtering (GF-CF)**.

**Context & Parameters:**
- `URM_train`: Sparse matrix `(n_users, n_items)` of implicit interactions  
- `num_factors`: Number of singular components to retain  
- `alpha`: Graph degree normalization parameter  

Complete the matrix construction and normalization lines marked with `# TODO`:

```
def fit(self, alpha, num_factors):
    D_I =  # TODO: Compute item degree array/matrix from URM_train
    D_U =  # TODO: Compute user degree array/matrix from URM_train
    
    D_I_inv = 1 / (self.D_I + 1e-6)
    D_U_inv = 1 / np.sqrt(np.array(URM_train.sum(axis=1))).squeeze() + 1e-6
    
    D_I = sp.diags(self.D_I)
    D_I_inv = sp.diags(D_I_inv)
    D_U_inv = sp.diags(D_U_inv)
    
    R_tilde =  # TODO: Construct the normalized adjacency/interaction matrix
    
    _, _, V = randomized_svd(
        R_tilde,
        n_components=num_factors,
        random_state=random_seed
    )
    
    D_I = sp.csr_matrix(D_I)
    D_I_inv = sp.csr_matrix(D_I_inv)
```

---

### Implementation Exercise: EASE_R (Embarrassingly Shallow Autoencoders)
Complete the closed-form weight matrix derivation inside the `fit()` method for an **EASE_R recommendation model**.

Complete the missing assignments marked with `# TODO`:

```
def fit(self, l2_norm=1e3, normalize_matrix=False):
    
    if normalize_matrix:
        self.URM = normalize(self.URM, norm='l2', axis=1)
        self.URM = sp.csr_matrix(self.URM)

    gram_matrix =  # TODO: Compute the item-item Gram matrix (X^T * X)

    diag_indices = np.diag_indices(gram_matrix.shape[0])
    gram_matrix[diag_indices] += l2_norm

    S_Num =  # TODO: Compute numerator matrix for closed-form weights
    S_Den =  # TODO: Compute diagonal denominator vector for normalization

    S = S_Num / S_Den
    S[diag_indices] = 0.0
```

---

# 📌 SECTION 2: Hybrid Systems, Recommendation Pipelines & Evaluation Metrics

## Hybrid Recommendation & Linear Combinations

### Implementation Exercise: PureSVD + Similarity Matrix Hybrid Pipeline
Consider an implicit interaction matrix `URM` of shape `(n_users, n_items)` and two pretrained base recommenders:
1. An item-item **similarity matrix** $S$ of shape `(n_items, n_items)`  
2. Latent factor components $U, \Sigma, V^T$ produced by **PureSVD**  

**Implementation Tasks:**
1. Implement a recommendation function `recommend(user_id, top_n=10, alpha=0.5)` that computes scoring profiles via a linear hybrid combination of the two models. The function must filter out all items already present in the user's training history.
2. Implement evaluation routines for **Precision@K** and **Recall@K** given ground-truth validation data.

---

### Implementation Exercise: SLIM + Two-Tower Hybrid with Grid Search Optimization
Consider an implicit interaction matrix `URM` of shape `(n_users, n_items)` and two base models:
1. A **SLIM** sparse item-item similarity matrix $S$ `(n_items, n_items)`  
2. Factor matrices $W$ and $H$ trained via a **Two-Tower Neural Network**  

**Implementation Tasks:**
1. Write a function `recommend(user_id, alpha, top_n=10)` that calculates combined prediction scores using linear weight $\alpha \in [0, 1]$:

Score = alpha * Score_SLIM + (1 - alpha) * Score_TwoTower

Ensure already interacted items receive a score of $-\infty$ or are excluded prior to selecting top-N elements.
3. Write an `evaluate(test_urm, alpha)` function that evaluates the hybrid system over a test split using **Mean Average Precision (MAP@10)**.
4. Write an `optimize(alpha_values, test_urm)` routine that performs a grid search over a sequence of $\alpha$ candidate values and returns the optimal hyperparameter $\alpha^*$ that maximizes MAP@10.

---

### Implementation Exercise: RP3beta + iALS Hybrid Pipeline
Consider an implicit interaction matrix `URM` of shape `(n_users, n_items)` and two model representations:
1. Graph-based similarity matrix $S$ generated by **RP3beta**  
2. User and item latent factor matrices $W, H$ generated by **iALS**  

**Implementation Tasks:**
1. Write a function generating top-N personalized recommendation vectors by linearly combining score arrays from both methods while excluding training interactions.
2. Write functions calculating **Precision@K** and **Recall@K** against hold-out test targets.

---

## Item-Based & Elastic SLIM Recommenders

### Implementation Exercise: Elastic SLIM Recommendation & Recall Metric
Consider an implicit `URM` matrix of shape `(n_users, n_items)` and an **Elastic Net SLIM** similarity matrix $S$ `(n_items, n_items)` optimized under $L_1$ and $L_2$ penalties.

**Implementation Tasks:**
1. Write a function `recommend(user_id, cutoff=10)` that computes predicted scores $\hat{R} = R \cdot S$ for a specific user, filters out items present in the user profile, and returns the top 10 item indices.
2. Write a function `evaluate_recall(test_urm, cutoff=10)` that measures the overall **Recall@K** metric across all test users.
