---
layout: post
title: Basic Convolution Overview
published: true
youtubeId: W8hBHKV91us
---

This is a basic overview of a convolutional neural network, which are used for tasks such as image recognition. 

##What is a convolution?

In a nutshell, when we 'look' at the pixel of a previous layer, we also look at the surrounding pixels so we have a bit of context of the tiny little area we are looking at. If we just look at the pixel of a previous layer, we can say "oh, it's dark", but if we look at the surrounding pixels maybe we can say "oh, this is maybe an edge". We pass the image through the network as is, 'looking' at the same spot on the previous layer.

##Ok, but what does this mean in a network?

Usually the way we organize the 'nodes' in a convolutional network is the same as the original image, a 2D grid. (say 4x4 for a very low res image) Each node is simply connected to the same spot on the image, a layer back, but also contains input from the surrounding pixels. In practice as we move through the layers, the network will detect more and more complex 'features'. 

Features can thought of as 'relevant, interesting bits about the image which help the brain to recognize it'. These will naturally fall out of training the network. An example of a very simple features might be an edge or gradient (remember, 3x3 pixels). As the network moves through more and more layers, it will detect things like checkerboard patterns, circles, and eventually even things like faces or dogs (although this depends on the training data). Low level features tend to be similar across images. Neural networks can seem complicated at first, but really we are just creating (and training!) feature detectors, which we arrange like a giant sandwich so at first we detect very simple features, but through many layers can detect more and more complex features. Most convolution networks have something like 5-7 layers. 

It is interesting to note that every feature detector for a layer will run on every pixel of the previous layer. That's a lot of calculation! This below is me writing out the im2col implementation to try and understand it. This is commonly used to compute a convolution layer.

![Convolution]({{site.baseurl}}/images/convolution1.jpg)

* notice that the original 4x4 image is now 2x2, padding can be added to the original image to keep the shape.
