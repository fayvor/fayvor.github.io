---
layout: post
title:  "Battery Model - An Ion Diffusion Simulation"
date:   2020-05-23 13:11:27 -0700
tags: batteries, 
---
To make sense of some of the data I was working with at Voltaiq, I created a model of a battery using a simple diffusion mechanism to simulate the flow of ions from cathode to anode during charge, and back again during discharge. I am currently working on adding a relationship between cell potential and ion concentration according to the [Nernst equation](https://en.wikipedia.org/wiki/Nernst_equation).

#### Presentation
A slide deck describing the mechanism and showing a charge/discharge animation using the battery model can be found [here](https://docs.google.com/presentation/d/1LLgCsxfwwLnb27xaBQQDY7WngTbKWJailY0dJrO9XdE/edit#slide=id.p).

#### Code
The code used for the model and visualizations is [here](https://github.com/fayvor/battery-model).