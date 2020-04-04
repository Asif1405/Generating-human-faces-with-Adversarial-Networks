# Generating-human-faces-with-Adversarial-Networks

### Overview:
We'll train a neural net to generate plausible human faces in all their subtlty: appearance, expression, accessories, etc using autoencoders. This neural network is called Generative Adversarial Networks or GANs.
It has two parts:
 1. Generator - takes random noize for inspiration and tries to generate a face sample. Let's call him G(z), where z is a gaussian noize.

 2. Discriminator - takes a face sample and tries to tell if it's great or fake. Predicts the probability of input image being a real face. Let's call him D(x), x being an image.
D(x) is a prediction for real image and D(G(z)) is prediction for the face made by generator.

We train the two networks concurrently:
- Train discriminator to better distinguish real data from current generator
- Train generator to make discriminator think generator is real
- Since discriminator is a differentiable neural network, we train both with gradient descent.


### Requirements:
- python 3.x, 
- google colab
