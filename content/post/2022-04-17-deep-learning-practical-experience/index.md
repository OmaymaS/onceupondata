---
title: NOT Just Tweaking Some Parameters
subtitle: 'What data practitioners talk about when they talk about deep learning '
author: ''
date: '2022-04-17'
slug: [deep-learning-practical-experience]
categories: []
tags: [machine learning, algorithms, deep learning, Convolutional neural networks]
type: ''
---
**In the world of data science and machine learning, people tend to talk about the shiny stories, publishable methods, state of the art experiments, the rainbows and butterflies. In reality, practitioners struggle with lots of challenges while learning and applying new methods, but their practical lived experiences are rarely shared for different reasons.**

I was recently following one of the few examples, in which someone shared their journey to the world of deep learning, without a lot of filtering. In [Not So Standard Deviation](https://nssdeviations.com/), the podcast [Roger Peng](https://twitter.com/rdpeng) co-hosts with [Hilary Parker](https://twitter.com/hspter), Roger explained his thought process and experiments with a specific use case involving images used to predict air pollution levels. He described the practical caveats which are under-documented in the online material directed to anyone who is starting with model development including machine learning, deep learning or whatever people call them at any point!

I found this experience sharing very valuable in a field that lacks such informal discussions, as Roger did bouncing ideas with Hilary and [Lucy](https://twitter.com/lucystats). I decided to take this blog post as an opportunity to talk about different points, inspired by Roger’s comments but not limited to them. So here are some statements that may come from anyone who goes through a similar experience:

- **I have NO mental model/intuition about how deep learning works.**
- **I don’t have a clear strategy for hyperparameters selection/tuning.**
- **I cannot experiment quickly because an iteration takes a long time.**
- **I am not sure what to do after training a model and checking the metrics.**
- **I find all computer vision examples about classification.**

In the following sections, I’ll share my perspective on some of these points.

## Developing a mental model of deep learning

When it comes to dealing with deep learning or any complex models, I believe there are different types of people. Two of the most common groups as per my observations are:

1. The type that doesn’t care about how things work as long as they get good results on their test data and new instances once they put their models into production or win a competition. They have their arguments and perspective on why it doesn’t matter.

2. The type that really cares about the inner workings of models and appreciates having good intuition about any tool they are using. They might even feel irritated as long as they don’t have a good grasp of a certain method even if it outperforms others. 

I belong to the second group. That’s why I can relate to experiences through which people go, while getting *“deeply”* into deep learning. 

When I started to experiment with deep learning a few years ago, I had this inner repulsion towards it because I couldn’t completely get comfortable dealing with a black box. The "Getting Started" tutorials were not satisfactory. What altered this feeling **a bit** was gaining a better understanding of how it worked and what to expect, by going through the math and building better intuition. 

I’d recommend you diversify your sources. It will take a bit of time, but you’ll be able to gather the bits and pieces from different perspectives. I’d say the following are some of the good resources, mainly focusing on computer vision:
 
- **Stanford Course CS-230/1** [Cheat Sheet on Convolutional neural networks (CNN)](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-convolutional-neural-networks) and [material](https://cs231n.github.io/convolutional-networks/) (+[lectures](https://youtu.be/bNb2fEVKeEo)). If you’d like to have a visual representation of concepts like convolution layers, filters, padding, pooling, etc. you’ll find this helpful.

- **Fastai material by Jermey Howard** *([fastai](https://www.fast.ai/) is a high level API on top of pytorch)*. For instance [this part](https://www.youtube.com/watch?v=9C06ZPF8Uuc&t=2996s) simplifies the concept of a convolution layer and filters (+[relevant material](https://github.com/fastai/courses/tree/master/deeplearning1/excel)).[^1] 

- **Brandon Rohrer's** [material on CNN](https://end-to-end-machine-learning.teachable.com/courses/516029/lectures/9533964).

## Model/Hyperparameter tuning

After gaining better understanding, it is normal to feel overwhelmed by the amount of parameters and combinations. So how to pick the hyperparameters is a valid question to ask. The short answer is: **it’s a mix of experimentation, mostly starting with recommended values used in libraries like keras/torch/fastai for specific problems.** In practice, there are different levels of control and strategies from starting with default values to AutoMl.

### Start with default values

It is worth noting that the common start point is the high level APIs that allow you to use a pre-trained model with known architecture like Resnet as a base for your model. So you are not expected to build something from scratch when you have the option to use transfer learning, as long as it fits your use case and goals.

### Use your domain knowledge to improve your strategy
Apart from the default values you can develop a better strategy of hyperparameters tuning especially if you know the properties of your data. So if you are working with images, you should have some hypotheses about the transformations *(e.g. cropping, squishing)* or data augmentation *(e.g. flipping, rotating)* options to avoid. I assume that your curiosity already led you to read about data augmentation but if not, I recommend you have a look and play with the options using your library of choice. 

### Automate hyperparameter tuning if applicable

The other extreme is to automate your experiments by giving a range of values, similar to the process used with other tree-based models. You can just specify different combinations of hyperparameters, or use AutoML tools to do this for you in a more efficient way. This can be done once to get the best values in order to use them with this type of data. If you reach this point, it is definitely better to do it on an instance with good resources in terms of memory, GPU, etc. You’ll find tools on cloud platforms that make the process easier (e.g. [GCP](https://cloud.google.com/vertex-ai/docs/training/using-hyperparameter-tuning)). Also open source libraries like [AutoGluon](https://auto.gluon.ai/stable/index.html) usually provide examples about [cloud training](https://auto.gluon.ai/stable/tutorials/cloud_fit_deploy/cloud-aws-sagemaker-training.html). 

I’d say that you don’t have to jump immediately to Automl because it is a time/resource consuming process and there’s usually something to do with the data first to improve your results. But whatever strategy you take, you may still wonder about what to do after checking the model performance and looking into the metrics. 

## What to do after checking the metrics

I believe the strategies here are not limited to deep learning models. It is about any model development process. Assuming that you had a baseline model *(e.g. random predictions, linear model, etc.)* and the first iteration of your deep learning model *(or any other type)* gave you a better result but you’d like to try more. Some people will jump into changing hyperparameters or AutoML but as mentioned before, inspecting data is also a crucial part. 


### Refine your data

Talking about data and refining datasets was a bit undervalued in the data/machine learning community in the previous years although many did it in the background. It didn’t seem “cool” enough until recently when more groups started to talk about it like the [Data-Centric AI](https://datacentricai.org/), a concept that is highlighted as *“the discipline of systematically engineering the data used to build an AI system”*.

So as you look into residuals in linear models, you can check the “loss” value here and inspect instances with the worst predictions. Having the domain knowledge will help you form hypotheses about the failure points of the model. You might find out that there were irrelevant examples, wrong annotations, lack of coverage of different cases/classes etc. This should guide you to take action before the next training iteration. It could be:
- removing some examples.
- fixing your train/valid splits with similar distributions.
- correcting wrong annotations/target values.
- changing your data input format or quality.
- adding examples.
- questioning how your dataset was built in the first place! 


**What if you decided you needed to add more examples?**

1. Make sure that data comes with the same format, annotations are added based on the same guidelines, and all cases are represented in your train/valid/test datasets. 

2. Consider NOT to outsource the whole process to data curators/annotators with whom you don’t have any contact, *but dataset creation and annotation is a different story to write about!*

It is also useful to consider having several challenge datasets, and testing on unseen examples *(not included in the test data)* after you commit to a certain model to try it out in the wild. This depends on the type of your use case and the flow of data. 

### Revisit model hyperpatameters

While iterating, you'll find out that you might repeat the steps of refining data, adjusting  hyperparameters, etc. With more trials and exploration, you'll find some methods to reduce training time and improve performance like [**Learning Rate Finder**](https://fastai1.fast.ai/callbacks.lr_finder.html), [**Discriminative Learning Rates**](https://github.com/fastai/fastbook/blob/master/05_pet_breeds.ipynb) or other ideas. But try not to overwhelm yourself with everything at the same time.


## Problem framing (classification/regression)

Till now, everything mentioned here is about models in general. You might have noticed that most of the computer vision tutorials online are about **image classification, object detection, action recognition, etc.**. Coming with a different problem like Roger’s including **“predicting air pollution level as a continuous variable based on images”** is uncommon to see. When you are faced with an uncommon use case, you have some options to consider:
1. Reframe the problem to fit into common use cases. For instance, bin your target value, turn it into a categorical variable indicating “pollution level” and turn it into a classification problem where you'll get the probability for each pollution level group. This might be unfavorable for you but it is worth trying if applicable.

2. If you want a close comparison with your linear model, use the same pre-generated features with dense layers as in any regression problem. But this won’t give you the power of feature generation in CNNs.

3. Dig deeper for use cases similar to yours. You might find methods using the CNN with the last layer replaced, or using the features generated to feed to another model, etc. But all this will require more search and experimentation.

## Conclusion 

If you reached this point, you might feel that the post didn't make things easier or answer your question about *"what to do exactly"*, but it wasn't meant to provide a particular path or answers. The main point was to share tips and thoughts based on my experience while being aware that others might have different strategies or perspectives. And to conclude, here are my final  recommendations 

- **Come to terms with the fact that you won’t find a way to explain things in deep learning in the same way you do with linear/logistic regression, etc. It is a different mindset.**

- **Try to develop a better intuition to help you improve your model development strategies. Additionally, do the math or look into visual representations to understand the significance of the hyperparameters.**

- **Expect to spend a significant time checking, filtering and adding to your data if possible as long as you are not using a benchmark data set. Don’t assume that deep learning methods will solve your data problems.**

- **Consider reframing your problem if applicable. If not, dig deeper beyond the "Getting Started" tutorial and ask in public. There's a lot of hidden research and libraries about narrow applications and different methods.**


[^1]:There are new versions of the fastai course. I just included this part from 2018 as I could locate it in the linked video.
