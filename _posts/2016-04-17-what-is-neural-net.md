---
layout: post
title: What is a Neural Network?
published: true
---

# What is a Neural Net?

A neural network is a simulation which emulates the structure of a brain. Instead of directly telling the computer what to do, we create _neurons_ and _connections_, then train the simulation with data. For example, to classify a picture, if we show it enough pictures of **cats** and **dogs**, we can train the network to tell the difference.

## How exactly do we train them?

Well, we cheat. We show it images we know the answer to. If it guesses wrong, we look at the network and 'tweak' the values so it gives the right answer. We can calculate how much we need to change values of the connections to get the 'correct' answer. If we do this tens of thousands of times we can train the network.

![Neural Net Structure]({{site.baseurl}}/images/neuralNet1.jpg)

> Does a real brain learn in the same way?