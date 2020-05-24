https://arxiv.org/pdf/1901.07884.pdf

[Ordinal Regression](https://en.wikipedia.org/wiki/Ordinal_regression) is a problem between regression and classification. This paper proposed an approach to let neueral nets handle this problem.

Let take the word difficulty question as an example. Let's say a word's difficulty can be classified as 1 - 6. If we do this as a regression problem, we get a real number as output, then we classify (-inf, 0.5) as level 1, (0.5, 1.5) as level 2, and so on. However, the problem is, the relationship between level may not be linear in the output scale. The optimal divider between level 1 and level 2 may be 0.6, instead of 0.5.

**To overcome this problem, this paper adds a bias layer after the regression output, and then use sigmoid func to classifiy each class. Effectively, this makes the border between each level trainable.**

This paper also proves that the output will be consistent with the order. See the paper for more details.

Another take away here is, we can add a **task importance weights** for each class during training. If a class has a higher task importance weight, it will be more sensitive to Loss during training. This paper sets this weights based on the imbalance-level of one class and mentioned this can improve the overall prediction performance.
