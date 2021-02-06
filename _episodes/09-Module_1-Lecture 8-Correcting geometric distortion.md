---
title: Module 1 Lecture 8
teaching: 
exercises:
questions:
- "How do you compensate the geometric errors in remote sensing imagery?"
objectives:
- "Understand the two common approaches to correcting errors in image geometry"
- "**I**. Set up a mathematical model of the distortion(s), by using  the appropriate equations for each of the distortion types treated in the last lecture."
- "**II**. Account for all distortions in one process by setting up two equations that allow the pixels in a distorted image to be relocated spatially so that they appear in their correct positions with respect to a known map base"
keypoints:
- "Distortions in image geometry can be corrected by establishing a  mathematical relationship between the positions of pixels in the recorded (distorted) data and their correct positions relative to the landscape."
- "A separate relationship is needed for each distortion type (earth rotation, panoramic effects, earth curvature) but these corrections can be combined through matrix multiplication to produce  a single correction formula."
- "Correction of geometric distortion can also be carried out by ignoring the precise correction formulae and, instead, setting up a mathematical (polynomial) relationship between the positions of pixels in the recorded image and their (correct) positions on a known map grid."
---

### Correcting geometric distortion

We now come to methods for correcting any errors in the geometry of a recorded image. This is a fairly large topic and it will occupy the next two lectures using two different approaches. Both methods for compensating or correcting geometric errors in remote sensing imagery are used in practice. The first involves setting up mathematical equations which describe the types of distortion and then using those equations to correct the distortions. That can be a complicated process if many different sources of distortion are of concern, but it is regularly used for systematic correction by satellite operators. It also depends on a good knowledge of the ephemeris, that is the velocity, position, and pointing with time of the platform. The second method accounts for all sources of distortion in a single operation. It avoids the need to model mathematically the various types of distortion, and instead, uses a mathematical relationship between where pixels appear in an image and where they should appear in a map. This is a very common approach and it has the added advantage that the map basis can be chosen according to the projection preferred by the user. 

![RS05801](..\fig\Lec_8\RS05801.png)



We will illustrate the first approach by using the error introduced into an image by the rotation of the Earth during image acquisition. The above figure shows the image lie down on a regular rectangular grid, which is known to be incorrect geometrically, and beside it, the version which has been compensated for this rotation. To start the process of correction, we need to define two coordinate systems: one for the image as recorded, and one for the corrected version. 



The coordinate systems have their origins at the top because the platform is assumed to be moving down the page as it acquires its image, this is equivalent to a satellite in a descending node. We use the coordinates u and v to describe the recorded image laid on the regular grid, and the coordinates x and y to describe the pixels in their correct positions with respect to the Earth's surface, i.e., with respect to the chosen map grid. Clearly, what we have to do now is form a mathematical relationship between the pairs of coordinates. 

We now set up two equations that describe the position of a pixel in the correct coordinate system as a function of the position of the pixel as recorded. Note that the line coordinate, v and y respectively, does not change, therefore, we get the second unchanged equation shown at the bottom of the figure below. However, to compensate for Earth's rotation, the coordinate across a scan line has to be adjusted progressively to the West as we increment down the lines of the image. In other words, as well as being a function of u, x must also be a function of v, representing this shift. The coefficient Alpha describes the degree of correction to the West as the platform moves southwards. 

![RS06801](..\fig\Lec_8\RS06801.png)

It is convenient to express the pair of equations in matrix form because that helps when we have to make several corrections. The value of Alpha depends on the platform orbital properties and the location at which the image was recorded. 

If we examine the geometric characteristics of other distortion types, it is possible to set up similar equations as shown on the figure above. The next step would be to use these relationships to create a geometrically correct image, that requires inverting them to root u and v in terms of x and y. Because the technique we are going to treat in the next lecture is so flexible in terms of correcting any types of geometric distortion, we will not proceed any further with mathematical modeling. 

We have only reviewed the most significant sources of geometric distortion here, please consult some standard textbooks to see the very large range of mechanisms that can cause geometric errors in an image. 

The first question here has been treated in the lecture, the idea of the question is for you to derive the matrix form of the correction. The third question is particularly interesting. Later in this course, we're going to treat methods for attaching labels to pixels indicating what they represent in terms of ground cover types. This question asks you to consider whether the geometry of an image should be corrected before that labeling process is carried out, or whether the labeling should be done first and then the labeled pixels corrected for the geometric positions. 

> ## Quiz
>
> 1. One form of geometric distortion is a scale change  horizontally that resultsfrom over• or under-sampling along  a scan line.  What do you think the correction matrix might look like?
>
> 2. Show how the corrections for several different distortions can be combined into a single
> step.
>
> 3. Later in this course we are going to look at methods for deciding what ground cover type is represented by each pixel.  We will then give the pixel  a label.  Do you think  it would better to do that before removing geometric distortions, or should the geometry be corrected beforehand?
>
> > ## Solution
> >
> > 1. The recorded image would have its horizontal scale distorted compared with the correct scale on the map.  The vertical scale is unaffected.  To correct the error, we can scale either the horizontal (x) axis or the vertical (y) axis to get the correct aspect ratio.  In practice the vertical scale is usually adjusted.  For example, in the case of the Landsat multispectral scanner the vertical scale is expanded by 1.411 to account for the over-sampling along a scan line (see J.A. Richards, Remote Sensing Digital Image Analysis, 5th ed., Springer, Berlin, 2013, page 65.) 
> >
> >    Thus: x = u and y =av. In matrix form this distortion is described by
> >
> >    ![matrix1](..\fig\Lec_8\Quiz\matrix1.png)
> >
> >    To correct the image, we have to compute the map coordinates from the image coordinates, which means inverting this expression to give![matrix2](..\fig\Lec_8\Quiz\matrix2.png)
> >
> >    2. Let M1,M2,M3 etc. be matrices that correct for different types of geometric 
> >       distortion.  Then the combined distortion can be described by 
> >
> >       ![matrix3](..\fig\Lec_8\Quiz\matrix3.png)
> >
> >    , which needs to be inverted to produce the correction equation. 
> >
> >    3. In principle it shouldn’t really matter, especially if nearest neighbor resampling is used (see later lecture).  However, there is a school of thought which says that is it better not to do anything to the original pixel values that might introduce noise or some small difference into their values.  In that case, it would be better to analyse the original data to create class labels beforehand and then carryout the correction of geometry.
> >       {: .solution}
> >       {: .challenge}



{% include links.md %}

