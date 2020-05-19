Find the original paper
[here](https://research.duolingo.com/papers/settles.tacl20.pdf).

Try Duolingo CEFR Checker [here](https://cefr.duolingo.com/).

Blog post about their CEFR checker
[here](https://blog.duolingo.com/the-duolingo-cefr-checker-an-ai-tool-for-adapting-learning-content/).

## TL;DR:
They developed models to classify the difficulty of words/passages and
introduced how they applied this to their online English capability test.

What I am interested in here is how they are predicting the difficulty of a
single word. It turns out they just extrct several features(e.g. frequency,
length, Fisher score, etc.) for each word and then trained a linear regression
model. This requires to memorize the word frequency in a map during
preprocessing, which is not feasible for on-device features.
