# 🤖 SARSA Implementation using Cliff Walking Environment

This project demonstrates the implementation of the **SARSA (State-Action-Reward-State-Action)** algorithm using the **CliffWalking-v1** environment from Gymnasium.

SARSA is an **On-Policy Reinforcement Learning** algorithm that learns by interacting with the environment and updating its Q-table using the action actually selected by the current policy.

---

## 📌 Project Overview

- **Algorithm:** SARSA
- **Environment:** CliffWalking-v1
- **Framework:** Gymnasium
- **Programming Language:** Python
- **Learning Type:** Model-Free On-Policy Reinforcement Learning

The objective is to train an intelligent agent that safely reaches the goal while avoiding the cliff and maximizing cumulative rewards.

---

## 🛠️ Technologies Used

- Python
- NumPy
- Gymnasium
- Random

---

## 📂 Project Structure

```
SARSA/
│
├── SARSA.ipynb
└── README.md
```

---

## 📖 Workflow

1. Install the required libraries.
2. Create the Cliff Walking environment.
3. Initialize the Q-table with zeros.
4. Define the ε-Greedy policy.
5. Train the agent for multiple episodes.
6. Update Q-values using the SARSA update rule.
7. Test the trained agent.
8. Visualize the learned path.

---

## 🔄 SARSA Update Equation

\[
Q(s,a)=Q(s,a)+\alpha\left[R+\gamma Q(s',a')-Q(s,a)\right]
\]

Where:

- **Q(s,a)** → Current Q-value
- **α (Alpha)** → Learning Rate
- **γ (Gamma)** → Discount Factor
- **R** → Immediate Reward
- **s′** → Next State
- **a′** → Next Action selected by the current policy

---

## ⚙️ Hyperparameters

| Parameter | Value |
|-----------|------:|
| Episodes | 500 |
| Learning Rate (α) | 0.5 |
| Discount Factor (γ) | 0.99 |
| Epsilon (ε) | 0.1 |

---

## 🎯 Environment

The project uses the **CliffWalking-v1** environment.

### Environment Features

- Grid World Environment
- 48 States
- 4 Possible Actions
- Start State
- Goal State
- Cliff Region
- Negative reward for falling into the cliff
- Episode resets after falling into the cliff

The agent learns to navigate safely toward the goal while minimizing penalties.

---

## 🧠 Exploration Strategy

This project uses the **ε-Greedy Policy**.

- **90%** of the time → Choose the best known action.
- **10%** of the time → Explore a random action.

Since SARSA is an **On-Policy** algorithm, the same policy is used for both selecting actions and updating Q-values.

---

## 📊 Training Process

During training:

- Environment is reset at the start of every episode.
- The agent selects actions using ε-Greedy exploration.
- Q-values are updated after every action.
- Training continues for **500 episodes**.
- The learned policy gradually improves through interaction with the environment.

---

## 📈 Results

After training:

- The trained agent successfully navigates the Cliff Walking environment.
- The learned Q-table stores the estimated value of each state-action pair.
- The final policy demonstrates safer navigation toward the goal.

---
