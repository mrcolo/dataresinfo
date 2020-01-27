# Research@Datares - Winter 2020

## The problem

This quarter you're gonna work on a computer vision problem. In order to solve these types of problems, we often use a Convolutional Neural Network, similar to the one  you "fixed" in our challenge. 

In specific, we are gonna work on the [comma.ai speed_challenge](https://github.com/commaai/speedchallenge).

The challenge provides us with a video of a car running, where every frame contains a label with the speed of the car at frame *f*. 

Our task is to create a network to model video frames in correspect to speed of the car, so that, in the end, we can just input a video and be able to output the current speed of the car. 

### Ok, but how?

This is clearly not a straight-forward problem to tackle. A hard-coding solution would be to pull out the GPS of the car at frame *f* and try to compute out the difference, which indicates its position. From there, we could take a derivative which would correspond to the car's speed. 

Hard-coded solutions [are not cool anymore](https://medium.com/@karpathy/software-2-0-a64152b37c35). So let's try to find an alternative. 

Let's think about what we want to achieve:  we want to exploit the ease of implementation of so-called "function approximators" (neural nets), to match video frames to continuous values (speed).

Uhm. 

This problem appears to be very intriguing when approached with a "neural perspective". 

If you start thinking about the way humans drive, you'll notice that after a person gets used to their own car, they don't really pay much attention to their current speed, but just kind of "know" when to speed up and down. This intuition makes us think that modeling a neural network to do the same thing is "possible".

#### Team Organization

We will structure our workflow with **two** different teams, which will attempt to use different strategies to achieve state of the art results on this dataset. 

The first team will attempt to solve the problem just by using fast.ai, which shouldn't be too harsh in terms of software development. So, if you feel like you'd rather learn the basics of deep learning  you should join **Team LeCun**.

If you like a challenge and feel like you understand deep learning a little better, consider joining **Team Hinton**, which will implement a more complicated (and fun!) network. For this implementation, we will use and familiarize ourselves with PyTorch. 

The two teams are structured to balance the difficulty in the two implementations. Both teams should have the same the same ability to reach success: 

Below is an accurate description and tentative schedule of our work as a team. 

## The Teams

#### Team LeCun

This team, which takes the name from the inventor of ConvNets, Yann LeCun, will deal with an implementation that uses fastai. A newbie to AI might think that concise, short code is weaker than a PyTorch implementation. This is inherently wrong: people have been able to achieve [state of the art results](https://www.fast.ai/2019/05/03/decrappify/)

with the library that you used to pass our challenge. 

The cool thing about fastai is that, with it, we have access to several pretrained networks that can boost our performance up. This technique is called "transfer learning". The idea is for you to use a pretrained ConvNet

In specific, our workflow will consist of the following deadlines: 

| Progress                                                     | Deadline        |
| ------------------------------------------------------------ | --------------- |
| Part 1: Create a program that takes a video and processes its frames into images with corresponding speed into an ImageDataset (or similar data structure) | Week 3 - Week 4 |
| Part 2: implement a simple network that processes the dataset into an ImageDataBunch | Week 4 - Week 5 |
| Part 3: Use the network to train it on the dataset and start accumulating data of your different trials. | Week 6 - Week 7 |
| Part 4: Win the challenge! Adjust your hyper-parameters, do as you like and get creative to achieve better accuracy than the other team! | Week 8 - Week 9 |

#### Where do I start?

Your starting point is to read about how to predict continuous values using the fastai library. Think about what you are trying to achieve here: 

You are inputting an image in the network (a frame) and hope to get a scalar value in return; in other words, you are trying to predict continuous (and not discrete, like a classification task) values. This task shouldn't be too hard, as it will give you the ability to understand how to setup a proper dataset for a fastai network.

[This discussion](https://forums.fast.ai/t/prediction-of-a-scalar-with-a-cnn/26714) contains the solution you're looking for. 

As for now, your program should just be able to ouput a dataset with video frames in it. 

#### Team Hinton

This team, which takes the name from the inventor of neural nets, Geoffrey Hinton, will deal with an implementation that uses a relatively recent paper from Facebook AI. 

The biggest flaw of supervised learning is the inherent bias that is introduced when feeding data that was labeled by a human.

Facebook AI found a way to achieve state of the art results in image classification (a computer vision problem!) using a very interesting technique called semi-supervised learning.

You can learn more about it by reading [this paper.](https://arxiv.org/abs/1905.00546)

| Progress                                                     | Deadline        |
| ------------------------------------------------------------ | --------------- |
| Part 1: Create a program takes a video and processes its frames into images with corresponding speed. | Week 3 - Week 4 |
| Part 2: Use a network (teacher) trained on a bigger dataset to label samples that are going to be used to train another network (student) | Week 4          |
| Part 3: Improve the student teacher model in the way described by the paper | Week 5          |
| Part 3: Train a few models and start accumulating data of your different trials. | Week 6 - Week 7 |
| Part 4: Win the challenge! Adjust your hyper-parameters, do as you like and get creative to achieve better accuracy than the other team! | Week 8 - Week 9 |

Your starting point is to read this awesome paper by Facebook AI. 

Also, try to familiarize yourself with PyTorch and DataLoaders. You can learn more about this by visiting 

[this link](https://discuss.pytorch.org/t/how-preprocess-video-and-work-with-that/20569) and looking at the code for [this example](https://github.com/NVIDIA/nvvl/tree/master/examples/pytorch_superres)

## Questions?

Please be aware that this schedule is temptative and there might happen changes, here in there. 

Also, make sure to **email me your team choice by tonight**.

We are planning to have 7 people on each team, so make sure to let us know as soon as possible so that we can accomodate everybody's preference :)

All we hope as Research@DataRes is that you guys are gonna have fun competing against each other and  could actually achieve good results on the challenge.

Our first commits, as the schedule says, are due **at the end of the next week.** 

Don't hesitate to ask me any questions through slack or my email, fcolonnese@ucla.edu

