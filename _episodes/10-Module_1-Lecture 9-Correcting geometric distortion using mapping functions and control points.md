---
title: Module 1 Lecture 9 
teaching: 30
exercises: 10
questions:
- "?"
objectives:
- ""
keypoints:
- ""
---

### Correcting geometric distortion using mapping functions and control points

This lecture introduces a very powerful and common method for correcting errors in geometry. 

As noted earlier, the technique also allows us to register one image to another image, or an image to a map. In fact, by doing this registration, any errors are removed entirely. It is an alternative technique to the mathematical modeling approach of the previous lecture. 

And it is based upon two principal requirements. 

First, we assume we have available a map of the region, which is correct geometrically, and is in scale not too different from that of the image we wish to current. 

Secondly, we need to be able to identify points called control points, in both the map and the image, so that we can tie the two together mathematically. The real power of this technique lies in setting up mathematical equations that link points in the image, with corresponding points in the map. 

We will use the control points to set up those mathematical equations. In a sense, we are assuming that if we can relate the control points, from the image and the map mathematically. And that the control points are indicative of the map and image geometries, than other points in the map image will also be related by those same equations. 

This figure shows what we have in mind. 



![M1L9](..\fig\Lec_9\Using_mapping_functions.gif)



The geometrically correct map is on the left hand side. And the image to be corrected is on the right hand side. 

Notice that these are in the opposite positions, from the treatment of the previous lecture. 

It is just more convenient in this analysis to have them in this new order. As before, we have chosen the coordinates x and y, to describe the position of a point, or pixel in the map. And the coordinates u and v to describe position in the image. 

In principle, it should be possible to set up equations that relate the coordinates of a point in the image, knowing its position in the map. 

This is shown here by the pair of functions, in which both of the image coordinates are shown as functions of both map coordinates. 

Those functions will contain unknown coefficients, which when given explicit values, will allow us to go between the map and the image. 

To find those explicit values, we need some points in common, that is simultaneous sets of x, y, and u, v, that we can substitute into the equations. Those points are the control points, or sometimes they're called Ground Control Points. 

Here, we show the relationship between points in the map and the corresponding points in the image. By drawing a grid or pixel centers in each case. 

What we are going to do is choose a grid position on the map, and by using the mapping functions, find the corresponding grid position in the image. 

What sorts of functions should we use for this? Well the simplest are polynomials. 

Here we show the mapping functions expressed as polynomials. 

In this case of order or degree two. 

In principle, any order could be used, expecting that higher orders will give more accurate results. 

However, higher order polynomials introduce their own problems, as we will see later. 

The unknown coefficients to be found using the control points are the a sub zero, b sub zero, etc. 

If we assume that we have used the control points, and identified the unknown coefficients. Then we use the two mapping polynomials, in the following manner. 

We've moved over the map grid, point by point, that is, grid intersection by grid intersection. 

And for each point, use the mapping polynomials to find the corresponding point in the image.

We find the pixel value at that image point, and transfer it onto the map position we started with.

That is done for all grid positions on the map. Thereby building up a geometrically correct image, essentially using the recorded image as a source of pixels. This slide shows the process broken into the two individual steps. 

At the top, we find pixel locations in the image, which correspond to pixel positions on the map. 

On the bottom, we transfer the pixel from the image onto the map grid. This is just a small point, but it is worth noting, the pixels that are centered on an image grid. The map or record image are of such a size that adjacent pixels join up against each other. 

There are now two important matters to be considered, before the method is workable. The first is how to determine the unknown coefficients in the mapping polynomials. And I've said earlier that involves the use of control points. 

The second practical matter is that the mapping from a map grid position using the polynomials, may not project exactly onto a pixel position in the image grid, that will form the focus of our next lecture. 

Remember that the control points are pairs of coordinates, in the map and the image. 

Essentially, each control point is represented by the set of values of x, y, u and v. If we had, say 20 control points, we would have 20 sets of those four numbers. 

What we do is, substitute those knowing values into the mapping polynomials, and thus set up a set of simultaneous equations, which when sold, yield the required values of the unknown coefficients. 

Clearly, we need to have at least as many control points, as there are unknown coefficients, in one of the mapping polynomials. 

We can use the same set of control points to generate the unknown coefficients in the other mapping polynomial. We do not need the same percent. 

For a second order mapping polynomials, a minimum of six control points is required. 

Three are needed for a first order colinear mapping polynomial. And ten are required, if third order mapping polynomials are used. 

Usually we choose more control points than necessary and generate least squares estimates of the unknown coefficients. 

A particular advantage in choosing greater than the minimum number of control points is that, any specific control point which may not be well placed in either the map or the image, will not have an undue influence on the values of the coefficients being generated. 

Effectively, this technique depends upon having an accurate way of relating points in a map to the corresponding points in an image. 

We do this, by the process of choosing control points and establishing mapping polynomials. We will see an example in a later lecture. 

Pay particular attention to the second question. 

You might like to think about the similar problem of fitting a curve through a set of data points, using curves of increasing order.

Will a straight line always do a better job, than a cubic polynomial or not? 



> ## Quiz
>
> - One form of geometric distortion is a scale change  horizontally that resultsfrom over• or under-sampling along  a scan line.  What do you think the correction matrix might look like?
>
> - Show how the corrections for several different distortions can be combined into a single
>   step.
>
> - Later in this course we are going to look at methods for deciding what ground cover type is represented by each pixel.  We will then give the pixel  a label.  Do you think  it would better to do that before removing geometric distortions, or should the geometry be corrected beforehand?
>
> > ## Solution
> >
> > ???
> > ???
> > {: .solution}
> > {: .challenge}

{% include links.md %}
