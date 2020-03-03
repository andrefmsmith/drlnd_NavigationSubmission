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
**1.** Clone this repository.  
**2.** Download the environment from the appropriate link for your operating system:  
- [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- [Mac OS X](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- [Windows (32-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- [Windows (64-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip) 
  - [Not sure which version of Windows you have?](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64)  

Place the downloaded file 



environment.

Place the file in the DRLND GitHub repository, in the p1_navigation/ folder, and unzip (or decompress) the file.

The README has instructions for installing dependencies or downloading needed files.
The README describes how to run the code in the repository, to train the agent
