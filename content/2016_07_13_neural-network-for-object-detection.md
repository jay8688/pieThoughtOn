Title: Neural Network for Object Detection
Date: 2016-7-13 15:14
Category: machine learning
Tags:
Slug: neural-network-for-object-detection
Authors:

For years, neural network has always been mystic to me and I never thought that I would do serious learning in this area until recently. I encountered an awesome book [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/) by Michael Nielsen. The book is written in an narrative way and quite interesting to read. After spending several days digesting most content from the book, I am equipped with essential tools to explore neural networks. Hence, in this blog let me discuss how to do object detection with neural networks and deep learning. 
<!-- PELICAN_END_SUMMARY -->

Foremost, big acknowledgment to [Michael Nielsen](http://michaelnielsen.org/) for enormous dedication to his book on [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/) and generously making it freely accessible to everyone. To me, it is much more than a free book. Not quite like many other books you can find, it describes every classical element you need to know about neural networks in a way that it is made easiest possible for understanding. Before jumping into the content, please do checkout [What this book is about](http://neuralnetworksanddeeplearning.com/about.html) where you will also get an idea on the approaches adopted to help you understand the fundamentals both in theory and practice, and the philosophy advocated by the author:

> Technologies come and technologies go, but insight is forever.

####Neural networks for image recognition/classification
Not until recently, research and development in neural networks has proven powerful in solving vision problems like image classification. You probably heard that "deep" neural networks are great. While it's true that networks are usually deep for image classification, they also adopt a particular type of architecture different from the conventional one, which is called [convolutional networks](http://neuralnetworksanddeeplearning.com/chap6.html#introducing_convolutional_networks), or deep convolutional networks. 

In classifying handwritten digits from the MNIST data set, Michael showed that using one convolutional-pooling layer, accuracy rate is considerably improved to 98.78 percent versus 97.80 percent by a conventional shallow network. Furthermore, a second convolutional-pooling layer gets the accuracy to 99.06 percent. Some additional steps are found to yield even better results, that include using rectified linear units, expanding the training data, inserting an extra fully-connected layer and apply dropout, using an ensemble of networks. After all these steps, a 99.67 percent accuracy is achieved. Getting to a satisfying accuracy is more of an experimentation, and I am sure it helps to visit [Chapter 3 Improving the way neural networks learn](http://neuralnetworksanddeeplearning.com/chap3.html) back and forth. 

####Google's TensorFlow
You would be able to find some popular deep learning software. But according to Google senior fellow Jeff Dean, "There are currently 1500 repositories on GitHub which mention TensorFlow". I will choose TensorFlow for my image classification and object detection task. 

There are good tutorials about TensorFlow. To get hands on experience with constructing convolutional neural network, check out [Deep MNIST for Experts](https://www.tensorflow.org/versions/r0.9/tutorials/mnist/pros/index.html#deep-mnist-for-experts). 

[Here](https://medium.com/@ageitgey/machine-learning-is-fun-part-3-deep-learning-and-convolutional-neural-networks-f40359318721#.lmkz7nf08) is another good blog I encountered using [TFLearn](http://tflearn.org/), a wrapper around Tensorflow. The author also talked about [Precision and Recall](https://en.wikipedia.org/wiki/Precision_and_recall) metrics that are useful indication of the performance for binary classification. 

####Neural networks for object detection
Deep-learning based object detection based on deep learning is not as popular as its image classification success. I will point to some papers to get started

- [Paper-CVPR14](http://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Girshick_Rich_Feature_Hierarchies_2014_CVPR_paper.pdf) Ross Girshick, Jeff Donahue, Trevor Darrell, Jitendra Malik, Rich feature hierarchies for accurate object detection and semantic segmentation, CVPR, 2014. 

By reading on such latest research, I have a feeling that the methods are suitable enough from an academic point of view, but complex enough for immediate need, as fully understanding and implementing those algorithms could require more cycles than we anticipated. The code for object detection with neural network is also not as accessible as that is for classification. While it is necessary to investigate algorithms on frontier research papers to keep up with latest ideas and find potentially good solutions to problem at hand, there are also such commonalities to academic papers from an industry point of view, application scope may be limited, more effort need to be spent in research, implementation could be difficult etc. It looks to me the problem of object detection is still not fully standardized. So we should keep an eye on any development. 
