
  

# Introduction and Colabs

  

Regardless of your previous experience with neural nets, AIs can be really easy to implement. Take as an example this course by Jeremy Howard, [fast.ai](http://fast.ai)

  

When I'll show you content, I'll most likely use Google Colab (Jeremy Howard uses Jupyter, same thing but local). Take a look at these notebooks to learn more about them. Basically, they allow you to run code in cells. I feel like this is a great way for me to show you code interactively and I'd highly recommend you check it out!

  

-  [introduction to colabs (and python)](https://colab.research.google.com/github/tensorflow/examples/blob/master/courses/udacity_intro_to_tensorflow_for_deep_learning/l01c01_introduction_to_colab_and_python.ipynb)

  

-  [introduction to pandas (visualizing stuff is cool!)](https://colab.research.google.com/notebooks/mlcc/intro_to_pandas.ipynb)

  

Hopefully at this point you got a gist of Python (for whoever wasn't fresh already).

If you have ANY question about code, you know you can message me at [fcolonnese@ucla.edu](fcolonnese@ucla.edu) at any time.

  

Following is a list of projects I think would open up to a lot of cool add-ons:

  

# Project 1 - Sequence Prediction

  

The idea for this project is to use different AIs to predict the value of *insert_something* at the next time step.

  

**How are we gonna do it?**

This is a sequence prediction problem. When it comes to [neural networks](https://www.youtube.com/watch?v=ILsA4nyG7I0), there's a branch of them called recurrent neural networks that can predict, provided with an array of timesteps t1 to tx, the value of a function at timestep x + 1. In specific, we should start this project by using an [LSTM](http://karpathy.github.io/2015/05/21/rnn-effectiveness/), which is just a fancier name for a recurrent neural network, as that great post by Andrej Karpathy explains.

  

**In practice...**

In practice we are going to use a framework called [Keras](https://keras.io/) that has a prebuilt version of this neural network. The tasks, in your case, would be:

  

- To understand what we are dealing with. Experiment with Keras and google a colab that works with the framework. [or click on this link i guess](https://colab.research.google.com/github/zaidalyafeai/zaidalyafeai.github.io/blob/master/sketcher/Sketcher.ipynb)

- To not panic if this stuff does not make sense at all. Again, just email me and we can talk about it before the next meeting.

  

Now, for the projects:

  

## Stock Predictor

  

An RNN that predicts the value of the stock price the next day.

For training, the neural net takes as input a [dataset with a lot of tickers](https://www.kaggle.com/borismarjanovic/price-volume-data-for-all-us-stocks-etfs) and outputs a value corresponding to t + 1. The hardest task with this problem is literally to understand [how to implement an LSTM in Keras](https://towardsdatascience.com/understanding-lstm-and-its-quick-implementation-in-keras-for-sentiment-analysis-af410fd85b47) and be able to process data to be inputted in this specific architecture.

  

# Project 3 - Classification

  

For these problems, we are gonna be dealing with a classification task. That means that based on on our inputs, we are gonna classify a data entry in a certain number of classes.

For whoever is not familiar with classification using neural nets, [here's a very interesting Medium article](https://towardsdatascience.com/classification-using-neural-networks-b8e98f3a904f) that I think you should check out in case you're interested with this project.

  

## Giving predictions on the restaurants you will like based on the ones you have visited

  

In my spare time I love to find new places to dine at. Problem is, many times you explore a new area and you really don't know what to eat. Easiest solution: pull out your phone and open Yelp. Now, as appealing as it may sound, many times I was disappointed with the restaurant I picked. This was, for the most part, due to the fact that I didn't like their menu. So let's fix that.

  

**In practice...**

The idea for this project is to create a neural net to predict the rating (1 to 5) that a user would probably give to a restaurant based on several pieces of information, scraped from [Yelp's AWESOME dataset](https://www.yelp.com/dataset)

  

**Also!**

This project would have a lot of opportunities to be expanded.

  

For my fellow CS/Tech majors that are familiar with web development, we could also create a web app to gather data about a user in an easier way. Again, hit me up if interested.

  

Additionally, we could run a [Convolutional Neural Network](https://towardsdatascience.com/a-comprehensive-guide-to-convolutional-neural-networks-the-eli5-way-3bd2b1164a53) to understand how much the person will like food pictures from the restaurant even prior to seeing them and include that in the assessment of our rating.

  

# Project 3 - Reinforcement Learning

  

This branch of machine learning is probably one of the most interesting and, at the same time, obnoxious ones. Basically, as explained in the meeting, an agent interacts with an environment and, through the use of a policy, makes decision which are aimed at maximizing a value. More on this [here](https://towardsdatascience.com/reinforcement-learning-demystified-36c39c11ec14)

  

**ok, but in practice?**

In practice we are gonna start by using frameworks that make our life easier. There's always going to be time to replace the framework with a home-made implementation of an environment or agent.

Probably one of the most important frameworks when it comes to reinforcement learning is [OpenAI Gym](https://gym.openai.com/), which provides a variety of environments and emulators to experiment with.

  

**and for the algos?**

We have a lot of choices when it comes to reinforcement learning algorithms. Again, frameworks are your friends, when learning the basics! [Stable Baselines](https://github.com/hill-a/stable-baselines) gives you access to an innumerable amount of algorithms.

  

In specific, I would suggest you experiment with [DQNs](https://medium.com/@jonathan_hui/rl-dqn-deep-q-network-e207751f7ae4) or [PPO](https://openai.com/blog/openai-baselines-ppo/).

  

## Make an AI play Roulette

  

The game of [Roulette](https://www.youtube.com/watch?v=ru2bYDG2FBw) is one of the most played games at casinos. Our job is to experiment with several different agents and understand which one can play best and why. This project would be rather simple to implement, given the amount of frameworks available in terms of reinforcement learning BUT would allow for a lot of expansion as implementing our own versions of the algorithms would always allow for more control over the entire system (and debugging process, which for RL is key)[Link to an awesome environment for roulettes](https://gym.openai.com/envs/Roulette-v0/)

  

# Project 4 - Generative Adversarial Networks 
  

This project is sort of an extra. I spoke to a few people that were interested in working with a [generative adversarial network](https://www.wikiwand.com/en/Generative_adversarial_network)

  

[This](https://arxiv.org/pdf/1702.01983.pdf) is a great attempt at using generative adversarial networks to alter an input to the generator. For whoever is not familiar with it, I encourage you to look at [this article](https://skymind.ai/wiki/generative-adversarial-network-gan) which explains pretty well the idea of a GAN. I would like to point out that you cannot find a lot about this online, so this would be a really cool project.

Basically, the way a GAN works is by using two neural networks (full explanation of what an nn is in the introduction). One acts as a discriminator, the other one as a generator. The generator in this case is supposed to create data (randomly or, as in our case, from predefined inputs) that resembles a specific distribution, which is being inputted to the discriminator. Think of the discriminator as a detective who looks at mini batches of real data where, every once in a while, we plug in a fake datapoint created by the generator. The goal of the generator is to foul the discriminator in thinking the data is real. The discriminator, at the end of line, just outputs a probability of how real the data is.

## Predict a kid's face from two adult's faces
Our job in this case would be to input two images of adults and output another image, which corresponds to the hypothetical kid that those two people would have. 

**how are we gonna do this?**
As that article from NVIDIA states, one could make use of conditional generative adversarial networks to be able to access the input of the generator. In this way, one could input two images and see what happens. 


# Conclusion
Alright! If you made it here it means you watched a lot of videos and googled a lot of stuff. Congrats. Make sure to email me at [fcolonnese@ucla.edu](fcolonnese@ucla.edu)  with your preference and I'll make sure to assign all the groups before our next meeting. 

See ya!
