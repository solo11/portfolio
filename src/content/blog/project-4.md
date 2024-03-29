---
author: Solomon
pubDatetime: 2023-01-30T15:57:52.737Z
title: Grid world problem - Reinforcement Learning
slug: project-4
featured: false
AI: true
ogImage: https://www.suny.edu/media/suny/content-assets/images/SUNY_Logo_278and424-600.jpg
tags:
 - project 
 - AI/ML
 - Reinforcement Learning
description: Training and applying RL methods to solve a grid world envorment

---
Training and applying RL methods to solve a grid world envorment, the agent should be able to navigate to the goal efficiently.

[Github](https://github.com/solo11/ub-rl)
<svg
    xmlns="http://www.w3.org/2000/svg"
    class="icon-tabler"
    stroke-linecap="round"
    stroke-linejoin="round">
    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
    <path
      d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5"
    ></path></svg>


## Table of contents
<svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
<rect width="1.5" height="9" x="22.75" y="1" fill="#78909c"></rect><rect width="9" height="1.5" x="19" y="4.75" fill="#78909c"></rect><rect width="1.5" height="9" x="40.75" y="19" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="37" y="22.75" fill="#5c6bc0"></rect><rect width="1.5" height="9" x="4.75" y="19" fill="#78909c"></rect><rect width="9" height="1.5" x="1" y="22.75" fill="#78909c"></rect><rect width="1.5" height="9" x="22.75" y="37" fill="#5c6bc0"></rect><rect width="9" height="1.5" x="19" y="40.75" fill="#5c6bc0"></rect><rect width="17" height="3" x="15" y="22" fill="#e8762d"></rect><rect width="3" height="17" x="22" y="15" fill="#e8762d"></rect><rect width="2" height="14" x="11" y="6" fill="#ffa000"></rect><rect width="14" height="2" x="5" y="12" fill="#ffa000"></rect><rect width="2" height="14" x="34" y="6" fill="#607d8b"></rect><rect width="14" height="2" x="28" y="12" fill="#607d8b"></rect><rect width="2" height="14" x="11" y="27" fill="#c62828"></rect><rect width="14" height="2" x="5" y="33" fill="#c62828"></rect><rect width="2" height="14" x="34" y="27" fill="#0d47a1"></rect><rect width="14" height="2" x="28" y="33" fill="#0d47a1"></rect>
</svg>

## Environment
The environment defined is a 4x4 grid where the agent has to reach the goal state from the initial state, the environment defined is identical for both deterministic and stochastic environments.

<table>
  <tr>
    <th style="text-align: center; padding:2px">Action</th>
    <td>The agent has 4 possible actions at any given state.
    <br>
up=0; down=1; right=2; left=3</td>
  </tr>
  <tr>
 <th style="text-align: center; padding:2px">State</th>
    <td>In this 4x4 grid environment there are 16 states</td>
  </tr>
    <tr>
 <th style="text-align: center; padding:2px">Rewards</th>
    <td>4 rewards are defined in this environment, the position and value of the rewards: <br>
(2,0): -3, (1,2): -4, (1,0): 2, (3,1): 5, (3,3): 20 <br>
The goal position (3,3) has the highest reward value (20)</td>
  </tr>
    <tr>
 <th style="text-align: center; padding:5px">Objective</th>
    <td>To reach the goal state</td>
  </tr>
</table>

- Deterministic: 
In a deterministic environment, the agent can determine the next state given the current state and action there is no randomness or probability involved in the environment.
- Stochastic: Here stochasticity is defined in the step function by choosing between executing the given action or choosing a random action.
The probability of performing the given action is 0.6 and performing a random action is 0.4.

## Algorithms
- SARSA
- Q Leaerning

For the defined deterministic and stochastic environments, the Q-learning algorithm and SARSA is used to solve the environment, the deterministic environment consists of a 4x4 grid world where the agent starts at an initial position (0,0) and needs to reach the goal state (3,3) and should collect rewards on the way, there are negative and positive rewards defined in the grid, the agent should not collect the negative rewards and stay away from them and collect the positive rewards and reach the goal state.

## Analysis
- Both the algorithms are able to navigate the deterministic environment successfully, obtaining the higest possible reward each episode
- The algorithms perform equally when evaluated for 50 episodes in Graph 6.1 and also obtain the highest reward
- Q-Learning took more no. of episodes to train and to get a liner graph while training, but SARA was able to achieve it in 200 episodes

## Screenshots

- Initial state
<img width="385" alt="Screenshot 2024-03-29 at 2 48 40 AM" src="https://github.com/solo11/ub-rl/assets/32461868/24a6f2b2-d3f9-496e-93c0-9c0b9e629e9e">

- When the agent is navigating
<img width="385" alt="Screenshot 2024-03-29 at 2 48 48 AM" src="https://github.com/solo11/ub-rl/assets/32461868/0ef6bda8-ce07-41d2-b67b-cc7870938a60">


- When the agent collects the reward
<img width="385" alt="Screenshot 2024-03-29 at 2 48 55 AM" src="https://github.com/solo11/ub-rl/assets/32461868/288e002f-ce1b-43a7-86e6-1d61635d4283">


- When the agent is at the goal state
<img width="385" alt="Screenshot 2024-03-29 at 2 49 04 AM" src="https://github.com/solo11/ub-rl/assets/32461868/6b16f1a6-86ff-4155-a2bc-e8174579b528">


Read more - [Project Report](https://github.com/solo11/ub-rl/blob/main/report/spanduga_assignment1_final_combined.pdf)