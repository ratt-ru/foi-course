---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.7
kernelspec:
  display_name: Python 2
  language: python
  name: python2
---

+++ {"deletable": true, "editable": true}

***

* [Outline](../0_Introduction/0_introduction.ipynb)
* [Glossary](../0_Introduction/1_glossary.ipynb)
* [1. Radio Science using Interferometric Arrays](1_0_introduction.ipynb)  
    * Previous: [1.6 Synchrotron emission](1_6_synchrotron_emission.ipynb)
    * Next: [1.8 Astronomical radio sources](1_8_astronomical_radio_sources.ipynb)
   
***

+++ {"deletable": true, "editable": true}

Section status: <span style="background-color:orange">&nbsp;&nbsp;&nbsp;&nbsp;</span>

Import standard modules:

```{code-cell} ipython2
:deletable: true
:editable: true

import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from IPython.display import HTML 
HTML('../style/course.css') #apply general CSS
```

+++ {"deletable": true, "editable": true}

Import section specific modules:

```{code-cell} ipython2
:deletable: true
:editable: true

pass
```

+++ {"deletable": true, "editable": true}

## 1.7.1 Line emission<a id='science:sec:line_emission'></a>

+++ {"deletable": true, "editable": true}

In [$\S$ 1.3 &#10142;](../1_Radio_Science/1_3_radiative_transport.ipynb) <!--\ref{science:sec:radiative_transport}--> we discussed how radiation propagates through space for given macroscopic quantities, the linear emission coefficient $\varepsilon_\nu$ and the linear absorption coefficient $\kappa_\nu$. It is possible to connect both these quantities to the so-called Einstein coefficients, which measure the the probability of the emission or absorption of photons by an atom or a molecule. 

+++ {"deletable": true, "editable": true}

The Einstein coefficients are:
* $A_{21}$: Einstein coefficient for *spontaneous* emission for a transition from atomic level 2 (higher energy) to level 1 (lower energy)
* $B_{21}$: Einstein coefficient for *induced* emission for a transition from atomic level 2 (higher energy) to level 1 (lower energy)
* $B_{12}$: Einstein coefficient for *photo-absorption* for a transition from atomic level 1 (lower energy) to level 2 (higher energy).

+++ {"deletable": true, "editable": true}

They are connected via the following relation

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_001'></a><!--\label{science:eq:07_001}-->$$
\begin{align}
    g_1 B_{12} \,&=\, g_2 B_{21}\\
    A_{21}\,&=\,\frac{8\pi h\nu_0^3}{c^3}\,B_{21}
    \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

where $g_1$ and $g_2$ are the statistical weights of the energy state (in the presence of degenerate energy states these are larger than 1), $\nu_0$ is the central frequency of the transition ($\bar{E}_{12}\,=\,h\nu_0$), and $c$ is the speed of light ($c\,=\,299\,792\,458\,{\rm m}\,{\rm s}^{-1}$). To account for the fact that spectral lines are not perfectly sharp (i.e. they can have a narrow spectrum), we define a profile function $\varphi(\nu)$ representing the probability of emission/absorption at frequency $\nu$.  The condition $\int \varphi\,d\nu\,=\,1$ ensures that we have a normalized probability, such that the mean frequency can be calculated as $\int\ \varphi(\nu)\, \nu \,d\nu\,=\,\nu_0$. With this definition it is possible to describe the absorption and emission coefficients as functions of microscopic parameters. Denoting the volume density of atoms in state 1 as $N_1$ and the volume density of atoms in state 2 as $N_2$, we have the following relation with the emission and absorption coefficients

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_002'></a><!--\label{science:eq:07_002}-->$$
\begin{align}
    \kappa_\nu \,&=\, \frac{h\nu_0}{c}N_1\,B_{12}\left(1-\frac{g_1\,N_2}{g_2\,N_1}\right)\varphi(\nu)\\
       \varepsilon_\nu \,&=\, \frac{h\nu_0}{4\pi}N_2\,A_{21}\varphi(\nu)
   \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

Under the condition of Local Thermal Equilibrium with "spin" temperature $T$, the ratio of $N_2$ and $N_1$ is known to be

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_003'></a><!--\label{science:eq:07_003}-->$$
\begin{align}
    \frac{N_2}{N_1}\,&=\,\frac{g_2}{g_1}e^{-\frac{h\nu}{kT}} \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

which can be used to determine $\varepsilon_\nu$ and $\kappa_\nu$ from the population density of atoms in state 1 or 2. Consequent evaluation of above formulae and identification of extragalactic lines with certain atomic or molecular transitions can be used to learn about the state of the interstellar gas in general.

+++ {"deletable": true, "editable": true}

These relations have been taken from [<cite data-cite=''>Tools of Radio Astronomy </cite> &#10548;](http://adsabs.harvard.edu/abs/2012tra..book.....W) which can be consulted for further details.  

+++ {"deletable": true, "editable": true}

## 1.7.2 Atomic hydrogen<a id='science:sec:atomic_hydrogen'></a>

+++ {"deletable": true, "editable": true}

Atomic hydrogen is formed during the transition from hot ionized hydrogen plasma to the molecular hydrogen gas in galaxies. As hydrogen is the most abundant element in the universe, atomic hydrogen (denoted $\rm H\,{\scriptsize\rm{I}}$) is one of the most abundant emission lines in the universe. Since hydrogen gas fuels star formation, this type of line emission is frequently observed in galaxies undergoing active star formation eg. spiral galaxies. However, it is important to know under which circumstances line emission from neutral hydrogen can occur in other astrophysical sources such as Active Galactic Nuclei and the Cosmic Microwave Background.

+++ {"deletable": true, "editable": true}

Neutral hydrogen emits in the radio regime through a hyperfine transition of the total angular momentum of the ground state of the atom $F = 1$ (electronic quantum number $n\,=\,1$, orbital angular momentum of electrons $L\,=\,0$, electron spin $S\,=\,\frac{1}{2}$, total electron angular momentum $J = L+S = \frac{1}{2}$, nuclear spin $I\,=\,\frac{1}{2}$, the total spin quantum number, $F$, can hence be 0 or 1). The transition frequency is $1.420\,405\,751\,786\times 10^9\ {\rm Hz}$ (what is the corresponding wavelength associated with this frequency?) and the Einstein coefficient for spontaneous emission is $A_{10}\,=\,2.86888\times 10^{-15}\,{\rm s}^{-1}$. The spontaneous mean half-life time of the state in which both the proton and electron have the same spin direction is $1.11\times10^{7} \rm yr$. This means that the excitation state of atoms in neutral hydrogen clouds is almost always determined by collisional excitation. The low transition probability results in many cases in an optically thin structure of neutral hydrogen clouds.

<span style="background-color:red"> LB:IC: Missing from this discussion is the fact the emission occurs when the electrons', which have spins aligned in the excited state, spin anti-align. I don't see the point of introducing all the different spins if we are not going to do it properly. Also, what is with all the significant figures?</span>

+++ {"deletable": true, "editable": true}

Defining the radio velocity $V_{\rm radio}$, which is an approximation to the recession velocity of the gas particles as measured by the Doppler Shift

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_004'></a><!--\label{science:eq:07_004}-->$$
\begin{align}
    \frac{V_{\rm radio}(\nu)}{c}\,&=\,\frac{\nu_0-\nu}{\nu_0} \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

One can, under the assumption of local thermodynamic equilibrium (LTE) and a constant "spin" temperature $T_{\rm spin}$ derive the column density from the optical depth

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_005'></a><!--\label{science:eq:07_005}-->$$
\begin{align}
    \frac{N_{\rm H\,\scriptsize I}}{{\rm atoms} \,{\rm cm}^{-2}}\,=\,1.823\times10^{18}\cdot\frac{T_{\rm spin}}{\rm K}\int \tau_\nu(V_{\rm radio})\,\frac{dV_{\rm radio}}{\rm km\,s^{-1}} \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

which reduces in the optically thin case to

+++ {"deletable": true, "editable": true}

<a id='science:eq:07_006'></a><!--\label{science:eq:07_006}-->$$
\begin{align}
    \frac{N_{\rm H\,\scriptsize I}}{{\rm atoms} \,{\rm cm}^{-2}}\,=\,1.823\times10^{18}\int \frac{T_{\rm b}}{\rm K}\,\frac{dV_{\rm radio}}{\rm km\,s^{-1}} \\
\end{align}
$$

+++ {"deletable": true, "editable": true}

with $T_{\rm b}$ being the brightness temperature (see [$\S$ 1.5.1 &#10142;](1_5_black_body_radiation.ipynb#science:sec:blackbody_emission) <!--\ref{science:sec:blackbody_emission}--> ). This makes it rather simple to derive column densities or masses of neutral-hydrogen clouds. The full derivation will be developed later on. <span style="background-color:yellow"> LB:IC: where is this done? Add a link.</span>

High angular resolution has become an important ingredient for the study of galaxy evolution, especially for extra-galactic sources (i.e. sources outside our own galaxy). Interferometric imaging has proved an indispensable tool in obtaining high resolution radio maps.

+++ {"deletable": true, "editable": true}

The sharpness of spectral lines is a very useful feature of this kind of emission. Indeed it allows astronomers, by making use of the Doppler effect, to determine recession velocities of astronomical sources (including neutral Hydrogen gas) to very high precision. This leads naturally to the concept of redshift $z$ which is defined as

$$ z = \frac{\nu_e - \nu_o}{\nu_o} = \frac{\lambda_o - \lambda_e}{\lambda_e}$$

where the subscripts ${}_e$ and ${}_o$ denote emitted and observed respectively. The sharp feature of spectral lines has been extremely important for mapping not only the location, but also the kinematics of the $\rm H\,{\scriptsize\rm{I}}$ gas found inside galaxies. Indeed, in the 1980's, such maps further supported the idea that there must be dark matter in spiral galaxies.

<span style="background-color:yellow"> LB:IC: should we maybe mention the double horn profile of the H1 line here? </span>

+++ {"deletable": true, "editable": true}

## 1.7.3 Other line emission<a id='science:sec:other_line_emission'></a>

+++ {"deletable": true, "editable": true}

Several other emission lines are also observed in the radio band. Some examples are:

* Radio recombination lines, which are high-level transition lines of electrons captured by an atom.
* Molecular lines, which are transitions of rotational or vibrational excitation states, and can be used to trace the cold interstellar medium.

However, since we are more focussed on observational techniques, we will not attempt to explain the emission mechanisms associated with these phenomena. The reader is referred to [<cite data-cite='1999ASPC..180.....T'>Synthesis Imaging in Radio Astronomy II</cite> &#10548;](http://adsabs.harvard.edu/abs/1999ASPC..180.....T) for further details regarding spectral line emission and its applications. 

+++ {"deletable": true, "editable": true}

***

* Next:[1.8 Astronomical radio sources](1_8_astronomical_radio_sources.ipynb)

+++ {"deletable": true, "editable": true}

Future Additions:

* example: spectrum figure pointing out prominent emission and absorption features
* expand on what causes broadening: natural, doppler, pressure
* example: plot figure of the galactic HI velocity curve
