---
title: Module 3 Lecture 10 - Other interpretation methods
teaching: 
exercises: 
questions:
- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---

### Module 3 Lecture 10: Other interpretation methods

We don't always have to use supervised or unsupervised techniques for pixel identification in remote sensing. Other approaches are used in practice. Most of our analytical focus in the course has been on Machine Learning. There are, however, a number of other approaches used regularly in practice, often founded on scientific as against data analysis principals. Lab searching using pixels spectra in hyperspectral images is one example of that, which we have already seen. One of the most longstanding and effective methods for assessing cover types recorded in a remotely sensed image involve indices, which are metrics computed from the brightness values of the pixels in sets of bands. For example, a simple vegetation index might just be the ratio of a near infrared measurement and the visible red measurement. The rationale for which becomes evident when we look at common spectral reflectance curves, such as shown on the bottom left of this slide. If we apply that vegetation index to all the pixels in an image, it will produce a map in which pixel brightness is correlated with a strong vegetation signature. The indices should be defined as functions of surface reflectance, which is implied by our reference to the spectral reflectance curves. But in practice, the formulas are often based on the digital numbers in the received image product. There are better vegetation indices, such as the two shown here. The most common is the Normalized Difference Vegetation Index or NDVI. Here we see an application of NDVI to know our AVHRR images for which the pixel size is one kilometer. This allows us to develop a continental scale vegetation index map, which demonstrates, in this case, the evolution of drought conditions over the past four years in Australia. The spring sequence is perhaps the most profound during the huge change in green biomass over the four year period. Many other indices are used in remote sensing, including those shown here, which allow compensation for the amount of soil reflectance in a pixel and those for monitoring water conditions, soil, green biomass and so on. Again, by way of summary, vegetation and other indices are the result of band arithmetic. That is, computing new values for the brightness value of a pixel from sums, differences, and questions of the originally recorded bands. Those new values emphasize properties of importance such as greenness. Secondly, used in time-series, indices can follow the development of important phenomena, such as the development of a crop or the evolution of a drought. Answering this question requires you to plot the equations of straight lines that result from the index definitions. For example, from the simple vegetation index, we have near infrared equals vegetation index times red, where vegetation index is the slope of a straight line through the origin. 


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
