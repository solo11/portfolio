---
author: Solomon
pubDatetime: 2023-01-30T15:57:52.737Z
title: Solving Atari Pong - Reinforcement Learning 
slug: project-6
featured: false
AI: true
ogImage: https://www.suny.edu/media/suny/content-assets/images/SUNY_Logo_278and424-600.jpg
tags:
 - project 
 - AI/ML
 - Reinforcement Learning
description:  Using Open AI Gym library to solve Atari Pong game by implementing Reinforcement Learning techniques

---
Using Open AI Gym library to solve Atari Pong game by implementing Reinforcement Learning techniques


## Table of contents


## Atari Pong Environment
Pong is a two-dimensional sports game that simulates table tennis. The player controls an in-game paddle by moving it vertically across the left or right side of the screen.

Players use the paddles to hit a ball back and forth.
The goal is for each player to reach eleven points before the opponent;points are earned when one fails to return the ball to the other

- Actions - There are 6 actions noop, fire, right, left, rightfire, leftfire
- Reward - 10 points for passing the ball to the opponent, minus points for missing
the ball
- Goal – Make the agent play pong

## Algorithm
The model is trained using the Actor Critic method.
**Actor critic:**
Actor critic combines both value-based and policy-based algorithms, here we have both networks actor and critic the actor-network is used to perform an action for a given state it chooses the best action. The critic network calculates the Q value for that state action and helps the actor to improve the policy for selecting the action
<img src="https://huggingface.co/blog/assets/89_deep_rl_a2c/step2.jpg" alt="Screenshot-2024-03-30-at-6.11.03PM81dcf73860cc3da8.png" border="0">


## Screenshots

- Final trained model playing the pong game:
![DEMO](https://res.cloudinary.com/lucidb/image/upload/v1711843580/projects/pong_deterministic_rcu08n-ezgif.com-video-to-gif-converter_b1ause.gif)

Read more - [Colab Notebook](https://colab.research.google.com/drive/1X_LTsTSMbIQeUrlr5hHne8MqR1sLk_-x?usp=sharing)