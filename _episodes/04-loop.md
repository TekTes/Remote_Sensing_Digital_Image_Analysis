---
title: Module 1 Lecture 3
teaching: 30
exercises: 0
questions:
- "What platforms are used for imaging the earth's surface?"
objectives:
- "Understand important characteristics of the orbit of a remote sensing satellite."


keypoints:
- "Earth imaging can be carried  out using drones, aircraft or satellites as imaging platforms to view the earth from above.  Satellites allow the greatest field of view, whereas aircraft and drones tend to give the best spatial resolution."
- "Most general purpose remote sensing satellites are placed in a sun-synchronous orbit."
- "In a sun-synchronous orbit a satellite crosses the equator at the same local time on each orbit."

- "The point in an orbit where the equator is crossed during the day is called a node: ascending if the travel is from south to north, and descending if the travel is from north to south."

- "Most remote sensing satellites have a mid-morning descending node, in order to allow sufficient shadowing to reveal geomorphological features."

- "Remote sensing satellites tend to be at altitudes a little under 1000km, and take about 90 minutes to orbit the earth."
---

In the last episode, we wrote Python code that plots values of interest from our first
inflammation dataset (`inflammation-01.csv`), which revealed some suspicious features in it.

### What platforms are used for imaging the earth's surface?

In Lecture 3, we want to look at the platforms that are routinely used for gathering remote sensing imagery. Over the past 40 years or so, the most common platform has been the earth orbiting satellite. Nevertheless, aircraft platforms are often used, and more recently, imaging from drones has become popular. In this lecture, we will say a little about each platform type concentrating on satellites. Since their orbital characteristics are quite specific to the need for operationally monitoring the globe. There are several differences among spacecraft, aircraft, and drones for imaging. Many of which we will explore in the slides to follow. The most obvious though, is that the further one is from the Earth, the greater the area that can be imaged. Whereas based on our own experience, higher spatial resolution would seem to be possible with platforms closer to the Earth's surface. That immediately sets satellites apart from the other two. By using spacecraft platforms, it is technically feasible to image the whole of the Earth's surface in a practical time-frame. Aircraft and drone missions, by comparison, are not global images, but tend to be focused on mission specific areas of interest. We will now look at each of the three platforms in a little more detail.

![RS00851](..\fig\RS00851.png)



#### TAKING IMAGES OF THE LANDSCAPE

1. Allow the whole globe to be covered in a given  time.

2. Are very stable imaging platforms because they are not moving through an atmosphere.

3. Have to image through the whole column of the atmosphere over the earth's surface. That can lead to radiometric (brightness and contrast) errors in the images recorded.

4. Satellites, in general, are expensive to build and launch.

5. The images recorded can meet the needs of many thousands of users.

6. The sensors and their properties are specified in the satellite design and cannot, in general, be changed  once the satellite is in orbit.

7. There is a move  towards clusters of micro-satellites, which are less expensive to build and launch. At present, they tend to be special purpose imaging platforms, rather than general purpose, global imagers.

As listed above,satellites will allow the whole Earth globe to be imaged within a reasonable time frame. Also importantly, they operate above the Earth atmosphere. While that means imaging must be carried out through the atmospheric column, as we discussed in the previous lecture, they benefit from not having to travel through the atmosphere, meaning the platform is quite stable. The atmosphere can often be turbulent. Meaning the platforms that travel through it can have variations in their altitudes and attitudes. That is a point in causing variations in the geometry of recorded images. Nevertheless, imaging through the atmospheric column will introduce brightness and contrast errors into the recorded image data, which often require correction before the image is usable. Because satellite programs are so expensive to develop,build, and launch, the data tends to be made available to many thousands of users and thus tends to be regarded as a common good product. Not withstanding the fact that some countries restrict access to the images recorded by their national programs. The same of course, is true of commercial satellite operators. The user base is very large, even though the products are sold at commercial rights. 

Two final points should be noted. Because satellites are placed in orbit and thus are not easily revisited. 

- The sensor characteristics are fixed by design when the program was under development. As a consequence, the imaging modality cannot easily be reconfigured. 
- Secondly, there is a move now to clusters of micro satellites for imaging purposes. This approach benefits from the much lower cost of the platforms, and with time will also benefit from collaborative decision-making among the platforms. That is still a little way off. 

When aircraft are used to carry imaging sensors, a number of benefits are immediately apparent, including 

- The ability sometimes to choose the imaging wavelengths which best match the application of interests. 
- The ability to achieve high spatial resolutions,and 
- The control given over the region to be imaged and how frequently imaging should take place. 

On the negative side, atmospheric influences,including turbulence, affect the stability of the platform and therefore tend on the average to introduce more geometric distortion than will be the case with satellites. However, since the atmospheric column is generally small, distortions in brightness and contrast tend not to be as significant as with satellites. Or that satellite missions are expensive to launch and to maintain, they have an economic benefit in that the imagery is available to a large number of users. For aircraft missions,the end-user generally has to pay for the full mission cost. So that aircraft imaging is an expensive option, if satellite-based imagery is a viable alternative. 

![RS01301](..\fig\RS01301.png)

We still have much to learn about the use of a powerful vehicles such as drones for serious remote sensing purposes. Most of the characteristics of aircraft imaging apply to drones as well, apart from cost. In general, the use of quad-copters and the like is a fairly inexpensive imaging modality. Although some concerns have been expressed to have a privacy with aircraft imaging, most of the time that is not a problem because of the altitude at which the platform flies. With drones however, privacy is a major consideration, particularly in urban regions because of the low flying altitudes. We now need to understand a bit more about the orbital characteristics of satellites when used as remote sensing imaging platforms. Of particular importance is how we can arrange a satellite in orbit so that it can be used to image all of the Earth's surface in a practical time frame, and do so repetitively. 

![RS02251](..\fig\RS02251.png)

First without going into the details of orbital mechanics, it is sufficient to notice that most remote sensing satellites orbit quite close to the Earth's surface, typically between 600,and 900 kilometers. That is referred to as a low earth or LEO orbit. In such an orbit,the satellite takes about 90 minutes to do one complete revolution about the Earth. Here is a neat trick which is fundamental to almost all operational remote sensing missions. The orbits are arranged to be near polar. As such, the earth is rotating Eastwards underneath the satellite, and on each adjacent orbit, the satellite is traveling over a different portion of the earth's surface. The orbital inclination is arranged so that it is possible to have a joining strips of image on each orbital paths. 

![RS02701](..\fig\RS02701.png)

Also on each path, say over the equator, the satellite sees that same local or sun time. Such an orbit is called Sun-synchronous. If the orbit crosses over the equator during the daytime, traveling from North to South, that crossing is called a descending node. A descending node of about mid-morning is chosen for most programs, so that there is also a sufficient shadowing to make topographic detail visible. The sensors carry image directly underneath the satellite so that the forward motion of the platform allows a strip or sways of imagery to be recorded. In order to achieve global imaging, the orbits are arranged to repeat on a given cycle called the repeat cycle. Typical examples are 16days for Landsat and Terra, and 26 days for Pleiades and Spot. So Landsat seven for example, records all of the Earth's surface in 16 days, and does so repetitively. 

The figure above shares a sun-synchronous orbit in a little more detail, this time for each satellite in an ascending node configuration. As seen, the first orbit comes up over the Indian Ocean. The next, the second over Central Africa, and the third over the Atlantic Ocean, just off the African Coast. Note that it is not the orbit of the satellite itself that moves, but the rotation of the earth underneath that orbit. 

This summary effectively is a statement of the important characteristics of the orbit of a remote sensing satellite. The third question in this set asks you to think in each case about whether a satellite, aircraft or drone would be the most appropriate imaging platform.

> ## Quiz
>
> Would a satellite with a 12 noon descending  node be good for mapping landscape features? Landsat 7 takes 16 days to image the whole earth surface. How many orbits does it make in that time? Its orbital period is 98.9 minutes. called `range` that generates a sequence of numbers. `range` can
> accept 1, 2, or 3 parameters.
>
> * If one parameter is given, `range` generates a sequence of that length,
>   starting at zero and incrementing by 1.
>   For example, `range(3)` produces the numbers `0, 1, 2`.
> * If two parameters are given, `range` starts at
>   the first and ends just before the second, incrementing by one.
>   For example, `range(2, 5)` produces `2, 3, 4`.
> * If `range` is given 3 parameters,
>   it starts at the first one, ends just before the second one, and increments by the third one.
>   For example, `range(3, 10, 2)` produces `3, 5, 7, 9`.
>
> Using `range`,
> write a loop that uses `range` to print the first 3 natural numbers:
>
> ~~~
> 1
> 2
> 3
> ~~~
> {: .language-python}
>
> > ## Solution
> > ~~~
> > for number in range(1, 4):
> >     print(number)
> > ~~~
> > {: .language-python}
> {: .solution}
{: .challenge}

In the last episode, we wrote Python code that plots values of interest from our first
inflammation dataset (`inflammation-01.csv`), which revealed some suspicious features in it.

### What platforms are used for imaging the earth's surface?

![Analysis of inflammation-01.csv](G:\Российский Университет Дружбы Народов\PYEE01 - Class Materials\!Teaching\1 Lab\Carpentry_templates_Content\python-novice-inflammation\fig\03-loop_2_0.png)

We have a dozen data sets right now, though, and more on the way.
We want to create plots for all of our data sets with a single statement.
To do that, we'll have to teach the computer how to repeat things.

An example task that we might want to repeat is printing each character in a
word on a line of its own.

~~~
word = 'lead'
~~~

{: .language-python}

In Python, a string is basically an ordered collection of characters, and every
character has a unique number associated with it -- its index. This means that
we can access characters in a string using their indices.
For example, we can get the first character of the word `'lead'`, by using
`word[0]`. One way to print each character is to use four `print` statements:

~~~
print(word[0])
print(word[1])
print(word[2])
print(word[3])
~~~

{: .language-python}

~~~
l
e
a
d
~~~

{: .output}

This is a bad approach for three reasons:

1.  **Not scalable**. Imagine you need to print characters of a string that is hundreds
    of letters long.  It might be easier to type them in manually.

2.  **Difficult to maintain**. If we want to decorate each printed character with an
    asterisk or any other character, we would have to change four lines of code. While
    this might not be a problem for short strings, it would definitely be a problem for
    longer ones.

3.  **Fragile**. If we use it with a word that has more characters than what we initially
    envisioned, it will only display part of the word's characters. A shorter string, on
    the other hand, will cause an error because it will be trying to display part of the
    string that doesn't exist.

~~~
word = 'tin'
print(word[0])
print(word[1])
print(word[2])
print(word[3])
~~~

{: .language-python}

~~~
t
i
n
~~~

{: .output}

~~~
---------------------------------------------------------------------------
IndexError                                Traceback (most recent call last)
<ipython-input-3-7974b6cdaf14> in <module>()
      3 print(word[1])
      4 print(word[2])
----> 5 print(word[3])

IndexError: string index out of range
~~~

{: .error}

Here's a better approach:

~~~
word = 'lead'
for char in word:
    print(char)

~~~

{: .language-python}

~~~
l
e
a
d
~~~

{: .output}

This is shorter --- certainly shorter than something that prints every character in a
hundred-letter string --- and more robust as well:

~~~
word = 'oxygen'
for char in word:
    print(char)
~~~

{: .language-python}

~~~
o
x
y
g
e
n
~~~

{: .output}

The improved version uses a [for loop]({{ page.root }}/reference/#for-loop)
to repeat an operation --- in this case, printing --- once for each thing in a sequence.
The general form of a loop is:

~~~
for variable in collection:
    # do things using variable, such as print
~~~

{: .language-python}

Using the oxygen example above, the loop might look like this:

![loop_image](G:\Российский Университет Дружбы Народов\PYEE01 - Class Materials\!Teaching\1 Lab\Carpentry_templates_Content\python-novice-inflammation\fig\loops_image.png)

where each character (`char`) in the variable `word` is looped through and printed one character
after another. The numbers in the diagram denote which loop cycle the character was printed in (1
being the first loop, and 6 being the final loop).

We can call the [loop variable]({{ page.root }}/reference/#loop-variable) anything we like, but
there must be a colon at the end of the line starting the loop, and we must indent anything we
want to run inside the loop. Unlike many other languages, there is no command to signify the end
of the loop body (e.g. `end for`); what is indented after the `for` statement belongs to the loop.


> ## What's in a name?
>
>
> In the example above, the loop variable was given the name `char` as a mnemonic;
> it is short for 'character'.  We can choose any name we want for variables.
> We can even call our loop variable `banana`, as long as we use this name consistently:
>
> ~~~
> word = 'oxygen'
> for banana in word:
>  print(banana)
> ~~~
>
> {: .language-python}
>
> ~~~
> o
> x
> y
> g
> e
> n
> ~~~
>
> {: .output}
>
> It is a good idea to choose variable names that are meaningful, otherwise it would be more
> difficult to understand what the loop is doing.
> {: .callout}

Here's another loop that repeatedly updates a variable:

~~~
length = 0
for vowel in 'aeiou':
    length = length + 1
print('There are', length, 'vowels')
~~~

{: .language-python}

~~~
There are 5 vowels
~~~

{: .output}

It's worth tracing the execution of this little program step by step.
Since there are five characters in `'aeiou'`,
the statement on line 3 will be executed five times.
The first time around,
`length` is zero (the value assigned to it on line 1)
and `vowel` is `'a'`.
The statement adds 1 to the old value of `length`,
producing 1,
and updates `length` to refer to that new value.
The next time around,
`vowel` is `'e'` and `length` is 1,
so `length` is updated to be 2.
After three more updates,
`length` is 5;
since there is nothing left in `'aeiou'` for Python to process,
the loop finishes
and the `print` statement on line 4 tells us our final answer.

Note that a loop variable is a variable that's being used to record progress in a loop.
It still exists after the loop is over,
and we can re-use variables previously defined as loop variables as well:

~~~
letter = 'z'
for letter in 'abc':
    print(letter)
print('after the loop, letter is', letter)
~~~

{: .language-python}

~~~
a
b
c
after the loop, letter is c
~~~

{: .output}

Note also that finding the length of a string is such a common operation
that Python actually has a built-in function to do it called `len`:

~~~
print(len('aeiou'))
~~~

{: .language-python}

~~~
5
~~~

{: .output}

`len` is much faster than any function we could write ourselves,
and much easier to read than a two-line loop;
it will also give us the length of many other things that we haven't met yet,
so we should always use it when we can.

> ## From 1 to N
>
> Python has a built-in function called `range` that generates a sequence of numbers. `range` can
> accept 1, 2, or 3 parameters.
>
> * If one parameter is given, `range` generates a sequence of that length,
>   starting at zero and incrementing by 1.
>   For example, `range(3)` produces the numbers `0, 1, 2`.
> * If two parameters are given, `range` starts at
>   the first and ends just before the second, incrementing by one.
>   For example, `range(2, 5)` produces `2, 3, 4`.
> * If `range` is given 3 parameters,
>   it starts at the first one, ends just before the second one, and increments by the third one.
>   For example, `range(3, 10, 2)` produces `3, 5, 7, 9`.
>
> Using `range`,
> write a loop that uses `range` to print the first 3 natural numbers:
>
> ~~~
> 1
> 2
> 3
> ~~~
>
> {: .language-python}
>
> > ## Solution
> >
> > ~~~
> > for number in range(1, 4):
> >  print(number)
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}




> ## Understanding the loops
>
> Given the following loop:
>
> ~~~
> word = 'oxygen'
> for char in word:
>  print(char)
> ~~~
>
> {: .language-python}
>
> How many times is the body of the loop executed?
>
> * 3 times
> * 4 times
> * 5 times
> * 6 times
>
> > ## Solution
> >
> > The body of the loop is executed 6 times.
> >
> > {: .solution}
> > {: .challenge}



> ## Computing Powers With Loops
>
> Exponentiation is built into Python:
>
> ~~~
> print(5 ** 3)
> ~~~
>
> {: .language-python}
>
> ~~~
> 125
> ~~~
>
> {: .output}
>
> Write a loop that calculates the same result as `5 ** 3` using
> multiplication (and without exponentiation).
>
> > ## Solution
> >
> > ~~~
> > result = 1
> > for number in range(0, 3):
> >  result = result * 5
> > print(result)
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

> ## Reverse a String
>
> Knowing that two strings can be concatenated using the `+` operator,
> write a loop that takes a string
> and produces a new string with the characters in reverse order,
> so `'Newton'` becomes `'notweN'`.
>
> > ## Solution
> >
> > ~~~
> > newstring = ''
> > oldstring = 'Newton'
> > for char in oldstring:
> >  newstring = char + newstring
> > print(newstring)
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

> ## Computing the Value of a Polynomial
>
> The built-in function `enumerate` takes a sequence (e.g. a list) and generates a
> new sequence of the same length. Each element of the new sequence is a pair composed of the index
> (0, 1, 2,...) and the value from the original sequence:
>
> ~~~
> for idx, val in enumerate(a_list):
>  # Do something using idx and val
> ~~~
>
> {: .language-python}
>
> The code above loops through `a_list`, assigning the index to `idx` and the value to `val`.
>
> Suppose you have encoded a polynomial as a list of coefficients in
> the following way: the first element is the constant term, the
> second element is the coefficient of the linear term, the third is the
> coefficient of the quadratic term, etc.
>
> ~~~
> x = 5
> coefs = [2, 4, 3]
> y = coefs[0] * x**0 + coefs[1] * x**1 + coefs[2] * x**2
> print(y)
> ~~~
>
> {: .language-python}
>
> ~~~
> 97
> ~~~
>
> {: .output}
>
> Write a loop using `enumerate(coefs)` which computes the value `y` of any
> polynomial, given `x` and `coefs`.
>
> > ## Solution
> >
> > ~~~
> > y = 0
> > for idx, coef in enumerate(coefs):
> >  y = y + coef * x**idx
> > ~~~
> >
> > {: .language-python}
> > {: .solution}
> > {: .challenge}

{% include links.md %}