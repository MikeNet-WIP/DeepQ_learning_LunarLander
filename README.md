[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135612-cbff24aa-7d12-11e8-9b6c-2b41e64b3bb0.gif "Trained Agent"

# Deep Q-Network (DQN)

### Instructions

implement Deep Q-Learning to solve OpenAI Gym's LunarLander environment.  

### Results

![Trained Agent][image1]



### Install

1. creat the conda environment 

    `conda create --name enforedlearning python=3.6`
    
    `source activate enforedlearning`
    
    

2. install the latest pytorch with cuda 

    `conda install pytorch-nightly cudatoolkit=10.0 -c pytorch`
    
    
    
3. install pip packages

    `cd enforedlearning/python`
    
    `pip install .`
    
    `cd enforedlearning`
    
    
    
4. get gym for the enviroments

    `git clone https://github.com/openai/gym.git`
    
    `cd gym`
    
    `pip install -e .`
    
    
    
5. (optional) make kernel

    `python -m ipykernel install --user --name drlnd --display-name "drl"`
    


### Instructions

start jupyter notebook `jupyter notebook --allow-root`



### Resources

- [Human-Level Control through Deep Reinforcement Learning](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)
- [Deep Reinforcement Learning with Double Q-Learning](https://arxiv.org/abs/1509.06461)
- [Dueling Network Architectures for Deep Reinforcement Learning](https://arxiv.org/abs/1511.06581)
- [Prioritized Experience Replay](https://arxiv.org/abs/1511.05952)


### Hyperprameters 
    1.  fc1_units=64, fc2_units=64
        BUFFER_SIZE = int(1e6)  # replay buffer size
        BATCH_SIZE = 64         # minibatch size
        GAMMA = 0.99            # discount factor
        TAU = 1e-3              # for soft update of target parameters
        LR = 5e-4               # learning rate 
        UPDATE_EVERY = 4        # how often to update the network
        
            Results Episode 3000	Average Score: 220.08
            
    2.  fc1_units=664, fc2_units=364
        BUFFER_SIZE = int(1e5)  # replay buffer size
        BATCH_SIZE = 64         # minibatch size
        GAMMA = 0.99            # discount factor
        TAU = 1e-3              # for soft update of target parameters
        LR = 5e-4               # learning rate 
        UPDATE_EVERY = 4        # how often to update the network
        
            Results Episode 3000	Average Score: 274.31

    3.  fc1_units=64, fc2_units=64
        BUFFER_SIZE = int(1e5)  # replay buffer size
        BATCH_SIZE = 20         # minibatch size
        GAMMA = 0.99            # discount factor
        TAU = 1e-3              # for soft update of target parameters
        LR = 2e-4               # learning rate 
        UPDATE_EVERY = 4        # how often to update the network
        
            Results Episode 3000	Average Score: 194.05
            

            