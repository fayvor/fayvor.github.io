---
layout: post
title:  "dQdV Kernel Smoothing"
date:   2020-05-23 13:11:27 -0700
tags: batteries, 
---

Outline:
- Reactions happen at specific voltages
- Cyclic Voltammetry
    - peaks
    - separation of peaks
    - peak width
- dQ/dV curves
- CC charge/discharge curves
- smoothing
- smoothing and differentiation
    - convolution is commutative
- peaks
- smoothing along V vs Q
- 3D plot
- smoothing along cycle
- references

###Reactions [2]
To make a battery, we can use a reversible redox reaction.  A redox reaction is one where a species loses or gains an electron (oxidation is loss, reduction is gain).

Zinc and copper in solution will exchange electrons in the reaction:

Zn + Cu<sup>2+</sup> → Zn<sup>2+</sup> + Cu

## TODO: is this negative?
The Zinc half-reaction has a potential energy E1/2 of 0.76V, so this reaction will happen if the electrons have somewhere to go.

Zn → Zn<sup>2+</sup> + 2e<sup>−</sup>

The Copper half-reaction has a potential of 0.34V, so this reaction will happen if the electrons are present.

Cu<sup>2+</sup> + 2e<sup>−</sup> → Cu
<sup></sup>

Since Zinc will give away 2 electrons at 0.76V and Copper will accept 2 electrons at 0.34V, the transaction happens and energy is released. If we want to know how much energy is released, we can multiply Coulombs * Volts to get Joules. The energy in Joules released by 1 Coulomb of electrons involved in this reaction is (1 * 0.34J) - (1 * -0.76J) = 1.10J

If this happens for one mole each of Zn and Cu in solution, that makes 2 Coulombs of charge transferred (since each reaction involves 2 electrons) and the energy released is:
(0.34V + 0.76V) * 2C = 1.10V * 2C = 2.20J

###Reaction Energy
- Reaction Coordinate Diagram
- Thermodynamics describes energy and equilibrium
- Kinetics describes rates of reactions

As the reaction proceeds, concentrations of the reactants change, and so the potential energy changes according to the Nernst equation.

###Kinetics
- Factors, from [Wikipedia](https://en.wikipedia.org/wiki/Chemical_kinetics)   :
    >The main factors that influence the reaction rate include: the physical state of the reactants, the concentrations of the reactants, the temperature at which the reaction occurs, and whether or not any catalysts are present in the reaction.
- The rate constant k is experimentally determined.
- The equilibrium constant k<sub>c</sub> is the ratio of rate of forward reaction k<sub>f</sub> and rate of backward reaction k<sub>b</sub>
    - Q: does this vary with the ratio of the concentrations of the reactants and products?


###Diffusion
The reaction is not the whole story.  Members of the two species must find each other, or each other's electrons, during their random walk in solution.

[Diffusion Sim][3]

###Diffusion-limited vs Reaction-limited process
A chemical process can be diffusion-limited or reaction-limited.
- [Explaining the Transition from Diffusion Limited to Reaction Limited Surface Assembly of Molecular Species through Spatial Variations](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5763283/#:~:text=In%20the%20diffusion%20limited%20or,and%20an%20%E2%80%9Couter%E2%80%9D%20compartment.)

###Diffusion-controlled Reaction
Simulate a diffusion-controlled reaction for Zn and Cu:
-  Use the Nernst equation and plot [Example 1][5] on the [desmos.com](https://www.desmos.com/calculator/nfzlwifayz) calculator.
- Show dQ/dV idealized from Nernst.
- Add diffusion.
- Show the CV plot using a linear potential sweep.

###Voltammetry
Voltammetry uses a linear potential sweep.

###dQ/dV vs Voltammetry
The dQ/dV curve looks like a Voltammogram, since:
dQ/dV = (dQ/dt)/(dV/dt)
dQ/dt is current, and dV/dt is constant in a linear potential sweep.  So dQ/dV is a constant multiple of current in the voltammogram.  However, the results may not be the same, since current is kept constant in a CC charge/discharge step, whereas it is allowed to vary in voltammetry.



[1]: <https://pubs.acs.org/doi/pdf/10.1021/acs.jchemed.7b00361> "A Practical Beginner’s Guide to Cyclic Voltammetry"
[2]: <https://opentextbc.ca/introductorychemistry/chapter/applications-of-redox-reactions-voltaic-cells-2/> "Applications of Redox Reactions: Voltaic Cells"
[3]: <https://phet.colorado.edu/en/simulation/diffusion> "Diffusion Sim"
[4]: <https://www.youtube.com/watch?v=egqcSscZl_g> "Reaction Rates"
[5]: <https://chem.libretexts.org/Bookshelves/Analytical_Chemistry/Supplemental_Modules_(Analytical_Chemistry)/Electrochemistry/Nernst_Equation> "Nernst Equation Example 1"

## Links

[Standard Cell Potentials](https://courses.lumenlearning.com/cheminter/chapter/electrochemistry/)