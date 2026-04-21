## Instructions
- You must score **at least 9/10** to proceed to the oral exam.  
- This written test **does not influence your final grade**.  
- You have **20 minutes** to complete the exam.  
- You must fill in a **separate answer sheet**, marking your answers in a table (no explanations required).

---


## March 2026

### 1. Consider a stochastic process {Xₜ} with finite state space S. Suppose that for all t:  
P(Xₜ₊₁ | Xₜ, Xₜ₋₁, …, X₀) = P(Xₜ₊₁ | Xₜ)  
However, the transition probabilities depend explicitly on time.

- (A) The process is stationary but not Markovian  
- (B) The process is not Markovian because transition probabilities are time-dependent  
- (C) The process is Markovian but not stationary ✅  
- (D) The process is neither Markovian nor stationary  


### 2. Consider the Policy Iteration algorithm applied to a finite MDP. Which statement is correct?

- (A) If the policy does not change after an improvement step, then it is optimal ✅  
- (B) Policy Iteration may cycle indefinitely between policies with equal value  
- (C) Policy iteration always improves the policy strictly at each iteration  
- (D) Policy Iteration requires stochastic policies to guarantee convergence  


### 3. Consider Monte Carlo (MC) and Temporal Difference (TD(0)) methods for policy evaluation in a finite MDP.

- (A) MC methods require the Markov property, while TD methods do not  
- (B) MC methods are biased but have lower variance than TD methods  
- (C) TD methods are unbiased because they use bootstrapping  
- (D) TD methods typically have lower variance but introduce bias compared to MC ✅  


### 4. Consider the SARSA algorithm applied to a finite MDP. Which assumption is required to guarantee convergence of Q(s,a) to the optimal action-value function Q\*(s,a)?

- (A) All state-action pairs are visited infinitely often ✅  
- (B) The discount factor satisfies γ = 1  
- (C) The MDP has deterministic transitions  
- (D) The learning rates satisfy ∑αₜ < ∞ and ∑αₜ² = ∞  



### 5. A main purpose of value function approximation is to:

- (A) Remove the need for rewards  
- (B) Generalize from visited states to unseen states ✅  
- (C) Avoid bootstrapping entirely  
- (D) Make the environment Markovian  


### 6. A target network in DQN is used to:

- (A) Mitigate the overestimation bias  
- (B) Generate actions during exploration only  
- (C) Stabilize bootstrapping targets by updating them less frequently ✅  
- (D) Reduce correlation between consecutive samples and reuse data  


### 7. Expectation models approximate:

- (A) The full density p(s' | s, a)  
- (B) The expected next state E[S' | s, a] ✅  
- (C) The advantage function  
- (D) Only terminal transitions  


### 8. In which of the following situations would you use a Softmax policy with logits that are a linear function of the state?

- (A) Finite state space, continuous action space  
- (B) Continuous state space, finite action space ✅  
- (C) Continuous state space, continuous action space  
- (D) Finite state space, finite action space  



### 9. The essential way in which G(PO)MDP mitigates the variance of REINFORCE is by:

- (A) Exploiting the causal structure of the problem ✅  
- (B) Using a critic  
- (C) Employing an average-reward baseline  
- (D) Clipping importance weights  

### 10. DDPG

- (A) Optimizes the parameters of a stochastic policy by playing a stochastic policy  
- (B) Optimizes the parameters of a deterministic policy by playing a stochastic policy ✅  
- (C) Optimizes the parameters of a deterministic policy by playing a deterministic policy  
- (D) Optimizes the parameters of a stochastic policy by playing a deterministic policy  
