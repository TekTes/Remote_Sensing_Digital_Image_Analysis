title: Module 2 Lecture 14: Deep learning and the convolutional neural network, part 1
teaching: 
exercises: 
questions:

- "???"
  objectives:
- "= = ="
  keypoints:
- "- - -"

### Module 2 Lecture 14: Deep learning and the convolutional neural network, part 1

Now start a series of four lectures on the transition of the neural network that we met in the past few lectures into the convolutional neural network that has become a cornerstone of Artificial Intelligence Research over the last few years. It has also been widely applied to remote-sensing problems, as we will see when we look at some examples. At the completion of this work, we will then do a detailed comparison of the major classification techniques we have covered in the course. As we will see by comparison to the classifiers, we have looked at so far the convolutional neural network does not have a standard form or topology instead it is composed of a number of building blocks that can be configured in many ways according to the approach chosen by a particular user. We will develop the tools and show several configurations helpful in remote sensing, especially for taking special neighborhoods or pixels into account when performing semantic mapping. The book by Goodfellow, and the others referenced here has become a bit of a standard treatment for Deep Learning and convolutional neural networks. It's true is at a higher mathematical level then we have adopted in these lectures but nevertheless, for those with the right background it should be consulted to fill in the gaps in the theory. Note, especially it's warning listed here about non standardization in convolutional neural networks. Before we embark upon the development of the convolutional neural network, it is important to reflect on the fact that for many decades, image analysts in remote sensing have been critically aware of the matter of a spatial context. That is, when considering the liable for a central pixel in the diagram on the slide we know for many scenes that there is a high likelihood that the surrounding pixels will be from the same class. That is especially the case for agricultural regions and many natural landscapes, and yet the classifiers we have been dealing with up to now have ignored that property. In that sense, they are simply called point or pixel specific classifiers because they focus just on a pixel independently of its neighbors. Over the use though, there have been many suggestions about how to treat spatial context, some of the more successful approaches are shown here. Echo was perhaps the earliest, developed in the mid 19 seventies, it works by growing homogeneous regions in an image. It then classifies that as objects or regions as a whole, it applies point classification methods for pixels that are not found to be part of an object, such as those on the boundaries between regions. In the late 1970s, the method of relaxation labeling was developed, it takes the results of a point classification at expressed as posterior probabilities of class membership such as in the output of a maximum likelihood classifier. Those posteriors are updated iteratively by reference to the posteriors on the neighbors, linked by a set of joint probabilities. Finally, measures of texture can be used to characterize the neighborhood about a pixel. Local texture is then used as another feature in a point classification method along with the spectral measurements of a pixel. As we will see soon, the convolutional neural network is another technique that embeds spatial context in its decisions. To employ the neural network spatial context sensitive applications, we have to use it in a slightly different way than we have up to now. Let's commence this discretion by recalling the topology we had been dealing with so far, in which the inputs are the individual components of the pixel vector. Suppose now though, we make the seemingly bold move of inputting all the pixels of an image in one go so that we have enough input nodes to accommodate the full set of spectral measurements for a full set of image pixels. For practical image, that will be a very large number of inputs, we still have a number of hidden layers and for the moment, the network is still fully connected, thus there will be a huge number of unknown white vectors and offsets to be learned through training. One immediately obvious problem with feeding the network in this manner is that the spatial interrelationships among the pixels appears to be lost. Even though this is really just a problem of how the pixels are addressed, it is more meaningful to arrange them as shown in the next slide. Suppose we present the image to the network as a square or rectangular array with the pixels in their correct special relationships, this doesn't change anything about the network other than arranging the nodes or processing elements into an array rather than a column format. For convenience, we have shown the hidden layers to be the same size and shapes as a input layer, but in general they could be any size. Note that the output layer is still one-dimensional since it represents a set of classes. With such an arrangement, the number of potential connections is enormous. Let's do a calculation of the number of unknowns between just the input and the first hidden layer. Remember that the input to each processing element in the hidden layer is z equals w transpose x plus Theta. The dimensionality of the weight vector will be equal to the number of elements in the input layer, which is N times N for an N-dimensional image. Also, there are as many weight vectors as there are nodes in the hidden layer. If we assume, for the sake of this calculation, that the hidden layer has the same dimensions as the input layer, that means altogether, we have to have N to the fourth different weights, values for which have to be found during training to make the network usable. In a similar fashion, there will be N squared values of Theta. If we had N equals 100, which would be a very small image in remote sensing, then there are more than 100 million unknowns, that would require an extraordinarily large amount of training data. Added to this, is the fact that we have multiple bands and images usually much larger than 100 by 100. Clearly, a simpler approach needs to be found, but one in which spatial inter-relationships among the pixels are still represented effectively. In this slide, we just simplify the diagram by removing the explicit input layer and just let it be represented by the image itself, perhaps with scaling, if that is found to be beneficial in some applications. In this simplified representation, each image pixel is connected to all the nodes of the first hidden layer. Also, we are still focusing on just a single band of data. We will come to multispectral images later. Here, we show the major deviation of the convolutional neural network from the fully connected neural network we have been considering so far. Instead of implementing all connections, that is as in a fully connected network, we are selective in the connections we make between the layers. In particular, we restrict the connections to a node in the hidden layer to be just those of a neighborhood of non-pixels from the input image as shown. Because of the geometry, the grip of three by three pixels is centered on the one which is in the second row and second column. The processing element in the hidden layer is also that in the two, two position, as seen in the slide. In contrast to the need to determine N to the fourth plus N squared weights and offsets overall, there are now 10 unknowns; that is nine weights and one offset. So 10 unknowns to determine per hidden layer node. Overall, therefore there are, in principle, 10 N squared unknowns defined, a considerable reduction but still a large number if N is large. We do the same thing for the 3 by 3 group, which is one column to the right. Now we take a decision that significantly reduces again, the number of unknowns to be found in training. Rather than using new set of weights and offsets, we assume we can employ the same set as for the previous slide. This is called weight reuse. While that sounds like it will reduce substantially the pair of the network to learn complicated spatial patterns in the image, it gives surprisingly good results in practice. There is also a rationale to this decision, which we will say soon. Continuing though, we then do the same thing for the next pixel group along the row, and then for all rows until the whole image is covered. While this example suggests that the actions happen sequentially, in fact all the operations are in parallel. They are just sets of connections. This is important to recognize. As we have realized, there is a problem with the edge pixels. Given the large numbers of pixels in an image, we could ignore the edge problem. But sometimes, an artificial border of zeros is created so that the edge processing elements in the hidden layer can receive inputs and thus preserve dimensionality if that is important. Even though many of the connections of a fully connected neural network have now been removed, it turns out we can still use backpropagation, surprisingly, to train this new sparser network. So thankfully, we do not need to develop a new training procedure. Let's summarize where we are at this stage. In looking at the neural network, the convolutional neural network, we are partly driven by the desire to take spatial context into account when labeling a pixel. Again, in the convolutional neural network, all the image is fed to the network in one go, but the numbers of node-to-node connections is greatly reduced and thus, so the number of unknown parameters to be found during training. The first question here asks you to think about the importance of spatial context. The last two questions are particularly important when thinking about the use of convolutional neural networks 

> ## Quiz
>
> 1. ?
>
> > ## Solution
> >
> > 1. {: .solution}
> >    {: .challenge}

{% include links.md %}