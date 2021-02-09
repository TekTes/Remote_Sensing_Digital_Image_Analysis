---
title: Module 2 Lecture 10 - The support vector machine—an example
teaching: 
exercises: 
questions:

- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---
### Module 2 Lecture 10: The support vector machine—an example

In this lecture, we present two examples of the application of the support vector classifier in remote sensing. We start with a simple example using a segment of QuickBird imagery recorded in 2002. The image segment consists of 500 by 600 pixels with four bands of data as shown in this slide. Several cover types are evident in the image. Two of the information classes each consist of two spectral classes. The support vector machine was trained on the identified spectral classes. As required, the authors chose a set of training pixels, in this case, as fields of pixels. And a separate set of pixels, again, as fields to be used for testing the accuracy of the result of the classification. Here we see the numbers of training and testing pixels for each spectral class used by the authors. The next step is to design the classifier, including the choices of kernel, and multiclass strategy, and the values of the kernel, and regularization parameters. The one against one multiclass strategy was used, which required 36 different binary SVM's. A grid search procedure is commonly used to find optimal values for the kernel and regularization parameters. In this example, a slightly simpler approach was employed, which involved two linear searches as described in the slide. The same parameter values were used in all 36 classifiers. This slide shows the results as a thematic map, and as a table of class by class accuracies. Overall, the average accuracy was 76.9%. Although the water class was handled perfectly, the performance on the rock and bare soil classes was quite poor, and would not be acceptable if those classes were of interest in practice. If we compare the thematic map to the image, we can see immediately the classification errors in the rock and bare soil classes. Some of the rock pixels have been labeled as tree. Whereas many of the bare soil class pixels have been labeled as asphalt. This is a very crude accuracy assessment. We will be much more precise when talking about classifier errors, when we come to Module 3. We now look at the results of a classification of hyperspectral imagery. A problem for which the support vector machine is said to be more suitable than most other classifiers is taken from a 2004 paper and involves a 220 band dataset called Indian Pines, recorded by the AVIRIS Sensor. This slide shows the image itself and a ground truth map. That is a map of pixels which have been labeled by site visits, use of photo interpretation, and other sources of reference data. Only 9 of the 16 classes were used in this exercise. The one against all multiclass strategy was used, as was the radial basis function kernel. By running a number of trial classifications, optimal values of the regularization, and group parameters were determined, the number of training and testing pixels are also shown in this slide. Although we don't have a thematic map in this case, we do have a table of accuracies, showing remarkably good results on all classes. That the interesting sensitivity analysis, which, at least for this example, indicates that the performance is not strongly dependent on getting the values of the kernel and regularization parameters exactly right. Here we summarize some of the practical aspects of using the support vector machine. Here we ask you to look at the support vector machine compared with other classification methods. 



> ## Quiz
>
> 1. ?
>
> > ## Solution
> >
> > 1. 
> >    {: .solution}
> >    {: .challenge}

{% include links.md %}