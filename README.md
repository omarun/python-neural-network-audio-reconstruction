# Neural Network Audio Reconstruction

These are a variety of ideas about audio signal reconstruction using 
neural networks.  Of course this generalizes to pretty much any time
series, nothing special about audio.  The general idea is that data 
that is known is used as a label, and feature data is generated by 
various means of either reducing the information content of the label
or by adding noise to the label.  The goal, of course, is that the 
networks learns how to fill in the data, remove noise, etc.

The original idea of this is based on my predilection for the Wadia 
digital to analog converters. These use relatively high order polynomial
interpolation to smooth sampled audio data.  Wadia spent a lot of effort 
identifying which algorithms produced results that study participants 
thought sounded better.  The inspiration for this collection of audio
reconstruction experiments is based on the ideas that Wadia was doing 
decades ago, but tempered with the amazing neural network visual 
reconstruction examples that we have today (Alex Champandard's 
[Neural Enhance](https://github.com/alexjc/neural-enhance) being just
one of many examples).

These are just a number of experiments in convenient Jupyter notebooks, 
nothing is a finished product.  You will need `numpy` and `tensorflow`
to run them.  The basic notion of the models is the encoder-decoder, 
but of course this can be broadened to things like the u-net.  The 
generators are quite slow, so don't expect amazing performance, even
on your GPU, since this is not as memory-bound a problem as many 
training exercises.
