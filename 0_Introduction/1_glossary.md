---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.7
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

## Glossary <a id='preface:sec:glossary'></a>

+++

### A

+++

**azimuth:** the azimuth angle is measured in the celestial horizon from due north towards the east.

**altitude:** altitude of a celestial object is the angle between it and the celestial horizon.

**altitude-azimuth mount:** an antenna mount which allows the antenna to track a source in the sky by rotating along two axes - altitude (vertical) and azimuth (horizontal).

+++

### B

+++

### C

+++

**celestial equator:** the celestial equator is in the same plane as the equator of the earth and is obtained by projecting the equator of the earth onto the celestial sphere.

**celestial horizon:** observer's horizontal plane and is the fundamental plane of the horizontal coordinate system.

**celestial sphere:** imaginary unit sphere surrounding the earth onto which all the celestial objects in the universe is projected.

+++

### D

+++

**declination:** the declination of an object is the  angular distance it is away from the celestial equator measured along its hour circle (it is positive in the northern celestial hemisphere and negative in the southern celestial hemisphere).

**density weighting function:** see *weighting, density*

**direction cosine coordinates:** an astronomical coordinate system based on the direction cosines $l$, $m$ and $n$ which is often used in radio interferometry to create local sky maps around a target source. The fourier relationship that exists between the visibility and the image space in interferometry becomes apparent in this coordinate system.

**direction-dependent effects:** propagation effects which vary with direction.

**direction-independent effects:** propagation effects which are the same in all directions.

**dirty image:** see *image, dirty*

+++

### E

+++

**ecliptic:** the imaginary path the sun transverses on the celestial sphere.

**elevation:** see *altitude*.

**equatorial coordinate system:** widely used coordinate system which is used to keep track of celestial objects.The fundamental plane of this coordinate system is obtained by projecting the earth's equator onto the celestial sphere.  

**equatorial mount:** an antenna mount which allows the antenna to track a source in the sky by rotating about the polar axis (i.e., an axis which points towards the celestial pole).

+++

### F

+++

**field centre:** see phase centre.

**fringe pattern:** sinusoidal function describing the position of a spatial domain source in the spatial frequency domain.

**first point of Aries:** the point on the celestial sphere where the sun crosses the celestial equator from south to north.

**full width at half maximum (FWHM):** the extent of a function between the two extreme positions which are at the half value point of the peak value, a metric used to define the scale of various distributions and beams.

+++

### G

+++

**great circular arc**: a great circular arc is an arc segment of a great circle.

**great circle**: a great circle is formed by the intersection of a sphere and a plane that passes through the center of the sphere.

+++

### H

+++

**horizontal coordinate system:** the horizontal coordinates is used to enable an observer on earth to locate celestial objects in an observer's local sky.  

**hour circle:** the hour circle of an object is the circle on the celestial sphere that crosses the NCP and the object itself and is perpendicular to the celestial equator.

**hour angle:** hour angle of a celestial body is the angular distance (measured in hours) between the hour circle of a celestial object and the local meridian measured along the celestial equator in a westerly direction.

+++

### I

+++

**image, dirty:** the image produced by Fourier transforming the sampled visibilities of an interferometric observation, approximately the ideal sky image convolved with the array PSF response. This is the initial image input to deconvolution algorithms.

+++

### J

+++

### K

+++

### L

+++

**latitude:** the angular distance of a location north or south of the earth's equator. 

**local meridian**: is the hour circle on the celestial sphere which we form when we connect the NCP with zenith.

**local sidereal time (LST)**: hour angle of the vernal equinox.

**longitude:** the angular distance of a location east or west of the meridian at Greenwich.

**low noise amplifier (LNA):** the first amplifier in the analogue electronics front-end chain, used to amplify the weak sky signal at the cost of introducing a small amount of system noise.

+++

### M

+++

### N

+++

**nadir:** the position on the celestial sphere opposite zenith.

**natural weighting:** see *weighting, natural*

**north celestial pole (NCP):** obtained by projecting the north pole of the earth onto the celestial sphere.

+++

### O

+++

### P

+++

**parallactic angle:** spherical angle between the great circle on the celestial sphere through the source and the zenith, and the great circle through the source and the north celestial pole.

**phase centre:** the position on the sky in which an array has been 'phased' to, the reference position in the direction cosine coordinate system. 

**point spread function (PSF):** the effect of the measuring system has on a point source in the image domain. This is effectively the Fourier transform of the visibility domain sampling function. In historical literature it is often called the *synthesized beam*.

**Polaris:** a star located close to the NCP.

**precession:** a change in the orientation of the rotational axis of a rotating body.

**primary beam:** directional dependence of the gain of an antenna.

+++

### Q

+++

### R

+++

**radiation pattern**: see **primary beam**.

**radio frequency interference (RFI):** man-made radio waves which corrupt the desired sky signal.

**right ascension:** the right ascension of an object is the angular distance between the vernal equinox and the hour circle of a celestial object measured along the celestial equator and is measured in an easterly direction.

**robust weighting:** see *weighting, robust*

+++

### S

+++

**sampling function:** in signal processing a discrete function which transforms a continuous signal to a discrete signal.

**sidereal day:** a sidereal day is the amount of time it takes for an arbitrary star to return to the same location in the sky.

**solar day:** a solar day is the time it takes for the sun to return to the same position in the sky. 

**spatial domain:** a signal domain in which the relative distance between sample positions is directly related to the physical relative position of the signals, e.g. an image of a field of stars.

**spatial frequency domain:** a signal domain where the amplitude and phase of sampled position describes the intensity and offset of a complex sinusoidal wave. The relative position of samples represents how similar the frequency and angle of the two samples are.

**spherical triangle:** a spherical triangle is formed by the pairwise intersection of three great circular arcs in three vertices.

**south celestial pole (SCP):** obtained by projecting the south pole of the earth onto the celestial sphere.

**synthesized beam:** see *point spread function (PSF)*.

**system temperature:** a measure of the noisiness of the telescope and electronics, related to the sensitivity of the telescope.

+++

### T

+++

**transit:** a celestial body is at transit when it crosses the local meridian. 

**taper weighting function:** see *weighting, taper*

+++

### U

+++

**uniform weighting:** see *weighting, uniform*

+++

### V

+++

**vernal equinox:** see *first point of Aries*.

**visibilities:** discrete measurements of the spatial frequency (visibility) domain from a set of interferometric baselines.

+++

### W

+++

**weighting, density:** a function used to set the data sample significance when combining overlapping visibility samples, necessary for producing a synthesised image.

**weighting, natural:** weighting scheme which maximizes sensitivity, minimizes PSF side-lobes but at the cost of resolution. Also called inverse variance weighting.

**weighting, robust:** a parameterized weighting scheme to balance between resolution and sensitivity.

**weighting, taper:** a function which acts as a spatial filter to select out certain scales when producing a synthesised image.

**weighting, uniform:** weighting scheme which maximizes resolution but at the cost of higher PSF side-lobes. Also called unity weighting.

+++

### X

+++

### Y

+++

### Z

+++

**zenith:** zenith is the position on the celestial sphere which lies directly above an observer on earth.

+++

### Symbols

+++

* $\lambda$ : Wavelength (m)
* $\nu$ : Frequency (Hz)

* $\mathbf{B}$ : Brightness Coherence Matrix
* $\boldsymbol{\mathcal{D}}$, $\boldsymbol{\mathcal{M}}$ : Unpolarized Visibility Matrices.
* $\mathbf{e}$ : Electric Field Vector
* $\varepsilon_{\nu}$: Radiative emission coefficient
* $\boldsymbol{\mathcal{G}}$ : Unpolarized gain Matrix
* $\boldsymbol{\mathscr{G}}$ : $\mathbf{g}\mathbf{g}^H$
* $I$ : Sky Brightness
* $I,Q,U,V$ : Stokes Parameters. Not to be confused with sky brightness and visibilities.
* $\mathbf{J}$ : Jones matrix, standard examples:
    * $\mathbf{D}$ : feed leakage
    * $\mathbf{E}$ : primary beam
    * $\mathbf{F}$ : Faraday rotation
    * $\mathbf{G}$ : gain
    * $\mathbf{K}$ : geometric delay
    * $\mathbf{P}$ : parallactic angle
* Jy : Jansky, Flux density unit, $1\ \mathrm{Jy} = 10^{-26} \ \mathrm{W\, m^{-2}\, Hz^{-1}}$
* $\kappa_{\nu}$ : Radiative absorption coefficient
* $L$: Bolometric Luminosity ($\mathrm{W}$ or $\mathrm{erg,s^{-1}}$)
* $L_{\nu}$: Spectral luminosity ($\mathrm{W\ s^{-1} \ Hz^{-1}}$ or $\mathrm{ergs\, s^{-1} \, Hz^{-1}}$)
* $\boldsymbol{\mathcal{M}}$ : see $\boldsymbol{\mathcal{D}}$
* $P$ : Power (W, ergs)
* $\mathbf{S}$ : Stokes Vector, contains Stokes Parameters $I,Q,U,V$
* $S_{\nu}$: Flux density ($\mathrm{W m^{-2} s^{-1}}$ or $\mathrm{ergs\ cm^{-2} s^{-1}}$)
* $s_{\nu}$: Radiative efficiency: $s_\nu = \frac{\varepsilon_\nu}{\kappa_\nu}$
* $T$ : Temperature (K)
* $\tau_\nu$ : Optical depth
* $\mathbf{v}$ : Voltage Vector
* $\mathscr{V}$ : Visibility function (not the measurement, but underlying continuous function).
* $V$ : Visibilities (set of measurements)
* $\mathbf{V}$ : Polarized visibilities

+++

#### Constants
* Imaginary Number: $\imath$ = $\sqrt{-1}$
* Speed of light in vacuum: $c= 299 \ 792 \ 458 \ \mathrm{m\, s^{-1}}$
* Boltzmann Constant: $k_{B}= 1.38064852 \times 10^{-23} \ \mathrm{m^2\, kg\, s^{-2}\, K^{-1}}$
* Planck constant: $h = 6.62607015 \times 10^{-34}\ \mathrm{J\, Hz^{-1}}$

+++

#### Instrumental parameters
* $N$ - Number of antennas
* $D$ - Diameter of Dish
* $A$ - Area of Dish
* $A_\text{eff}$ - Effective area 
* $\mathbf{b}$ - Baseline vector
* $|\mathbf{b}|$ - Baseline length
* $\theta_r$ - Angular resolution (e.g. FWHM of PSF)
* $\Delta \theta$ - Field of view or angular area
* $uv$ - Shortcut when speaking about uv coverage in general, uv components ...


#### Reference frame
* $L_a$ - Observer latitude
* $L_o$ - Observer longitude
* $\gamma$ - Vernal point
* $\alpha$ - Right Ascension
* $\delta$ - Declination (can also represent a delta function)
* $H$ - Hour Angle
* $\mathcal{A}$ - Azimuth
* $\mathcal{E}$ - Elevation
* $q$ - Parallactic Angle


* ($x, y, z$) - Cartesian coordinates
* ($\rho,\theta,\varphi$) - Spherical coordinates
* ($l,m$, $n$) - Direction Cosines
* ($X,Y$, $Z$) - Equatorial Coordinate Reference Frame (Baselines)
* ($u,v$, $w$) - Visibility Coordinate System


* $\mathbf{\hat{e}_x},\mathbf{\hat{e}_y},\mathbf{\hat{e}_z}$ - Basis for cartesian
* $\mathbf{\hat{e}_{\rho}},\mathbf{\hat{e}_{\theta}},\mathbf{\hat{e}_{\varphi}}$ - Basis for spherical
* $\mathbf{\hat{e}_X},\mathbf{\hat{e}_Y},\mathbf{\hat{e}_Z}$ - Basis for equatorial XYZ
* $\mathbf{\hat{e}_u},\mathbf{\hat{e}_v},\mathbf{\hat{e}_w}$ - Basis for uvw
* $\mathbf{\hat{e}_l},\mathbf{\hat{e}_m},\mathbf{\hat{e}_n}$ - Basis for lmn

#### Math & Operators

* $\Re \{\cdot\},\Im\{\cdot\}$ - Real and imaginary part
* $(\cdot)^*$ - Conjugation
* $|\cdot|$ - Magnitude of a vector or determinant of a matrix
* $\|\cdot\|$ - Norm

* $\angle F$ - Phase of F (in radians)
* $\phi$ - Phase (e.g. $e^{i\phi}$) (in radians)

* $\mathbf{a}\cdot \mathbf{b}$ - Scalar product
* $\circ$ - Convolution
* $\star$ - Cross-correlation
* $C$ - Convolution Kernel
* $\mathcal{O}(\cdot)$ dominated
* $(\cdot)^T$ - Transpose
* $(\cdot)^H$ - Hermitian Transpose
* $(\cdot)^{-1}$ - Matrix Inversion
* $\mathbb{J}$ - Jacobian matrix
* $\mathbb{H}$ - Hessian matrix
* $\odot$ - Hadamard Product
* $(\cdot)^{\odot-1}$ - Hadamard Inverse

* $(\cdot)_L$ - Lower Half of Vector
* $(\cdot)_U$ - Upper Half of Vector
* $\textrm{vec}(\cdot)$ - Vectorization
* $\textrm{vec}^{-1}(\cdot)$ - Matrization

* $\textrm{diag}(\cdot)$ - Creates a matrix by placing operand (which should be a vector) on diagonal, all other entries are zero


* $\mathscr{F}\{\cdot\},$ - Fourier transform operator
* $\mathscr{F}_D\{\cdot\}_k,$ - Discrete Fourier transform operator. The subscript denotes its $k^{th}$ element.
* $\mathscr{F}^{-1}\{\cdot\}$ - Inverse Fourier transform operator
* $\mathscr{F}^{-1}_D\{\cdot\}_n$ - Inverse discrete Fourier transform operator The subscript denotes its $n^{th}$ element.
* $F \stackrel{\mathscr{F}}{\rightleftharpoons} E$ - Fourier pairs


* $\Omega$ - Solid angle
* $\widehat{\beta}$ - Angular quantity (when context is ambiguous) otherwise nothing
* $\mathbb{C}$ - field of complex numbers
* $\mathbb{C}^0$ - field of continuous functions
* $\mathbb{R}$ - field of real numbers
* $\mathbb{N}^0$ - set of natural numbers (including 0)
* $\Rightarrow$ - symbol for "leads to"
* $\Leftrightarrow$ - symbol for "is equivalent with"
* $\frac{d}{dx}$ - derivative

#### Signal processing & Algorithm

* $\delta x$ - Update Step
* $\tau$ - Integration Time
* $\Delta \nu$ - Bandwidth 
* $<\cdot>_t$ - Averaging in time
* $<\cdot>_\nu$ - Averaging in frequency


* $\delta$ - Delta function
* $\Pi$ - Boxcar function
* $III$ - Shah function
* $S$ - Sampling function
* $\text{sinc}_{\mathrm u}$ - Unnormalized Sinc function
* $\text{sinc}$ - Normalized Sinc function
* $H$ - Heaviside function
* $\mathbf{r}$ - Residual Vector
* $\mathbf{g}$ - Gain Vector
* $\breve{\mathbf{g}}$ - $[\Re\{\mathbf{g}\},\Im\{\mathbf{g}\}]$
* $\mathbf{d}$ - Data Vector
* $\mathbf{m}$ - Model Vector
* $\lambda_{\textrm{LM}}$ - Levenberg-Marquardt Damping Factor
