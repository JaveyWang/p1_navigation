# Project1 - Navigation (Udacity DRLND)
This is a project that trains a agent that can navigate in the collect bananas task. ([details](https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation))

## Requirements
1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
2. Place the file in the `p1_navigation/` folder, and unzip (or decompress) the file. 

3. Packages
    - torch==1.4.0
    - unityagents==0.4.0
    - numpy==1.18.1

## Getting Started
* navigation.ipynb - training code
1. We implement a Double-DQN algorithm which selects action and evaluates action using seperate networks. More details can be seen in model.py file.
2. The network architecture is a 4 layers fully-connected network along with the ReLU activation function, the number of output units are 256, 128, 32, 4 respectively.
3. Hyperparameters. The code is similar to the DQN excersise solution, except for the hyperparameter TAU, we set it from 1e-3 to 5e-3 for updating the target network much faster, because this Pick-Banana task need less episodes to convergence (up to 2000).

* report.ipynb - 
Provide a description of the implementation and plot average reward curve that using the pretrained model weights.

* model.py - network and agent using Double-DQN algorithm.