https://arxiv.org/pdf/2002.01322.pdf

This paper is about training **keywords spotters** with a pre-trained speech embedding structure and limited synthesized examples.

The speech embedding layer is trained on 200M audio pieces from YouTube, and it can convert each 80ms audio piece into a 96-dimensional feature vector. With this speech embedding layer, the paper mentioned it only takes very few examples (e.g. only 10 examples to achieve > 90% accuracy) to train a workable spotter. We can use either synthesized data or real data or a mixture.

They posted the speech embedding to TF Hub: https://tfhub.dev/google/speech_embedding/1
