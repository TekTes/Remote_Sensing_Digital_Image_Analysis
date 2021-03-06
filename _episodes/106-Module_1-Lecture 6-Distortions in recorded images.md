---
title: Module 1 Lecture 6 - Distortions in recorded images
teaching: 
exercises: 
questions:
- "what are the distortions in recorded images?"
objectives:
- "Understand the different kinds of distortions and methods for mitigating their effects. "
keypoints:
- "when images are recorded they invariably contain distortions which must be corrected."

- "Distortions in the recorded brightness values, called radiometric distortion, can result from sensor
non-idealities, the wavelength variation in solar radiation and the absorbing and scattering behaviour
of the atmospheric path of the energy to and from a pixel."

- "when several detectors are used to record an image in a particular waveband (i.e. one image channel or band) mismatches in their input-output characteristics can lead to transverse or longitudinal line striping."

- "The wavelength dependence  of the solar energy incident on the earth's surface is described by Planck's radiation law.  The dependence  is particularly strong from the visible to the reflected infrared range."

- "As seen in lecture three, atmospheric gases have absorption features at specific wavelengths.  They will
superimpose themselves on the spectrum of the ground  cover type being imaged."

- "Atmospheric scattering adds to the signal recorded by the sensor, and should be removed."
---

### Distortions in recorded images

Images are never perfect when recorded. It is the purpose of this lecture and those which follow to understand that the image is acquired by remote sensing missions contain errors compared with the region on the ground being imaged. 

We are familiar with image errors in our day to day life. When we take photographs with hand held cameras, we often encounter distortions because the subject or camera has moved, or because sunlight glints in from the side, or because the contrast and brightness of the image are poor compared with reality. Exactly the same is true with the images recorded by satellite sensors. 

Before we can make sensible use of those images, we need to understand the source of error, and distortion, and the means by which we can correct them to create an image which is as close to the actual landscape as possible. In this lecture, we will concentrate on the most important types of distortion that frequently occur in remote sensing imagery. Often they are corrected before the images are sold to the user. 

In your work, you may not be particularly aware of them. Nevertheless, it is important that we understand how distortions arise and the means by which they are corrected. 

In some cases, most notably when images are recorded using aircraft and drone platforms, you may have no alternative than to correct the errors yourself. 

An important reason for understanding the corrections of distortions in image geometry is that the techniques we employ for correction can also be used to register images to maps and images to other images. 

Finally, as with any computer processing in image analysis and remote sensing, if you understand the basis of the algorithms employed, you are in a much better position to understand their limitations and characteristics. 

Distortions can occur in the geometry of an image and in its brightness. We will look at each of those in turn, commencing with brightness distortions. Distortions in brightness are generally known as radiometric distortions. Radiometry, you will recall, describes the brightness levels in an image. 

As seen in figure below, we subdivide radiometric distortions into three subcategories: those caused by the persons of the instruments themselves, those caused by the shape of the solar radiation curve, that is the Planck radiation graph for solar radiation, and those caused by the effect of the atmosphere, and particularly how the effect of the atmosphere varies with wavelength, any radiometric characteristics that are wavelength dependent or cause relative brightness distortions among the bands. That is a critical concern because band to band relative brightness differences are what allow us to understand the spectral reflectance characteristics of Earth surface types. Recall the differences between the spectral reflectance curves for vegetation, soil, and water from the previous lecture. We don't want those relativities upset by radiometric distortions. 

![distortions](..\fig\Lec_6\distortions.gif)

Let's start by looking at the effect of instrumentation errors on brightness. We are particularly interested in the behavior of the radiation detectors that measure the upwelling energy in each band. 

As seen on the bottom left-hand side of the following figure, the ideal radiation detector has a linear characteristic that indicates the magnitude of the electrical signal generated by a certain level of incident radiation. Ideally, the curve has to be linear so that variation of the output signal mirror those of the input signal. That is, of the input radiation level. 

![distortions](..\fig\Lec_6\distortions.png)

There are two important detector properties described in this graph. The first is the slope, which is referred to as the gain of the detector. A higher gain detector will generate a larger electrical signal for a given input level of radiation. The second property is the offset, which indicates that the detector will generate a very small signal even if there is no radiation input. That is just a characteristic of electrical devices and is sometimes called dark current. It can be reduced by cooling the detector. If a particular imaging sensor consists of a number of detectors such as the ETM+ and the HRV family, it is important that their gains and offsets be matched as closely as possible. In practice, however, the situation is more like that shown on the bottom right-hand side of the the figure below.

![radiometric_distortion](..\fig\Lec_6\radiometric_distortion.gif)


Although the drawing is exaggerated, the detectors will often have slight variations in their offsets, and slight differences in their gains. In the simple case of the Landsat Multispectral Scanner, there are six detectors per band. If there are noticeable differences in gains and offsets, it is possible to see its dropping in an image, which repeats every six lines. 

The figure below shows an example of the land striping in the Landsat Multi Spectral Scanner image resulting from detector mismatches. You will see that the land striping is very noticeable in the water part of the image. How can we reduce the land striping distortion caused by a mismatch in sensor characteristics? A simple method is to compute the histograms of the signals recorded by each individual detector and then match the means and standard deviations of those histograms. We will not go into detail here, but it is a fairly simple process and is often employed in practice. 

![radiometric_distortion](..\fig\Lec_6\radiometric_distortion.png)

When we get to image contrast modification in a later lecture, you will be able to see how this is done. When that procedure is applied, the corrected image on the bottom of the slide results. You will see that the striping has been reduced considerably. Next, we examine the variation with wavelength of the solar radiation curve. As seen here over the optical range of wavelengths, there can be a significant change in the level of radiation falling on the Earth's surface. That would suggest that the visible wavelengths would appear brighter than those in the infrared range just because of the level of sunlight and not because of the spectral reflectance variation of a given [inaudible]. Clearly, that solar variation needs to be corrected if meaningful spectral reflectance information is to be obtained in a recorded image. 

![atmospheric_layer](..\fig\Lec_6\atmospheric_layer.gif)

Correction can be carried out by using the ideal Planck curve for broadband sensors. For hyperspectral instruments, however, in which the spectral resolution is very high, the actual solar curve measured above the Earth's atmosphere needs to be used because the real solar spectrum contains fine spectral detail, notably Fraunhofer lines. Now let's look at the effect of the atmosphere on the brightness of the image. The atmosphere absorbs radiation on its path from the sun to the pixel and from a pixel to the sensor, as we saw in a previous lecture, but the atmosphere also scatters radiation directly into the sensor, as depicted in this figure. 

![atmospheric_layer](..\fig\Lec_6\atmospheric_layer.png)

There is a third more subtle effect and that is scattering from the atmosphere onto the pixel via a diffuse and not a direct path, also shown here. There are other less obvious scattering pathways as well, all of which need to be considered when looking at the effect of the atmosphere on recorded image data. 

To make the situation simpler, consider just the two mechanisms shown here. We know that the direct path from the sun to the pixel and the pixel to the sensor suffers selective absorption. But what does the atmospheric scattering pathway do to the recorded signal? 

The answer to that question is quite complex, and depends on the size of the particles that make up the particular atmosphere through which imaging takes place. Here we show three different atmospheres. At the bottom, we have a clear atmosphere in which the only scattering elements are the molecules of the gases that make up the atmosphere itself. In the middle, the atmosphere also contains some smaller particulates such as mist. At the top, the atmosphere is foggy, containing large scattering particles of water. Scattering from a clear atmosphere is called Rayleigh scattering. It is strongly wavelength dependent, as illustrated in the graph, with blue light being scattered the most. The net effect is a blue coloring. That is why we see the sky as blue on a clear day. Scattering from a light haze is called Mie scattering. It is not as strongly dependent on wavelength as Rayleigh scattering, so that the effect is a bluish-white appearance. Scattering by large particulates is almost independent of wavelength, so that the atmosphere then appears almost white. That is why we see fog as white. These scattered signals superimpose on the direct path signal, from the previous slide. As you might expect, the short wavelengths are affected more than the long wavelengths. 

One simple means for compensating the wavelength dependent effect of atmospheric scattering, is to produce histograms of each of the recorded image bands. The effect of atmospheric scattering shows up in the histograms as offsets from zero, as illustrated in the histograms of this example. Recall that the shorter wavelengths are affected more. This is seen in the visible blue histogram in this example. As wavelength increases, the offset [inaudible] atmospheric scattering reduces as depicted. In order to correct for the effect of the atmosphere, the offsets are subtracted in each case, so that the image histograms are reset to start from zero. In fact, the offsets are subtracted from the brightness of every pixel in the image, which leads to the corrected histograms. 

Correcting for the effects of atmospheric absorption on the direct path signal usually requires a knowledge of the wavelength dependence of the various actual absorbers in the atmosphere. There are a number of quite comprehensive software packages that can be used for that task. 

The figure below shows an illustration of the effect of all atmospheric constituents on the spectrum of a vegetation pixel at the top. It also includes the distortion caused by the shape of the solid irradiation curve. The corrected version is at the bottom. Note that complete absorption due to water vapor cannot be compensated, but that is not a problem, because there is usually no significant information available in any case in those regions. 





![atmospheric_scattering](..\fig\Lec_6\atmospheric_scattering.gif)



As we noted at the start of this lecture, many of the distortions discussed will have been compensated in the image product repurchase, particularly from satellite missions. Nevertheless, as a remote sensing practitioner, it is essential that you have some background knowledge of what constitutes errors in radiometry so that you are mindful of what corrections have been carried out and what might be needed in the case of imagery you acquire, which has had no corrections applied.

 ![methods_of_compensation](..\fig\Lec_6\methods_of_compensation.gif)

In the first of these questions, use your own experience, particularly if you have flown over regions of patchy fog and mist. The last question, in a sense asks you to build up what might actually be recorded by a sensor as against what we think might be recorded. 

![absorption_of_atmoshphere](..\fig\Lec_6\absorption_of_atmoshphere.png)

![example_of_correction](..\fig\Lec_6\example_of_correction.gif)

> ## Quiz
>
> 1. Suppose a natural colour photograph of a vegetated region is taken from a satellite.  Describe the 
>general appearance of the image under the three scattering conditions illustrated in the last slide of 
>this lecture.
>
> 2.   Can you think of a simple  way to correct line striping caused by mismatches in the input-output 
>characteristics of a detector?
>
> 3. what would be recorded in each of the following situations, over the visible to reflected infrared 
>range of wavelengths;
>
>    a - No atmosphere and an ideal reflecting surface that reflects all incident energy, irrespective of 
>wavelength
>
>    b - A clear atmosphere and an ideal reflecting surface
>
>    c - No atmosphere, but a vegetated surface (use the spectral reflectance curve for vegetation from 
>Lecture Three)
>
>    d - A clear atmosphere and a vegetated surface
>
> > ## Solution
> >
> > 1. There will be significant scattering of blue sunlight under all three conditions, so that the blue band would appear hazy; the other two would look moderately free of any atmospheric effect.  At the other extreme of particulates (fog, for example) all visible bands would be affected showing a whitish haze over the scene.  For the in-between scattering condition, the blue band would look hazy, the green band slightly so, and the red band clear of any major effects.
> > 2. The histogram matching technique could be used as described in the lectures, in which the histograms of the lines of pixels recorded by each detector are matched. 
> > A simpler approach is to compute the mean and standard deviation of the lines of pixels recorded by each detector and match the signals of all other detectors to the first one such that the means and standard deviations then become all the same.  A formula for doing that will be found on page 30 of J.A. Richards, Remote Sensing Digital Image Analysis, 5th Ed., Springer, Berlin, 2013.
> > 3. 
> >
> > a - The surface would appear white
> >
> > b - The surface would appear white, with some blue haze
> >
> > c - The surface would be coloured according to the positions of the bands on the
vegetation reflectance spectrum
> >
> > d - The surface would be coloured according to the positions of the bands on the
vegetation reflectance spectrum but with a slight emphasis to the blue end of
the spectrum
> {: .solution}
{: .challenge}

{% include links.md %}