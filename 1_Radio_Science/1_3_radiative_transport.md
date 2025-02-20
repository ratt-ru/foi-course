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

***

* [Outline](../0_Introduction/0_introduction.ipynb)
* [Glossary](../0_Introduction/1_glossary.ipynb)
* [1. Radio Science](1_0_introduction.ipynb)  
    * Previous: [1.2 Electromagnetic radiation and astronomical quantities](1_2_electromagnetic_radiation_and_astronomical_quantities.ipynb)
    * Next: [1.4 Radio regime](1_4_radio_regime.ipynb)

***

+++

Section status: <span style="background-color:orange">&nbsp;&nbsp;&nbsp;&nbsp;</span>

Import standard modules:

```{code-cell} ipython2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from IPython.display import HTML 
HTML('../style/course.css') #apply general CSS
```

Import section specific modules:

```{code-cell} ipython2
from IPython.display import Image
```

## 1.3. Radiative transport<a id='science:sec:radiative_transport'></a>

+++

In this section we briefly review how electromagnetic radiation propagates through non-empty space in which radiation may be absorbed or generated. To keep things simple we will refrain from going too far into the details. However the concept of radiative transport plays a fundamental role in interferometry and therefore cannot be omitted. 

+++

In the previous section we discussed the fact that specific intensity is independent of the distance to a source as long as no emission is generated and nothing is absorbed. In reality a ray bundle may gain or lose intensity on its way to the observer, along a path, $x$, say. The *loss* of intensity is generally proportional to the intensity itself (imagine an absorption probability for radiation). We will adopt a linear model and assume that, as the ray bundle propagates through a medium along an infinitesimal path length $dx$, $I_\nu$ loses a fraction 

$$ -\kappa_\nu(x)\,I_\nu \,dx $$

Here $\kappa_\nu(x)$ is called the linear absorption coefficient. Furthermore, intensity will be *generated* independently of the incoming radiation in such a way that the intensity will increase by a constant amount of $\varepsilon_\nu \,dx$ along the infinitesimal path length $dx$. Here $\varepsilon_\nu $ is called the emission coefficient. Note that, in general, $\kappa_\nu$ and $\varepsilon_\nu$ may be functions of $I$. In what follows we will neglect this effect and assume that they only depend on $x$. From the above, we can write down a simplified version of the equation describing radiative transfer i.e.

+++

<a id='science:eq:03_001'></a><!--\label{science:eq:03_001}-->$$
\begin{align}
    dI_\nu \,&= -\kappa_\nu\,I_\nu\,dx+\varepsilon_\nu\,dx\\
    &\Leftrightarrow\\
    \frac{dI_\nu}{dx} \,&= -\kappa_\nu\,I_\nu+\varepsilon_\nu \\
\end{align}
$$

<span style="background-color:red">HLB:IC: Pretty much all the calculations below this comment seems unnecessarily convoluted and needs to be revised. In particular many of the integrations seem unnecessary, work with the differentials where possible. </span>

+++

The equation of radiative transfer has simple solutions for $\kappa_\nu\,=\,0$ or $\varepsilon_\nu\,=\,0$:

+++

<a id='science:eq:03_002'></a><!--\label{science:eq:03_002}-->$$
\begin{align}
     \kappa_\nu\,&=\,0 &\Rightarrow\quad& I_\nu(x)\,=\,I_\nu(x_0)+\int_{x_0}^{x}\varepsilon_\nu(t)\,dt\\
     \varepsilon_\nu\,&=\,0 &\Rightarrow\quad& I_\nu(x)\,=\,I_\nu(x_0)\,e^{-\int_{x_0}^{x}\kappa_\nu(t)\,dt} \\
\end{align}
$$

+++

To proceed to the *general solution* of the equation of radiative transfer, one defines the optical depth, $\tau_\nu$, via

+++

<a id='science:eq:03_003'></a><!--\label{science:eq:03_003}-->
$$ d\tau_\nu \underset{def}{=} -\kappa_\nu dx \quad \Rightarrow \quad \tau_\nu = \int_x^{x_0}\kappa_\nu(t) dt $$

+++

Here the observer is at the position $x_0$ and $\tau_\nu\,=\,0$ at the position of the observer. With that, one basically introduces a more relevant quantity than the actual path length as a parameter. Substituting via the chain rule

+++

<a id='science:eq:03_004'></a><!--\label{science:eq:03_004}-->$$
\begin{align}
    \frac{dI_\nu}{dx} \,&= \,\frac{dI_\nu}{d\tau_\nu}\frac{d\tau_\nu}{dx}\\
    &=\, -\kappa_\nu\frac{dI_\nu}{d\tau_\nu}\\
    &=\, -\kappa_\nu\,I_\nu+\varepsilon_\nu \\
\end{align}
$$

+++

The figure below shows the radiative transport process in a pictorial form. 

```{code-cell} ipython2
Image(filename='figures/radiative_transport.png', width=800)
```

By defining the source function or efficiency, $s_\nu$, (note that, unfortunately, the same symbol $S_\nu$ as for the flux density is often used for $s_\nu$) as

+++

<a id='science:eq:03_005'></a><!--\label{science:eq:03_005}-->$$
\begin{align}
    s_\nu\,&\underset{def}{=}\,\frac{\varepsilon_\nu}{\kappa_\nu}\\
\end{align}
$$

+++

we get

+++

<a id='science:eq:03_005'></a><!--\label{science:eq:03_005}-->$$
\begin{align}
    \frac{dI_\nu}{d\tau_\nu}\,=\,I_\nu-s_\nu 
\end{align}
$$

+++

which can be solved via multiplication with $e^{-\tau_\nu}$ and integration (i.e. using an integrating factor)

+++

<a id='science:eq:03_006'></a><!--\label{science:eq:03_006}-->
\begin{align}
    \frac{d\left(I_\nu \,e^{-\tau_\nu}\right)}{d\tau_\nu}\,&=\,\frac{dI_\nu}{d\tau_\nu}\,e^{-\tau_\nu}-I_\nu\,e^{-\tau_\nu}\\
    &=\,-s_\nu\,e^{-\tau_\nu}\\
    &\Rightarrow\\
    \int_0^{\tau_\nu(x)} \frac{d\left(I_\nu \,e^{-\tau_\nu}\right)}{d\tau_\nu}\,d\tau_\nu\,&=\,I_\nu(\tau_\nu(x))\,e^{-\tau_\nu(x)}-I_\nu(0)e^{0}\\
    &=\,I_\nu(\tau_\nu(x))\,e^{-\tau_\nu(x)}-I_\nu(0)\\
    \\&=\,-\int_0^{\tau_\nu(x)}s_\nu\,e^{-\tau_\nu}\,d\tau_\nu\\
    &\Leftrightarrow\\
    I_\nu(0)\,&=\, I_\nu(x_0)\\
    &=\, I_\nu\left(\tau_\nu(x)\right)\,e^{-\tau_\nu(x)}+\int_0^{\tau_\nu(x)}s_\nu\,e^{-\tau_\nu}\,d\tau_\nu
\end{align}

+++

Kirchhoff's law of thermal radiation (see [here](https://en.wikipedia.org/wiki/Kirchhoff's_law_of_thermal_radiation) for example) implies that, in a local thermodynamical equilibrium (LTE), at temperature $T$, the emissivity equals the absorbed radiation. Thus we have that

+++

<a id='science:eq:03_007'></a><!--\label{science:eq:03_007}-->$$
\begin{align}
    \varepsilon_\nu\,&\underset{LTE}{=}\,\kappa_\nu\,B_\nu(T)\\
    s_\nu\,&=\,B_\nu(T)
\end{align}
$$

+++

where $B_\nu(T)$ is the radiation emitted, at frequency $\nu$, by a black body of temperature $T$ ([see section 1.5.1 &#10142;](1_5_black_body_radiation.ipynb#science:sec:blackbody_emission) <!--\ref{science:sec:blackbody_emission}--> ). 

+++

Thus, starting at any position $x$, we have that

+++

<a id='science:eq:03_008'></a><!--\label{science:eq:03_008}-->$$
\begin{align}
    I_\nu(0)\,&=\, I_\nu(x_0)\\
    &=I_\nu\left(\tau_\nu(x)\right)\,e^{-\tau_\nu(x)}+\int_0^{\tau(x)}s_\nu\,e^{-\tau_\nu}\,d\tau_\nu\\
    &=I_\nu\left(\tau_\nu(x)\right)\,e^{-\tau_\nu(x)}+\int_0^{\tau(x)}B_\nu(T)\,e^{-\tau_\nu}\,d\tau_\nu
\end{align}
$$

+++

If the temperature $T$ is constant, $B_\nu(T)$ is constant, and

+++

<a id='science:eq:03_009'></a><!--\label{science:eq:03_009}-->$$
\begin{align}
    I_\nu(0)\,&=\, I_\nu(x_0)\\
    &=I_\nu\left(\tau_\nu(x)\right)\,B_\nu(T)\,e^{-\tau_\nu(x)}+\int_0^{\tau(x)}B_\nu(T)\,e^{-\tau_\nu}\,d\tau_\nu\\
    &=I_\nu\left(\tau_\nu(x)\right)\,B_\nu(T)\,e^{-\tau_\nu(x)}+B_\nu(T)\left(1-e^{-\tau_\nu(x_0)}\right)
\end{align}
$$

+++

It is easy to see that for an opaque source

+++

<a id='science:eq:03_009'></a><!--\label{science:eq:03_009}-->$$
\begin{align}
 \tau(x) \,&=\, \infty\\
 &\Rightarrow\\
 I_\nu(x_0) \,&=\, B_\nu(T)
 \end{align}
 $$

+++

Generally, if the source function is constant (substitute $B_\nu$ for $S_\nu$ for LTE)

+++

<a id='science:eq:03_010'></a><!--\label{science:eq:03_010}-->$$
\begin{align}
    s_\nu \,&=\, s_\nu^0 = const.\\
    &\Rightarrow\\
    I_\nu(0)\,&=\, I_\nu(x_0)\\
    &=I_\nu\left(\tau_\nu(x)\right)\,s_\nu\,e^{-\tau_\nu(x)}+\int_0^{\tau(x)}s_\nu\,e^{-\tau_\nu}\,d\tau_\nu\\
    &=I_\nu\left(\tau_\nu(x)\right)\,s_\nu\,e^{-\tau_\nu(x)}+s_\nu\left(1-e^{-\tau_\nu(x_0)}\right) 
\end{align}
$$

+++

From this it follows that, when all emission comes from an optically thin slab of material, we have

+++

<a id='science:eq:03_011'></a><!--\label{science:eq:03_011}-->$$
\begin{align}
    s_\nu \,&=\, s_\nu^0 = const.\\
    I_\nu(\tau_\nu(x)) \,&=\, 0\\
    \tau_\nu(x) \,&\ll\, 1\\
    &\Rightarrow\\
    I_\nu(0)\,&=\, I_\nu(x_0)\,=\, s_\nu^0\,\tau_\nu(x) \\
\end{align}
$$

+++

which is proportional to $\kappa_\nu$ if $\kappa_\nu$ is constant. Thus, for a background source (in the optically thin case), we have

+++

<a id='science:eq:03_011'></a><!--\label{science:eq:03_011}-->$$
\begin{align}
    s_\nu \,&=\, s_\nu^0 = const.\\
    I_\nu(\tau_\nu(x)) \,&\neq\, 0\\
    \tau_\nu(x) \,&\ll\, 1\\
    &\Rightarrow\\
    I_\nu(0)\,&=\, I_\nu(x_0)\,=\, I_\nu(\tau(x))-\tau_\nu(x)(I_\nu(\tau(x))-s_\nu^0) \\
\end{align}
$$

+++

Note that, if the background intensity $I_\nu(\tau(x))$ is larger than the source function $s_\nu^0$, the emission gets reduced (absorption). On the other hand, if $I_\nu(\tau(x))$ is lower than the source function, we witness an increase in brightness (emission case). As the blackbody radiation is always larger for a larger temperature, we can say that absorption occurs when a background source of a certain temperature is obscured by an optically thin slab of gas of lower temperature. On the contrary, when the source is colder than the medium in propagates through, the additional emission makes the source look brighter than it really is. 

<span style="background-color:yellow">HLB:IC: Is all of this really necessary to
show that a source will appear brighter when it's light passes through a hotter
medium and dimmer when it passes through a cold absorbing medium?</span>

+++

***

* Next: [1.4 Radio regime](1_4_radio_regime.ipynb)
