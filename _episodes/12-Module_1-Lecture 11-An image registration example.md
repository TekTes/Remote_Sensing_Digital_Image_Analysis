---
title: Module 1 Lecture 11 
teaching: 30
exercises: 0
questions:
- "?"
objectives:
- ""
keypoints:
- ""
---

### An image registration example

In this lecture, we will demonstrate the application of the procedure just developed by registering one image to another. The same procedure is used for registering an image to a map to remove geometric distortions. By using an image to image example though, it is easy to highlight some pitfalls that must be avoided. The example we have chosen involves portions of two Landsat multispectral scanner images of a region in the northern suburbs of the city of Sydney, Australia. One was acquired in 1979 and the other in 1980. We have only shown one of the near infrared bands here. Once those bands have been registered, all bands can be registered using the same control points and mapping polynomials to generate registered color products. Clearly there are major brightness differences between the two images. Since they have been recorded in the near infrared, both healthy green vegetation and urban regions, show as bright, water shows as black and the dark gray regions are bird vegetation resulting from fires. In the 1979 image. There is a major fast guy in the center by 1980, much of that has revegetated but two new fast cars are evident. One to the northwest on the boundary of the river and the other in the central southern part of the same. There are geometric differences between the images as well, even though they are less evident. It is by registering the knot in ATMs to the 1979 image that we will remove the geometric differences between them. Had the 1979 image spending map then that would amount to remove in geometric distortion from the 1980 image. Our first task is to choose a set of ground control points. On this slide, we have shown two different sets. Those on the top tier of images are well distributed over the scene. Whereas, those on the bottom images tend to be clumped with none towards the image edges. Notice that we have chosen some control points on the water, land boundaries. As much as possible, those sorts of control points should be on headlands and not river inlets. So the title variations are minimized. In general, we should choose as control points, features which do not change in position from image to image. Road intersections are good as our corners, our buildings, and fields. In this example, we are going to use third order mapping polynomials and cubic convolution resampling. This slide shows the results of registering the 1989 image, The Slave. To the 1979 image the master using the good set of control points. That is a set that was well distributed over the image. In order to demonstrate how well the registration has worked, we have displayed the master image as red and the slide image as green. The reason for doing that is that where the images are in alignment geometrically and have approximately the same brightness, the combination will appear yellow, which is the additive combination of red and green. Here we see that the registration is very good. Apart from the color differences due to the 1979 and 1980 fire scars, the combination is yellow with no obvious red green separation. The other red border is just part of the 1979 scene for which there is no not in AD coverage. The fire scars colors are interesting, the 1979 scar shows as green because there is very little red signal from the 1979 pixels. Whereas the 1980's scars show as red for the same reason. That is there is very little 1980 signal in those portions of the image. This slide shows the result of registration using the poorer set of control points. Where the control points were bunched, the registration is very good. But beyond the distribution of control points, the registration is particularly bad. Note especially the red and green offsets around the edges of the water. Note in the yellow color, we can see that the 1980 image has been stretched out of shape across the diagonal. We now wish to understand that behaviour. We can get a good idea of well behaved and poorly behaved registration by looking at fitting a curve through a set of points as shown in this slide. The first order equation matches the distribution of points moderately will and seems to extrapolate in a well behaved manner beyond the set of points. The second order curve gives a slightly better match to the points, but seems to diverge unnecessarily beyond the data points. Finally, the third automatic polynomial can be made to fit the data points more closely than the other two. But it behaves quite radically beyond the extent of the data. In other words, it does not extrapolate well. The general lesson we learned from this exercise in curve fitting is that low order polynomials may not fit a set of data points as well as higher order polynomials. But in general terms, they will extrapolate better. In contrast, higher order polynomials may match the available data better, but will extrapolate poorly. Returning to the previous slide, the third order mapping polynomial fits a region of the image in the cluster of control points very well. But beyond that region it extrapolates poorly. That gives us a particularly important guide in the choice of control points. As far as possible, the set of control points should be distributed uniformly across the same and enclose the region of the image for which accurate registration is important. If there's any data about the distribution of control points, a lower order mapping polynomial should be used. This example demonstrates the benefit of using lower order mapping polynomials when the distribution of control points, is not good, it uses a poor set of control points from the previous example. The result of that example, is shown on the left hand side of the slide. Remember, this was generated, using third, order mapping polynomials. Without changing anything else, the image on the right hand side was generated using first automatic polynomials. As observed, the extrapolation of the rich sit not in it image ingrained, is much better than when the third order polynomials we use. There will be greater registration error in the vicinity of the control points. But that is not noticeable visually in this simple case. Just by whatever Amanda every band of an image has to be registered or corrected in this manner. Provided the band to band registration from the image supplier is good, the same control points and mapping polynomials can be used. These questions relate to practical aspects of image registration, including geometric correction. And not so much to the theory of the process itself. They ask you to think about we might generate unintentional problems if you're not careful with your choice of technic scale, and methodology. 

{% include links.md %}