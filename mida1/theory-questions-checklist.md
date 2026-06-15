> ⚠️ **Notice:** This file is completely student-made. No official course materials, questions, or solutions were used or reproduced here. This document serves strictly as a personal concept checklist and structural study overview. You should always consult and verify your knowledge against the professor's officially validated materials and answer keys on your student portal.

---

## 📌  Stochastic Processes & Estimation

This section covers the fundamental mathematical definitions of stationary stochastic processes across different frameworks, alongside non-parametric estimation techniques for extracting statistical properties directly from raw data. For rigorous formal proofs and officially validated step-by-step mathematical derivations, please refer to the primary course textbook and official lecture notes.

### 🟩 Core Concepts to Master

- [ ] **Equivalent Representations of Stationary Processes:** Be prepared to define a stationary stochastic process and articulate how it is modeled across four distinct lenses:
  - **Time Domain:** Described via mean, variance, and the auto-covariance function $\gamma(k) = \mathbb{E}[(v(t) - m)(v(t-k) - m)]$.
  - **Transfer / Operatorial Domain:** Modeled using shift operators ($q, q^{-1}$) and rational transfer functions acting on white noise inputs: $v(t) = W(q)e(t)$.
  - **Frequency Domain:** Represented analytically via power spectral density (PSD) $S(\omega)$ and spectral decomposition.
  - **Probabilistic Domain:** Characterized by joint probability density functions (PDFs) that remain invariant to absolute time shifts.
- [ ] **Non-Parametric Estimation from Empirical Data:** Master the empirical formulas used to estimate core statistical properties when a underlying parametric model ($\text{ARX, ARMAX}$, etc.) is unavailable:
  - **Sample Mean ($\hat{m}_N$):** Computing the empirical average over $N$ observations.
  - **Sample Covariance Function $\hat{\gamma}_N(k)$ :** Constructing the biased or unbiased empirical auto-covariance from data samples.
  - **Spectral Density $\hat{S}_N(\omega)$:** Estimating power distribution across frequencies (e.g., via the periodogram method).
- [ ] **Estimator Accuracy and Mathematical Correctness:**
  - **Unbiasedness:** Define what it means for an estimator to be correct/unbiased ($\mathbb{E}[\hat{\theta}] = \theta_0$).
  - **Proof of Mean Correctness:** Be ready to write out the formal algebraic proof demonstrating that the sample mean estimator $\hat{m}_N$ is an unbiased estimator of the true ensemble mean $m$.
  - **Consistency of Covariance Estimators:** Discuss why the sample covariance estimator is asymptotically unbiased, and analyze the trade-offs between the biased ($1/N$) and unbiased $(1/(N-k))$ formulations regarding mean squared error (MSE).
- [ ] **Asymptotic Behavior & Dataset Scaling:** Explain how estimator variance scales as a function of the total dataset size ($N$). Understand the conditions under which an estimator achieves consistency ($\lim_{N \to \infty} \text{Var}(\hat{\theta}) = 0$).


> 📐 **Proof Bottleneck:** The proof for the unbiasedness of the sample mean estimator is a frequent theory question. Ensure you can comfortably handle the linearity of the expectation operator ($\mathbb{E}[\cdot]$) when expanding the summation $\frac{1}{N}\sum_{t=1}^N v(t)$.

> ⚠️ **Common Pitfall:** Remember that the standard raw periodogram estimator for the spectral density  $\hat{S}_N(\omega)$ is **not** a consistent estimator on its own—its variance does not go to zero as $N \to \infty$ due to random fluctuations. Note how smoothing windows (like the Bartlett or Welch methods) are required to fix this issue.

## 📌  Spectral & Statistical Analysis

This section deals with evaluating how empirical estimators behave asymptotically as the data pool grows infinitely large, with a particular focus on the frequency domain properties. For full analytical derivations and official theorems regarding stochastic convergence, please consult the course handouts.

### 🟩 Core Concepts to Master

- [ ] **Estimation Procedures from Empirical Data:** Review the standard mathematical algorithms used to compute non-parametric statistical metrics from $N$ samples:
  - **Sample Variance:** Computing the spread of the data relative to the sample mean.
  - **Sample Covariance:** Evaluating cross-dependence or auto-dependence across different time lags.
  - **Spectral Density:** Moving from time-domain lags to frequency-domain distributions using the discrete Fourier transform framework.
- [ ] **Asymptotic Estimator Quality ($N \to \infty$):** Analyze the limiting behavior of your estimators as the dataset size approaches infinity:
  - **Asymptotic Unbiasedness:** Determine if the expected value of your estimator converges exactly to the true value ($\lim_{N \to \infty} \mathbb{E}[\hat{\theta}_N] = \theta_0$).
  - **Consistency:** Evaluate whether the estimator converges in probability to the true parameter, requiring both the bias and the variance to drop to zero as $N \to \infty$.
  - **The Periodogram Paradox:** Discuss why the raw sample spectral density estimator $\hat{S}_N(\omega)$ fails to achieve consistency despite a growing $N$, and explain how data windowing/smoothing resolves this.

> ⚠️ **Key Distinction:** Be ready to clearly distinguish between a *biased* estimator that is *asymptotically unbiased* (where the error vanishes as $N$ grows) versus an estimator that remains permanently structurally biased regardless of dataset scaling.

## 📌  Canonical Representation

This section focuses on the fundamental properties of canonical stochastic processes and the critical implications of non-canonical models on prediction framework stability and optimality. For the complete mathematical proofs and officially validated solution steps, please consult the course textbook and lecture notes.

### 🟩 Core Concepts to Master

- [ ] **Properties of Canonical Form:** Understand the four defining structural pillars of a stationary stochastic process in canonical form $W(z) = \frac{C(z)}{A(z)}$:
  - **Monic:** The leading coefficients of both the numerator and denominator polynomials are exactly equal to 1 ($c_0 = 1, a_0 = 1$).
  - **Coprime:** The polynomials $C(z)$ and $A(z)$ share no common roots (no pole-zero cancellations).
  - **Equal Degree:** The numerator and denominator polynomials share the same degree (deg(C) = deg(A)).
  - **Analyticity / Stability Constraints:** All poles and zeros must reside strictly inside the open unit disk ($|z| < 1$).
- [ ] **Implications of Non-Canonical Representations:** Analyze why trying to build an optimal predictor from a non-canonical model fails or yields suboptimal results:
  - Explain how non-invertible zeros (roots outside or on the unit circle) lead to unstable, diverging filters when calculating the inverse system $W^{-1}(z)$.
  - Understand how common factors (non-coprime polynomials) introduce redundant, unobservable, or uncontrollable dynamics into the predictor state-space.
- [ ] **One-Step-Ahead Predictor Derivations (Non-Canonical Cases):** 
  - Trace the step-by-step process of converting an explicitly non-canonical process into its spectral equivalent canonical counterpart before running a prediction algorithm.
  - Detail the operational pitfalls—such as the explode/divergence risks of the tracking error filter—if the one-step-ahead predictor formula is blindly applied to an uncorrected, non-minimum phase system.


> ⚠️ **Critical Checkpoint:** Pay extremely close attention to the roots of the numerator polynomial $C(z)$. If any root sits outside the unit circle ($|z| \ge 1$), you **must** apply spectral factorization to flip the zero inside the unit circle ($|z| < 1$) before you can safely write the stable predictor expression.

> 📝 **Notation Note:** Make sure your spectral factorization scaling constants match the exact algebraic conventions utilized by the professor during the exercise sessions to ensure your steady-state variance computations remain perfectly consistent with the official answer keys.



## 📌  Prediction & Predictors

This section outlines the key theoretical concepts regarding predictors that you should master. For exact proofs, derivations, and official answer keys, please refer to the professor's official solution sheets.

### 🟩 Core Concepts to Master

- [ ] **The $k$-Steps Ahead Predictor:** Be able to derive the general formula for an $\text{ARMAX}(n, m, p + k)$ model in canonical form.
- [ ] **Canonical Representation Necessity:** Understand the underlying theoretical reasons why a stochastic process must be in its canonical form to derive an optimal predictor.
- [ ] **Prediction Error Variance ($k$ vs. Horizon):**
  - Analyze how the variance of the $k$-steps ahead prediction error behaves as a function of $k$.
  - Be ready to describe its qualitative behavior relative to the prediction horizon and explain its asymptotic behavior.
- [ ] **The 1-Step Case ($k = 1$):** Understand the relationship between the identification cost function and the white noise variance when $k = 1$ (assuming the system matches the model set).


> 🔍 **Tip 1:** Make sure you practice the algebraic manipulations for the polynomial divisions required to get the canonical form; this is a frequent bottleneck on the exam.

> 📚 **Tip 2:** Cross-reference your notes on this section with the official lecture slides to ensure your notation matches the professor's preferred format exactly.

## 📌  Identifiability

This section covers the conditions required to uniquely determine the true parameters of a system from its structural equations and experimental data. For the formal algebraic proofs, rank conditions, and persistently exciting input theorems, please refer to the official course documentation.

### 🟩 Core Concepts to Master

- [ ] **Structural Identifiability (A Priori):**
  - Define structural identifiability as a purely theoretical property of the chosen model structure $\mathcal{M}(\theta)$. 
  - Understand that it assumes ideal conditions: an infinite amount of noise-free data ($N \to \infty$).
  - Explain the core question it answers: Does there exist a unique parameter vector  $\theta$  that yields a given input-output transfer function?
  - Distinguish between globally structurally identifiable structures (one unique parameter vector matches the behavior) and locally identifiable structures (a finite number of isolated parameter configurations share the same behavior).
- [ ] **Experimental Identifiability (A Posteriori):**
  - Define experimental identifiability as a practical property that depends heavily on the actual data collected during a specific test run.
  - Analyze the constraints that prevent a structurally identifiable model from being identified in practice, such as finite data length ($N$), poor signal-to-noise ratio, or poorly chosen input signals.
  - Explain the concept of a **Persistently Exciting (PE)** input signal. Understand why the input spectrum must contain a sufficient number of distinct frequencies to excite all the modes of the system, and what happens to experimental identifiability if the input is under-exciting (e.g., using a single step input to identify a high-order system).


## 📌  Estimator Consistency

This section focuses on the rigorous asymptotic property of mathematical estimators as the available data approaches infinity. For the stochastic convergence proofs (convergence in probability or almost surely), please check the course textbook.

### 🟩 Core Concepts to Master

- [ ] **Definition of Consistency:**
  - Define a consistent estimator as one where the parameter estimate $\hat{\theta}_N$ converges directly to the true parameter value $\theta_0$ as the dataset size $N$ goes to infinity.
  - Master the technical distinction between **Weak Consistency** (convergence in probability: $\lim_{N \to \infty} P(|\hat{\theta}_N - \theta_0| > \varepsilon) = 0$) and **Strong Consistency** (convergence with probability 1 / almost sure convergence).
- [ ] **The Importance of Consistency:**
  - Explain why consistency is the ultimate validation metric for any system identification algorithm: it guarantees that with enough data, the algorithm is mathematically guaranteed to uncover the true underlying physical system.
  - Contrast a consistent algorithm with an inconsistent one, noting that if an estimator is inconsistent, accumulating more data will *not* eliminate the systematic estimation error or bias.


> ⚠️ **Key Distinction:** A common written exam question asks you to explain how structural and experimental identifiability interact. Remember: **Structural identifiability is a prerequisite for experimental identifiability.** If your model structure is structurally unidentifiable (e.g., trying to fit too many coefficients to a simple transfer function), no input signal or dataset in the world—no matter how perfect—can save you or yield a unique solution.

> 📈 **Signal Check:** When checking for experimental identifiability in a linear regression or ARX setup, remember to look at the information matrix (or the covariance matrix of the regressors). If this matrix is singular or poorly conditioned, your input signal is not persistently exciting, and your parameter variance will explode.



## 📌  Model Identification (ARMA / ARMAX)

This section details the algorithmic and optimization frameworks used to identify parametric $\text{ARMAX}$ and $\text{ARMA}$ models from empirical data streams. For complete matrix calculus derivations, convergence proofs, and officially validated pseudo-code, please consult the core course textbooks and lecture slides.

### 🟩 Core Concepts to Master

- [ ] **The $\text{ARMAX}$ Identification Framework:** Understand the structural layout of an $\text{ARMAX}(n, m, p)$ model governed by the difference equation:
  $$A(q)y(t) = B(q)u(t) + C(q)e(t)$$
  - Map how the identification algorithm must simultaneously estimate the deterministic plant dynamics ($A, B$) alongside the stochastic noise dynamics ($C$).
- [ ] **The Prediction Error Method (PEM):** 
  - Define the PEM objective function based on minimizing a scalar quadratic norm of the prediction error channel: $V_N(\theta) = \frac{1}{N} \sum_{t=1}^N \varepsilon^2(t, \theta)$.
  - **Consistency Proof:** Outline the formal proof showing that if the true system dynamics $\mathcal{S}$ reside directly inside the chosen model set $\mathcal{M}$ ($\mathcal{S} \in \mathcal{M}$), the parameter estimate $\hat{\theta}_N$ converges asymptotically with probability 1 to the true parameter vector $\theta_0$ as $N \to \infty$.
- [ ] **Quasi-Newton Data Processing & Optimization Schemes:** Because $\text{ARMAX}$ models feature adjustable $C(q)$ polynomial parameters in the denominator of the predictor filter, the prediction error $\varepsilon(t, \theta)$ is inherently non-linear with respect to $\theta$, demanding iterative optimization:
  - **Residual Generation:** Track how the prediction error residuals $\varepsilon(t, \theta) = C^{-1}(q)[A(q)y(t) - B(q)u(t)]$ are recursively filtered and generated at each iteration step.
  - **Gradient Computation:** Master the sensitivity filtering technique used to compute the gradient vector $\psi(t, \theta) = -\frac{\partial \varepsilon(t, \theta)}{\partial \theta}$. Note how this requires passing the data through recursive filters dependent on the current estimate of $C(q)$.
  - **Iterative Optimization Algorithms:** Be prepared to contrast the update laws, computational footprints, and search directions of the **Gauss-Newton** approximation method versus the **BFGS** (Broyden–Fletcher–Goldfarb–Shanno) quasi-Newton update rule.
- [ ] **System Outside the Model Set ($\mathcal{S} \notin \mathcal{M}$):** Analyze the systemic consequences when the structural complexity of the true system exceeds your model order. Explain how PEM behaves in this scenario (i.e., finding the best approximation that minimizes the mean square prediction error under the experimental input spectrum).


> 📐 **Derivation Bottleneck:** Practice taking partial derivatives of the recursive prediction expression with respect to individual coefficients ($a_i, b_i, c_i$) so you can comfortably write down the respective filtering operations.

> ⚠️ **Common Pitfall:** During iterative optimization, stability must be strictly checked at every single iteration step. If an update pushes the roots of the estimated polynomial $C(q)$ outside the unit circle ($|z| \ge 1$), the residual generation filter will instantly explode. Be ready to explain how projection algorithms or line-search constraints are applied to prevent this.

## 📌  Model Selection & Overfitting

This section focuses on structural validation techniques used to find the optimal balance between model complexity and generalization performance, ensuring identified parameters capture actual system dynamics rather than high-frequency noise. For the formal statistical derivations of information criteria and exact testing procedures, please refer to the official course documentation.

### 🟩 Core Concepts to Master

- [ ] **The Concept of Overfitting:** Explain how an excessively complex model (too many parameters relative to the dataset size) fits the training data perfectly but fails to generalize to fresh validation data. 
  - Be ready to illustrate this with a clear system identification example (e.g., an over-parameterized $\text{ARX}$ model capturing the random realizations of white noise instead of the true plant transfer function).
- [ ] **Cross-Validation in Parametric Models:**
  - **Motivation & Implementation:** Detail the process of splitting data into independent estimation and validation subsets.
  - **Advantages Over the Whiteness Test:** Explain why evaluating model performance on an independent validation set is a more robust indicator of true prediction capability than simply checking if the estimation residuals look like white noise.
- [ ] **Model Selection Methodologies (Comparative Analysis):** Understand the trade-offs, assumptions, and use cases across the following validation frameworks:
  - **Cross-Validation:** Purely data-driven, non-parametric validation; does not rely on asymptotic statistical assumptions.
  - **Whiteness Test:** Evaluates the sample auto-correlation function $\hat{r}_\varepsilon(\tau)$ of residuals to verify if any unmodeled dynamics remain in the error channel.
  - **AIC (Akaike Information Criterion) & FPE (Final Prediction Error):** Analytical metrics that mathematically penalize the loss function based on the number of estimated parameters to prevent over-parameterization.
- [ ] **Alternatives to Cross-Validation:** Discuss fallback options (such as BIC/MDL criteria or looking for structural stabilization in the loss function curve via elbow analysis) when data length ($N$) is too short to split into independent subsets.
- [ ] **The Whitening Filter & Prediction Dynamics:**
  - Define the whitening filter $W^{-1}(q)$ as the inverse of the canonical noise model. Explain how it structurally decouples the correlated process observations into an uncorrelated white noise sequence $e(t)$, acting as the fundamental operational stage inside an optimal predictor.
- [ ] **Non-Minimum Phase System Complications:** Analyze what occurs if the true plant or noise model exhibits non-minimum phase behavior (zeros lying on or outside the unit circle $|z| \ge 1$). Detail why a direct inversion yields an unstable, unbounded predictor filter and how this structural constraint impacts the initialization of the whitening process.


> ⚠️ **Key Distinction:** Remember that the Whiteness Test is a *necessary but not sufficient* condition for optimal model selection. A heavily over-parameterized model can easily yield perfectly white residuals on its training data, yet perform terribly on new datasets. This is why cross-validation or information criteria (AIC/FPE) are mandatory additions to the validation workflow.

> 📊 **Metric Application:** Be prepared to explain when to favor AIC over FPE. While both penalize model order to estimate the average prediction error on an independent dataset, FPE is structurally tailored specifically for linear regression settings, whereas AIC is derived from a more general Kullback-Leibler information theoretic framework.


