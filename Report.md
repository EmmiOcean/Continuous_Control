# Conclusion and Outlook
In this article, I discuss the training result of the implemented **Continous Control for the Reacher Environment**.
I solved the given problem with the DDPG algorithm since DDPG works very well in continuous action space.

## Learning Algorithm

#### - Actor
The actor was initialized:
* Fully connected - inputState -> 128 -> 128 -> actionSize
* ReLu Activation Function 
* first Layer with - BatchNorm1d(x)
* Adam Optimzer was used to caluclate loss

#### - Critic
*Build a critic (value) network that maps (state, action) pairs -> Q-values.*
The critic was initialized;
* Fully connected - 128 -> 128 -> Q-Value
* ReLu Activation Function 
* first Layer with - BatchNorm1d(x)
* Adam Optimzer was used to caluclate loss


### Experience Replay

Fixed-size buffer to store experience tuples and use them for training

## Hyperparameters
* Replay Buffer size - BUFFER_SIZE = int(1e5)
* Minibatch size - BATCH_SIZE = 128
* Discount factor - &gamma; = 0.99 
* For soft update target parameters - &tau; = 1e-2
* actor learning rate - lr = 2e-4 
* critic learning rate - lr = 2e-4
* weight decay = 0  

## Results
* [version 1]
The required criterion of an average of 30 points (averaged over 100 episode) was achieved in round about 300 episodes.

![Plot- Rewards](./result.png)

## Outlook
How the agent can be improved:
* Priorized Experience Replay
* Playing around with the parameters
* Use PPO
* Use version_2 (20 agents) to train simultaneously
