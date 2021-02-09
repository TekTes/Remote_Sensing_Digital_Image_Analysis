---
title: Module 2 Lecture 9 - The support vector machine—multiple classes and the classification step
teaching: 
exercises: 
questions:

- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---
### Module 2 Lecture 9: The support vector machine—multiple classes and the classification step

Now come to the fourth step in the support vector machine. That is how to turn a binary classifier into a multi-class process. The classical way of turning a binary classifier into a multi-class machine is to embed it in a decision tree. The simplest of which is that shown in this slide. Here, each class is separated from the remainder sequentially. It is immediately obvious though, that a problem with this approach is that the training sets used to effect each binary decision are very unbalanced, particularly near the top of the tree. Furthermore, there's probably an optimal order in which to do the class separations but we don't know that beforehand. A preferable approach is to use the one against all strategy in which a set of binary classifiers are trained in parallel. Each classifier separates one class from the rest. So there are as many classifiers as there are classes. Having been trained then when used to classify unknown pixels, the decision rule applied at the output of the tree selects the most favored label based on the SVM decision rule. Another approach is the one against one strategy. The topology is the same as in the one against all approach of the previous slide but here each classifier is trained to separate just two of the set of classes, all class pairs are implemented so that m into m minus 1 divided by 2 separate classifiers are needed. We get that number by looking at the number of times two classes can be selected from the available m. The calculation is m factorial divided by m minus 2 factorial. Note that each class will appear m minus 1 times among the set of classifiers. An unknown pixel is placed into the class which has the greatest number of recommendations in favor of it among the m times m minus 1 over 2 decisions. Because of the large number of individual classifiers involved, training can be quite time consuming. We have now covered the four stages in the development of the support vector classifier, as shown in this slide. We now wish to see how the machine can be used in practice, which we do by way of example, in the next lecture. There are a number of decisions that must be taken by the user before applying the support vector machine to real remote sensing classification problems. Effectively, we have to choose some multi-class strategy to be used, and the kernel. We then have to implement some process to find the best value for the kernel parameter and for the regularization parameter C. In the next slide, we put these steps into the overall classification methodology we outlined in the case that the maximum likelihood at minimum distance classifiers. In this slide, we examine the support vector machine from an operational strategic perspective. Recall, we did that in lecture seven for the maximum likelihood and minimum distance classifiers. The table here is identical to that earlier one but has some steps particularized to the support vector machine. Again, the three steps which are common to all classifier methods are highlighted in blue. Please note that software is freely available for implementing a support vector machine. Some of the most common are shown here. This slide simply summarizes the four important steps in the SVM. These quiz questions focus you on the practical aspects of using a support vector machine. 



> ## Quiz
>
> 1. ?
>
> > ## Solution
> >
> > 1. 
>    {: .solution}
{: .challenge}

{% include links.md %}