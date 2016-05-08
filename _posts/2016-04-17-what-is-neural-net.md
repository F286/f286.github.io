## What is a neural network?

A neural network is a program which emulates the structure of biological brains. Instead of telling the computer very specifically what to do, we create _neurons_ and connections between them, then train the networks with a large amount of data. So for example, to detect if a picture is a cat or a dog, if we provide the network with enough pictures of 'a cat' and 'a dog', we can train it to be able to tell the difference.

This is different from regular computer programs, which work by adding, multiplying and comparing numbers. We simulate the networks, so we are adding and multiplying numbers, but the _structure_ is quite different.  A neural network works in a much more fuzzy way, a large number of neurons connected to each other is created, then _trained_ to do a specific task. 

## So.. how do we train them?

**image -> neurons -> neurons -> answer**

We show it images that we know the answer, if it gives the wrong answer we look and say, "What do we have to _tweak_ in the network to give the right answer?", then adjust the network.  The technical term for this is _back propogation_, and it works by calculating the derivative for each piece of the network with respect to the answer. The hard part about neural networks is training them, it can often take days or weeks to train complex ones. 

It's interesting to think about parallels to the human brain when training a network, I've read that when two neurons fire at the same time in a brain the connection strengthens, it's probably more complex than that in the brain, but this is a very new field so there's still lots of exciting breakthroughs waiting to be made. 

> Regular programming is like math class, but more fun. Neural nets are like training an uncooperative monkey.