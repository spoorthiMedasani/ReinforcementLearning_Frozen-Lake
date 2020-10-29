# Frozen Lake

In this project we'll see how to solve Frozen Lake problem from OpenAI gym. "https://gym.openai.com/envs/FrozenLake-v0/"

## Introduction:

- Frozen Lake's environment is an n x n matrix in which first cell is **'S' - starting position**, **'H' - Hole** is assigned to a random cell, **'G' - Goal** is assigned to a random cell and other cells are **'F'- Frozen**.

- **Action space** is also discrete- Left, down, right and up.

- There's also stochasticity in the environment. There's a 2/3th chance the agent can move orthogonal to the action chosen. For instance, if the agent chooses to move right, there's 1/3th chance that the agent moves up and 1/3th chance for the agent to move down. Only 1/3th of the times the agent moves along the action taken.

- An epsiode ends if the agent reaches the goal or falls into the hole. The agent gets a reward of +1 if the episode ends successfully.

- The goal here is for the agent to learn optimal actions to take at each cell to maximize the reward.

## Implementation:

#### Packages Used- Numpy, Gym and Tensorflow

- For solving this, we'll be using building a basic DQN that updates weights after each step in the epsiode. This project has been done without expereince replay. We'll also look at the implementation with expereince replay in the future.

- DQN- Deep Q Network is most used algorithm in Reinforcement Learning which uses sophisticate Neural networks to update the Q-table. The general practice is to use DQN for continuous state spaces. Though the Frozen Lake environment is discrete, we'll try and see how DQN performs on this experiment set up.

- Also, epsilon greedy policy has been used at each step to find the next step of the epsiode. Epsilon has been decayed exponentially at a scale of 0.99
