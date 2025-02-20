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

# Editing Guide

This is a general guide for section editors to help create a unified editing process.

The editing guise is divided into two categories.

+++

## Format Editing

+++

When format editing a section add comments by starting with your initials, the formatting tag abbreviation and wrap the comment in a css span tag to color the text so that it sticks out, an example is:
    
```
<span style="background-color:cyan">GSF:LF:this is the comment text</span>
```

renders as:

<span style="background-color:cyan">GSF:LF: this is the comment text</span>

We use cyan for format editing comments.

In the chapter introduction place the following list to indicate which of the formatting 
errors were checked by the editors in each chapter. This is not to indicate if the author corrected the suggestions. Only to indicate whether the content was checked by an editor. If they are red they were not checked. If they are green they were. The aim is to as far as possible correct formating errors without involving the author. Except for big changes like 
a conclusion section. So there ought to be very few cyan editor commments. 

#### Format status:

* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : LF: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : NC: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : RF: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : HF: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : GM: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : CC: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : CL: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : ST: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : FN: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : TC: Date
* <span style="background-color:red">&nbsp;&nbsp;&nbsp;&nbsp;</span> : XX: Date

The following formatting errors are to be checked for. The formatting guide for the book is discussed in more detail in the [outline &#10142;](0_introduction.ipynb).

+++

### Links functioning (LF)

+++

Check that all the links are functioning. Check that they point to the correct destination.  

+++

### Numbering and naming convention (NC)

+++

Check that the sections, figures, equations etc... are in the correct numerical order. Including table of contents. Also check numbering convention. 
* Sections: For Chapter 3: 3.1, 3.1.1, ..., 3.2, etc...
* Figures, Tables etc...: For each main section you order the figures per section. In other words the first three figures in Section 3.1 would be Figure 3.1.1, Figure 3.1.3, Figure 3.1.2. We do not abbreviate Figure, Table, Equation etc... in the caption.
* Number all sections, figures and tables.

+++

### Referencing (RF)

+++

We reference internal, external sections, figures, tables as follow:

* `[Fig. xxx &#10142;](#destination)`: [Fig. 3.1.1 &#10142;](../3_Positional_Astronomy/3_1_Equatorial_Coordinates.ipynb#pos:fig:geo). Note we used the external symbol here &#10142; as we are pointing to another notebook. If we were pointing within the current notebook we would use &#10549;, i.e. `&#10549;`. 
* We use the abbreviated version of Figure when we reference (Fig. xx). We do not when we are refferring to a Chapter or Table.
* `[$\S$ xxx &#10142;](#destination)`: [$\S$ 3.1. &#10142;](../3_Positional_Astronomy/3_1_Equatorial_Coordinates.ipynb). To refer to sections we use the $\S$ (`$\S$`) symbol.
* All links within chapters using &#10142; or &#10549; must point to a numbered Figure, Section etc... 
* `[<cite data-cite='Duffett2011'>Practical Astronomy with your calculator or spreadsheet </cite> &#10548;](https://books.google.co.za/books?id=MTGYxQyW998C&dq=astronomy+with+your+calculator+or+spreadsheet)` : [<cite data-cite='Duffett2011'>Practical Astronomy with your calculator or spreadsheet </cite> &#10548;](https://books.google.co.za/books?id=MTGYxQyW998C&dq=astronomy+with+your+calculator+or+spreadsheet). Make sure that citations are as follows and that the text that is displayed is the name of book article. Make sure reference is in chapters .bib file. 
* An equation is only numbered if it is referenced. Use same standard as Figure. Also use abbreviated Eq. when reffering to it.
* Check that the reference label is correct, is it the same as the actual Figure etc.. caption.

+++

### Header and Footer (HF)

The header and footer should look exactly like this. If someone is including some code in the standard modules cell that should be in section specific modules correct it. Are the names of links in headers and footers correct.

+++

***

* [Outline](0_introduction.ipynb)
* [Glossary](1_glossary.ipynb)
* [3. Positional Astronomy](../3_Positional_Astronomy/3_0_Introduction.ipynb)
    * Previous: [3.1 Equatorial Coordinates (RA,DEC)](../3_Positional_Astronomy/3_1_Equatorial_Coordinates.ipynb)
    * Next: [3.3 Horizontal Coordinates (ALT,AZ)](../3_Positional_Astronomy/3_3_Horizontal_Coordinates.ipynb) 

***

+++

Import standard modules:

```{code-cell} ipython3
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from IPython.display import HTML 
HTML('../style/course.css') #apply general CSS
```

Import section specific modules:

```{code-cell} ipython3
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from IPython.display import HTML 
HTML('../style/course.css') #apply general CSS
```

***

Next: [3.3 Horizontal Coordinates (ALT,AZ)](../3_Positional_Astronomy/3_3_Horizontal_Coordinates.ipynb)

+++

### Glossary and Nomenclature (GM)

+++

Are all the new definition in *italics* when first used in a chapter and described in the glossary. Are the mathematical symbols in nomenclature. Is the basic mathematic style guide followed: 

1. Vector, scalar and matrix:
 * $a, A$ - Denotes a scalar quantity
 * $\mathbf{A}$, $\boldsymbol{\mathcal{A}}$ - Denotes a matrix
 * $\mathbf{a}$ - Denotes a vector

2. $2\times2$-Polarized vs. $N\times N$-Unpolarized matrices: 
 * $\mathbf{A}$ - Denotes a $2\times2$ polarized Jones matrix. Number a Jones matrix
 with any other subscript than $N$.
 * $\boldsymbol{\mathcal{A}}$ - Denotes a $N\times N$ unpolarzed matrix (contain all the unpolarized quantities associated with an array in one matrix).

3. Jones versus Jacobian:
 * Please use $\mathbf{J}$ to denote a Jones matrix and $\mathbb{J}$ to denote a
 Jacobian matrix.

4. Fourier transform:
 * Please use $\mathscr{F}\{\cdot\}$ to denote the Fourier transform. 
 
5. Subscript to avoid ambiguity:
 * If one symbol is used to denote two quantities use a subscript to remove ambiguity. For instance $\lambda$ can mean wavelength or the LM-damping factor. Add a subscript, for
instance $\lambda_{\textrm{LM}}$ now refers to to the LM-damping factor, while $\lambda$ still refers to wavelength. Please add any new subscripted symbol to the glossary.  

The general list of symbols can be found in the [glossary &#10142;](1_glossary.ipynb#preface:sec:glossary).

+++

### Chapter Introduction and Conclusion (CC)

+++

Chapter Introduction:
* Provide an overview of the topics in the chapter.
* Outline of the notebooks in the chapter.
* Include a list of editors and contributors of the chapter.
See [$\S$ 5.0. &#10142;](../5_Imaging/5_0_introduction.ipynb) for exact format. Make sure editors are filled in. Add year to editor name.

Chapter Conclusion:

Should have following sections:
* Summary: Summarizes chapter
* References: All external references
* Further reading: Material not reference but is for enrichment

No good example as everyone does it different.

+++

### Correct labelling (CL)

+++

Make sure that all figure, section, equation and citation strings contain the correct label string format, i.e. `chapterStr:type:uniqueID`. Do they use the correct label string (see [outline &#10142;](0_introduction.ipynb)).

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

+++

### Styling (ST)

+++

Is styling used at all if not it should. Is it used correctly. Where can it be applied.

+++

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

+++

### File Names (FN)

+++

Are the file names in the correct format. Example: `6_1_sky_models.ipynb`. All small letters. Name of section. Single digits if possible.

+++

### Table of Contents (TC)

Check that the table of contents accurately reflects the contents of the chapter you are editing. Also check that the table of content links are working. Please create github issues for TC format errors and assign to Trienko.

+++

### Spelling (SP)

+++

Check spelling. Copy text to some spell-checker.

+++

### General Formatting Comment (XX)

If you have other formatting comments that are not summurazide above. 

+++

## Content Formatting

+++

The main goal of the editors is to consider the quality of the content, each editor should consider these questions and hopefully answer them by the end of editing a section.

* What is the point of the section?
* Is that point clear or could it be presented in a different way?
* Are the examples useful?
* Are there holes or assumptions in the section content which need to be improved?
* What could be added or removed to improve the quality of the section?

When content editing a section add comments by starting with your initials, the formatting tag abbreviation and wrap the comment in a css span tag to color the text so that it sticks out, an example is:
    
```
<span style="background-color:red">GSF:MC:this is the comment text</span>
```

renders as:

<span style="background-color:red">GSF:MC: this is the comment text</span>

We use red and yellow for content comments. Red means that the comment should definitely be implemented by the original author. Yellow means that the comment should be seen as a suggestion only. The different content tags are listed below. Please make github issues for the different editor comments.

+++

### Move Content (MC)

+++

Move content somewhere else. Be specific as to why and to where it should be moved. 

+++

### Re-Write Content (RC)

+++

Content needs to be rewritten as it is written in incorrect language. Or the sentences are not clear. These are the comments that the editors may be able to adress themselves.
You may want to postpone correcting until you finish the chapter.

+++

### Improve Content (IC)

+++

The content is logically flawed and needs to be improved. It is not clear or simple enough for a student to grasp.
Be specifc in your comments.

+++

### Add Content (AC)

+++

Add content. State the reason why.

+++

### Remove Content (EC)

Completely remove the content.

+++

### General Comment (GC)

+++

Add other general comments.

+++

## Additional Information


### Spelling Style

Since we all come from different backgrounds on our spelling stylea we need to formalize the text on one style, we will use the [MNRAS style](http://www.oxfordjournals.org/our_journals/mnras/for_authors/#6.2 Spelling, grammar, punctuation and mathematics) which is essentially British English spelling, e.g. colour instead of color, but uses 'z' in most '-ize' ending words. The specific direction taken from the MNRAS style guide:

> ##### Punctuation 
> Hyphens (one dash in LaTeX) should be used for compound adjectives (e.g. low-density gas, least-squares fit, two-component model). This also applies to simple adjectival units (e.g. 1.5-m telescope, 284.5-nm line), but not to complex units or ranges, which could become cumbersome (e.g. 15 km s–1 feature, 100–200 µm observations). Some words (e.g. time-scale) are always hyphenated as part of journal style (see below). 
> 
> N-rules (two dashes in LaTeX): these are longer than hyphens and are used (i) to separate key words, (ii) as parentheses (e.g. the results – assuming no temperature gradient – are indicative of …), (iii) to denote a range (e.g. 1.6–2.2 µm), and (iv) to denote the joining of two words (e.g. Kolmogorov–Smirnov test, Herbig–Haro object). 
> 
> M-rules (three dashes in TeX/LaTeX) are not used in MNRAS.
> 
> ##### Spelling and grammar 
> Please use British English spellings – e.g. centre not center, labelled not labeled. For words ending in -ise/yse or -ize follow this style: use -ise/yse for devise, surprise, comprise, revise, exercise, analyse; use -ize for recognize, criticize, minimize, emphasize, organize, ionize, polarize, parametrize (note the spelling of this word in particular). 
> 
> ‘None’ is a singular word (none of the stars is a white dwarf), whilst ‘data’ is a plural word (these data show…). 
> 
> Miscellaneous journal spellings: acknowledgements, artefact, best-fitting (not best-fit), disc (except computer disk), haloes (not halos), hotspot, none the less, non-linear, on to, time-scale. 
> 
> For any other spellings, use whichever version is listed first in the Oxford English Dictionary.

### Editor/Author Collaboration

#### 2016

We leave it to the editors and authors on how best to collaborate on incorporating edits and comments into the text. A suggestion is for the editor to send a pull request to the author's github fork. Once the edits are worked out, the author will then do a pull request to the main github repository.

#### 2017

We will be using an edit branch to keep a stable version which can be released to the students. I have created a branch called edit in the ratt-ru repository. So the steps 
to work on this branch is as follow:

* `git fetch upstream`.
* `git checkout edit`.
* `git merge upstream\edit`.
* Make the edits you wish to `edit` branch.
* `git add, commit and push origin edit`.
* Go to local fork edit branch and create a pull request to ratt-ru edit branch.

Only after the authors have corrected the edits will I merge it into the main branch of ratt-ru.

### Editing Attribution

At the introduction of each chapter there is a list of chapter writers and editors. Please add your name to the editor's list, include the particular section number which you edited. We need this so we can keep track of who knows about each section. And, we want to give you recognition for your work.
