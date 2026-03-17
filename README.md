# Ants_RL

## Overview

This repository contains the implementation of a simulation environment for ant foraging obtained from a pre-existing one focused on slime mold aggregation.

Furthermore, the possibility of applying MARL to the topic has been explored, focusing on the implementation of the Q-learning algorithm in an independent learning setting.

### Simulation details

The environment is represented by a grid of square patches, each one capable of containing:

- Agents: artificial counterpart of real ants
- Food pheromone: substance released by the agents, which diffusion and evaporation is managed by the environment itself
- Nest pheromone: intrinsic substance of the environment radiating from the nest
- Food: nourishment particles that the agents are supposed to bring to the nest

The environment accomodates a nest and three food piles.

At each time step, agents can perform one of the following actions:

- Walk randomly
- Release food pheromone
- Follow food pheromone
- Follow nest pheromone
- Follow nest pheromone while releasing food pheromone
- Walk randomly while releasing food pheromone
- Take food
- Drop food

## Project structure

### Core files
- `hard_coded_ants.py` : implementation of the ant agent as a class and of a simulation in which the agents are hard-coded to    perform the actions that they are supposed to do at any moment in time.
- `iql.py` : implementation of the Q-learning algorithm in an independent learning setting.
- `ants_iql.py` : training, evaluation and simulation of the learning ants.

### Configuration files
- `config/env_visualizer-params.json` : parameters relating to the visualization of the simulation (FPS, font size, agent size, ...).
- `config/env-params.json` : parameters concerning the environment in which the ants wander (population size, agent's behaviour, pheromones behaviour, ...) .
- `config/learning-params.json` : parameters relating to the reinforcement learning algorithm (training and evaluation episodes, hyperparameters, ...).
- `config/logger-params.json` : parameters concerning logging purposes (frequency, file naming, ...).

### Logging files
- `runs/weights` : collection of .npy files containing the weights obtained from each training run performed.
- `runs/train` : collection of folders, each of which containing the training results (.csv file) and a summary of the parameters (.txt file) of a run.
- `runs/eval` : collection of folders, each of which containing the evauluation results (.csv file) and a summary of the parameters (.txt file) of a run.

## Author

This project has been carried out independently for the Distributed Artificial Intelligence exam.
