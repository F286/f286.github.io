---
layout: post
title: Visualizing Neural Networks
published: true
youtubeId: W8hBHKV91us
---

I've been testing of different types of visualizations for neural networks in unity recently. I think this is one of the biggest challenges, especially once the networks become very large. Generally the information is presented as a 'wall of numbers' which is quite opaque, I'm experimenting with size, color and movement to visualize the simple add, multiply, and sigmoid nodes of a single LSTM (long short term memory) unit. Being able to get my hands on and 'tweak' the values is important to get a feel for how these systems work I think.

{% include youtubePlayer.html id=page.youtubeId %}

In this example, the block size and color shows the value of the block. The block spin speed show the derivative. 

This is the basic structure for a single LSTM (long short term memory unit). This is simply a type of 'network' that can remember values over multiply frames. This is possible because the network is recursive. For example, the box that starts red is telling the system whether to _memorize_ or not.

**note** - a derivative, in a nutshell, is _if I increase this node's value by 1, how much will in output increase?_
