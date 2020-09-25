---
layout: post
title: Deep Learning and tailoring a model to the system 
---

Deep Learning
=============

The last 15 years has seen an incredible increase in the power of artificial intelligence systems. It is increasingly recognised that AI is going to be a very significant part of future data analysis. In tandem with this, the terms Machine Learning and Deep Learning have become common. The three terms are often used interchangeably, however they represent distinct concepts.

**Artificial Intelligence** is a system that has learnt a relationship using a training method. From the earliest neural networks emplying gradient descent to optimise a handfull of neurons to a newer convolutional neural network trained using Bayesian parameter optimisation, they share a characteristic: the training process tailors the model to fit the data. Once the training stops, the model ceases to adapt.

In **Machine Learning**, the model is considered to be "on line". This does not mean on the internet, instead it means that the model receives feedback during its use and uses that feedback to refine its operation. In practical terms, the feedback is used to continually refine the models internal parameters. This model continues to learn.

**Deep Learning** employs networks that have many layers and attempt to mimic, in some way, the operation of biological systems (such as visual systems). Essentially, a Deep Learning system is a network with many layers.

The danger of buzzwords
=======================
The ability of these systems to exhibit complex behaviours is astounding, and it has captured the imagination of people in many different fields. Unfortunately, like many new concepts, the idea can run away from the reality. I have worked with businesses who have strongly desired to include "Machine Learning" and "Deep Learning" in their products, without really having a clear idea why they wanted it or how they thought it would help them.

In one situation, I was strongly reminded of a washing powder commercial, and could imagine a shiny sales rep telling me that their washing powder was better because it contained "Deep Learning"!

![_config.yml]({{ site.baseurl }}/images/washPowder_with_deepLearning.png)

The Limits of Machine Learning and Deep Learning
================================================
At heart, what we are talking about here, are models. They accept input, and produce an output -- hopefully an output that conforms to the real world in some useful way. The model does this by performing a series of operations on the input, and these operations are governed, internally, by parameters that control how the model works. These parameters have generally been "learned" during the models training process.
An important concept to understand, when discussing a model, is that the more parameters the model has, the more sophisticated and complex the model is, the more complex is its representation of a system and **the more data are required to train it**.

If we consider a very simple system, and want to model it by a linear equation, then the model could have the form

y = mx + c

where the output, _y_, is equal to the input _x_ multiplied by the learned parameter _m_ and offset by the learned parameter _c_. Hence, this model has two parameters that need to be learned. In theory, this model needs two data points to ascertain these parameters.
However, if we want to build a quadratic model instead, eg.

y = ax^2 + bx + c

then the three parameters (_a_, _b_, and _c_) cannot be ascertained with only two data points -- we need at least 3.

I have not discussed statistical power yet, but with real data there are always noise -- our ability to estimate parameters is limited by our ability to measure input and output data accurately, as well as the amount of confounding that is occuring. In essence, for a given amount of data, the simpler the model (and the fewer parameters it contains) then the more accurate will be our estimates of its parameters, and the more certain we can be that our model corresponds to something that is actual rather than being a quirk of the data.

What does this mean in practical terms?
=======================================
Artificial Intelligence and Machine learning are great tools (I have worked with AI and ML since about 2005), but they are not always the best tool for the job. There are many, many situations where a simple linear or non-linear model (which might have 1/1000th the number of parameters or less) can be a better choice -- even for situations where the real world system seems complex. Often, there are physics principles that can be exploited to help us better model the system with a simpler model. Such a model will be 
 - simpler, 
 - cheaper, 
 - require a smaller data set to train, and
 - be understandable/comprehensible.

These are significant advantages.

So why is Machine Learning and Deep Learning popular?
=====================================================
Simply, Machine Learning and Deep Learning are able to represent systems that linear and non-linear models simply can not model.
There are times when they are the right tool for the job. I have worked on and supervised students on projects that absolutely have required the use of Machine Learning and Deep Learning systems, that would not have been possible otherwise. But they are not always the best option. In particular, if your problem requires such systems, you should expect at minimum to be collecting thousands of data points.

Summary
=======
Every tool has pros and cons. A sledge-hammer is sometimes necessary, but one would not use a sledge hammer to hang a painting in one's lounge room! Make sure you are clear, at the outset, about what you want from your model, and how you want it to work. The more you know about the system you are attempting to model, the simpler your model can often be. I have much experience in this area, and am happy to advise.

If you would like help with constructing models of complex systems, please contact me.

![_config.yml]({{ site.baseurl }}/images/business_card_front.png)

This article is Copyright 2020 by Angus Wallace.
