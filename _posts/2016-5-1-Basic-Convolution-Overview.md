---
layout: post
title: Basic Convolution Overview
published: true
youtubeId: W8hBHKV91us
---

This is a basic overview of a convolutional neural network, which are used for tasks such as image recognition. 

## What is a convolution?

In a nutshell, if we look at the pixel of a previous layer, we also peek at the surrounding pixels so we have a bit of context of what we're looking at. If we only look at the pixel directly, we can't infer too much, maybe 'oh, it's dark'. However if we peek at the surrounding pixels we can say 'maybe this is a vertical edge'. This tends to be more useful, and works well for images since how pixels are located relative to each other is important.

## Ok, but what does this mean in a network?

The way we organize the 'nodes' in a network is a 2D grid, and generally we look at the same 'spot' on the previous layer. Remember though, that we are also slightly 'peeking' at the surrounding pixels. In practice, as we pass through layers we can detect more and more complex **features**.

We can think of **features** as important bits of the image which help us recognize it. Neural networks are amazing because they can _learn_ these features without any specific input from the programmer. (networks are usually trained with _gradient descent_) An example of a simple feature on the first layer is an edge, a more complex feature would be a checkerboard pattern. It seems neural networks are essentially pattern detectors, if we sandwich a large number of pattern detector layers we can eventually do things like detect if a picture is a cat or dog. For a 'hand wavey' sense of what these things are, we generally need something like 5 layers to detect if this is a dog or cat.

Below is how to compute a convolutional layer written out. The first function is called im2col, which converts squares on the original image to columns. We can then compute the convolution using matrix multiplication. Note that every feature detector will run on every pixel position of the image.

![Convolution]({{site.baseurl}}/images/convolution1.jpg)

> The final output is 2x2, less than the original 4x4. Padding can be added to the image to avoid this.
