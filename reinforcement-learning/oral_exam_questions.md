⚠️ Notice: This document contains unofficial exam questions recollected by students who have previously sat for this oral exam.

- No Academic Review: These questions have not been reviewed, confirmed, or corrected by the course instructors.

- Dynamic Content: As this is an oral exam, questions may vary significantly based on the student's specific academic background, the professor's focus, and the current course curriculum.

- Unofficial Resource: This file is intended solely for study purposes to help students understand the scope and general level of difficulty of the oral exam. It should not be considered an official source of exam material.

---

# Reinforcement Learning – Oral Exam Questions

## Restelli

- What is the **Bellman operator**?
- What are the **properties of the Bellman operator**?
- Where is the Bellman operator **used**?
- What is the **convergence bound** of the Bellman operator?

- What is a **Markov Process (MP)**?
- What is the **Markov property**?
- What are the **different types of states**?
- What is the **stationary distribution** of a Markov Decision Process (MDP)?
- How can we **compute the stationary distribution**?
- Under what conditions does a stationary distribution exist? (e.g., **regular processes**)
- What information is **lost** when reaching the stationary distribution? (initial state information)

## Metelli

### Convergence

- What is **convergence in prediction**?
- What is **convergence in control**?
- What are the **fixed points of convergence**?

- What is the **Projected Bellman Equation (PBE)**?
  - Provide and explain the formula


### Temporal Difference Methods

- What is **TD(0) for prediction**?
- To what does **TD(0) converge**?
- Be able to explain using **error decomposition (drawings/intuition)**


### Deep RL

- What is **DQN**?
- What are the **main issues with DQN**?
- How does DQN **mitigate these issues**?

- What is **Double DQN**?
- How does it improve over standard DQN?


### Additional Concepts

- What is an **open-loop policy/system**?

## Papini

- Why do we use **parametric policies**?
- What is the difference between:
  - **value-based methods**
  - **policy-based methods**

- Provide an example of a **policy parameterization**.

- Questions on **Soft Actor-Critic (SAC)**:
  - (expect detailed and advanced questions)

- What is the **policy gradient**?
- Why does policy gradient suffer from **high variance**?
- How can we **reduce variance**? (e.g., baselines)
- What happens if we introduce a baseline that **increases bias**?
- What happens if the baseline depends only on the **state** and not on the full trajectory?
  - (reduced bias while maintaining variance reduction)
 
---

This question bank is a community-driven effort. To keep this document accurate and helpful for future students, please contribute if you have recently taken this exam:

Telegram: Please share your recollections in the Reinforcement Learning Group Chat.

Email: If you prefer, send your notes directly to syao.yana@gmail.com.

All contributions will be anonymized before being added to this bank. Thank you for helping your fellow students!
