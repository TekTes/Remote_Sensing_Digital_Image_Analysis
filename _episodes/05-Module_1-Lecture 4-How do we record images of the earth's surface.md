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





> ## `True` and `False`
>
> `True` and `False` are special words in Python called `booleans`,
> which represent truth values. A statement such as `1 < 0` returns
> the value `False`, while `-1 < 0` returns the value `True`.
> {: .callout}

## Checking our Data

Now that we've seen how conditionals work,
we can use them to check for the suspicious features we saw in our inflammation data.
We are about to use functions provided by the `numpy` module again.
Therefore, if you're working in a new Python session, make sure to load the
module with:

~~~
import numpy
~~~

{: .language-python}

From the first couple of plots, we saw that maximum daily inflammation exhibits
a strange behavior and raises one unit a day.
Wouldn't it be a good idea to detect such behavior and report it as suspicious?
Let's do that!
However, instead of checking every single day of the study, let's merely check
if maximum inflammation in the beginning (day 0) and in the middle (day 20) of
the study are equal to the corresponding day numbers.

~~~
max_inflammation_0 = numpy.max(data, axis=0)[0]
max_inflammation_20 = numpy.max(data, axis=0)[20]

if max_inflammation_0 == 0 and max_inflammation_20 == 20:
    print('Suspicious looking maxima!')
~~~

{: .language-python}

We also saw a different problem in the third dataset;
the minima per day were all zero (looks like a healthy person snuck into our study).
We can also check for this with an `elif` condition:

~~~
elif numpy.sum(numpy.min(data, axis=0)) == 0:
    print('Minima add up to zero!')
~~~

{: .language-python}

And if neither of these conditions are true, we can use `else` to give the all-clear:

~~~
else:
    print('Seems OK!')
~~~

{: .language-python}

Let's test that out:

~~~
data = numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

max_inflammation_0 = numpy.max(data, axis=0)[0]
max_inflammation_20 = numpy.max(data, axis=0)[20]

if max_inflammation_0 == 0 and max_inflammation_20 == 20:
    print('Suspicious looking maxima!')
elif numpy.sum(numpy.min(data, axis=0)) == 0:
    print('Minima add up to zero!')
else:
    print('Seems OK!')
~~~

{: .language-python}

~~~
Suspicious looking maxima!
~~~

{: .output}

~~~
data = numpy.loadtxt(fname='inflammation-03.csv', delimiter=',')

max_inflammation_0 = numpy.max(data, axis=0)[0]
max_inflammation_20 = numpy.max(data, axis=0)[20]

if max_inflammation_0 == 0 and max_inflammation_20 == 20:
    print('Suspicious looking maxima!')
elif numpy.sum(numpy.min(data, axis=0)) == 0:
    print('Minima add up to zero!')
else:
    print('Seems OK!')
~~~

{: .language-python}

~~~
Minima add up to zero!
~~~

{: .output}

In this way,
we have asked Python to do something different depending on the condition of our data.
Here we printed messages in all cases,
but we could also imagine not using the `else` catch-all
so that messages are only printed when something is wrong,
freeing us from having to manually examine every plot for features we've seen before.

> ## How Many Paths?
>
> Consider this code:
>
> ~~~
> if 4 > 5:
>  print('A')
> elif 4 == 5:
>  print('B')
> elif 4 < 5:
>  print('C')
> ~~~
>
> {: .language-python}
>
> Which of the following would be printed if you were to run this code?
> Why did you pick this answer?
>
> 1.  A
> 2.  B
> 3.  C
> 4.  B and C
>
> > ## Solution
> >
> > C gets printed because the first two conditions, `4 > 5` and `4 == 5`, are not true,
> > but `4 < 5` is true.
> > {: .solution}
> > {: .challenge}

> ## What Is Truth?
>
> `True` and `False` booleans are not the only values in Python that are true and false.
> In fact, *any* value can be used in an `if` or `elif`.
> After reading and running the code below,
> explain what the rule is for which values are considered true and which are considered false.
>
> ~~~
> if '':
>  print('empty string is true')
> if 'word':
>  print('word is true')
> if []:
>  print('empty list is true')
> if [1, 2, 3]:
>  print('non-empty list is true')
> if 0:
>  print('zero is true')
> if 1:
>  print('one is true')
> ~~~
>
> {: .language-python}
> {: .challenge}

> ## That's Not Not What I Meant
>
> Sometimes it is useful to check whether some condition is not true.
> The Boolean operator `not` can do this explicitly.
> After reading and running the code below,
> write some `if` statements that use `not` to test the rule
> that you formulated in the previous challenge.
>
> ~~~
> if not '':
>  print('empty string is not true')
> if not 'word':
>  print('word is not true')
> if not not True:
>  print('not not True is true')
> ~~~
>
> {: .language-python}
> {: .challenge}

> ## Close Enough
>
> Write some conditions that print `True` if the variable `a` is within 10% of the variable `b`
> and `False` otherwise.
> Compare your implementation with your partner's:
> do you get the same answer for all possible pairs of numbers?
>
> > ## Hint
> >
> > There is a [built-in function `abs`][abs-function] that returns the absolute value of
> > a number:
> >
> > ~~~
> > print(abs(-12))
> > ~~~
> >
> > {: .language-python}
> >
> > ~~~
> > 12
> > ~~~
> >
> > {: .output}
> > {: .solution}
>
> > ## Solution 1
> >
> > ~~~
> > a = 5
> > b = 5.1
> > 
> > if abs(a - b) <= 0.1 * abs(b):
> >  print('True')
> > else:
> >  print('False')
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
>
> > ## Solution 2
> >
> > ~~~
> > print(abs(a - b) <= 0.1 * abs(b))
> > ~~~
> >
> > {: .language-python}
> >
> > This works because the Booleans `True` and `False`
> > have string representations which can be printed.
> > {: .solution}
> > {: .challenge}

> ## In-Place Operators
>
> Python (and most other languages in the C family) provides
> [in-place operators]({{ page.root }}/reference/#in-place-operators)
> that work like this:
>
> ~~~
> x = 1  # original value
> x += 1 # add one to x, assigning result back to x
> x *= 3 # multiply x by 3
> print(x)
> ~~~
>
> {: .language-python}
>
> ~~~
> 6
> ~~~
>
> {: .output}
>
> Write some code that sums the positive and negative numbers in a list separately,
> using in-place operators.
> Do you think the result is more or less readable
> than writing the same without in-place operators?
>
> > ## Solution
> >
> > ~~~
> > positive_sum = 0
> > negative_sum = 0
> > test_list = [3, 4, 6, 1, -1, -5, 0, 7, -8]
> > for num in test_list:
> >  if num > 0:
> >      positive_sum += num
> >  elif num == 0:
> >      pass
> >  else:
> >      negative_sum += num
> > print(positive_sum, negative_sum)
> > ~~~
> >
> > {: .language-python}
> >
> > Here `pass` means "don't do anything".
> > In this particular case, it's not actually needed, since if `num == 0` neither
> > sum needs to change, but it illustrates the use of `elif` and `pass`.
> > {: .solution}
> > {: .challenge}

> ## Sorting a List Into Buckets
>
> In our `data` folder, large data sets are stored in files whose names start with
> "inflammation-" and small data sets -- in files whose names start with "small-". We
> also have some other files that we do not care about at this point. We'd like to break all
> these files into three lists called `large_files`, `small_files`, and `other_files`,
> respectively.
>
> Add code to the template below to do this. Note that the string method
> [`startswith`](https://docs.python.org/3/library/stdtypes.html#str.startswith)
> returns `True` if and only if the string it is called on starts with the string
> passed as an argument, that is:
>
> ~~~
> 'String'.startswith('Str')
> ~~~
>
> {: .language-python}
>
> ~~~
> True
> ~~~
>
> {: .output}
> But
>
> ~~~
> 'String'.startswith('str')
> ~~~
>
> {: .language-python}
>
> ~~~
> False
> ~~~
>
> {: .output}
> Use the following Python code as your starting point:
>
> ~~~
> filenames = ['inflammation-01.csv',
>       'myscript.py',
>       'inflammation-02.csv',
>       'small-01.csv',
>       'small-02.csv']
> large_files = []
> small_files = []
> other_files = []
> ~~~
>
> {: .language-python}
>
> Your solution should:
>
> 1.  loop over the names of the files
> 2.  figure out which group each filename belongs in
> 3.  append the filename to that list
>
> In the end the three lists should be:
>
> ~~~
> large_files = ['inflammation-01.csv', 'inflammation-02.csv']
> small_files = ['small-01.csv', 'small-02.csv']
> other_files = ['myscript.py']
> ~~~
>
> {: .language-python}
>
> > ## Solution
> >
> > ~~~
> > for filename in filenames:
> >  if filename.startswith('inflammation-'):
> >      large_files.append(filename)
> >  elif filename.startswith('small-'):
> >      small_files.append(filename)
> >  else:
> >      other_files.append(filename)
> > 
> > print('large_files:', large_files)
> > print('small_files:', small_files)
> > print('other_files:', other_files)
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

> ## Counting Vowels
>
> 1. Write a loop that counts the number of vowels in a character string.
> 2. Test it on a few individual words and full sentences.
> 3. Once you are done, compare your solution to your neighbor's.
>    Did you make the same decisions about how to handle the letter 'y'
>    (which some people think is a vowel, and some do not)?
>
> > ## Solution
> >
> > ~~~
> > vowels = 'aeiouAEIOU'
> > sentence = 'Mary had a little lamb.'
> > count = 0
> > for char in sentence:
> >  if char in vowels:
> >      count += 1
> > 
> > print('The number of vowels in this string is ' + str(count))
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

[]: 

> ## Quiz
>
> 1. CCD array sensors tend to have higher spatial and spectral resolution than those based on scanning mirrors.  Why?
>
> 2. With  aircraft systems, why is IFOV a more  meaningful term than pixel size? Has it to do with the flying height?
>
> 3. Will pixel size vary across the swath for an image recorded by a remote sensing platform?
>
>    {: .callout}
>
> > ## Solution
> >
> > ~~~
> > 
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

 {% include links.md %}