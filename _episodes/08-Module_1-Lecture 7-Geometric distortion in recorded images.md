---
title: Module 1 Lecture 7
teaching: 
exercises:
questions:
- "What are the sources of geometric distortion and how they can be corrected?"
objectives:
- "Identify the different sources of geometric distortion"
- "Familiarize with techniques used to correct geometric distortion"
- "Understand how an image can be registered to a map coordinate system."
keypoints:
- "Distortions in image geometry can arise because of:"
- "~~ Instrumentation effects"
- "~~ Platform and sensor motion "
- "~~ Wide fields of view"
- "~~ Earth curvature"
- "To understand the effect on the image product it is important to envisage the pixels laid down on a rectangular grid.  The result is often opposite to what might be expected.  For example, if the sampling rate across  a scan line is too fast, so that the recorded IF0Vs overlap, the recorded image ls too broad, not too narrow"
---

### Geometric distortion in recorded images

We now come to the rather more important matter of geometric distortions in remote sensing imagery. This is important because images from aircraft and drones are often not corrected for these error. So you need to know how to do that yourself if geometric integrity is important. 

In this lecture we are going to look at sources of geometric distortion and how they can be corrected. This will also lead us to see how an image can be registered to a map coordinate system.

 

- The major causes of geometric distortion are:
  - The rotation of the earth during imaging
  - Variations in platform attitude, altitude and velocity
  - The curvature of the earth  when viewed from space
  - The wide field of view of some sensors
  - Instrumentation effects

As we mentioned earlier, the techniques used for correcting errors in geometry are the same methods we use for making sure an image is registered to a non-map basis. There are many sources of geometric error, including the fact that the earth and platform are in motion during image acquisition. The fact that the platform can vary in altitude, attitude, and velocity, the fact that the earth is curved when seen from space, and the fact that the instruments themselves introduce geometric variations by virtue of their design. We make the assumption that all recorded bands are affected equally. Therefore, we apply our techniques to each band in an image separately, but only have to develop our correction methods on a single band. 

It helps for much of what is to follow. If we look carefully at how an image is built up from recorded pixels. The diagram in this the figure below shows a group of pixel or grid centers. The grid centers are spaced apart by the IFOV of the sensor and in this case, we have shown an array of L lines of M pixels each. What is the pixel? It is a sample of the earth surface equal in size to the IFOV of the sensor. A set of pixels is therefore just a set of those samples. The rate of sampling is arranged ideally so that when we form an image by laying down a record of pixels on the grid, the pixels join up with each other as depicted here. We need to keep this model in mind in everything we do now, with respect to image geometry. 

![geometric_distortions](..\fig\Lec_7\geometric_distortions.gif)

The first time this rectangular grid concept becomes useful is in understanding the error introduced into an image as a result of the rotation of the earth. The signal coming from a remote sensing platform is just a string of pixels for each recorded line of data. Knowing nothing better, we just lay them down on a regular image grid, as discussed in the previous slide. That gives the screen looking image on the left hand side of this slide. However, during satellite image acquisition, the earth is moving to the East, underneath the platform. In this case, image in the platform is moving down the slide. A part of the image that is recorded last was actually to the West when the recording of this image segments started, and has moved itself directly under the platform by the time the last line of pixels is recorded. Therefore, to make the image geometry reflect that of the actual portion of the earth surface being imaged, the second and last lines of pixels need to be shifted progressively to the West, as shown in the right-hand image. If we know the velocity of the spacecraft, the earth velocity of that location, and the size of the image, it is relatively easy to work out how much each line of pixels needs to be shifted by. 

We now consider a very unusual form of geometric distortion. It occurs when the scan of the sensor is very wide. In other words, it has a large FOV or field of view. The diagram on the left-hand side shows the relevant geometry. Notice that the area of earth image at the swayed extremity is much larger than that at nadir, that is directly under the sensor. Yet, even though it corresponds to a larger region on the ground, the actual pixel is displayed as the same size as the pixel at nadir, when used to construct an image. When those recorded pixels are placed on a regular display grid, the pixels towards the swath edges, even though displayed in the same size as those towards the center of the scan, cover a much larger ground region and thus appear compressed by comparison to those at the swath center. To illustrate what this does to an image, consider the ground scene on the right-hand side of the slide. Be careful here. The regular grid shown might represent a set of BigQuery size square fields, it is not the display grid. Image in the ratio of those fields consists of many pixels. The two broader diagonal lines might represent roads that cut across the fields at 45 degrees as shown. When the recorded pixels are laid down on the regular display grid, the effect is to compress the edges of the image as shown on the very right-hand side image. That is because the pixels at the edges represent a greater geographical region than those at the center, and yet are displayed as the same size. The visual effect is to give the impression that the image rolls off at the edges. The diagonal roads take on the S shape shown, so that sometimes this panoramic distortion is called S binned distortion. 

From satellite altitudes, sensors with a wide field of view are sensitive to earth curvature as seen in this slide. Without going into too much detail, the net effect on the image is to exaggerate the panoramic distortion of the previous slide. 

Now let's look at some of the errors caused by the instruments themselves. For an oscillating mirror scanner as seen here, the mirror has to slow down, stop, and reverse direction at the end of each scan. By definition, the scan has to be non-linear at the swath edges. To minimize the non-linearity, a scanning window is defined over which data is recorded and beyond which any other detected radiation is ignored. Clearly, the scanning window is chosen to exclude the extreme non-linearities at the scan edges. 

We now look at two other instrumentation problems. The first is related to the fact that some scanners take a finite time to cross the swath while a platform is moving forward during data acquisition. That means that the portion of the earth being scanned is further forward on the swath edge at the end of the scan. To correct for this effect, the display pixels had to be shifted progressively backwards towards the age of the image. The second error is called aspect ratio distortion. It is caused by the pixel sampling rate across the scan line not being synchronous with respect to the IFOV of the instrument. If the sampling rate is too fast, the pixels overlap. If it is too slow, the pixels have spaces between them. Again, when these pixels sequences are displayed on a regular grid, the effect is to expand or compress the image across the track. 

The last point in this summary demonstrates the expansion of the image across the trend caused by oversampling with respect to the IFOV of the instrument. This is a particular problem with the landsat multispectral scanner. When answering the questions in this quiz, you should keep in mind that the displayed version of the image almost mirrors what is happening on the ground in terms of geometric errors. For example, to correct for the effect of earth's rotation to Eastwards, pixels have to be shifted to the West. 

> ## Quiz
>
> 1. How would each of the following sources of geometric distortion appear in a displayed image?
>
>   - Earth curvature
>   - Finite sensor scan time
>   - Platform roll
>   - Platform gradually rising in height during orbit
>
> 2. Would the following be sources of geometric distortion *for* a pushbroom scanner?
>
>    - Finite scan time?
>    - Scanning non-linearities
>    - Wide field of view systems
>
>    
>
> > ## Solution
> >
> > ???
> > ???
> {: .solution}
> {: .challenge}

{% include links.md %}
