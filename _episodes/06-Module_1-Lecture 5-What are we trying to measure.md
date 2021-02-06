---
title: Module 1 Lecture 5
teaching: 
exercises:
questions:
- "What are we trying to measure?"
objectives:
- "Look at the properties of the earth's surface that can be detected by remote sensing instrumentation."
- "Examine those properties and understand why certain weapons have been chosen in the design of sensors commonly used in civilian remote sensing missions"
keypoints:
- "Optical remote sensing systems measure reflected sunlight."
- "We can also image  heat coming from the earth itself - that is the basis of thermal imaging."
- "Fires burning on the earth's surface can also be detected  and mapped."
- "Some sensors image with hundreds of closely spaced wavebands so that fine details in reflectance spectra can detected.  Those sensors are called hyperspectral, as against multispectral when fewer than about 10 wavebands are used."
- "Water absorption bands are generally avoided with multispectral sensors."
---

## What are we trying to measure?

In this lecture, we want to look at the properties of the earth's surface that can be detected by remote sensing instrumentation. When we examine those properties, we will understand why certain weapons have been chosen in the design of sensors commonly used in civilian remote sensing missions. 

Once you have assimilated this material, you may wish to consult some of the many websites available, that include information on remote sensing programs and their sensors. As we develop further knowledge and light lectures, these websites will become valuable additional sources of information with which to illustrate the lecture presentations. The NASA website in particular is especially valuable. 

First, remember that most remote sensing missions record images of the earth's surface using reflected sunlight, just as you and I see the earth as a result of reflected sunlight. In remote sensing, though, wavelengths outside the range of human vision can also be used for imaging. But let's just concentrate on reflected sunlight. If the earth's surface was an ideal reflector, such as a sheet of white material, then all wavelengths would be reflected equally. 

Real earth surface materials, however, are not ideal reflectors. They selectively absorb sunlight at different wavelengths, giving the appearance of color in the visible range. 

For example, green vegetation appears to us as green, because in the visible range of wavelengths, there is a strong absorption of incident blue and red radiation from the sun, but less absorption of green sunlight. As a result, there is more green energy reflected from most plant matter. So that we see grass, trees, and other green vegetative matter as green, depending on their pigmentation, some plants are differently colored. For example, plants which appear red, strongly absorb incident blue and green radiation. But reflect a significant proportion of the incident red radiation from the sun. 

To develop a better idea of what satellite sensors detect, including in the ranges of wavelengths beyond human vision, we will now examine in a little detail the reflectance properties of earth surface materials as a function of wavelength.

 ![what_is_measured](..\fig\Lec_5\what_is_measured.gif)

The above figure shows how the three simple fundamental earth-covered types of vegetation, soil, and water reflect incident sunlight across just the optical range of wavelengths. Note that the vertical axis is calibrated in percentage terms and is expressed as reflectance. 

Note also that the range of visible wavelengths shown on the left hand end of the abscissa is quite small, compared with the full range of optical wavelengths. 

It is important to note that the amount of green energy reflected by green vegetation is really quite small. Nevertheless, it is larger than the blue and red reflections, meaning that we see most vegetation as green. Even that the energy levels are quite small. 

By contrast, in the near infrared range, vegetation reflects about 30% or more of the incident sunlight. If we were able to see in the near infrared region, vegetation would look much brighter than it does in the optical range.

As we move to longer wavelengths still, we see that the vegetation reflectance curve drops away. It contains two large absorption dips resulting from the water content of the vegetative matter, depending upon the moisture content of the vegetation those dips can be very deep or quite shallow. 

If the vegetation is most distressed, the dips will be shallow to non existent. Most remote sensing instrumentation tends to avoid imaging in those regions. The water absorption dips also occur for soil, although, in this real example, the soil is quite dry, so that the dips are very shallow. Soil with a high moisture content will show dips comparable to those, in this case to the vegetation curve. 

The other interesting property about soil is that the reflectance curve rises steadily with increasing wavelength, in the visible and the infrared ranges. As a result, the visible color of soil is determined mostly by reflected green and red radiation, so that the color tends toward reddish yellow. That is particularly the case for clays and sand. Dark loamy soil will appear blackish, because there is high absorption at all wavelengths. 

The water reflection curve is dark everywhere, showing just small amounts of reflected energy in the blue, green range consistent without experience of watercolor. 

These three curves are typical of what we encounter in remote sensing, but they will vary considerably depending upon the moisture and mineral contents of soil, the moisture and pigmentation contents of vegetation, and the clarity and depth of water. 

If water contains a lot of sediment, for example, the water curve will be a combination of the reflectance of pure water, and that of the suspended soil matter. If the water is shallow, there can be reflectance from the bottom material. So when looking at cover types such as water, the remote sensing specialist needs to be aware that the reflectance observed can be mixtures of more than one pure material. 

In figure above, we show how the wave bands of some common remote sensing satellite instruments are chosen specifically, so that they sample the most significant region, of the spectral reflectance curves of common earth surface covered hops. 

To consider a simple example, the Landsat ETM+ takes three measurements in the visible range, roughly corresponding to blue, green, and red. Another measurement just at the start of the near infrared range, and two broad measurements further out in the infrared, avoiding the water absorption dips. 

Sensors such as hyperion take a very large number of samples across the spectrum, with sufficiently fine spectral resolution that in principle, the full reflectance spectra could be reconstructed for each pixel. Remember, each pixel is sampled in all of the available light bands, so that the spectral information recorded by any of these sensors is done for every pixel in the image. 

Whenever you come across a sensor, have a look at the wave bands it operates with, and form an opinion as to its likely applications. If a sensor operates largely in the visible range, it is probably designed for surveillance, mapping, or urban studies. If it has wide bands in the near infrared, it is then good for mapping and monitoring cover types such as natural vegetation, crops, and forests. It operates further out in the infrared range, it is likely to be designed for geological studies as well. Since a number of important spectral features of minerals occur in the wavelengths up to about 2.5 micrometers. 

We are now in the position to introduce some further definitions. 

If an instrument records up to about ten wave bands, it is generally referred to as a **multispectral** sensor. If it records a very large number of bands say more than 100, it is often referred to as a **hyperspectral** sensor. 

At this stage, it is worthwhile re-examining other portions of the electromagnetic spectrum. And in particular, the region beyond the optical wavelengths. Remember though, we have to be mindful of the presence of atmospheric absorption, and can only reliably image over those wavelengths which correspond to atmospheric windows. As we noted in a previous lecture, there are good atmospheric windows in the vicinity of 10 micrometers. And in the very broad radio wave region of the spectrum. They are identified on the slide and we need to ask ourselves once again, whether those regions are useful for earth surface imaging. 

Let's look at the wavelengths in the vicinity of 10 micrometers first. 

There is a very famous law called Planck's radiation law, which describes how a body, a so-called black body radiates energy as a function of wavelength. The radiation emitted is also, importantly, a function of the temperature of the body. 

Planck's law is described by an equation, that allows us to plot radiation curves as a function of wavelength and temperature.

![planck_radiation_formula](..\fig\Lec_5\planck_radiation_formula.JPG)

In this lecture, we show three examples of Planck's radiation law in practice. 

- The first example is for the sun, whose surface temperature is taken to be 5,950K. 
- The second is for the earth, which has a temperature of approximately 300K. 
- The third is for an object with a temperature of 1,000K, which roughly corresponds to a burning fire. 

As seen, they have maximum radiation outputs at different wavelengths. It is important to note that the vertical scale is logarithmic, so that each editor spacing represents a power of ten or an order of magnitude. Also the sun curve has been scaled down to represent the reduction in radiation. Because of the distance it has traveled from the sun to the earth. 

The solar curve has radiation maximum at a wavelength of about one-half a micrometer. Whereas the earth's maximum emission is at a wavelength of about 10 micrometers. The two curves crossover a little below 5 micrometers, meaning that any observations of the earth's surface at wavelengths less than about four micrometers are dominated by reflected sunlight. Whereas emissions above about six micrometers are dominated by natural emissions from the earth itself. 

If we want to measure the natural energy emanating from the earth, which is a sensor with weapons in the range of 10 to 12 micrometers, near where the earth's radiation is at a maximum. That is the basis of so called thermal remote sensing, since we are effectively detecting variations in the earth's heat output. 

Although we have shown the curve as a simple continuous line, it does vary from place to place on the earth as a result of a property called emissivity. It is variations in emissivity that thermal remote sensing missions measure and map. 

If we extrapolated both the earth and solar curves of the previous slide out to the radio wavelengths, we would see that there is negligible emitted or scattered energy from the earth's surface at those very long wavelengths. 

In fact, there is some, and it can be detected with very low spatial resolution instruments. But in general, we assume that the earth is quiet at radio wavelengths. As a result, we can radiate the surface using an artificial energy source, such as a radio transmitter carried on an aircraft or spacecraft. 

A receiver on the platform detects scattered radiation, which is then used to create a radio or microwave map of the earth's surface. That is the basis of radar remote sensing. There are three important messages here. 

1. Imaging can be done with reflected sunlight, thermal emissions from the earth itself, or via scattered radio waves or radar. 

2. Note the difference between hyperspectral and multispectral imaging. 

3. Remember water absorption bands need to be avoided. 

   When thinking about the first question, ask yourself how a burning fire front could be mapped against significant surface features such as roads, rivers, and forests. 

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
> > 1. Scanning sensors allow each “pixel” to be seen for only a short time during the across-track sweep, compared with a push broom CCD array which allows each “pixel” to be seen for a longer time.  The reason for this is that the scanning mirror has to cover all the pixels in a scan line compared with the CCD, which has one detector per pixel across the scan.  Because of the longer observation (or dwell) time per pixel, more energy per unit area is received by the CCD sensor allowing finer spatial resolutions to be achieved and narrower spectral bands, if needed.  We can look at this mathematically, in an approximate manner, as follows.
> > > >   ![landsat_ETM+](..\fig\landsat_ETM+.png)
> > The spectral power density from the sun created at the earth’s surface can be regarded as a constant at a given time.   It has units of watts per square metre per micrometre of wavelength (Wm-2µm-1).  From this density field the actual energy at the ground captured by a sensor, with a given pixel size and over a particular band can be expressed as
> > Energy in joules = spectral power density (Wm-2µm-1) x pixel size (m2) x width of the spectral band (µm) x dwell time (sec)
> > Thus, if the dwell time is much larger, as in the case of a CCD array, the pixel size and width of the spectral band can be smaller for the same energy capture.
> > 2. Pixel size is defined by the product of IFOV (in radians) and the altitude of the sensor (in metres).  Since aircraft fly at different altitudes in different missions the concept of spatial resolution, or pixel size on the ground, is not helpful because it can be different from mission to mission.  By contrast IFOV is a constant from mission to mission since it is a characteristic of the sensor and not the platform.  Satellites fly at a constant altitude so it is meaningful to talk in terms of spatial resolution, or pixel size.
> > 3. Yes, because the IFOV of the sensor is a constant.  The pixel size on the ground is defined by the product of the IFOV and the distance from the sensor to the spot on the ground.  That distance is smallest directly under the platform (at nadir) and is largest at the swath edges.  Thus, the pixel areas imaged across the swath gets larger from nadir to the swath edge.  For many sensors (e.g. on Landsat) that can be a negligible difference, but for wide FOV sensors, such as that on Aqua and Terra, the effect is quite large. 
> {: .solution}
{: .challenge}

 {% include links.md %}

