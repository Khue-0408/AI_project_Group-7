# **APPLYING AI INTO TETRIS**

## **MOTIVATION**

Our project aims to bring a new breath to Tetris - a classical arcade video game by integrating artificial intelligence. Motivated by the desire to explore AI's potential in gaming, we seek to enhance gameplay, showcase adaptive strategies, and contribute to the evolving landscape of AI-powered entertainment.

## **ALGORITHMS**

We trained our AI agent using ***Genetic Algorithm*** and ***Reinforcement Learning***.

### **Genetic Algorithm**

The training heuristics are developed and written in the ```field.py``` and ```genetic.py```.

The ```logs.txt``` file in ```Logs``` contains all of our training process, in which the number of tetrominoes is limited to 1000 per game.

Each individual in the population in the ```logs.txt``` file is represented into the following form:

```
[[score, lines cleared], [weights for the heuristics]]
```
You can access the ```DataVisualization``` folder and run ```DataVisualization.py``` for visualizing the training data.

When the training process ends, an ideal set of weights, is used in
```ai.py``` for selecting the most promising rotation and position for a tetromino.

### **Reinforcement Learning**

The ```src``` folder contains the core codebase, in which

- ```deep_q_network.py```: Initializes the Deep Q-Network for training.

- ```tetris.py```: Sets up the Tetris game environment.

Pre-trained models are available at: ```trained_models/tetris```. These can be used for immediate testing or further fine-tuning.

However, you can start training the model from scratch yourself by running ```train.py```

During training ( running ```train.py``` ), ```tensorboard``` is automatically created. The file inside will visualize collected data in the training process into graphs and metrics, helping you track and analyze the model's performance.

### **Installation & Running The Game**

**Requirements**:
* python 3.6 or higher
* PIL 
* cv2
* pytorch
* numpy
* matplotlib
* pygame

**Install external libraries**: In your terminal, run the following command to downloaded the required libraries:
```
pip install numpy
pip install pygame
pip install opencv-python
pip install torch
pip install tensorboardX
```
You are now able to observe the AI agent properly.

By running ```game.py``` in 
        
* ```GeneticAlgorithm``` folder: Tetris will be played by the AI agent which is developed using genetic algorithm.

*  ```ReinforcementLearning``` folder: Tetris will be played by the AI agent which is developed using reinforcement learning

* ```requirement.txt``` folder:
```bash
$ pip install -r requirement.txt
```
 





