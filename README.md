# Submission for Project 1 of Udacity DRLND: Navigation

## Introduction and task overview
In this project, we will train an agent to navigate and collect bananas in a Unity environment, which is a bounded square arena. The agent is free to move within the arena, and in it it will encounter blue and yellow bananas.  
![](bananas.gif)  
The task has an episodic structure.

### Reward structure
Collecting a yellow banana results in a reward of +1, whereas a blue banana gives a reward of -1. The agent's goal is to move in the environment collecting as many yellow bananas as possible, whilst avoiding the blue ones.

### State and Action Space
The state space is a 37-dimensional vector and the values within this vector are **continuous**. They report the agent's velocity and ray-based perception of objects, amongst other variables. 
Here is an example of a state vector:  

![](states.png)  

The action space is **discrete** and contains 4 actions:
- ```0```: move forward
- ```1```: move backward
- ```2```: turn left
- ```3```: turn right

### Solving the environment
The environment is solved when the agent averages a **score above 13 over 100 consecutive episodes**.  

## Setting up
**0.** To run the exact same environment I used for this repo, please follow the instructions [here](https://github.com/udacity/deep-reinforcement-learning#dependencies).  
**1.** Clone this repository.  
**2.** Download the environment from the appropriate link for your operating system:  
- [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- [Mac OS X](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- [Windows (32-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- [Windows (64-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip) 
  - [Not sure which version of Windows you have?](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64)  

Then, unzip the downloaded file into a convenient directory and take note of its path. We will point to in in this repo's code.  
**3.** You may need to install Unity. Please follow the steps indicated [here](https://github.com/Unity-Technologies/ml-agents/blob/latest_release/docs/Installation.md)

## Training the agent
The Jupyter Notebook ['Report'](https://github.com/andrefmsmith/drlnd_NavigationSubmission/blob/master/Report.ipynb) provides a detailed walkthrough explaining the algorithm used and how the code written to implement it ['TrainingCode'](https://github.com/andrefmsmith/drlnd_NavigationSubmission/blob/master/TrainingCode.ipynb) works.  

To train an agent to solve this environment, you should open the ['TrainingCode'](https://github.com/andrefmsmith/drlnd_NavigationSubmission/blob/master/TrainingCode.ipynb) Jupyter Notebook and run the code cells in it.  
**Important notes:**
- Remember to change the variable ```env = UnityEnvironment(file_name=" ")```, found in the code block titled **Setup**, to the path pointing to your downloaded and unzipped copy of the 'Banana' environment;
- When defining the ```QNetwork``` class under code block **QNetwork Class** you can change the number of units per hidden layer by setting ```fc1_units``` and/or ```fc2_units``` to whichever integer value you'd like. You could also change the depth of the network by adding new layers, in which case you should specify them both in ```__init()__``` and ```forward()``` methods.
- In the code block **Hyperparameters and GPU**, you can change hyperparameter values and decide if you'd like to train using CPU or GPU
- When beginning training, in block **Train & Plot results**, control whether you'd like to save a checkpoint by setting the ```dqn``` training function argument ```output_toggle``` to True or False. If you choose to save a checkpoint, define its title with the argument ```output```.
