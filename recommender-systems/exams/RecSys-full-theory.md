# RECOMMENDER SYSTEMS – FULL THEORY

## Example (officially released sample)

### Question: Taxonomy

- **(2 points)** Discuss the main differences between personalized and non-personalized recommendation algorithms. Provide an example for each category and explain why it belongs to it.

### Question: User-Based Collaborative Filtering

- **(2 points)** Describe the main idea behind it and the formula to compute the predictions given a URM with explicit ratings and the similarity S, with and without the user bias  
- **(1 point)** Write the formula to compute the Cosine Similarity  
- **(1 point)** Write the formula to compute the Pearson Correlation Coefficient and explain when and why it should be used instead of the Cosine Similarity  
- **(1 point)** Explain how the equation of the model can be simplified when applied to implicit interactions and used for a Top-N recommendation task  
- **(1 point)** Explain what is the purpose of the shrink term  
- **(1 point)** Explain what KNN is, why it improves the quality of recommendation, and how the equations of the model change

### Question: Factorization Machines for Collaborative Filtering

- **(1 point)** Describe the structure of the input data used by a Factorization Machine  
- **(1 point)** Write the equation used to compute the predicted ratings and identify the model parameters  
- **(1 point)** Explain how the parameters of the model can be learned  
- **(2 points)** Explain the relationships between Factorization Machines and Matrix Factorization + Global Effects when using explicit ratings  
- **(1 point)** Explain how Factorization Machines can be used for context-aware recommendation

### Question: Bayesian Personalized Ranking

- **(2 points)** Describe the main idea and the assumptions it relies upon  
- **(1 point)** Write the loss function using a generic predicted rating  
- **(2 points)** Derive from the loss function how to compute the parameter gradients for a Matrix Factorization model

### Question: Graph-Based Models for Collaborative Filtering

Considering a scenario with implicit ratings:

- **(1 point)** Describe the structure of the graph used to represent the data  
- **(1 point)** Describe the structure of the adjacency matrix  
- **(1 point)** Describe how to compute the transition probability matrix  
- **(2 points)** Describe how the number of hops in a random walk is related to the personalization of the recommendations  
- **(1 point)** Describe how to extend the graph to include both item attributes and user attributes

---

## Student-Collected / Crowdsourced Questions

## 16/01/2026

### Question: Taxonomy

- **(4 points)** Describe the differences between **implicit and explicit ratings**. Provide an example of an algorithm specifically designed for each of the two types of ratings and explain why.  
- **(2 points)** Briefly describe what a **multi-stage recommender** is and what is the purpose of each stage.

### Question: User-Based Collaborative Filtering

- **(2 points)** Describe the **main idea** behind it and the **formula** to compute the predictions given a URM with explicit ratings and the similarity S, with and without the user bias.  
- **(1 point)** Write the formula to compute the **Cosine Similarity**.  
- **(2 points)** Write the formula to compute the **Pearson Correlation Coefficient** and explain when and why it should be used instead of the Cosine Similarity.  
- **(1 point)** Explain how the equation of the model can be simplified when applied to implicit interactions and used for a **Top-N** recommendation task.  
- **(1 point)** Explain what is the purpose of the **shrink term**.

### Question: P3

Considering a scenario with implicit ratings:

- **(1 point)** Describe the structure of the **graph** used to represent the data.  
- **(1 point)** Describe how to compute the **transition probability matrix**.  
- **(2 points)** Describe how the model is related to **item-based Collaborative Filtering** algorithms.  
- **(3 points)** Explain the differences between **P3, P3alpha, and RP3beta**.

### Question: Two-Tower Models

Consider a two-tower collaborative recommender system, with each tower constituted by a fully-connected neural network with one hidden layer:

- **(1 point)** Draw the **architecture** of the model.  
- **(2 points)** Write the **equations** for each tower, clearly specifying their input and output vectors, and how ratings are computed.  
- **(2 points)** Explain why and under which conditions traditional **Matrix Factorization** algorithms based on machine learning can be considered as a special case of Two-Tower models.  
- **(1 point)** Explain whether Two-Tower models are **model-based or memory-based**.

## 17/02/2026

### Question: Taxonomy

Discuss the main differences between **model based and memory based** recommendation algorithms. Provide an example for each category and explain why it belongs to it.

### Question: Evaluation Metrics

Describe the difference between **error metrics, classification metrics, and ranking metrics**. Provide an example for each category.

### Question: Bayesian Personalized Ranking (BPR)

- **(2 points)** Describe the main idea and the assumptions it relies upon  
- **(1 point)** Write the loss function using a generic predicted rating  
- **(2 points)** Derive from the loss function how to compute the parameter gradients for a Matrix Factorization model

### Question: Graph Convolutional Networks

- Describe the main idea behind Graph Convolutional Networks and the concept of **nodes and edges** in recommendation scenarios.
- Describe the aggregation mechanism used in **LightGCN**.
- Describe how LightGCN is trained, including the optimization objective.
