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

# Fundamentals of Radio Interferometry for Aperture Synthesis

+++

Interferometry is a fundamental technique used in radio astronomy but is often presented in an overly complicated way. It is true that the technique is rarely used in other fields of astronomy and physics. Many of our intuitions about imaging, which comes from cameras and out own eyes, hide the underlying transformations which are central to aperture synthesis theory. With this book we hope to present a useful entry point into the topic by sticking to the fundamentals, this work is intended for a masters or doctoral student who is starting on the subject.

As this is meant to be a living and evolving document with a number of contributors, any help in regards to content, editing, or presentation are welcome. We are striving to create the book we did not have when first learning interferometry and aperture synthesis.

+++

### Outline <a id='preface:sec:outline'></a>

* [Outline](#preface:sec:outline)
* [A Note on Software](#preface:sec:software)
* [Style Guide](#preface:sec:style)
* [Known Issues](#preface:sec:issues)
* [Glossary](1_glossary.ipynb#preface:sec:glossary)
* [Mathematical Symbols](1_glossary.ipynb#preface:sec:symbols)
* [Editing Guide](editing_guide.ipynb)
* [Appendix](2_Appendix.ipynb#preface:sec:glossary)

#### Colour Status

There is a colour next to each section link which provides a quick status update on that particular section. The colours indicate:

* <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span> : Status unknown.
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : Need significant edits and rewrites.
* <span style="background-color:orange">&nbsp;&nbsp;&nbsp;&nbsp;</span> : For the ambitious to edit. Needs language rewrites or clarification/has major comments. Missing major content.
* <span style="background-color:yellow">&nbsp;&nbsp;&nbsp;&nbsp;</span> : Could be edited again. Needs minor edits/has minor comments. Missing minor content.
* <span style="background-color:green">&nbsp;&nbsp;&nbsp;&nbsp;</span> : Ready for another edit, just needs to be checked for style, notation, code, and figures.

#### Content

1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Radio Science using Interferometric Arrays](../1_Radio_Science/1_0_introduction.ipynb)
    1.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Remarks on Basic Astrophysics](../1_Radio_Science/01_01_a_brief_introduction_to_basic_astrophysics.ipynb)
    2.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Electromagnetic Radiation and Astronomical Quantities](../1_Radio_Science/01_02_electromagnetic_radiation_and_astronomical_quantities.ipynb)
    3.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Radiation Transport](../1_Radio_Science/01_03_radiation_transport.ipynb)
    4.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Radio Regime](../1_Radio_Science/01_04_radio_regime.ipynb)
    5.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Black-body Radiation](../1_Radio_Science/01_05_black_body_radiation.ipynb)
    6.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Synchrotron Emission](../1_Radio_Science/01_06_synchrotron_emission.ipynb)
    7.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Line Emission](../1_Radio_Science/01_07_line_emission.ipynb)
    8.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Astronomical Radio Sources](../1_Radio_Science/01_08_astronomical_radio_sources.ipynb)
    9.  <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[A Brief Introduction to Interferometry](../1_Radio_Science/01_09_a_brief_introduction_to_interferometry.ipynb)
    10. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Limits of Single Dishes](../1_Radio_Science/01_10_limits_of_single_dishes.ipynb)
    11. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Modern Interferometric Arrays](../1_Radio_Science/01_11_modern_interferometric_arrays.ipynb)
    12. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../1_Radio_Science/01_x_further_reading_and_references.ipynb)
2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Mathematical Groundwork](../2_Mathematical_Groundwork/2_0_introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Complex Numbers](../2_Mathematical_Groundwork/2_1_complex_numbers.ipynb)
        1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Field of Complex Numbers](../2_Mathematical_Groundwork/2_1_complex_numbers.ipynb#math:sec:the_field_of_complex_numbers)
        2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Euler's Formula](../2_Mathematical_Groundwork/2_1_complex_numbers.ipynb#math:sec:eulers_formula)
        3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Periodic Functions and Complex Numbers](../2_Mathematical_Groundwork/2_2_special_functions.ipynb#math:sec:periodic_functions_and_complex_numbers)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Important Functions](../2_Mathematical_Groundwork/2_2_important_functions.ipynb)
        1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Gaussian Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:gaussian_function)
        2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Sinc Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:sinc_function)
        3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Dirac Delta Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:dirac_delta_function)
        4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Shah Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:shah_function)
        5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Heavyside (step) Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:heavyside_function)
        6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Box Function](../2_Mathematical_Groundwork/2_2_important_functions.ipynb#math:sec:box_function)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Fourier Series](../2_Mathematical_Groundwork/2_3_fourier_series.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Fourier Transform](../2_Mathematical_Groundwork/2_4_the_fourier_transform.ipynb)
        1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Definition](../2_Mathematical_Groundwork/2_4_the_fourier_transform.ipynb#math:sec:fourier_transform_definition)
        2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Examples](../2_Mathematical_Groundwork/2_4_the_fourier_transform.ipynb#math:sec:fourier_transform_examples)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Convolution](../2_Mathematical_Groundwork/2_5_convolution.ipynb)
    6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Auto-correlation and Cross-correlation](../2_Mathematical_Groundwork/2_6_auto_correlation_and_cross_correlation.ipynb)
    7. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Fourier Theorems](../2_Mathematical_Groundwork/2_7_fourier_theorems.ipynb)
        1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Similarity Theorem](../2_Mathematical_Groundwork/2_7_fourier_theorems.ipynb#math:sec:similarity_theorem)
        2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Shift Theorem](../2_Mathematical_Groundwork/2_7_fourier_theorems.ipynb#math:sec:shift_theorem)
        3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Convolution Theorem](../2_Mathematical_Groundwork/2_7_fourier_theorems.ipynb#math:sec:convolution_theorem)
        4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Auto-correlation Theorem](../2_Mathematical_Groundwork/2_7_fourier_theorems.ipynb#math:sec:auto_correlation_theorem)
    8. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Discrete Fourier Transform (DFT) and the Fast Fourier Transform (FFT)](../2_Mathematical_Groundwork/2_8_the_discrete_fourier_transform.ipynb)
    9. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Sampling Theory](../2_Mathematical_Groundwork/2_9_sampling_theory.ipynb)
    10. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Linear Algebra](../2_Mathematical_Groundwork/2_10_linear_algebra.ipynb)
    11. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Least-squares Minimization](../2_Mathematical_Groundwork/2_11_least_squares.ipynb)
    12. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Solid Angle](../2_Mathematical_Groundwork/2_12_solid_angle.ipynb)
    13. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Spherical Trigonometry](../2_Mathematical_Groundwork/2_13_spherical_trigonometry.ipynb)
    14. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../2_Mathematical_Groundwork/2_x_further_reading_and_references.ipynb)
3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Positional Astronomy](../3_Positional_Astronomy/3_0_Introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Equatorial Coordinates (RA, Dec)](../3_Positional_Astronomy/3_1_Equatorial_Coordinates.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Hour Angle (HA) and Local Sidereal Time (LST)](../3_Positional_Astronomy/3_2_Hour_Angle.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Horizontal Coordinates (ALT,AZ)](../3_Positional_Astronomy/3_3_Horizontal_Coordinates.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Direction Cosine Coordinates ($l$,$m$,$n$)](../3_Positional_Astronomy/3_4_Direction_Cosine_Coordinates.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../3_Positional_Astronomy/3_x_further_reading_and_references.ipynb)
4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Visibility Space](../4_Visibility_Space/4_0_introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Baseline and Its Representations in Space](../4_Visibility_Space/4_1_The_Baseline.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The 2-element Interferometer](../4_Visibility_Space/4_2_The_2-element_Interferometer.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Visibility Function](../4_Visibility_Space/4_3_The_Visibility_Function.ipynb)
    4. UV Coverage
        1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[UV Tracks](../4_Visibility_Space/4_4_1_UV_Coverage_UV_Tracks.ipynb)
        2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Improving Your Coverage](../4_Visibility_Space/4_4_2_UV_Coverage_Improving_Your_Coverage.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Fourier Approximation & van Cittert-Zernike Theorem](../4_Visibility_Space/4_5_The_Fourier_Approximation_VanCittert-Zernike_Theorem.ipynb)
    6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../4_Visibility_Space/4_x_further_reading_and_references.ipynb)
5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Imaging](../5_Imaging/5_0_introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Spatial Frequencies](../5_Imaging/5_1_spatial_frequencies.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Sampling and Point Spread Functions](../5_Imaging/5_2_sampling_functions_and_psfs.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Gridding and Degridding for using the FFT](../5_Imaging/5_3_gridding_and_degridding.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Dirty Image and Visibility Weightings](../5_Imaging/5_4_imaging_weights.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Break Down of the Small Angle Approximation and the W-Term](../5_Imaging/5_5_widefield_effect.ipynb)
    6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../5_Imaging/5_x_further_reading_and_references.ipynb)
6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Deconvolution in Imaging](../6_Deconvolution/6_0_introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Sky Models](../6_Deconvolution/6_1_sky_models.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Interactive Deconvolution with Point Sources (CLEAN)](../6_Deconvolution/6_2_clean.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[CLEAN Implementations](../6_Deconvolution/6_3_clean_flavours.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Residuals and Image Quality](../6_Deconvolution/6_4_residuals_and_iqa.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Source Finding and Detection](../6_Deconvolution/6_5_source_finding.ipynb)
    6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../6_Deconvolution/6_x_further_reading_and_references.ipynb)
7. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Observing Systems](../7_Observing_Systems/7_0_introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Jones Notation](../7_Observing_Systems/7_1_jones_notation.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[The Measurement Equation (RIME)](../7_Observing_Systems/7_2_rime.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Analogue Electronics](../7_Observing_Systems/7_3_analogue.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Digital Correlators](../7_Observing_Systems/7_4_digital.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Primary Beam](../7_Observing_Systems/7_5_primary_beam.ipynb)
    6. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Polarization and Antenna Feeds](../7_Observing_Systems/7_6_polarization.ipynb)
    7. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Propagation Effects](../7_Observing_Systems/7_7_propagation_effects.ipynb)
    8. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Radio Frequency Interference (RFI)](../7_Observing_Systems/7_8_rfi.ipynb)
    9. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../7_Observing_Systems/7_x_further_reading_and_references.ipynb)
8. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Calibration](../8_Calibration/8_0_Introduction.ipynb)
    1. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Calibration as a Least Squares Problem](../8_Calibration/8_1_Calibration_Least_Squares_Problem.ipynb)
    2. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[1GC calibration](../8_Calibration/8_2_1GC.ipynb)
    3. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[2GC calibration](../8_Calibration/8_3_2GC.ipynb)
    4. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[3GC calibration](../8_Calibration/8_4_3GC.ipynb)
    5. <span style="background-color:gray">&nbsp;&nbsp;&nbsp;&nbsp;</span>[Further Reading and References](../8_Calibration/8_x_further_reading_and_references.ipynb)
9. Practical Advice for Reducing a Data Set and Recognizing Errors
    1. Imaging
        1. W-Term Correction
        2. Residual Artefacts
        3. Practical Settings for CLEAN
        4. Primary Beam Correction
        5. Image Quality Assessment
    2. Calibration
        1. Frequency and Time Solution Intervals
        2. Visibility Flagging
        3. Including Direction-Dependent Solutions
    3. Observing
        1. Accumulation interval and smearing
    4. Line observations: calibration and imaging issues
        1. Source finding
        2. Normalization
        3. What now? How do we get to the science?
    5. Continuum observations: calibration and imaging issues
        1. Dynamic Range
        2. Multi-Frequency Synthesis (MFS)
        3. Source Finding
        4. What now? How do we get to the science?

+++

### A Note on Software <a id='preface:sec:software'></a>

This book is developed and tested with the following software dependencies (a guide for setting up a virtual environment with the current versions is available in the git repository readme):

* python 2.7.6
* ipython 4.2.0
* numpy 1.10.1
* matplotlib 1.5.0
* astropy 1.1.1
* aplpy 1.0
* ipywidgets 4.1.1
* healpy 1.10.3
* ephem 3.7.6.0

The very first entry in a notebook will import our current standard modules:

```{code-cell} ipython3
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from IPython.display import HTML 
HTML('../style/course.css') #apply general CSS
```

Followed by an optional import of any section specific modules, e.g. :

```{code-cell} ipython3
import matplotlib.image as mpimg
from IPython.display import Image
```

If a section contains a significant amount of code, for readability it might be useful to suppress the code and only show the output. To do this an additional code block should be added:

```{code-cell} ipython3
from IPython.display import HTML
HTML('../style/code_toggle.html')
```

### Style Guide <a id='preface:sec:style'></a>

#### Mathematical Notation:

A global glossary defines all mathematical notation and useful definitions. 

Adhere to the following general mathematical notation:

1. Vector, scalar and matrix:
 * $a, A$ - Denotes a scalar quantity
 * $\mathbf{A}$, $\boldsymbol{\mathcal{A}}$ - Denotes a matrix
 * $\mathbf{a}$ - Denotes a vector

2. $2\times2$-Polarized vs. $N\times N$-Unpolarized matrices: 
 * $\mathbf{A}$ - Denotes a $2\times2$ polarized Jones matrix. Number a Jones matrix
 with any other subscript than $N$.
 * $\boldsymbol{\mathcal{A}}$ - Denotes a $N\times N$ unpolarized matrix (contain all the unpolarized quantities associated with an array in one matrix).

3. Jones versus Jacobian:
 * Please use $\mathbf{J}$ to denote a Jones matrix and $\mathbb{J}$ to denote a
 Jacobian matrix.

4. Fourier transform:
 * Please use $\mathscr{F}\{\cdot\}$ to denote the Fourier transform. 
 
5. Subscript to avoid ambiguity:
 * If one symbol is used to denote two quantities use a subscript to remove ambiguity. For instance $\lambda$ can mean wavelength or the LM-damping factor. Add a subscript, for
instance $\lambda_{\textrm{LM}}$ now refers to to the LM-damping factor, while $\lambda$ still refers to wavelength. Please add any new subscripted symbol to the glossary.  

The general list of symbols can be found in the [glossary &#10142;](1_glossary.ipynb#preface:sec:glossary).


If you want to include a specific definition to a word or phase, then italicize the text the first time you use it in a section or chapter and add the term to the glossary.

#### Notebook and Directory Naming Conventions:

Each chapter is contained in a separate directory, the directory name has the convention of the chapter number and chapter name, with spaces replaced by underscores, e.g. `6_deconvolution_in_imaging`. The directory will only contain notebooks, any data or additional files will be in a separate global data directory which includes a duplicately named directory for each chapter in which to store the data.

Notebook naming should be prefixed with the chapter number and either a sequential number  based on ordering in the chapter. Like directories, the notebook name should be the section name (with underscores to replace spaces), a shortened version of the section is also fine, e.g. the Sky Model section of Chapter 6 would be `6_1_sky_models.ipynb`.

#### Notebook Breadth:

Each chapter is made up of multiple sections, each of which is possibly made up of sub-section, et cetera. To keep notebooks a reasonable and consumable size, a notebook should only contain a single section. For long sections it may be reasonable to further break up a section into multiple notebooks.

#### Notebook Header:

The beginning of each notebook should with a set of navigation links including a link to the global outline (this notebook), glossary, the chapter specific introduction notebook, the previous section notebook, and the next section notebook. See example section 5.1.

Following the navigation links the standard python modules and any section specific modules should be imported, see 'A Note on Software' above for the current standard module import command. Following these import commands the notebook should start with a heading entry for the notebook with text that corresponds to the outline text above, see 'Section and Subsection Headings' for sizes below.

#### Notebook Footer:

At the end of a notebook, include a link to the next section notebook. If at the end of a chapter, provide a link to the next chapter.

#### Chapter Introduction:

Each chapter should contain a short introduction notebook which will provide an overview of the topics in the chapter and an outline of the notebooks in the chapter. At the end of the introduction include a list of editors and contributors of the chapter (indicate specific sections).

#### Chapter Conclusion:

The final notebook of a chapter should contain a section on further reading which contains links to papers and books, it may be useful to write a sentence about why a link is useful. Additionally, there should be a section which contains a list of all the external references noted in the chapter. Further, the conclusion to a chapter must contain a review of the topics covered in the chapter.

#### Section and Subsection Headings:

In a notebook, section names, e.g. 5.1 Spatial Frequencies, should use the heading size 2. While each subsequent sub-section should increase the heading size, e.g. a sub-section will be size 3, a sub-sub-section will be size 4,...

#### Emphasizing important points / key points / prerequisites: 

For clarity, it is possible to create emphasized point in the course of a paragraph, or a summary of important concepts at the end of a section/chapter. This relies on the use of a common CSS for every user. The CSS style is defined in course.css and will be applied to one notebook upon calling initcss.css_styling(). Those two files are located in the /style dir in the main course dir. 

First add these python lines to load the CSS file in the main style directory (might change after some housekeeping/discussion)
```
from IPython.display import HTML 
HTML('../style/course.css') ##apply general CSS
```

To write a "warning" text box, one can use in a markdown:

```
<div class=warn>
<b>Warning:</b> This relation assumes this particular hypothesis  
</div>
```

To write a note "note" or a piece of advice, use:

```
<div class=advice>
<b>Advice:</b> Check the homogeneity of your equations !!!
</div>
```

To create a green summary block:


```
<p class=conclusion>
  <font size=4> <b>Take-away message</b></font>
  <br>
  <br>
&bull; <b>Conclusion 1</b>: Important item to remember with a specific <em>emphasized</em> word <br><br>
&bull; <b>Conclusion 2</b>: A second important item to remember with a specific <em>emphasized</em> word.
</p>
```

To create a "Prerequisites"/"To read" header block:

```
<p class=prerequisites>
  <font size=4> <b>Prerequisites</b></font>
  <br>
  <br>
&bull; <b>Definition of ($u$,$v$,$w$):</b> [Go to 4.1](4_1_The_Baseline.ipynb) <br><br>
&bull; <b>The visibility function:</b> [Go to 4.3](4_3_The_Visibility_Function.ipynb)
</p>
```

#### References, Internal and External:

One of the limitations of the ipython notebook is the inability to render equation, figure, and table labels properly. For the moment, we have settled on a consistent, but inelegant standard.

Linking to internal (i.e. within the same notebook) and external (i.e. other notebooks in the book) references will use a dual method of using the standard markdown HREF and a LaTeX style so that dynamic links will work in the notebooks and conversion to PDF via LaTeX will contain references.

Links internal to a notebook references are created by adding the down arrow symbol &#10549; (HTML code `&#10549;`) as the link, e.g. `[hyperlink text &#10549;](#destination)`. A reference is created by including `<a id='destination'></a>` where the desired reference target is to be placed. In addition to the ipython notebook dynamic links LaTeX references should be included with the `\label{destination}` and `\ref{destination}` tags. An example of a complete internal reference is

```
[hyperlink text  &#10549;](#destination) <!--\ref{destination}-->
```

renders as: [hyperlink text  &#10549;](#destination) <!--\ref{destination}-->

And a complete internal label is

```
<a id='destination'></a> <!--\label{destination}-->
```

External links are similar to internal links, but use the right arrow symbol &#10142; (HTML code `&#10142;`) for a link. An example of a reference to another ipython notebook is `[hyperlink text &#10142;](another_notebook.ipynb#destination)` with a LaTeX tag `\ref{destination}`. An example of a complete external reference is

```
[hyperlink text &#10142;](another_notebook.ipynb#destination) <!--\ref{destination}-->
```

renders as: [hyperlink text &#10142;](another_notebook.ipynb#destination) <!--\ref{destination}-->

Note, HTML comment tags are wrapped around the Latex label and ref tags to hide them in the notebook.

#### Citations:

Citations to published work is a little tricky in our setup, we want to create two links. One for if we convert the notebook to latex we should be able to auto-generate a `\cite{}` tag, see the nbconvert [citation&#10548;](https://github.com/jupyter/nbconvert-examples/tree/master/citations) [example&#10548;](https://github.com/jupyter/nbconvert-examples/blob/master/citations/Tutorial.ipynb). And, the other as a hyperlink to a abstract or copy of the paper (e.g. a NASA ADS link). To do this we need to create a link and use the HTML `<cite data-cite='bibtexRef'>` tag where `bibtexRef` is the name of the reference in the bibtex file in the chapter directory. An up arrow symbol &#10548; (HTML code `&#10548;`) is used to denote an external to the book hyperlink. An example of a complete citation is

```
[<cite data-cite='1999ASPC..180.....T'>Synthesis Imaging in Radio Astronomy II</cite> &#10548;](http://adsabs.harvard.edu/abs/1999ASPC..180.....T)
```

which renders as:

[<cite data-cite='1999ASPC..180.....T'>Synthesis Imaging in Radio Astronomy II</cite> &#10548;](http://adsabs.harvard.edu/abs/1999ASPC..180.....T)

Where there is an entry in the bibtex file

```
@PROCEEDINGS{1999ASPC..180.....T,
    title = "{Synthesis Imaging in Radio Astronomy II}",
booktitle = {Synthesis Imaging in Radio Astronomy II},
     year = 1999,
   series = {Astronomical Society of the Pacific Conference Series},
   volume = 180,
   editor = {{Taylor}, G.~B. and {Carilli}, C.~L. and {Perley}, R.~A.},
   adsurl = {http://adsabs.harvard.edu/abs/1999ASPC..180.....T},
  adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```

#### Reference Naming Conventions:

In order to maintain uniform and informative reference labels we will use a standard naming convention of the form `chapterStr:type:uniqueID` where `chapterStr` is a unique, descriptive string for a chapter or chapter subsection, `type` is the type of content being labelled, and `uniqueID` is a unique ID for the content. For example a table in the Imaging chapter which contains information on weights could have the label `imaging:tbl:weights`. The `chapterStr` for each chapter is to be defined by the authors. If a section of a chapter is sufficiently large it shoud have its own `chapterStr`, perhaps with the prefix including the chapter `chapterStr`. The following are valid strings for `type`: `tbl` (table), `fig` (figure), `sec` (section), `code` (code block), `eq` (equation). The `uniqueID` is left to the authors, but suggested to contain a simple descriptive string and information on location within the chapter.

| Chapter    |  chapterStr  |
|------------|-------------:|
| Preface | `preface` |
| 1. Radio Science using Interferometers | `science` |
| 2. Mathematical Groundwork | `math` |
| 3. Positional Astronomy | `pos` |
| 4. Visibility Space | `vis` |
| 5. Imaging | `imaging` |
| 6. Deconvolution in Imaging | `deconv` |
| 7. Observing Systems | `instrum` |
| 8. Calibration | `cal` |
| 9. Putting it all together | `pract` |

| type     |  value  |
|----------|--------:|
| code     | `code`  |
| equation | `eq`    |
| figure   | `fig`   |
| section  | `sec`   |
| table    | `tbl`   |

#### Images and Pre-made Figures:

Though, ideally any figure that is included in a notebook can be generated from the code included in the notebook, this is not always possible. The preferred image type is PDF or SVG because these can be rescaled without aliasing issues, but PNG and JPEG can be used. If a figure or image is generated by some set of code, please include a reference or notes to that code so that if it needs to be regenerated then that will be possible. If a figure or image is made with a graphics programs such as Inkscape, GIMP, et cetera please include the working file in the git repository.

To display figures use the Image function, e.g.

```
Image(filename='figures/sidereal.png', width=300, height=100)
```

or in HTML in a markdown cell (will center the figure):
```
<img src='figures/sidereal.png' width=30%>
```
An include a description block below the figure, which can include a label for referencing.


#### Figures and Code Blocks:

Below each code block or figure include a cell which contains a description of what is presented, use italics, which in markdown means by starting and ending the text with stars, e.g. \*this text would be italicized in markdown\*. In this block one can include a label for referencing the figure or code block.

#### 3D Figures:

For a 3D figure include

```
%matplotlib nbagg
```

in the block to embed the figure in the notebook but allow for interaction.

#### Equation Blocks:

Equations can be written inline or in individual blocks. If you would like to reference an equation block, follow the label standard defined in 'References, Internal and External' above.

#### Coding style:

The majority of the code in this notebook is python, so please follow standard [Python PEP 8&#10548;](https://www.python.org/dev/peps/pep-0008/)

#### Committing to git repository:

Notebooks can get very large in size when they contain a number of generated figures. In order to keep the size of the repository down to a reasonable size please clear the output before making a new commit. This is done by selecting Cell > All Output > Clear from the menu at the top of the notebook.

Binary files should be stored in a directory in each chapter, for example images would be stored in a directory called figures.

+++

#### Crossing out in math mode
In calculus, it might be interesting to show simplifications as follow:
$\require{cancel}$

$B=\frac{x \cancel{a} y}{b \cancel{a}}$

To do that, you need to write this in a markdown:

```
$\require{cancel}$

$\frac{x \cancel{a} y}{b \cancel{a}}$
```
Please report to the "cancel" package for other crossing-out styles

+++

### Known Issues <a id='preface:sec:issues'></a>

As this is a working project there are a number of known issues we would like to resolve. If you have a nicer or more efficient solution then please let us know. For the moment, here is a list of known unknowns.

* Equation numbering does not render, this is due to a built-in setting to ipython notebook. The solution maybe to just hack the config files, see http://www.rbeesoft.com/blog/?p=6
* There is no built-in spellchecker in the notebook environment. There is a broken aspell notebook extension, maybe it will work soon.
