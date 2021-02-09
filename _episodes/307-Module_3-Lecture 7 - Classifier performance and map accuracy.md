---
title: Module 3 Lecture 7 - Classifier performance and map accuracy
teaching: 
exercises: 
questions:
- "???"
objectives:
- "= = ="
keypoints:
- "- - -"
---

### Module 3 Lecture 7: Classifier performance and map accuracy

We now wish to extend our analysis of the accuracy of a thematic map generated by a machine learning classifier. In the last lecture we looked at the difference between measures of the performance of a classifier class-by-class. And users accuracy which is related to the accuracy of the thematic map produced by the classifier. We now want to take this analysis further. Are focusing on the true accuracy of the thematic map. We will show that users accuracy only represents the accuracy of the map. If the selection of reference or testing pixels by class reflects the actual ground proportions of the classes. In other words, there prior probabilities. To do this, we need to use some simple probability theory. Let the variance t r and m represent the true labels for the pixels in terms of what is actually on the ground. They variables in the reference stay there. That is the data we have chosen to measure map accuracy. And their labels on the thematic map produced by the classifier. Hopefully the first two t and r are the same. But we will treat them separately for a moment. Let the two symbols Y&Z represent any of the available class labels for our three class example. They can be any of A B or C. Suppose we sampled the thematic map that has been produced by the classifier. If we check the accuracy of those samples against their true labels on the ground, then effectively we are estimating the map accuracy conditional probabilities which are expressed. The probability that the true label is said given that the map says it is it. That is what the user of a thematic map is interested in. More generally, the probability that the true label is, Y given at the map label is Z. Is the probability that Y is a correct class if the map shows it. This allows us to assess incorrectly as well as correctly label the pixels. If we use the reference pixels we have selected to assess accuracy and check the corresponding that labels, then we are in fact computing the classifier performance conditional probabilities. That is, the probability that the map sensor pixels Z. Whereas in fact the reference say that says it is Z. Or more generally, the probability that the map says it is said when the reference say that says it is, Y. If the pixels in the reference data set are chosen in the same class proportions as on the ground. We can assume that the variants r and t are the same. That means we have chosen how reference data set carefully so that the proportions of pixels in each of the classes are the same as, say, proportions in reality. We can then use r in place of 2 in our equations so that for example. The accuracy of the map from the previous slide is the probability the reference says Y. If the map says said, which is equivalent to the probability that the true label is, Y if the map so said? This is still a probability that the true label for the pixel on the ground is Y. If the classifier, then it's a thematic map, says it is in. Because we are assuming r&t are the same. We can now use Bayes theorem to relate the accuracy of the map to the performance of the classifier. So in other words, the probability that the reference datasets, Y given the map, says it is equal to the probability that the map says said if the reference letter says Y times probability that the reference say that is Y divided by the probability that the map label is Z. Now in this expression Pr = y. Represents the Lockley Hood that class why pixels exists in the region being image. This is in fact a property of the scene on the ground. In contrast he of =D. Is the probability that class Z pixels appear on the thematic map? And it is given by the. Equation shown at the bottom of the slide where we sum joint probabilities. Well, let's take stock of where we are at this stage of the analysis. The classifier labels pixels as m, whereas that labels in the reference later are r. Thus, a classifier generates the probabilities that the classifier output will be Y if the reference data is Y, shown as the conditional probability p m equals Y given r equals Y. Whereas we as users are interested in the probability that the reference data is a Y pixel if the map or the classifier says it is. That is a conditional probability, p r equals Y given m equals Y. We will now apply those concepts using our three class example from the previous lecture. Here, we'll show the error matrix we are working with on the upper left hand side of the slide. The table on the right shows a classifier performance or produces accuracies. The users accuracies and the map accuracies computed from the expressions from two slides back, involving Bayes theorem. If you wish to check the calculations, you will need to compute the full set of classifier performance probabilities. That is, the probability that the map says Z if the reference data says Y using the entries from the error matrix. Note, the effect of the class prior probabilities that is, the real proportions of the classes on the ground on the results. The map accuracies are only the same as they uses accuracies when the set of label pixels used for reference data is in the same proportion by class as the real situation on the ground. The second and third examples show the differences if that is not the case. The last is an extreme by the instructive example. The average map accuracies given here were computed by the formulas developed on the next slide. We now consider the average accuracy of the thematic map generated by the classifier. Based on what we have done so far, the accuracy by class is expressed as the probability that the true class is Y if the thematic map says it is, that is shown by this conditional probability. In computing an average accuracy of all classes, we could be tempted just to average the above expression over all values of Z. However, that gives too much weight to the smaller classes and diminishes the contribution to the average of the performance on the larger classes. It is better, therefore, to compute the map accuracy as the average but weighted by the probabilities of occurrences in a thematic map. That leads to the map accuracy expression shown here in two forms. The last expression is important. It tells such that the true average map accuracy can be obtained from the classifier performance provided the classifier performance probabilities are weighted by the class prior probabilities. The average map accuracies noted in the final column of the previous slide have been computed that way. Some analysts prefer to express classifier performance in terms of the Kappa coefficient. It is a measure intended to avoid any chance agreement between the performance of the classifier and the reference data. If we again use the results of the example from the last lecture, we can estimate the chance agreement. The two sets of calculations on the right hand side of the slide show the performance of the classifier by class and the allocation of pixels by class in the reference data. The probability that they both place a pixel in the same class is given by the products of their individual performances. The probability that both the classifier and the reference data place a pixel at random in the same class, overall classes is the sum shown her0,e 0.106 plus 0.108 plus 0.117 Which is 0.331. This is the random chance of their agreeing on the label for a pixel. On the other hand, the probability of a correct classification determined from the agreement of the classifier output and the reference data is 35 plus 37 plus 41 divided by 136, which is 0.831. In terms of those calculations, the Kappa coefficient is defined as shown here, and for our example has a value of 0.747. In order to give meaning to that number, we use the ranges shown in the table. Kappa is not strongly supported by all analysts because its value is not a unique function of its arguments as shown here. By way of summary note. There is a difference between the performance of a classifier and the accuracy of the resulting thematic map. Map accuracy can be obtained from classifier performance if the class prior probabilities are used. Classification errors on large classes can give significant errors of commission into smaller classes. The Kappa coefficient is a common alternative measure for expressing classifier performance. And finally Kappa suffers because its range of values does not naturally imply levels of performance. Nevertheless, it is often used as a comparative measure when jointly assessing different classification algorithms. In answering the first question here, you may wish to look at an extreme example. For example, consider a classification exercise with just two classes. Suppose in reality class A occupies 90% of the scene on the ground and class B the other 10%. Suppose your classifier is 100% accurate on class B, but has 50% error for class A pixels. What does that imply for the thematic map?

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