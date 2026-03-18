# PPO on CarRacing-v3 🚗

This project trains a reinforcement learning agent using **Proximal Policy Optimization (PPO)** on the `CarRacing-v3` environment from Gymnasium.

The agent learns to drive a car directly from visual observations (RGB images) and is evaluated based on cumulative reward over multiple episodes.



## 📌 Project Overview

Reinforcement learning is used to train an autonomous agent to navigate a procedurally generated racing track. The model interacts with the environment, collects rewards, and improves its policy over time.

This project demonstrates a complete RL workflow:
- environment setup and validation
- visual inspection of observations
- PPO agent training
- reward tracking and visualization
- evaluation over multiple episodes



## 🧠 Environment

**CarRacing-v3 (Gymnasium)**

- Observation space: `(96, 96, 3)` RGB images  
- Action space: continuous (steering, gas, brake)  
- Goal: maximize cumulative reward by staying on track and driving efficiently  



## ⚙️ Method

The agent is trained using **PPO (Proximal Policy Optimization)** from Stable-Baselines3.

Why PPO:
- stable and widely used policy-gradient algorithm
- works well for continuous control problems
- strong baseline for reinforcement learning tasks

A **CNN-based policy (`CnnPolicy`)** is used to process visual input.



## 📊 Results

After training for **100,000 timesteps**, the agent was evaluated over **50 episodes**.

- **Mean reward:** ~122  
- **Standard deviation:** ~115  

The agent shows clear learning progress, improving from negative rewards in early episodes to positive performance. However, the relatively high variance indicates that the learned policy is still unstable.



## 📈 Training Behavior

The reward curve shows a general upward trend, confirming that the agent learns over time. However, fluctuations in reward suggest that learning is not yet fully stable, which is common in reinforcement learning tasks with high-dimensional inputs.



## 🚀 Installation

```bash
git clone https://github.com/Mayatem/ppo-carracing-gymnasium.git
cd ppo-carracing-gymnasium
pip install -r requirements.txt

## ▶️ Run the Project

Open the notebook and run all cells:

```bash
jupyter notebook notebooks/ppo_carracing.ipynb

This will train the agent, generate the reward curve, and evaluate performance.

