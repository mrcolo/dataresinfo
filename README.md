

#  Introduction and Colabs

Regardless of your previous experience with neural nets, AIs can be really easy to implement. Take as an example this course by Jeremy Howard, [fast.ai](http://fast.ai)

When I'll show you content, I'll most likely use Google Colab (Jeremy Howard uses Jupyter, same thing but local). Take a look at these notebooks to learn more about them. Basically, they allow you to run code in cells. I feel like this is a great way for me to show you code interactively and I'd highly recommend you check it out!

- [introduction to colabs (and python)](https://colab.research.google.com/github/tensorflow/examples/blob/master/courses/udacity_intro_to_tensorflow_for_deep_learning/l01c01_introduction_to_colab_and_python.ipynb)

- [introduction to pandas (visualizing stuff is cool!)](https://colab.research.google.com/notebooks/mlcc/intro_to_pandas.ipynb)

Hopefully at this point you got a gist of Python (for whoever wasn't fresh already).
If you have ANY question about code, you know you can message me at [fcolonnese@ucla.edu](fcolonnese@ucla.edu) at any time. 

Following is a list of projects I think would open up to a lot of cool add-ons:

# Project 1 & 2 - Sequence Predictions
The idea for these projects is to use different AIs to predict the value of *insert_something* at the next time step. 

**How are we gonna do it?**
This is a sequence prediction problem. When it comes to [neural networks](https://www.youtube.com/watch?v=ILsA4nyG7I0), there's a branch of them called recurrent neural networks that can predict, provided with an array of timesteps t1 to tx, the value of a function at timestep x + 1. In specific, we should start this project by using an [LSTM](http://karpathy.github.io/2015/05/21/rnn-effectiveness/), which is just a fancier name for a recurrent neural network, as that great post by Andrej Karpathy explains. 

**In practice...**
In practice we are going to use a framework called [Keras](https://keras.io/) that has a prebuilt version of this neural network. The tasks, in your case, would be: 

 - To understand what we are dealing with. Experiment with Keras and google a colab that works with the framework. [or click on this link i guess](https://colab.research.google.com/github/zaidalyafeai/zaidalyafeai.github.io/blob/master/sketcher/Sketcher.ipynb) 
 - To not panic if this stuff does not make sense at all. Again, just email me and we can talk about it before the mext meeting.

Now, for the projects:

## Stock Predictor
A RNN that predicts the value of the stock price the next day. 
For training, the neural net takes as input a [dataset with a lot of tickers](https://www.kaggle.com/borismarjanovic/price-volume-data-for-all-us-stocks-etfs) and outputs a value corresponding to t + 1. The hardest task with this problem is literally to understand [how to implement an LSTM in Keras](https://towardsdatascience.com/understanding-lstm-and-its-quick-implementation-in-keras-for-sentiment-analysis-af410fd85b47) and be able to process data to be inputted in this specific architecture. 

## Peer Review Text Generator
An RNN that predicts the next word and gets trained on a large dataset of peer reviewed articles scraped from the databases we have access to as students at UCLA. Again, take a look at Karpathy's article at the top where he scrapes the entire work of Shakespeare and makes it predict the next letter. 
Later on, we can think of using [GPT2](https://openai.com/blog/better-language-models/) to achieve a better quality. 

# Project 3 & 4 - Classification

## Classification project 1 
More on this later. 
## Classification project 2
More on this later. 

# Project 5 - Generative Adversarial Networks to predict a kid's face from two adult's faces

[This](https://arxiv.org/pdf/1702.01983.pdf) is a great attempt at using generative adversarial networks to alter an input to the generator. For whoever is not familiar with it, I encourage you to look at [this article](https://skymind.ai/wiki/generative-adversarial-network-gan) which explains pretty well the idea of a GAN. I would like to point out that you cannot find a lot about this online, so this would be a really cool project. 

More on this later. 