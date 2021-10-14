# Continuous Control with deep reinforcement learning

## about
This repository is an implementation of deep reinforcement learning,
for the second project of [Udacity Nanodegree program "Deep Reinforcement Leraning."](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893)
The environment is based on "[Unity Reacher](https://github.com/ostamand/banana-collector)".
where an agent is a robot arm with double joints
and its hand is required to follow a moving target.

## environment
 - states : The state consists of 33 kinds of values,
 including the agent's position, rotation and angular momentum of the arm
 - actions : There are 4 variables with continuous values as the agent's action,
 corresponding to torque for the two joints.
 Each value should be between -1 and 1.
 - rewards : +0.1 for each time step if the agent's hand is in the correct position 
 (close to the target)
 - This is treated as an episodic-task problem with 1000 time steps,
 and the agent is required to get an average score higher than +30
 over 100 consecutive episodes.
 - In this project, there are two choices of the environment:
 a single agent option and an option with 20 identical agents.
 In this repository, the single agent option is used. 

## installation
You need to work with python 3.6.13.
Otherwise, you may fail installation some package,
especially an old version of tensorflow.
In addition, it is recommended to create with a new virtual environment
and work in it for the following processes.

[Unity ML-agents](https://github.com/openai/gym) and numpy need to be installed in adavance. 

```
pip install gym
pip install gym[box2d]
```

You also need to download a zip file of the Unity environment as follows:
 - [for linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
 - [for mac](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
 - [for 64-bit windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
 - [for 32-bit windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

It is convenient to unzip the downloaded zip file above
under the repository directory you will create next.


Then, after cloning this repository, go to the "deep-reinforcement-learning" submodule and install necessary libraries as below:

```
git clone https://github.com/maedamaeday/UdacityRL_p2.git --recursive
cd UdacityRL_p2/deep-reinforcement-leraning/python
pip install .
cd ../../
```

Note that you need "--recursive" option in cloning the repository
to incorporate deep-reinforcement-learning submodule properly.

Finally, create IPython kernel as below to run ipynb files:

```
python -m ipkernel install --user --name env_name --display-name "env_name"
```

Please replace "env_name" with your virtual environment.

## run training and watch trained agent actions
"my_Continuous_Control.ipynb" is the main file of this repository.
The notebook provided by Udacity is modified for thie repository.

Before running the notebook,
you need to specify the Unity environment in the cell #2,
following instructions in the notebook.

The details of the model architecture, training method and its performance is
summarized in [Report.md](Report.md)