# Project: Solving a Continous Control Environment (Reacher) 
#### *#Udacity: Deep-RL Nanodegree*

This project deals with solving a continous control environment called Reacher with a modern Actor-Critic model approach. 


## Game environment

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

### Observation Space

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Solving the Environment
#### - *Single Agent*
The agent must get an average score of +30 (over 100 consecutive episodes).

#### - *Multi-Agent(20)*
The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically:
- After each episode, the rewards that each agent received are added to get a score for each agent. 
- Then average the scores by the number of agents (20).
- This has to be higher than +30.

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 

## Getting Started - Dependencies

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
    
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
    
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
    
	
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
3. Clone [this repository]{https://github.com/udacity/deep-reinforcement-learning.git}, and navigate to the `python/` folder.  With `pip` it will install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

## Instructions for Jupyter Notebook
To train the agent, start jupyter notebook, open `Navigation.ipynb` and execute! For more information, please check instructions inside the notebook.


# Continous Control