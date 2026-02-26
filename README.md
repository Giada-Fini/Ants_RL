# Ants_RL

## Overview

This repository contains the implementation of a simulation environment for ant foraging.

Furthermore, the possibility of applying MARL, and in particular the Q-learning algorithm in an independent learning setting, to the topic has been explored.

## Project structure

### Core files
- hard_coded_ants.py : implementation of the ant agent as a class and of a simulation in which the agents are hard-coded to    perform the actions that they are supposed to do at any moment in time.
- iql.py : implementation of the Q-learning algorithm in an independent learning setting.
- ants_iql.py : training, evaluation and simulation of the learning ants.

### Configuration files
- config/env_visualizer-params.json : parameters relating to the visualization of the simulation (FPS, font size, agent size, ...).
- config/env-params.json : parameters concerning the environment in which the ants wander (population size, agent's behaviour, pheromones behaviour, ...) .
- config/learning-params.json : parameters relating to the reinforcement learning algorithm (training and evaluation episodes, hyperparameters, ...).
- config/logger-params.json : parameters concerning logging purposes (frequency, file naming, ...).

### Logging files
- runs/weights : collection of .npy files containing the weights obtained from each training run performed.
- runs/train : collection of folders, each of which containing the training results (.csv file) and a summary of the parameters (.txt file) of a run.
- runs/eval : collection of folders, each of which containing the evauluation results (.csv file) and a summary of the parameters (.txt file) of a run.
