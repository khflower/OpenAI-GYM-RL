# OpenAI-GYM-RL
This code is an example of learning and executing a reinforcement learning model using the A2C stands for Advantage Actor-Critical (A2C) algorithm using 'Breakout-v0', the Atari environment of OpenAI Gym.



## Setting
Anaconda3 Virtual Environment Settings
python 3.6

## Installing a library
pytorch, openAI GYM, stabale-baseline3, atarip_py, opencv


#### After that, you can proceed with the learning using the attached py file.


## Learning results
![image](https://github.com/khflower/OpenAI-GYM-RL/assets/105573554/e7df7b3d-936b-47a1-967c-323f1e0a3b02)

## Code Description
##### make_atari_env('Breakout-v0', n_envs=4, seed=0):

##### Creates and wraps the 'Breakout-v0' environment using a function specifically designed for Atari environments.
##### n_envs=4 indicates that 4 parallel environments should be created.
##### seed=0 sets the random seed for the environment.
##### VecFrameStack(env, n_stack=4):

##### VecFrameStack is a wrapper that stacks frames to expand the observation space.
##### n_stack=4 stacks 4 consecutive frames to create a single observation.
##### model = A2C('CnnPolicy', env, verbose=1):

##### A2C is a class implementing the Advantage Actor-Critic algorithm.
##### 'CnnPolicy' refers to a policy that uses convolutional neural networks.
##### env is the environment used for training the A2C model.
##### verbose=1 enables detailed output during the training process.
##### model.learn(total_timesteps=30000):

##### Calls the learn() function to train the A2C model for the given number of time steps (total_timesteps).
##### obs = env.reset():

##### Initializes the environment and retrieves the initial observation.
##### while True::

##### Enters an infinite loop to play the game.
##### action, _states = model.predict(obs):

##### Predicts an action based on the current observation using the model.
##### obs, rewards, dones, info = env.step(action):

##### Applies the predicted action to the environment and receives the next observation, reward, done status, and additional information.
##### env.render():

##### Visualizes the current state by rendering the game.
##### This code demonstrates how to play an Atari game, train a model using the A2C algorithm, and visualize the game using reinforcement learning techniques.


