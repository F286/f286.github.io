---
layout: post
title: Visualizing Neural Networks
published: true
youtubeId: W8hBHKV91us
---

I've been working in unity recently to try and get a feeling for neural networks, one of the biggest challenges I've found is visualizing the values and derivatives in an way that's easy to understand. If the information is presented as just a wall of numbers it can be hard to understand.

{% include youtubePlayer.html id=page.youtubeId %}

In this example, the block size and color shows the value of the block. The block spin speed show the derivative. 

This is the basic structure for a single LSTM (long short term memory unit). This is a special type of neuron that can remember values over multiply frames. The box that starts red is telling the system whether to _remember_ or not.

**note** - a derivative, in a nutshell, is _if I increase this node's value by 1, how much will in output increase?_

<iframe width="420" height="315" src="https://www.youtube.com/embed/W8hBHKV91us" frameborder="0" allowfullscreen></iframe>
