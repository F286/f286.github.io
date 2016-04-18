---
layout: post
title: Visualizing Neural Networks
published: true
youtubeId: W8hBHKV91us
---

I've been working on visualizations for neural networks recently, this is possible for small networks or inside neurons, but can become difficult as the networks become large. The information is sometimes presented as a 'wall of numbers', which I find hard to understand, so I'm experimenting with creating a simple visualization for the internal structure of a simple neuron 'unit', then extending that for more complex networks.

{% include youtubePlayer.html id=page.youtubeId %}

In this example, the block size and color shows the value of the block. The block spin speed show the derivative. 

This is the basic structure for a single LSTM (long short term memory unit). This is simply a type of 'network' that can remember values over multiply frames. This is possible because the network is recursive. For example, the box that starts red is telling the system whether to _memorize_ or not.

**note** - a derivative, in a nutshell, is _if I increase this node's value by 1, how much will in output increase?_
