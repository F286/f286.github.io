---
layout: post
title: Visualizing Neural Networks
published: true
youtubeId: W8hBHKV91us
---

I've been working on visualizations for neural networks recently, the example provided is for a simple type of recursive network. Looking at the information directly can be an opaque 'wall of numbers', so I'm experimenting with creating a simple visual repersentation to show the value and derivative (gradient) of each node.

![lstm1.png]({{site.baseurl}}/_posts/lstm1.png)
![lstm2.png]({{site.baseurl}}/_posts/lstm2.png)
![lstm3.png]({{site.baseurl}}/_posts/lstm3.png)
![jekyll-logo.png]({{site.baseurl}}/images/jekyll-logo.png)

In this example, the block size and color shows the value of the block. The block spin speed show the derivative. 

This is the basic structure for a single LSTM (long short term memory) unit. This is a commonly used in recursive neural networks to 'remember' a value over multiple frames.

**note** - when I first heard 'derivative' it seemed really complicated, but actually it turned out to be quick simple. It really just describes the relationship between two 'nodes' in our network. Basically it means, if I add **1** to node A, how much does Node B increase by?

Unity 5.4
Scene name is 'Scene Gradient'
[Machine Learning Repo](link:https://github.com/F286/Machine-Learning)

{% include youtubePlayer.html id=page.youtubeId %}
