
# Computational Neuroscience Tutorial 2021: Hands-on session
## NeuroSchool PhD Program

Computational neuroscience is an expanding field that is proving to be essential in neurosciences. The aim of this short intensive course will be to provide a common background in computational neuroscience. The course, after a brief historical overview of the field, will focus on the description of a few selected modelling and theoretical approaches that are currently developed, including details about their limits and advantages, and that can be applied to different scales of analysis (from the single neuron to the whole brain). In addition, we will provide a theoretical and a practical session on artificial neuronal networks of spiking neurons.

* Objectives: 	Understanding how computational modelling can be used to formulate and solve neuroscience problems at different spatial and temporal scales; learning the formal notions of information, encoding and decoding and experimenting their use on specific examples

* Where: Marseille (France)

* What: [Session #3 : Realistic spiking neural networks](https://ametice.univ-amu.fr/course/view.php?id=72868)

1. _Computational Neuroscience Tutorial_

  * Friday, April 23, 2021; 9:00-12:30
  * Objective: Applying the Theory on the eBrains platform
  * https://github.com/albertoarturovergani/CNT-2021 (forked in https://github.com/CONECT-INT/2021-04-23_PhDProgram-course-in-computational-neuroscience)
  * zoom link = https://univ-amu-fr.zoom.us/j/94280459110?pwd=b25zQytlQ1dIK0x2OTU5OXQ3dzFEZz09

2. _Hands-on practice_
  * Friday, April 23, 2021; 14:00-17:00
  * Objective: replicating Mainen & Sejnowski (1995)
  * github : https://github.com/CONECT-INT/2021-04-23_PhDProgram-course-in-computational-neuroscience_hands-on
  * zoom link : https://univ-amu-fr.zoom.us/j/95013129562?pwd=UEY5YThLaTUxQU0vWDFrUHNteTRqQT09  
  * AMETICE :  https://ametice.univ-amu.fr/course/view.php?id=72868#section-4 

# Hands-on session: reproduction of the article by Mainen & Sejnowski, 1995

* The aim of this task is to read a scientific article, to reproduce it with simulations of a neuron and to improve the understanding of the study.

* Modalities: students will organize themselves alone, in pairs or in triads to provide a brief in the form of a [notebook](https://jupyter.org/) completed from [the model that is provided](https://raw.githubusercontent.com/CONECT-INT/2021-04_PhDProgram-neurosciences-computationnelles/master/MainenSejnowski1995.ipynb). Follow the `QUESTION` tags in the notebook to guide you in this writing. Comments should be made in the notebook (don't forget to save your changes).

* Tools needed: [Jupyter](https://jupyter.org/), with [numpy](https://numpy.org/) and [matplotlib](https://matplotlib.org/). These are standard tools and are easily installed on any platform. Other hosted solutions exist:
  * [ebrains / HBP](https://wiki.ebrains.eu/bin/view/Collabs/neuromorphic/SpiNNaker/)
  * https://deepnote.com/
  * on [GoogleColab](https://colab.research.google.com)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CONECT-INT/2021-04-23_PhDProgram-course-in-computational-neurosciences/blob/master/MainenSejnowski1995.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/CONECT-INT/2021-04-23_PhDProgram-course-in-computational-neurosciences/blob/master/MainenSejnowski1995.ipynb)


## context

* The goal of this first task is to create a "raster plot" that shows the reproducibility of a spike train with repetitions of the same stimulus, as in this work in the [rodent retina](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/3) or in the [cat cortex (V1)](https://laurentperrinet.github.io/2019-04-03_a_course_on_vision_and_modelization/#/1/6).

Here, we will attempt to replicate Figure 1 of [Mainen & Sejnowski (1995)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.299.8560&rep=rep1&type=pdf):

![Mainen Sejnowski 1995](http://i.stack.imgur.com/ixnrz.png "figure 1")

## getting to know the tools: numpy and matplotlib

- we are going to create vectors representing the dynamics of a value as a function of time
- for that, we create a vector `time' representing 1 second with a precision of dt=.5 ms
- in a first step, we will create a plot of a spike, a slot & a sinusoid

## problem definition: leaky-integrate and fire neuron

- we will simulate 1 neuron for 2 seconds with a precision of dt=.5 ms
- for that, we use the equation of a leaky-IF
- then we show its response to the stimuli created above

## injection of a noise

- As in figure 1 of Mainen & Sejnowski (1995), we add a noise to the current injection
- this noise can be characterized by its amplitude and its characteristic time: what is the impact on the result?
- what happens when we include an internal noise to the dynamics of the neuron?

# Appendices

* an article to read about time in the brain: https://laurentperrinet.github.io/publication/perrinet-19-temps/ [direct link](https://theconversation.com/temps-et-cerveau-comment-notre-perception-nous-fait-voyager-dans-le-temps-127567)

* [From illusions to visual hallucinations: a door on perception](https://laurentperrinet.github.io/talk/2019-04-18-jnlf/) - ([slides](https://laurentperrinet.github.io/2019-04-18_JNLF/)) - article on visual perception: https://laurentperrinet.github.io/post/2019-06-06-theconversation/ [direct link](https://theconversation.com/illusions-et-hallucinations-visuelles-une-porte-sur-la-perception-117389)

* [Modelling spiking neural networks using Brian, Nest and pyNN](https://laurentperrinet.github.io/talk/2019-04-03-a-course-on-vision-and-modelization/) - ([slides](https://laurentperrinet.github.io/2019-01-14_LACONEU/))

* [Tutorial on predictive coding](https://laurentperrinet.github.io/talk/2018-03-26-cours-neuro-comp-fep/) https://laurentperrinet.github.io/talk/2017-06-30-telluride/ https://laurentperrinet.github.io/sciblog/files/2017-06-30_Telluride.html
