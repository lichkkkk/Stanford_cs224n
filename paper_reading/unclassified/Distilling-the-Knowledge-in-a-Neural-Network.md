https://arxiv.org/pdf/1503.02531.pdf

Knowledge Disdissation:
-     first you train a complex model with all techniques and data you could use, that's the **Teacher** model
-     then you create a simpler network, which can be deployed if well trained, that's the **student** model
-     then you train the student model with both original training data as well as **soft target** from teacher model
-     That meams, you are not allow try to predict the the current label, also try to predict the exact same softmax output of teacher model did
-     This can significantly improve the student model even if with the same traingin data
-     There is one more concept called **temperature**, which is used to tune the soft target to let it provide more info

Check more from this post: https://zhuanlan.zhihu.com/p/102038521
