---
title: Module 2 Lecture 18: Comparing the classsifiers
teaching: 
exercises: 
questions:
- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---
### Module 2 Lecture 18: Comparing the classsifiers

Having now completed our examination of the most popular classifiers used in remote sensing. It is now benefit to compare them both in terms of performance and in relation to the user if it required. We want to compare the attributes, so we know where their relative strengths and weaknesses lie. And so that we always choose the most appropriate method for the task at hand. Of the range of algorithms we have looked at, the following three are representative set for comparison purpose and other ones we have spent most time on. They are the maximum likelihood classifier, the support vector machine and convolutional neural networks. Let's commence by summarizing the maximum likelihood algorithm. Recall that the decision rule for allocating a pixel to a class is expressed in terms of discriminate functions. Each class is defined by its mean vector and covariance matrix, and if available, the class prior probability. And is represented also by those properties in the discriminant function. Here we summarized the attributes of the maximum likelihood classifier. The support vector classifier, finds a separating hyperplane that maximizes the margin between two classes of data. While minimizing the error caused by pixels that fall on the wrong side of the hyperplane. It uses kernels in place of dot products effectively to project the data into a higher order space, so that data which is not linearly separable can be handled. The attributes of the Support Vector Machine is summarized here. That in particularly that it has to be used in a decision tree to make it capable of handling multiple classes. The Convolutional Neural Network is a modern variant of the original multilayer perceptrons. And consists of a number of layers, each usually involving sets of filters that perform convolution, activation and pooling. Those layers can then be followed by fully connected neural network and or a softmax operation. And this slide summarizes the attributes of the convolutional neural network. In this table, we bring the most important attributes together so that the three principle algorithms can be compared. In summary, the maximum likelihood classifier is much simpler to construct in trying. But is limited when presented with data of high spectral dimensionality. By comparison, the support vector machine and the convolutional neural network are more challenging to configure and train. But the support vector machine is good for handling data of high dimensionality. It does however require a decision tree framework to handle more than two classes. The convolutional neural network naturally handles special context and, like the maximum likelihood classifier, is a multiclass algorithm. It can also handle data of high dimensionality. Here we summarize what the user needs to look for in selecting an algorithm for thematic mapping in remote sensing. Again, these test questions draw attention to the types of application the analyst may have to handle leading to a choice of the most appropriate classifier algorithm. 

> ## Quiz
>
> 1. ?
>
> > ## Solution
> >
> > 1. {: .solution}
> >    {: .challenge}

{% include links.md %}