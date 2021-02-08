---
title: Module 1 Lecture 13 - Enhancing image contrast
teaching: 
exercises: 
questions:
- "How do we enhance image contrast?"
objectives:
- "Understand the processes of contrast Enhancements"
keypoints:
- "Imagery. as originally recorded,is generally poor in contrast because It doesn't use the available brightness range."

- "Contrast can be enhanced effectively by adjusting the brightness value of each pixel according to a brightness value mapping function."

- "Because we only have a discrete number of brightness values (say 256, 512, etc), set by the radiometric resolution of the sensor, the brightness value mapping function is often implemented  in the form of a look-up table."
---


### Module 1 Lecture 13 Enhancing image contrast

This lecture is a little outside the mainstream of our treatment, but it is important because most of the images we deal with visually have had their contrasts enhanced in order to improve their visual quality and range of colors. Here we want to understand a little of how that is done. The detectors used to record each band of image data are calibrated so that they can respond to the darkest and brightest cover types anticipated. Typically, those cover types could be deep clear water or snow and cloud types. That means that most of the cover types that are imaged fall in a range of brightnesses well inside the range from total black to full white, as shown on this slide. For a typical recorded image, the appearance is therefore slightly dull and poor in contrast. It will be good if we could expand the range of recorded brightness so that the signal of interest covers the full range from black to white. What we need to do now is understand how that can be made to occur. In order to set up a process for changing the range of brightness values, we need first, some means for describing the distribution of brightness in an image or band. We choose for that, the image histogram, which is a bar graph of the number of pixels of a given brightness plotted as a function of that brightness value. Here we see an image as it has been recorded by an aircraft scanner. Note how poor it is in contrast, brightness, and color. Note particularly that it has a reddish appearance, as we mentioned in the last lecture. On the right-hand side, we have shown three histograms. One corresponding to each band and colored according to the color in which the band is displayed in the color composite image. Note that while each histogram commence as close to the lowest brightness value in each case, that is zero, the upper extremities of the histograms are well shorter the maximum available brightness of 255. Ideally, we would like the histograms to cover the full range of brightness. If we could stretch out the histogram as shown here, so that it covers the full brightness value range, we won't have an image with much better contrast, as we will now see. To do that, we introduce a graph called a brightness value mapping function. It shows us how to take the old brightness values in a histogram and change them to new values which cover the full brightness value range. Effectively, what it does is tell us how to relocate the bars in the histogram more favorably. We usually work out the nature of the brightness value mapping function by examining the recorded histogram and noting the desired new histogram distribution. Once we have that mapping function, we apply it to the image in the following manner. We start with the first pixel of the image, read its value onto the abscissa of the mapping function, and read off its new value from the ordinate. That new value is used in place of the old brightness value of the pixel. That is done pixel by pixel and line by line until all of the pixels in the image have had their brightness values modified according to the brightness value mapping function. The resulting image then maps a much better use of the available range of brightnesses. We have to do that for each band of data. The brightness value mapping function will be different in each case. Here we see the results. Commencing with the poorly contrasting original image, we construct the histogram for each band. Then expand those histograms via their own respective brightness value mapping functions. When applied to the pixels in each band, the color composite image, say generated, is a much nicer looking image product on the right-hand side. In that final product, we see a much better range of brightness and contrast, and certainly a much better use of color. You can see now why contrast enhancement is almost always used in remote sensing when visual interpretation is important. Because we are dealing with a discrete number of brightness levels when handling remote sensing imagery, the brightness value mapping functions of the previous slides are actually a set of points equal in number to the number of discrete brightness values. For 8-bit imagery, there will be 256 pairs of input old and output new brightness values. For 10-bit data, there will be 1024 pairs and so on. As a result, we represent the brightness value mapping function in a computer algorithm as a look-up table, as shown in the last point on this slide. Take particular note of the second question here. The brightness value mapping function does not always need to be linear, as discussed in this lecture. Instead, it can have a range of non-linear forms which can give added emphasis to particular ranges of brightness.

> ## Quiz
>
> 1. Explain why all cover types appears reddish in the as-recorded example of this lecture whereas in the enhanced version soils and bare regions appear blue and bluish-green.
> 2. The brightness value mapping function used in this example is linear.  Can you suggest other (non-linear) mapping functions that might be particularly useful?
> 3. Suppose a particular sensor has two wavebands.  We can construct two individual histograms, in which the independent variables (abscissas) are the brightness values in each waveband.  For this image can a histogram be constructed with two independent variables?
>
> > ## Solution
> >
> > 1. This is best illustrated in a diagram, as below:
> >
> >    ![EOL-quiz-answers-module-1](..\fig\Lec_13\Quiz\EOL-quiz-answers-module-1.png)
> >
> > 2. TThere is a whole range of possibilities.  Piecewise-linear functions can be used to control brightness changes in certain ranges, an exponential function will highlight differences in the higher brightness levels, whereas a logarithmic function will highlight differences at lower brightness levels.  See Section 4.3 in J.A. Richards, Remote Sensing Digital Image Analysis, 5th Ed., Springer, Berlin, 2013.
> >
> > 3. Yes, it will be a two-dimensional array of cells, with the axes corresponding to the brightness values in each of the two bands and the cell values being equal to the count of those pixels which have both of the brightness values.
>  {: .solution}
{: .challenge}

{% include links.md %}