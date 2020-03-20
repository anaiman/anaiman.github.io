---
categories:
- Code
- Science
date: 2015-11-16 19:53:00
layout: post
published: true
status: publish
tags: []
title: Machine Learning
type: post
---

A couple of months ago, some researchers at Google posted a [blog
entry](http://googleresearch.blogspot.ch/2015/06/inceptionism-going-deeper-
into-neural.html) about their work in artificial neural networks.  Normally,
this kind of thing probably wouldn’t make the news cycle, but the researchers
also shared some of the insane and trippy dreamscapes that they created by
visualizing the inner workings of their software:

![]({{ site.baseurl }}/assets/e83c9-building-dreams.png)

_Neural net “dreams”— generated purely from random noise, using a network
trained on places by[MIT Computer Science and AI
Laboratory](http://places.csail.mit.edu/)._

They also posted their source code.  Soon, enthusiasts were creating more
crazy synthesized images and posting them to [social
media](https://www.reddit.com/r/deepdream), and the story made it to the
[mainstream](https://www.washingtonpost.com/blogs/govbeat/wp/2015/07/08/why-
googles-nightmare-ai-is-putting-demon-puppies-everywhere/).

Neural networks belong to an area of computer science generally referred to as
“machine learning” (ML).  Despite the name, which to some conjures up thoughts
of HAL 9000, Skynet, and other malicious artificial intelligences, machine
learning is (at least for now) just a set of extremely useful algorithms
designed to build computational models from data.

### Algorithms that Learn

When I was in grad school, I took a course in ML (the famous
[CS229](http://cs229.stanford.edu/)).  Pretty far outside my research area,
but I thought the applications were really interesting.  It turned out that a
combination of tricky math and the fact that I was also taking quals that
quarter made it the toughest course I took at Stanford (and my grade reflected
that, ahem…), but the subject has continued to interest me.

In my area of research, I built computational models explicitly based on
underlying physics.  That is, the simulations that I was running solved
equations (the Navier-Stokes equations, for example, which describe the
relationships between different forces in fluids, and how they change the
fluid velocity and pressure fields over time) derived from physics (in the
case of the Navier-Stokes equations, the application of Newton’s second law to
a viscous fluid).  The actual solutions involved assumptions and
simplifications, but the underlying model was physical.

Machine learning, in contrast, typically does not use an underlying model with
a direct relationship to the problem being solved.  This is what puts the
“learning” in ML – you set up your learning algorithm, feed in a data set, and
out comes a model that “knows” things that you didn’t explicitly program.
It’s almost like magic.

### What’s in a Picture?

Neural networks have recently become the state-of-the-art in machine learning
because they exemplify this nearly magical ability to solve really tough
problems.  One of the best examples, and the one that led to the crazy art
above, is image classification.  The [image classification
problem](http://googleresearch.blogspot.com/2014/09/building-deeper-
understanding-of-images.html) is simply posed: what is this image a picture
of?

Of course, depending on the image, this can be a nuanced question (is there
more than one thing in the image?  how specific do you want to be?), but for a
person it’s usually trivial to answer.  For a computer, it’s really hard.
Attempts to directly program recognition of specific things might succeed, but
imagine trying to write a program to recognize “everything”.  It would take a
while.

Here’s what the Google researchers (note: lots of other groups have been
working on this, too) did, in a nutshell.  They gathered a large database of
images and tagged each one with labels describing what’s in the image.  They
fed these images and their labels into an artificial neural network learning
algorithm, which processed the images to create a model.  Now they have a
smart model that, given an image, can tell you what’s in it.

Want to try this out?  The new [Google Photos](http://recode.net/2015/06/02
/the-new-google-photos-free-at-last-and-very-smart/) uses this kind of image
classification model to label all of your photos.  This allows you to search
for things in your photos by typing in search terms… without you having to
manually label keywords.  And it works really well.

### Coding it Up

One of my colleagues recently pointed me toward a
[tutorial](http://ufldl.stanford.edu/tutorial/) for getting started with some
of the newer developments in ML, which involve setting up more complicated
neural networks, also known as “deep learning”.  This comes from the research
group headed by the professor that I took CS229 from, Andrew Ng.  I’ve been
slowly making my way through the material.

Unfortunately, the [example code](https://github.com/amaas/stanford_dl_ex) is
all written for MATLAB (I think – I guess I never actually tried running these
in Octave, not sure if that would work), an expensive proprietary piece of
software.  On the plus side, I have plenty of time on my hands at the moment,
and I’ve been looking for a project to practice writing Python.  So if for
some reason you’re interested in working through these examples yourself in a
free as in beer sort of way, you can find my progress on
[Github](https://github.com/anaiman/Stanford_DL_Python).