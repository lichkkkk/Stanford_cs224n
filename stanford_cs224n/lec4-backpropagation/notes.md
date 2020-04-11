
## Overview:
Neural nets is effectively a non-linear function with weights as its parameters.
To train it, is actually to learn the weights from the data. Gradient descent,
   as usual, is the way to get the best weights. Backpropagation is the algo
   used to compute the descents for each parameter and update them.

If we use a function to represent one layer in neural nets, a 3-layer network
can be represented as y = f(g(h(X))). It's very similar to the chain rule in
classic calculaus, dy/dh = dy/df * df/dg * dg/dh. Because df/dg and dg/dh are
fixed for each node, so we can store them in each node to reduce deplicated
computation.

So whenever you see a traing example, first do a forward propagation, and get
the predicted value. Then compute the delta, and use it to do a backpropagation
with the derivatives pree-calculated for each node.

Using matrix can make the computation much faster during implementation.

## Lecture Notes:
TODO:
