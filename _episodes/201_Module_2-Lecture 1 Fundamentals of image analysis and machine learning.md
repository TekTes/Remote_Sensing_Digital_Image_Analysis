title: Module 2 Lecture 1: Fundamentals of image analysis and machine learning
teaching: 
exercises: 
questions:

- "???"
  objectives:
- "= = ="
  keypoints:
- "- - -"

### Module 2 Lecture 1: Fundamentals of image analysis and machine learning

In the first module, we looked at how remote sensing imagery is acquired. We also looked at how the imagery is affected by atmospheric conditions and various geometric distortions. We are now at the stage where we can concentrate on how to analyze the image data in order to extract information of importance to operational remote sensing. This module focuses on the range of machine learning methods that are used commonly for image interpretation in remote sensing. We will start with some simple historical algorithms and move on to procedures that have gained popularity in the last two decades. The material we are going to develop in this module requires an understanding of basic statistics, calculus, and vector and matrix analysis. If you do not have that background, the summaries should provide an overview. Also, we will step through the analysis slowly and in detail so that you should at least pick up the essence of what is being developed. When we finish this module, you should be in the position to appreciate how a range of popular machine learning methods can be applied in remote sensing. It is important to understand that from an operational point of view, you will not have to engage yourself in the range of mathematics we are to encounter when applying the various algorithms in practice. Instead, commonly available software packages used for remote sensing purposes will contain the algorithms in the form that the user can employ easily. By way of summary, recall that what we are doing is taking the multispectral, or hyperspectral measurements recorded by satellite or aircraft instrument and via an appropriate machine learning technique, reducing a map of labels for each of the image pixels. Those labels represent classes of groundcover. In other words, we're doing a mapping and mapping from recorded data to a thematic map of labels. There are several different classification scenarios that we will come across, all are shown here. In the first, we analyze pixels individually based on their spectral measurements and produce labels for them. Those labels should represent the groundcovers in which we are interested. Sometimes these are called point classifiers because they focus on individual points of pixels. In the second, while we're still interested in labeling individual pixels, some algorithms allow us to do so by taking into account the possible labels on the surrounding pixels. That is called context classification, or more properly, spatial context classification. It is based on the idea that neighboring pixels are likely to be of the same groundcover type, that is the same class. In the third case, we show the need to identify pixels using a range of sensor and data types, here, optical, radar and thermal. Algorithms for this so-called multi-source problem are difficult to come by. Although some authors ignore the intrinsic differences in the data types and simply concatenate them into a single vector to which they then apply classification techniques. Finally, particularly with high spatial resolution imagery, we might be interested in identifying objects. Those objects might be buildings in urban landscapes or aircraft and other vehicles in surveillance applications. Most of our work in this module will focus on the first scenario, but we will later on engage with the concept of spatial contexts. Remember from our earlier work, classification or machine learning in remote sensing consists of a number of stages. The first is training. Here, sets of known pixels are used to train the classification algorithms that we're going to use. The second stage goes by a number of names. Most commonly, it is referred to as the classification step in remote sensing. In the machine learning community, it is called generalization. It can also be called labeling or allocation. The third stage is a central one. When developing a classification, we need to know how well the trained classifier works on real unseen data. It is generally called the testing phase and involves sets of labeled pixels that the analyst has put aside in order to check the performance of the classifier. We'll have more to say about this later, especially in Module 3, where we will treat the need to test the accuracy of a thematic map in some detail. We are now going to embark upon the development of four common classifiers. The first is the maximum likelihood classifier, which was the main algorithm used in remote sensing for many decades. It is still highly usable, particularly when the number of wavebands is small, but it does have limitations in respect of hyperspectral data, and these methods are employed to reduce data dimensionality beforehand. We will look at some of those methods in Module 3. The second method we will consider is the minimum distance classifier. Again, a long-standing technique which is often useful in its own right, but more importantly, it provides a good basis upon which to develop the next two methods. The third procedure we will analyze is the support vector machine. It is a popular classification method for use with hyperspectral data. Finally, we will look at the neural network. While that predates the support vector classifier, it has a later version called the convolutional neural network that has gained particular popularity in the last five to 10 years. It often goes by the title of deep learning, which we will explain during the treatment. It is important here that we differentiate between supervised and unsupervised learning. Supervised classification is that in which labeled training data is used to establish values for the unknowns in the classification algorithm. When training data is not available, unsupervised techniques can be used to discover the class structure of an image dataset. We will look at unsupervised methods in the last week of this module. They are based on the data analysis process called clustering. Before we commence developing the classifiers, it is important to distinguish between what we, as users, think of as classes in the landscape and what machine learning algorithms see as classes in the data. The two may not be the same, although we do hope there is a close mapping between them. For example, we would expect that pixels recorded by an instrument will tend to group in regions in spectral space if they belong to areas on the ground that exhibit the same spectral response. In remote sensing, such spectral groupings are called spectral classes, or sometimes data classes, since they are the natural groups or classes in the data. The set of classes in which the user is interested are called information classes. They have names like natural vegetation, water, forest, crops, and so on. One would hope that they would align one for one with the spectral classes, but that is often not the case. Part of the skill of the analyst is to discover whether such a mapping exists or whether several spectral classes may be needed to represent properly each information class. As a simple example, a single crop class may have several constituent spectral classes, because the crop will exhibit slightly different spectral responses depending on the soil types on which it is sown, the availability of groundwater, and whether any particular portion of a crop is in shadow. We will have more to say about the relationship between spectral and information classes when we come to Module 3 of this course. But unless we say otherwise, we will assume in this module that our information and spectral classes are the same. Here we've summarized the important points raised in this introductory lecture. We talked about the different types of classification, the steps involved in classification, the difference between supervised and unsupervised classification, and the difference between spectral and information classes. Use these quiz questions to rehearse what you understand classification will do for you. Also, pay particular attention to the last question because it reveals some interesting properties of the data space or spectral space used in remote sensing. 

> ## Quiz
>
> 1. ?
>
> > ## Solution
> >
> > 1. 
> >    {: .solution}
> >    {: .challenge}

{% include links.md %}