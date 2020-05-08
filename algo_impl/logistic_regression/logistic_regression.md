# Logistic Regression

[Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression) is a
linear classification model. In binary classification, we assume the logit
value of probability P(Y=1|X=x) is linear to x:
```
logit(P) = ln(P / 1-P) = -(ax + b)

P(Y=1|X=x) = 1 / ( 1 + exp(-ax - b)) = sigmoid(ax + b)
```
With this representation of P, we can then get the Loss function with [Maximum
Likelihood Estimation](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation):
```
Likelihood  = product(P(X=xi|Y=yi)) for all i

P(X=x|Y=y)  = P(Y=y|X=x) * P(X=x) / P(Y=y)
            = sigmoid(ax + b) * constant        if y = 1
            = (1 - sigmoid(ax + b)) * constant  if y = 0
            = (y * sigmoid(ax + b) + (1 - y) * (1 - sigmoid(ax + b))) * constant
            = (y * sigmoid(ax + b) + (1 - y) * sigmoid(-ax - b)) * constant

Loss  = -log(Likelihood)
      = -sum(log(P(X=xi|Y=yi))) for all i
```
Let's get the derivatives of the Loss:
```
d(Loss)/da  = sum(-xi * yi * sigmoid(-axi-b) + xi * (1 - yi) * sigmoid(axi+b))

d(Loss)/db  = sum(-yi * sigmoid(-axi-b) + (1 - yi) * sigmoid(axi+b))
```
Till here, we can use Gradient Descent to compute the parameter a & b.
