---
title: Module 1 Lecture 10 
teaching: 
exercises:
questions:
- "How do we register an image to a map grid?"
objectives:
- "Recapping from the previous lecture, plus a bit more:"
- "Find points in the image that correspond to each location in the map grid. "

If the points located in the image by the mapping polynomials are exactly pixel centres, then the pixels are simply relocated to the corresponding position on the map grid we saw in the last lecture.

But that will rarely be the case.  More often, the point in the image indicated by an application of the mapping polynomialswill not fall on a pixel centre, but will be somewhere between several
pixel locations as seen in the following"
keypoints:
- "When we want to register an image to a map grid the steps involved are:"

- "Select control points"

- "Use the control points to find the two mapping polynomials"

- "Use the mapping  polynomials  to find the grid positions in the image corresponding
to each grid location in the (geometrically correct) map"

- "Use a resampling (interpolation) method to determine the brightness value to use
for the location indicated by the mapping polynomials"

- "The overall procedure is sometimes called geocoding"
---

### Resampling

We now introduce a new term in this lecture. The process of finding an actual value for the pixel in the image to place onto the map grid using the process of mapping polynomials is called resampling. Remember, we determined the explicit mapping polynomials using the set of control points to find the unknown coefficients. We then used those polynomials to find points in the image which correspond to points in the map. If the points in the image indicated by the mapping polynomials fall exactly on a pixel grid center, then the pixel is simply relocated onto the corresponding or correct position in the map grid. However, rarely will that be the case. More often, the point in the image indicated by the mapping polynomials, will not fall exactly on a pixel center in the image, but somewhere between several pixel centers, as we see in the next slide. 

| ![grid_of_pixel](..\fig\Lec_10\grid_of_pixel.gif) | ![grid_of_pixel](..\fig\Lec_10\grid_of_pixel.png) |
| ------------------------------------------------- | ------------------------------------------------- |
|                                                   |                                                   |

Here we share the mapping from a geometrically correct map to the image for the general case, where the projected image coordinate does not match a pixel grid center exactly. Instead, the projected point lies somewhere in a region bounded by four grid centers. What we have to do is to estimate what the brightness of the original scene would have been at that position. Effectively, that means carrying out an interpolation over the neighboring measured pixels. Note here we have indicated the pixels explicitly by dashed lines centered on each of the grid intersections. How do we go about finding a brightness for a pixel that is for the scene at the location indicated by the mapping polynomials? A simple approach, and one which was often used in practice, is to choose the nearest recorded pixel as seen here. This is called nearest neighbor resampling. For it to work effectively, the grid spacings in both the map and the image should be about the same. There are two other resampling techniques often used in practice. Both are based on interpolations of brightness over neighboring pixels. The first involves linear interpolations over the four surrounding pixels. It starts by computing the two interpolated brightness values along each scan line above and below the projected pixel point using the real pixel values either side. These are shown as the intermediate interpolants in the top right-hand's diagram. The next step is to do a vertical interpolation over those two intermediate values to get the final brightness value for the pixel. This process is called bilinear interpolation. The second, more sophisticated procedure is to interpolate over four sets of four pixel brightnesses, as illustrated on the bottom right-hand side of the slide, and then interpolate over the four vertical intermediate interpolants. 

| ![geometrically_correct_image](..\fig\Lec_10\geometrically_correct_image.gif) | ![geometrically_correct_image](..\fig\Lec_10\geometrically_correct_image.png) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

Cubic polynomials are used to undertake the interpolation, so that the technique is generally called cubic convolution resampling. While a more complicated process, cubic convolution resampling, generally leads to a smoother looking image after geometric correction. By contrast, nearest neighbor resampling can produce a blocky looking product if the scales of the image and map are significantly different. Although we have developed the process of using mapping polynomials for registering an image to a map, and therefore effectively removing the major sources of geometric distortion, the same process can be used to co-register sets of images. This is often needed if the user has available for analysis, several images of the same geographical region, often taken by different platforms and sensor types. As noted here, we're not restricted in how many images we can co-register. It is just a matter of choosing one image as the master, taking the place of the map, and registering all other images to it. 

| ![two_other_methods](..\fig\Lec_10\two_other_methods.gif) | ![two_other_methods](..\fig\Lec_10\two_other_methods.png) |
| --------------------------------------------------------- | --------------------------------------------------------- |
|                                                           |                                                           |

As seen in this summary, the process of registering an image to a map in order to remove geometric errors is often called geocoding or sometimes geo-referencing, because the pixels can now be represented by their map coordinates, latitudes and longitudes, rather than by the original row and column numbers. 

The questions here, ask you to think about some practical aspects of using ground control points and mapping polynomials for geometric correction. Please give them serious thought because that will feature strongly in the next lecture. 

> ## Quiz
>
> - What would guide you in selecting good control points?
>
> - Is it preferable to use mapping polynomials of low or high order?
>
> - Nearest neighbor resampling uses recorded pixel brightness values for placement on the map grid, whereas cubic convolution resampling creates new, interpolated brightness values. Is either preferable?
>
> - Could the registration techniques treated in the last two lectures be used  to register one map to another map?
> > ## Solution
> >
> > ???
> > ???
> {: .solution}
{: .challenge}

{% include links.md %}
