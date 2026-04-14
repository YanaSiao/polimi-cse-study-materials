## 📌 Prediction & Predictors

- Provide the full proof of the **general formula for the k-steps ahead predictor** for an ARMAX(n, m, p + k) model in canonical form.

- Explain why we need the **canonical representation** of a stochastic process to derive the optimal predictor.

- Discuss the **behavior of the k-steps ahead prediction error variance** as a function of k.

- Show that when **k = 1** and the system belongs to the model set, the identification cost function coincides with the **variance of the white noise**.

- If the process is written in canonical form:
  - describe the qualitative behavior of the **prediction error variance vs prediction horizon**
  - explain the asymptotic behavior



## 📌 Canonical Representation

- Explain the **properties of a stationary stochastic process in canonical form**:
  - monic
  - coprime
  - same order numerator/denominator
  - stability (unit circle)

- Discuss the implications of using a **non-canonical model for prediction**.
- Provide an example of computing a **one-step-ahead predictor for a non-canonical process** and discuss possible issues.

## 📌 Stochastic Processes & Estimation

- Define a **stationary stochastic process** and describe its equivalent representations:
  - time domain  
  - transfer/operatorial  
  - frequency domain  
  - probabilistic  

- Describe how to estimate from data (without parametric model):
  - mean  
  - covariance function  
  - spectral density  

- Define when an estimator is **correct** and prove correctness for the mean estimator.

- Discuss the **consistency of covariance estimators**.

- Explain how the **accuracy of estimators changes with dataset size**.


## 📌 Spectral & Statistical Analysis

- Explain procedures to estimate:
  - variance  
  - covariance  
  - spectral density  

- Discuss how estimator quality changes as **N → ∞**


## 📌 Model Identification (ARMA / ARMAX)

- Describe in detail the **identification algorithm for ARMAX models**.

- Explain the **Prediction Error Method (PEM)**.
- Prove that if the model set contains the true system, PEM converges to the **true system**.

- Describe the **data processing scheme** for quasi-Newton identification of ARMA/ARMAX models.

- Explain:
  - gradient computation  
  - residual generation  
  - iterative optimization (Gauss-Newton / BFGS)

- Discuss what happens when the system is **outside the model set**.

## 📌 Model Selection & Overfitting

- Explain the concept of **overfitting** with an example and techniques to avoid it.

- Discuss **cross-validation** in ARMA models:
  - motivation  
  - advantages over whiteness test  

- Compare:
  - cross-validation  
  - whiteness test  
  - AIC / FPE  

- Discuss alternatives when **cross-validation is not feasible**.

- Define the **whitening filter** and explain its role in prediction.

- Explain what happens if the model is **not minimum phase**.


## 📌 Identifiability

- Explain the difference between:
  - **structural identifiability**
  - **experimental identifiability**


## 📌 Additional Topics

- Explain estimator **consistency** and its importance.
