# Recommender Systems - Conceptual Study Guide & Topic Checklist

> **Notice:** This document is a student-compiled learning checklist and theoretical self-assessment guide. It does not contain official exam questions or copyrighted course materials. Use it to track your study progress and test your mastery of key concepts.

# PART 1: STANDARD THEORY EXAM CHECKLIST

## 📌 1. Introduction to Recommender Systems & Taxonomy

### General Taxonomy
- [ ] **Personalized vs. Non-Personalized:** Articulate the fundamental operational differences between personalized and non-personalized algorithms. Provide a concrete algorithm example for each category and justify its classification.
- [ ] **Model-Based vs. Memory-Based:** Compare model-based and memory-based paradigms. Explain how data structures and computation times differ between them, providing clear examples for each.
- [ ] **Implicit vs. Explicit Feedback:** Detail the trade-offs between implicit interaction logs and explicit rating matrices. Identify algorithms tailored specifically for each data type and explain their underlying design choices.

### Multi-Stage Recommendation Architectures
- [ ] **Multi-Stage Pipelines:** Explain the architectural layout of multi-stage recommenders (e.g., candidate generation/retrieval vs. candidate ranking/re-ranking) and state the core purpose of each stage.
- [ ] **Production Trade-offs:** Analyze why multi-stage systems are standard in large-scale production, specifically focusing on conflicting operational requirements (e.g., latency constraints vs. model complexity).

### Sequence-Aware & Recurrent Systems
- [ ] **Sequence-Aware Modeling:** Define the core objectives of sequence-aware recommendation. Explain how Recurrent Neural Networks (RNNs) model sequential user behavior and write down the fundamental layer transition equations.

## 📌 2. Non-Personalized Recommenders

### Global Effects & Baseline Biases
- [ ] **Best-Rated Baselines & Shrinkage:** Explain how top-rated/best-rated recommenders function, identify their vulnerability to small sample sizes, and demonstrate how a shrink term mathematically stabilizes baseline predictions.

## 📌 3. Evaluation

### Evaluation Metrics & Trade-offs
- [ ] **Metric Categorization:** Distinguish between error-based metrics (e.g., RMSE, MAE), classification metrics (e.g., Precision, Recall), and ranking-based metrics (e.g., MAP, NDCG). State their formal mathematical definitions and primary use cases.
- [ ] **Beyond-Accuracy Metrics:** Define beyond-accuracy evaluation properties (e.g., novelty, coverage, diversity) and explain why optimizing solely for accuracy can degrade user experience.
- [ ] **Precision-Recall Dynamics:** Analyze the Precision-Recall curve, contrasting ideal theoretical performance against typical practical behavior in top-$N$ recommendation.

## 📌 4. Collaborative Filtering (CF)

### User-Based Collaborative Filtering
- [ ] **User-User Prediction Dynamics:** Master the core logic of User-Based CF. Write the mathematical prediction formulas for explicit User-Rating Matrices (URM) using similarity matrix $S$, both with and without explicit user bias correction.
- [ ] **Similarity Measures:**
  - Write the formula for **Cosine Similarity** between interaction vectors.
  - Write the formula for **Pearson Correlation Coefficient** and explain why and when mean-centering makes it superior to standard Cosine Similarity.
- [ ] **Implicit Adaptation & Top-$N$ Simplifications:** Explain how the prediction equation simplifies when transitioning from explicit ratings to implicit binary interactions for top-$N$ ranking tasks.
- [ ] **Regularization via Shrinkage:** Explain the purpose of the shrink term in similarity computation and how it penalizes low co-occurrence counts.
- [ ] **Neighborhood Selection ($k$-NN):** Define the $k$-Nearest Neighbors constraint, explain how restricting neighborhood size improves recommendation quality and computation speed, and show how the prediction equations update accordingly.

### Sparse Linear Methods (SLIM)
- [ ] **SLIM Optimization & Formulation:** Explain the Sparse Linear Methods framework, detail its prediction optimization objective (including $L_1$/$L_2$ regularization and non-negativity/zero-diagonal constraints), and explain how parameters are learned.

## 📌 5. Dimensionality Reduction & Matrix Factorization

### Bayesian Personalized Ranking (BPR)
- [ ] **BPR Assumptions & Pairwise Optimization:** Describe the core philosophy of BPR, highlighting its pairwise preference assumptions ($i \succ_u j$) over implicit data.
- [ ] **Loss Function Formulation:** Write the generic BPR optimization loss function using arbitrary predicted scoring functions $\hat{r}_{ui}$ and $\hat{r}_{uj}$.
- [ ] **Gradient Derivations:**
  - Derive the parameter gradient updates for a standard unconstrained prediction $\hat{r}_{ui}$.
  - Formally derive the exact gradient update step for user and item latent factor matrices when applying BPR to Matrix Factorization models.

## 📌 6. Hybrid Recommenders

### Factorization Machines (FM)
- [ ] **Input Data Structuring:** Describe how tabular data, user IDs, item IDs, and contextual features are encoded into sparse feature vectors for Factorization Machines.
- [ ] **Model Equation & Parameter Identification:** Write the 2-way Factorization Machine prediction equation, explicitly identifying global bias, 1st-order linear weights, and 2nd-order factorized interaction parameters.
- [ ] **Learning & Optimization:** Detail how parameters are optimized via Stochastic Gradient Descent (SGD) or Alternating Least Squares (ALS).
- [ ] **Relationship to Classical Matrix Factorization:** Prove mathematically how a 2-way FM reduces directly to Matrix Factorization + Global Effects when only user and item one-hot indicators are present.
- [ ] **Context-Aware Extensions:** Explain how side information and arbitrary environmental context are seamlessly incorporated into the FM feature matrix.

# PART 2: ADVANCED THEORY CHECKLIST

> **Note:** The topics below cover advanced modules and are tested specifically in the **Advanced Exam** (as well as comprehensive theory evaluations).

## 📌 7. Advanced Topics: Graph-Based Recommenders

### Graph Representations of Collaborative Data
- [ ] **Graph & Matrix Structuring:** Under implicit feedback scenarios, describe how user-item interactions are transformed into a bipartite graph structure. Write the exact form of the corresponding adjacency matrix.
- [ ] **Transition Probabilities:** Detail the mathematical construction of the row-stochastic or column-stochastic transition probability matrix from the adjacency graph.
- [ ] **Random Walks & Personalization:** Explain how the number of steps (hops) in a random walk impacts recommendation localization versus global convergence.
- [ ] **Heterogeneous Graph Extensions:** Explain how to extend bipartite graphs into tripartite or multi-layer graphs to incorporate user and item side attributes.

### Graph Random Walk Algorithms (P3, RP3beta)
- [ ] **Structural Relational Logic:** Describe how random walk paths (e.g., $U \to I \to U \to I$) inherently relate to Item-Based Collaborative Filtering similarity matrices.
- [ ] **Algorithmic Evolution (P3, P3$\alpha$, RP3$\beta$):** Detail the exact algorithmic differences between standard P3, alpha-reweighted P3 ($P3_\alpha$), and degree-penalized RP3 ($\text{RP3}_\beta$), focusing on how popularity bias is mitigated.

## 📌 8. Advanced Topics: Graph Convolutional Networks (GCN)

### Modern Graph Convolution Frameworks
- [ ] **GCN Principles in RecSys:** Explain how Graph Convolutional Networks perform neighborhood aggregation across user-item bipartite graphs.
- [ ] **LightGCN Simplifications:** Detail the architecture of LightGCN. Explain why non-linear activations and feature transformation matrices are removed for recommendation tasks, and write its linear aggregation expression.
- [ ] **Training Objectives:** Describe the optimization objective used to train LightGCN models (e.g., pairwise BPR loss over graph embeddings).

## 📌 9. Advanced Topics: Deep Learning & Content-Based ML Recommenders

### Machine Learning for Content-Based Filtering
- [ ] **ML-Based CBF Formulation:** Describe how pure content-based recommendation is cast as a supervised machine learning problem.
- [ ] **Mathematical Notation & Optimization:** Write the prediction and loss functions using both formal matrix notation and explicit summation notation over feature indices.
- [ ] **Constraint Requirements:** Explain what constraints (e.g., non-negativity, regularizations) are necessary during training and why.

### Two-Tower Neural Architectures
- [ ] **Structural Architecture:** Sketch and describe a Two-Tower neural network layout (User Tower and Item Tower with fully connected hidden layers).
- [ ] **Layer Equations & Output Scoring:** Write the forward-pass equations for both towers, clearly defining input feature representations, latent output vector embeddings, and the final scoring operation (e.g., dot product or cosine similarity).
- [ ] **Matrix Factorization Equivalence:** Explain under which structural conditions a Two-Tower neural model collapses into a standard Matrix Factorization model.
- [ ] **Model-Based vs. Memory-Based Classification:** Analyze whether Two-Tower systems are model-based or memory-based, detailing the conditions governing their classification.

### Autoencoder Recommenders
- [ ] **Autoencoder Architecture:** Sketch an item-based or user-based collaborative Autoencoder featuring one hidden layer.
- [ ] **Layer Formulations:** Write the encoding and decoding equations, identifying input vectors, weight matrices, bias terms, and reconstruction outputs.
- [ ] **Relation to Linear Models (SLIM):** Explain why linear item-based CF methods like SLIM can be viewed as a constrained, un-activated single-layer Autoencoder.
- [ ] **Classification Analysis:** Analyze under what operational constraints Autoencoder recommenders behave as model-based versus memory-based algorithms.
