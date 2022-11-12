# svtranga-SARSA-with-Function-Approximation

In this project, we will be performing SARSA with Linear approximation on Frozenlake, cartpole and lunar lander environment. 

**Package installation:**

- We need to install gym before running this code.
  - Use the command *pip install gym* to install
- We need to install Box2D. Use the below commands for installation:
  - *!pip install Box2D* 
  - *!pip install box2d-py* 
  - *!pip install gym[all]* 
  - *!pip install gym[Box\_2D]* to install

**About the environment:**

**FrozenLake:**

- There are four actions: LEFT, UP, DOWN, RIGHT represented as integers from 0-3. Since we are using a 8X8 map, there will be 64 states. 
- The environment is non-deterministic and there is an equal probability of landing in the neighboring three states. 
- The episode ends when we reach a goal or a hole
- We get a reward of 1 whenever we reach the goal. When we end up in a hole, we are stuck and the episode ends with 0 rewards

**Cart Pole:**

- There are two actions: LEFT, RIGHT represented as integers from 0-1. There are infinite number of states in cartpole but for our assignment we have restricted to 10000 
- The goal of the game is to prevent the cartpole from falling
  - The episode will end when the pole is > 15 degrees from vertical, or the cart moves > 2.4 units from the center
- We get a reward of 1 for every step we take that helps the pole stand upright

**Lunar Lander:**

- We can get the coordinates from the first two numbers in state vector. 
- Episode will end if the lander crashes or comes to rest, we get additional reward of -100 or +100

**Functions used:**

- prepFrozen()
  - Initializes an 8X8 frozenlake environment 
- quality():
  - Calculates the average rewards across all episodes
- policy\_eval():
  - Helper function that calls the quality function
- getdecayfactor ():
  - Takes in the episode, min and max epsilon as input and gives the decay factor 
- take\_action\_prob():
  - Take action based on e-greedy
  - Uses probabilistic approach in taking an action when there is a tie
- Q\_value():
  - Calculates the Q value from phi and w
- sarsa\_func\_approx ():
  - Function to implement SARSA with linear approximation
- prepCartPole():
  - Initializes a cartpole environment
- prepLunarLander()
  - Initialized a lunar lander environment
- frozenPhi8(), frozenPhi4(), LunarPhi()
  - Gives the phi value at state s


- References:
  - <https://www.coursera.org/lecture/prediction-control-function-approximation/expected-sarsa-with-function-approximation-q7z0G>

