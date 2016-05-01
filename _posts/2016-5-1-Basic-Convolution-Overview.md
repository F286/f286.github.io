---
layout: post
title: Basic Convolution Overview
published: true
youtubeId: W8hBHKV91us
---

This is a basic overview of a convolutional neural network, which are used for tasks such as image recognition. 

## What is a convolution?

In a nutshell, when we 'look' at the pixel of a previous layer, we also look at the surrounding pixels so we have a bit of context of the tiny little area we are looking at. If we just look at the pixel of a previous layer, we can say "oh, it's dark", but if we look at the surrounding pixels maybe we can say "oh, this is maybe an edge". This tends to be more useful, and works good for images since how pixels are positioned relative to each other tends to be important.

## Ok, but what does this mean in a network?

The way we organize the 'nodes' in a network is a 2D grid, and generally we look at the same 'spot' on the previous layer. Remember though, that we are also slightly 'peeking' at the surrounding pixels. In practice, as we pass through layers we can detect more and more complex **features**.

We can think of **features** as important bits of the image which help us recognize it. The incredible thing about neural networks that that these will be created naturally as we train the network with _gradient descent_. An example of a simple feature on the first layer is an edge, a more complex feature would be a checkerboard pattern. Neural networks (and maybe humans?) at the very core are pattern detectors, if we make a giant super sandwich of pattern detectors we can eventually do things like detect if a picture is a cat or dog. For a 'hand wavey' sense of what these things are, we generally need something like 5 layers to detect if this is a dog or cat.

This below is me writing out the im2col function, which is used to compute an entire layer (all pixels) at once, using matrix multiplication. Note that every feature (pattern) detector will run on every pixel position of the image.

![Convolution]({{site.baseurl}}/images/convolution1.jpg)

> The final output is 2x2, less than the original 4x4. Padding can be added to the image to avoid this.
