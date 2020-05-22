An implementation & visualization of various gradient descent algo

Includes:

- Naive Gradient Descent: fixed learning rate, no memory
- Momentum: less oscillations and down faster on target directions
- NAG: an improved momentum. look ahead and not too fast when it starts to be flat
- AdaGrad: adjust learning rate for each weights by memorizing past updates' square sum, but can stop early
- RMSprop: improved AdaGrad. will not stop too early
- Adam: a combination of RMSprop and Momentum

So basically there are two ideas: 1) use momentum(to be faster); 2) use adaptive rates.

In most cases we can rely on NAG or Adam.

You can find more good intros here:
* http://www.cs.toronto.edu/~tijmen/csc321/slides/lecture_slides_lec6.pdf
* https://zhuanlan.zhihu.com/p/32626442
* https://cs231n.github.io/neural-networks-3/#hyper
