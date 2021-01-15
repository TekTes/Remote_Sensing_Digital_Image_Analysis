---
title: Module 1 Lecture 3
teaching: 30
exercises: 0
questions:
- "What platforms are used for imaging the earth's surface?"
objectives:
- "Understand important characteristics of the orbit of a remote sensing satellite."


keypoints:
- "Earth imaging can be carried  out using drones, aircraft or satellites asimaging platforms to view the earth from above.  Satellites allow the greatest field of view, whereas aircraft and drones tend to give the best spatial resolution."
- "Most general purpose remote sensing satellites are placed in asun-synchronous orbit."
- "In a sun-synchronous orbit a satellite crosses the equator at the same local time on each orbit."

- "The point in an orbit where the equator is crossed during the day is called a node: ascending if the travel is from south to north, and descending if the travel is from north to south."

- "Most remote sensing satellites have a mid-morning descending node, in order to allow sufficient shadowing to reveal geomorphological features."

- "Remote sensing satellites tend to be at altitudes a little under 1000km, and take about 90 minutes to orbit the earth."
---

## What platforms are used for imaging the earth's surface?

In Lecture 3, we want to look at the platforms that are routinely used for gathering remote sensing imagery. Over the past 40 years or so, the most common platform has been the earth orbiting satellite. Nevertheless, aircraft platforms are often used, and more recently, imaging from drones has become popular. In this lecture, we will say a little about each platform type concentrating on satellites. Since their orbital characteristics are quite specific to the need for operationally monitoring the globe. There are several differences among spacecraft, aircraft, and drones for imaging. Many of which we will explore in the slides to follow. The most obvious though, is that the further one is from the Earth, the greater the area that can be imaged. Whereas based on our own experience, higher spatial resolution would seem to be possible with platforms closer to the Earth's surface. That immediately sets satellites apart from the other two. By using spacecraft platforms, it is technically feasible to image the whole of the Earth's surface in a practical time-frame. Aircraft and drone missions, by comparison, are not global images, but tend to be focused on mission specific areas of interest. We will now look at each of the three platforms in a little more detail. 

![sat_aero_drone](..\fig\sat_aero_drone.png)

#### TAKING IMAGES OF THE LANDSCAPE

![sat](..\fig\sat.png)

As listed above,satellites will allow the whole Earth globe to be imaged within a reasonable time frame. Also importantly, they operate above the Earth atmosphere. While that means imaging must be carried out through the atmospheric column, as we discussed in the previous lecture, they benefit from not having to travel through the atmosphere, meaning the platform is quite stable. The atmosphere can often be turbulent. Meaning the platforms that travel through it can have variations in their altitudes and attitudes. That is a point in causing variations in the geometry of recorded images. Nevertheless, imaging through the atmospheric column will introduce brightness and contrast errors into the recorded image data, which often require correction before the image is usable. Because satellite programs are so expensive to develop,build, and launch, the data tends to be made available to many thousands of users and thus tends to be regarded as a common good product. Not withstanding the fact that some countries restrict access to the images recorded by their national programs. The same of course, is true of commercial satellite operators. The user base is very large, even though the products are sold at commercial rights. 

![aero](..\fig\aero.png)

Two final points should be noted. Because satellites are placed in orbit and thus are not easily revisited. 

- The sensor characteristics are fixed by design when the program was under development. As a consequence, the imaging modality cannot easily be reconfigured. 
- Secondly, there is a move now to clusters of micro satellites for imaging purposes. This approach benefits from the much lower cost of the platforms, and with time will also benefit from collaborative decision-making among the platforms. That is still a little way off. 

When aircraft are used to carry imaging sensors, a number of benefits are immediately apparent, including 

- The ability sometimes to choose the imaging wavelengths which best match the application of interests. 
- The ability to achieve high spatial resolutions,and 
- The control given over the region to be imaged and how frequently imaging should take place. 

![aero_drone](..\fig\aero_drone.png)

On the negative side, atmospheric influences,including turbulence, affect the stability of the platform and therefore tend on the average to introduce more geometric distortion than will be the case with satellites. However, since the atmospheric column is generally small, distortions in brightness and contrast tend not to be as significant as with satellites. Or that satellite missions are expensive to launch and to maintain, they have an economic benefit in that the imagery is available to a large number of users. For aircraft missions,the end-user generally has to pay for the full mission cost. So that aircraft imaging is an expensive option, if satellite-based imagery is a viable alternative. 

![sat2](..\fig\sat2.png)

We still have much to learn about the use of a powerful vehicles such as drones for serious remote sensing purposes. Most of the characteristics of aircraft imaging apply to drones as well, apart from cost. In general, the use of quad-copters and the like is a fairly inexpensive imaging modality. Although some concerns have been expressed to have a privacy with aircraft imaging, most of the time that is not a problem because of the altitude at which the platform flies. With drones however, privacy is a major consideration, particularly in urban regions because of the low flying altitudes. We now need to understand a bit more about the orbital characteristics of satellites when used as remote sensing imaging platforms. Of particular importance is how we can arrange a satellite in orbit so that it can be used to image all of the Earth's surface in a practical time frame, and do so repetitively. 

![orbit](..\fig\orbit.png)

First without going into the details of orbital mechanics, it is sufficient to notice that most remote sensing satellites orbit quite close to the Earth's surface, typically between 600,and 900 kilometers. That is referred to as a low earth or LEO orbit. In such an orbit,the satellite takes about 90 minutes to do one complete revolution about the Earth. Here is a neat trick which is fundamental to almost all operational remote sensing missions. The orbits are arranged to be near polar. As such, the earth is rotating Eastwards underneath the satellite, and on each adjacent orbit, the satellite is traveling over a different portion of the earth's surface. The orbital inclination is arranged so that it is possible to have a joining strips of image on each orbital paths. 

![orbit_repeat_cycles](..\fig\orbit_repeat_cycles.png)



Also on each path, say over the equator, the satellite sees that same local or sun time. Such an orbit is called Sun-synchronous. If the orbit crosses over the equator during the daytime, traveling from North to South, that crossing is called a descending node. A descending node of about mid-morning is chosen for most programs, so that there is also a sufficient shadowing to make topographic detail visible. The sensors carry image directly underneath the satellite so that the forward motion of the platform allows a strip or sways of imagery to be recorded. In order to achieve global imaging, the orbits are arranged to repeat on a given cycle called the repeat cycle. Typical examples are 16days for Landsat and Terra, and 26 days for Pleiades and Spot. So Landsat seven for example, records all of the Earth's surface in 16 days, and does so repetitively. 

![sun-sync_orbit](..\fig\sun-sync_orbit.gif)

The figure above shares a sun-synchronous orbit in a little more detail, this time for each satellite in an ascending node configuration. As seen, the first orbit comes up over the Indian Ocean. The next, the second over Central Africa, and the third over the Atlantic Ocean, just off the African Coast. Note that it is not the orbit of the satellite itself that moves, but the rotation of the earth underneath that orbit. 



The summary at the bottom of this page is effectively a statement of the important characteristics of the orbit of a remote sensing satellite. The third question in this set asks you to think in each case about whether a satellite, aircraft or drone would be the most appropriate imaging platform.

> ## Quiz
>
> Would a satellite with a 12 noon descending  node be good for mapping landscape features?
> Would a satellite with a 12 noon descending  node be good for mapping landscape features?
> Landsat 7 takes 16 days to image the whole earth surface.  How many orbits does it make in that time?  
> Its orbital period is 98.9 minutes.
> - What platform would you choose in each of the following applications?
>   - Mapping forests on a continental scale.
>   - Daily monitoring fence conditions on a farm.
>   - Monitoring an actively burning forest fire that covers about 50ha.
>   - Seasonal monitoring of crop growth and condition in large scale agriculture.
>
> > ## Solution
> > ???
> > ???
> {: .solution}
{: .challenge}

{% include links.md %}