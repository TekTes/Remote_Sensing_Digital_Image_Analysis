---
title: Module 1 Lecture 4
teaching: 30
exercises: 15
questions:
- "How do we record images of the earth's surface?"
objectives:
- "Instrument technologies and those that are commonly employed"
keypoints:
- "Satellite sensors can be of different types - using oscillating mirrors or CCD arrays"
- "Those sensors could also be carried on aircraft or drone platforms."
- "The sensors include a dispersion mechanism that separates the measured radiation into
a number of wavelength ranges, or wavebands."
- "Images are described by their coverage, their spatial, spectral and radiometric resolutions, and the range of wavebands they cover."
- "The field of view (usually measured in degrees) defines the swath width being imaged, while the instantaneous field of view (usually measured in milliradians) defines the spatial resolution or pixel size."
---

### How do we record images of the earth's surface?

In this lecture, we want to examine how images of the earth surface are recorded. 

In the last lecture, we looked at the types of platform that are used to carry remote sensing instruments. We now wish to look at the instrument technologies themselves, and those that are commonly employed. That is the focus of this lecture. 

Earth imaging could, of course, be carried out by mounting a simple digital camera on a platform. Today, that is often done with drones. 

Many of the earlier images of the Earth, taken by astronauts, are captured by film cameras. And in the first three of the Landsats satellites, a television camera was used. It was called a Return Beam Vidicon, and was one of two primary imaging instruments. 

Most remote sensing satellites today carry scanners of one form or another, to capture images of the Earth surface. They tend to make use of the forward motion of the platform along with some form of scanning, either across or along the path of the satellite, in order to build up an image of the landscape. 

In this lecture, we will look at the three most common types of image scanner. 

The line scanner. The earliest digital imager was a line scanner, a technology which is still in use today. It uses that mirror to scan across the path of the satellite, as shown in the slide, in order to focus strips of the Earth's surface onto a detector carried on the platform. 

![Module-1-Lecture-4](..\fig\Module-1-Lecture-4.gif)

By design, the rate at which the mirror scans and the forward velocity of the satellite, are arranged so that consecutive scan lines are adjacent to each other. And together form an image, as the satellite traces out its path. The mirror has to oscillate from side to side. 

In sensors like the Landsat multispectral scanner, upwelling radiation from the landscape is detected on the forward scan of the mirror. The mirror then resets to the opposite side of the satellite track, ready for the next scan. By contrast, the Landsat Thematic Mapper and its later variants, records data on both the forward and reverse scans. Sometimes, particularly in early aircraft sensors, a rotating mirror is used. This slide also introduces some important definitions. First, the width of the image recorded is called the swath. It is defined by the field of view, or FOV, of the sensor, which is the total angle over which it scans. The resolution of the sensor or scanner is called the instantaneous field of view, or IFOV. Again, this is defined by an angle which, when projected onto the surface, defines the pixel size in or the spatial resolution of, the recorded image. Most often the IFOV is the same in the along track and cross track directions. 

The mechanism described in the previous slide accounts for the scanning process. But most remote sensing imaging instruments are capable of recording in several wavebands simultaneously. With the line scanner, that is achieved by placing a dispersive element in the path of the radiation. That can be a diffraction grating or prism, the effect of which is to break up the incoming beam into individual beams, corresponding to the wavebands of interest. Those beams are then focused onto separate detectors, one for each waveband. 

The push broom scanner. Another common means for forming an image is to use a linear array of individual detectors, arranged across the direction of satellite motion. Usually, this is a CCD or charge-coupled device array. With one element for each of a series of longitudinal scan lines, that is, scan lines along the track of the satellite. Radiation falling on each detector is sampled in time, allowing pixels to be formed. The pixel size is defined by the detector's instantaneous field of view at the surface, and the rate at which the radiation is sampled compared with the forward velocity of the platform. No mechanical scanning is involved, apart from the forward motion of the satellite. The advantage of this technology is that more radiation can be gathered per effective pixel, allowing higher special resolutions to be achieved. Again, a dispersive device is incorporated to allow the simultaneous recording of several wavebands. There will be a separate detector CCD array for each waveband. 

![push_broom](..\fig\push_broom.gif)

Perhaps the most recent imaging technology, used on spacecraft and aircraft platforms, is similar to the push broom concept just discussed. But, instead of having a separate set of linear CCD arrays to record a discrete set of different wavebands, a two-dimensional CCD array is employed. The second dimension is used to replicate the effect of a very large number of separate linear CCD arrays. In this manner, the number of wavebands recorded simultaneously can be very large, typically up to 200 or so. Therefore, these sensors typically record simultaneously several hundred carriers of images of the landscape, ranging over the visible and infrared wavebands. As we will see later, that will allow a great deal of information to be obtained about the landscape being imaged. 

When the number of recorded wavebands is small, say 20 or lower, as for the two previous instruments, the devices are typically called **multispectral scanners**. When the number of wavebands can be in the order of 100 or so, as in this slide, the instruments are usually called **hyperspectral scanners**.

 ![hyperspectral_Scanner](..\fig\hyperspectral_Scanner.gif)

Now that we have seen how images can be recorded, we can summarize their important properties when used for remote sensing purposes. Recall first the geometric properties of the scanner shown on the right-hand side of the slide. The IFOV of the scanner defines the spatial resolution or pixel size on the ground, whereas the FOV of the scanner defines its swath width. Also shown in this diagram are the typical units used to describe each of those properties in practice. On the left-hand side of the slide, we have summarized how an image, in remote sensing, is described. Overall, it is defined by the swath width in the cross track direction and the frame size in the along track direction. Most often, particularly for operational missions, the frame size is chosen to be the same as the swath width. The next important feature is the pixel size, which determines the level of detail about the Earth's surface being recorded. As indicated previously, we often refer to pixel size as the spatial resolution of the image. Clearly, we are also interested in the number of wavebands being recorded. As indicated here, the wavebands are all registered with each other geometrically. Finally, we need to know the number of brightness levels available for each pixel. For a black and white image, those levels will be graduations from black to white. In fact, any image recorded in a given waveband will effectively be a black and white image representing the levels of received radiation from zero to the maximum sensitivity of the detector. Later on, we will see how we display those recorded bands in color. The number of brightness values available per pixel is defined by binary arithmetic. For example, an 8-bit pixel is capable of representing 256 levels of gray, from 0 through to 255. Most current operational remote sensing images will have 8,10, or 12-bit pixels. The number of brightness values, often expressed as a number of bits, is called the dynamic range or radiometric resolution of the sensor. Although it is of interest to see how land scanners and hyperspectral instruments operate, the really important message from this lecture is the geometric characteristics of the sensor. That is, the instantaneous field of view, the field of view, and so on, and the properties of the image itself. These questions ask you to think a little more laterally about how images are recorded. In particular, the third question raises an important matter about the distortions in geometry that can occur for imaging systems with wide fields of view. 

![tech_char](..\fig\tech_char.gif)

> ## Quiz
>
> 1. CCD array sensors tend to have higher spatial and spectral resolution than those based on scanning 
> mirrors.  Why?
>
> 2. With  aircraft systems, why is IFOV a more  meaningful term than pixel size? Has it to do with the
> flying height?
>
> 3. Will pixel size vary across the swath for an image recorded by a remote sensing platform?
>
> > ## Solution
> 
> > ~~~
> > 
> > ~~~
> 
> > {: .solution}
{: .challenge}

 {% include links.md %}