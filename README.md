# CS 370 – Pirate Intelligent Agent  
**Edgar Pena**  
Southern New Hampshire University  

---

# Overview

## Technical Implementation

- Language: Python  
- Libraries: TensorFlow, Keras, NumPy  
- Algorithm: Deep Q-Learning (DQN)  
- Environment: 8x8 maze  

## Training Configuration

- Epochs: Up to 1000  
- Initial Epsilon: 0.9  
- Epsilon Decay: 0.98 per epoch  
- Minimum Epsilon: 0.05  
- Replay Memory Size: 16 × maze size (1024 experiences)  
- Batch Size: 32  
- Target Network Update Frequency: Every 50 epochs  

### Project Summary

In this project, I developed a Pirate Intelligent Agent that learns to navigate an 8x8 maze using Deep Q-Learning. The objective was for the agent to reach the treasure located in the bottom-right corner of the maze while maximizing cumulative reward.

The following components were provided in the starter code:

- `TreasureMaze.py` – Defines the maze environment, reward structure, valid movements, and termination logic  
- `GameExperience.py` – Implements experience replay  
- `build_model()` – Defines the neural network structure  

The primary component I implemented was the `qtrain()` function. In this section, I:

- Implemented an epsilon-greedy exploration strategy  
- Integrated experience replay for batch training  
- Added a target network for stability  
- Tuned hyperparameters including epsilon decay, batch size, replay memory size, and update frequency  
- Implemented win rate tracking and a completion check to verify consistent performance  

---
# Reflection

### What do computer scientists do and why does it matter?

Computer scientists are not just implementers; we are responsible for proving, testing, refining, and sometimes disproving solutions. Our work involves questioning whether a system actually performs as intended, identifying weaknesses, and improving it through iteration. Progress in the field comes from experimentation and optimization, whether that means improving model architectures, adjusting activation functions, or redesigning algorithms to make them more efficient and reliable. The role goes beyond writing code. It requires critical evaluation and continuous improvement.

---

### How do I approach a problem as a computer scientist?

This project was a good reminder that the first approach usually isn't the right one. I started with hyperparameters that seemed fine on paper, and the agent barely learned anything for hundreds of epochs. So I had to look at what the training output was actually telling me, form a hypothesis, and adjust. That cycle of testing, observing, and refining ended up being the most important part of the work.

---

### What are my ethical responsibilities?

This project reinforced my responsibility to ensure a model performs consistently and reliably across all conditions. A high win rate was not enough; I verified performance from every starting position. Ethical development requires careful validation and reward design so the system does not learn unintended or harmful behavior. With so many automated systems influencing real decisions today, building dependable and accountable models is essential.

---



