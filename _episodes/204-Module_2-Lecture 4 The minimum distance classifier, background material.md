---
title: Module 2 Lecture 4 - The minimum distance classifier, background material 
teaching: 
exercises: 
questions:

- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---
### Module 2 Lecture 4: The minimum distance classifier, background material

We now commence a journey towards the development of more complex classifiers. To do so, we're going to look at another very simple algorithm that underpins our further development. This is called the minimum distance classifier. It is even simpler than the maximum likelihood rule. Consider two classes of data which are linearly separable. That is, they can be separated by a linear surface or straight line in two dimensions. If we knew the equation of that line, we could determine the class membership for an unknown pixel by saying on which side of the line its spectral measurements lie. How can we express that mathematically? The equation of a straight line is pretty simple in two dimensions as shown here. It is helpful though to write it in the generalized form shown, since that allows it to be taken to any number of dimensions as seen on the bottom of the slide. Incidentally, in more than two dimensions, we refer to the linear surface as a hyperplane. Here we write the equation in vector form, which is compact and allows manipulation by the rules of vector algebra when needed. Note that we can use either the transpose expression or that using dot products, both are equivalent versions of the scalar product. When we use the equation of the hyperplane in classifier theory, we often refer to the vector of coefficients Omega_i as a weight vector. Usually Omega_n plus 1 is not included in the weight vector and instead sometimes called the offset or bias. Having expressed the hyperplane in vector form, we now have an elegant expression for the decision rule to apply in the case of a linear classifier. That's the rule shown in the box in the middle of the slide. The rule evaluates the polynomial for a given value of the measurement vector. If it is positive, then the corresponding pixel lies to the left of the hyperplane and thus is labeled is coming from class 1. If it is negative, then the pixel is from class 2. This decision rule will feature often in our later work and will be the basis of further developments. How do we find the hyperplane that requires finding values for the weights and offset? As with all supervised classification methods that entails using sets of training pixels, we will take that further in the next lecture. In summary, a simple classifier can be found by putting a linear surface or hyper plane between the two classes of pixels. The equation of the hyperplane expressed in vector analysis is simple. The unknowns in that equation are the weights , which we find by training onsets of labeled pixels from each class. These questions simply ask you to verify some of the mathematics in this lecture. 

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