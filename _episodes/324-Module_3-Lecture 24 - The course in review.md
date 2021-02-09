---
title: Module 3 Lecture 24 - The course in review
teaching: 
exercises: 
questions:
- "???"
objectives:
- "= = ="
keypoints:
- "- - -"

---

 
### Module 3 Lecture 24: The course in review

We have come to the end of our three modules, in which we have looked at optical and radar modes of image acquisition in remote sensing, and their applications. In this final short lecture, we'll look at the course in overview and consider what might be possible if we use more than one imaging technology in combination. In summary, our course has covered: sources of radiation for remote sensing, the importance of the atmosphere, optical remote sensing imagery, which included means for correcting errors and means for analysis, machine learning methods, including feature selection, and sampling and accuracy assessment, and radar remote sensing imagery, including distortions, understanding radar scattering, bistatic and multistatic radars, and interferometry and tomography. Now, let's look at how we can use the different images types together. Bringing different datasets together to extract information unable to be derived from a single source on its own is called data fusion. In remote sensing, that term is often applied just to the registration step, which ensures that the various image types are co-registered, and then registered to a map. But in many fields, data fusion refers to the fusion of evidence so that joint decisions can be made. We now wish to explore that interpretation briefly in remote sensing. To see why that is important, consider what we could do with registered optical and radar imagery. One example might be to use machine learning methods to create a thematic map of land cover from optical imagery and then overlay that on a digital terrain model derived from radar interferometry so that topographic influence on land cover can then be assessed visually. Another example is to use thermal imagery to map temperature gradients in the water outflows from a power station while using optical data to map the surrounding land use. In many cases, such combinations of different data types can be done manually, but the more general case is interesting. For example, how can we devise machine learning techniques to combine the diagnostic capabilities of both radar and optical imagery to identify land covers or land use? In this slide, we look at some possibilities of what could be done using the two data types together to make joint inferences about cover types. On the left-hand side, we see the sorts of labels one might find with thematic mapping from optical data, along with those which might result from the analysis of radar imagery. On the right-hand side, we see what refinements of the label for a pixel might be possible if we use the two data sources in combination. For example, a pixel which exhibits the characteristics of vegetation in optical imagery, but behaves as a corner reflector in radar imagery, would most likely be a forested pixel. Similarly, a vegetated pixel exhibiting Bragg scattering in radar might indicate row cropping, and so on. How can we perform such combined inferences? One approach is to fuse evidence at the label level, much as humans would do. The method for analyzing each individual data type would be matched to that data. For example, a support vector classifier might be used to analyze a contributing hyperspectral image whereas a knowledge of the incidence angle and polarization dependencies of scattering types in radar might be used to analyze co-registered radar imagery. We could then use several different approaches to combine those recommendations, including sets of rules, such as the one illustrated here. Such rules arise from the knowledge of expert image interpreters. There are other approaches, including probably the use of convolutional neural networks. We still have to see concrete examples of how they can merge evidence from different data types to derive pixel labels. One prospect might be to operate CNN's [inaudible]. The first layer is to analyze the individual data types, and the later layer is to do the fusion. Time will tell. In summary, radar, optical, and thermal imagery, each provide quite different diagnostic tools for understanding ground covers, that is, thematic classes. Optical imagery is determined by vegetation pigmentation, cellular structure and moisture content, by soil mineralogy and moisture content, and biomaterials suspended in water and by the bottom material. Radar scattering response is determined by the geometry of the scattering elements on the earth's surface and by moisture content, via the other property of dielectric constant. Finally, one way of forming joint inferences from the results of radar and optical image analysis is to make logical decisions based on user knowledge of how ground covers behave in both imaging modalities. This question illustrates how expert systems, based on production rules, can be used to merge evidence from different data types. 

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