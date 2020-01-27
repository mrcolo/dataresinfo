
# Start project

  

First and foremost you'll wanna install gym on your conda env. For whoever wasn't able to follow through with their installation of conda, no worries! Just [click here and follow the steps](https://docs.conda.io/projects/conda/en/latest/user-guide/install/)

  

Basically, create your environment

  

```c

conda create -n <name_of_your_project> python=3

```

  

and install gym

  

```c

conda install -c akode gym && conda activate <name_of_your_project>

```

  

As explained today, we are building a game of roulette. Luckily, Open AI gym already has a built-in, noob style environment of Roulette. Your job is to initialize a file **env.py** where you setup the environment and run for a certain number of time_steps.

  

Just follow the guidelines. Here's a basic implementation (this can be prettier)

  

```python

import gym

env = gym.make('CartPole-v0')

env.reset()

for _ in  range(1000):

env.render()

env.step(env.action_space.sample())  # take a random action

```

  

You should be able to find the env that we need pretty quickly. Careful though, there's going to be a bug, because Roulette's render method is not implemented (yet!)

  

It would also be nice and good practice to implement a [logger](https://docs.python.org/2/library/logging.html)

  

this should be pretty easy.

  

Easy things to implement to get you started:


- Implement a render method for Roulette. This should be pretty easy to achieve if you create a sub class of the Gym Roulette environment and just override render with your own version (this could output to a logger that you define in the constructor of the class)

```python

import gym
from gym import spaces
from gym.utils import seeding

class  RouletteEnv(gym.Env):
	def  __init__(self, spots=37):
		self.n = spots +  1
		self.action_space = spaces.Discrete(self.n)
		self.observation_space = spaces.Discrete(1)
		self.seed()
	def  seed(self, seed=None):
		self.np_random, seed = seeding.np_random(seed)
		return  [seed]
	def  step(self, action):
		assert  self.action_space.contains(action)
		if action ==  self.n -  1:
			# observation, reward, done, info
			return  0,  0,  True, {}
		# N.B. np.random.randint draws from [A, B) while random.randint 		draws from [A,B]
		val =  self.np_random.randint(0,  self.n -  1)
		if val == action ==  0:
			reward =  self.n -  2.0
		elif val !=  0  and action !=  0  and val %  2  == action %  2:
			reward =  1.0
		else:
			reward =  -1.0
		return  0, reward,  False, {}

	def  reset(self):
		return  0
		
class  NewRoulette(RouletteEnv):
	def  __init__(self):
		super().__init__()

if  __name__  ==  "__main__":
	n =  NewRoulette()
	print(n.action_space, n.observation_space)

```

- Improve the environment just created by introducing a variable called budget, and then print to the screen how we did financially on a session of ts timesteps.

I think it would be cool if for next Monday we could all come up with personal ideas on how to make this more efficient. We will also have a mini lecture of 30 minutes on an algorithm that we could start to implement to control our environment.

Feel free to add tasks on Trello that you think would be fun to develop, or just do it and 

For questions, text me or email me ([fcolonnese@ucla.edu](fcolonnese@ucla.edu))