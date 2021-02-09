---
title: Module 2 Lecture 8 - The support vector machine—non-linear data
teaching: 
exercises: 
questions:

- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---
### Module 2 Lecture 8: The support vector machine—non-linear data

In this lecture, we look at the third stage of the development of the support vector machine. We introduced a transform that in principle changes a dataset that is not linearly separable into one that is. We will see surprisingly that we don't actually have to know the transform itself. Let's examine critically the form of the decision rule. That particularly that the pixel vector doesn't actually appear on its own, but rather is always in combination with the support vectors in the form of x_i transpose x. Suppose we now apply an unspecified transformation to the data space, call it phi brackets x. Thus a product of the support vector and the unknown pixel vector will in the transform space, become phi of x_i transpose times phi of x, which we defined as k x_i of x. We call that transform product a kernel, and represent it by that symbol k. Now insert that kernel function into the decision rule. All that we have really done here is transform the original pixel space. But we can interpret the resulting expression as one which says that we need to know the kernel, that we don't actually need to know the transform phi of x that led to it. The real question then becomes, what functions can be used as kernels? Because they represent a scalar product, they have to be decomposable into that form. Some common kernels that satisfy that condition are shown on the next slide. The most common kernels encountered in remote sensing applications are the last two shown here. Although the polynomial could also be used. Note that they have parameters for which we need to choose values. That is often done by running a series of trials to find which value works best, as we will see later. To see how kernels work, we will look at a very simple example. We will use the first example from the previous slide, a quadratic kernel with a two-dimensional data space. First, we demonstrate that the chosen kernel can be decomposed into a scalar product, which we did by expanding it and then rewriting it as shown on the bottom half of this slide. Having decomposed it, we can now see what the underlying transformation function is. Remember, we don't need to know this in practice. We are just looking at it here in the context of this simple example to see how kernels work. The transformation projects the data into a three-dimensional space of the squares and cross products of the original data axis, at least for this example. We now apply the transformation to the dataset below on the left. The two classes of data lie on the other side of the quadrant of a circle and clearly are not linearly separable. After transformation, that data is linearly separable into two-dimensional space. Even though a third dimension has been created in the transform of the previous slide, it is not needed. This slide summarizes the essential points about the transform and the kernel. Again, these questions simply reinforce the important properties of the kernel. 

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