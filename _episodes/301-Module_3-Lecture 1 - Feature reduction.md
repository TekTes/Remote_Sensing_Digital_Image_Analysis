---
title: Module 3 Lecture 1 - Feature reduction
teaching: 
exercises: 
questions:
- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---

### Module 3 Lecture 1: Feature reduction

We now come to two practical aspects of machine learning in remote sensing. The first looks at the features we use in performing a classification, while the second addresses the very important topic of how to assess the accuracy of a thematic map. As part of this work, we will look at methodologies for use in the various machine learning techniques we developed in module two. But we start now with looking at the topic called feature reduction. Feature reduction techniques allow us to limit the number of features to be used in a classification. Most often, those features will be the spectral recordings or bands from the remote sensing instrument. But sometimes, there will be special features, particularly if the image data has high spatial resolution. We will not look at methods for reducing the number of special features, noting that convolutional neural networks do that well. Instead, here, we will develop techniques for reducing the number of spectral features. Why would we want to limit the number of features or bands? The answer is simple, it is because the number of training samples required per class to train a machine learning algorithm is lower for fewer features. With more features, more samples per class are required for accurate training. That is a major consideration for hyperspectral image data sets. Feature reduction is carried out to avoid the so called curse of dimensionality, or the Hughes phenomenon, when we train a classifier. There is a second consideration, with more features, training and classification times increase, in some cases more than linearly, so that classification cost also increases. Reducing features therefore reduces costs, provided the cost of the feature reduction step does not outweigh the savings gained in classification. This raises an intriguing question. If we have to go to all the trouble of reducing the feature subset in order to develop a reliable classifier, why not just record a small number of bands in the first place? To answer that question, we need to examine the rationale behind hyperspectral imaging. Hyperspectral imaging is often referred to as imaging spectroscopy. Indeed, that was its original name. As you probably know from your studies in science, spectroscopy means being able to identify something by reason of its spectral characteristics. Examples with which you might be familiar include mass spectroscopy, visible spectroscopy, and electron spectroscopy. Sometimes a spectrum results from the absorption of radiation, and sometimes it is a result of reflection or emission. Imaging spectroscopy is a development of the familiar field of visible absorption spectroscopy at the pixel level. For each pixel, we record the full reflectance spectrum of the substance using reflected sunlight, usually over the wavelength range of about 0.4 to 2.5 micrometers. We measure the sunlight reflected to the sensor on a remote sensing platform after a component of the sunlight has been absorbed by the surface material. The reason our field is called imaging spectroscopy is because such a complete reflectance spectrum is recorded for every pixel in an image. This slide summarizes the essential nature of imaging spectroscopy. On the left, we see an image which has been recorded in a very large number of wave bands, typically 200 or so. For a particular pixel, those bands represent samples of the reflectance spectrum of the corresponding region on the ground. Or more correctly, the reflectance spectrum of the surface material corresponding to the pixel. From those samples we can reconstruct the reflectance spectrum of the pixel as shown on the right hand side of the slide. Notice that the reconstructed spectrum, particularly if there are sufficient samples, shows various important diagnostic features such as the dip corresponding to chlorophyll absorption in the red region and the water absorption bands in the mid infrared. There are other finer absorption features too, especially for soils and minerals. They do not show up on this vegetation example. One of the great benefits of recording the full reflectance spectrum for a pixel is that we can use Scientific knowledge to identify the pixel rather than depend upon supervised learning and machine classification. Expert spectroscopists can undertake that analysis from their knowledge of the spectral response properties of materials. Well, that is a viable approach, most often in hyperspectral remote sensing. The recorded reflectance spectrum of the pixel is compared with the library or prerecorded spectra, as in the next slide. This slide illustrates the approach to image interpretation based on library searching. The image captured by the sensor consists of pixels for each of which are full reflectance spectrum has been recorded. That spectrum is in compared against the library of spectra previously recorded in the laboratory, allowing a label to be attached to the pixel. Often that can be facilitated by using expert system techniques in which the knowledge of an expert analyst is encoded in sets of rules that are applied to the data. Although spectroscopic analysis is regularly applied in the earth sciences using recorded hyperspectral image data in many applications, we still wish to use machine learning methods for labeling a pixel. This approach is convenient and does not rely on expert knowledge or recorded spectral libraries. But we then have to face the problem that there are too many bands recorded to allow all of them to be used as features in a supervised classification exercise. That is, be cause it is too difficult to obtain enough training data per class to allow our classifier parameters to be estimated reliably. We now therefore need to find methods that will allow us to identify a subset of the recorder bands that are still sufficient for the development of an accurate classifier. Before proceeding, there are some dimming clutcher that we should keep in mind. First features is the name given to the input measurements to our various classification algorithms. Most usually they're just the recorded bands or some transformed version of the bands after, say, the application of the principle components transform. In object detection, there may be special descriptors. In some applications, the feature set may include by spectral and spatial descriptors. We are now embarking on a search for methods to reduce the number of features to use, not unreasonably called feature reduction in general. One approach to feature reduction is to select subsets which still function effectively that is called feature selection. Feature selection is the most common form of feature reduction, but other approaches also exist, as we will see in the following material. Feature reduction has been a focus in the machine learning world ever since the first algorithms were developed. Many techniques have been proposed over the years in remote sensing, especially since hyperspectral image there they became available. In these lectures were going to look at some of the more common feature reduction techniques. For those of you who wish to take this study further, the paper referenced on the slide is a comprehensive overview of the field. Essentially, we are going to look at three different approaches. The first will depend upon an analysis of the correlations among the recorded bands of data. We will see that those correlations allow us to consider groups of bands and will let us ignore correlations from group to group. The second approach we will look at involves transforming the spectral data in such a way that we can ignore the least significant transformed bands. The third approach we will look at involves measures that got us in discarding some of the original bands of data without significantly compromising the quality of classification. These techniques fall into two groups. One assumes that the classes can be described by probability distributions, while the other does not require any such assumption. Let's take stock of what we have said so far before we embark upon the actual procedures for feature reduction. Remember hyperspectral data can have as many as 200 or so bands. The field of imaging spectroscopy depends on reconstructing their reflectance spectrum for a given pixel from the set of hyperspectral measurements. Often the reflectance spectrum is identified by reference to a library. A prototype spectra. It is important for that to be effective that the recorded spectrum is radiometrically calibrated. Most of our focus will be on analysis by machine learning methods. To be effective, they require the number of features to be reduced. In the second question here, pay particular attention to the correlations of each of the four bands, with all three of the other bands. 

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