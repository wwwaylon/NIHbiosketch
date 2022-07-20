# RmdNIHbio - Easily create your biosketch

This is an NIH biosketch tool written with [R Markdown](https://rmarkdown.rstudio.com/), integrated with content coming from Excel (.XLSX) and exported as a Word (.DOCX) document.


#### Note: The work on this app has focused on automating an NIH biosketch. 

- [What does RmdNIHbio do?](#what-does-RmdNIHbio-do)
- [But, why?](#buy-why)
- [How do I use this?](#how-do-i-use-this)
- [Current features](#current-features)
- [Future features](#future-features)
- [Feedback](#feedback)
- [Notes](#notes)

#### What does `RmdNIHbio` do?

The idea of `RmdNIHbio` is to let you create and share your NIH formatted biosketch as a Word document, *formatted* and populated easily within R Markdown.    

#### But, why?

Efficientcy. A biographical sketch (also referred to as biosketch) documents an individual's qualifications and experience for a specific role in a project. NIH requires submission of a biosketch for each proposed senior/key personnel and other significant contributor on a grant application. I've genrated numerous biosketches for grant submissions and used lots of time searching for a template, updating a previous version (hoping I've located the most recent version) and just needed a *free* solution that could easily update.   

#### How do I use this?

First, clone `nih_template.docx` and `nih_template.Rmd` into the working directory where your R Markdown will be rendered. Next, clone the supporting files (`mydata.xlsx`).  

Then open the template file in [RStudio](https://www.rstudio.com/), and load the required libraries.  

```
library(scholar)
library(tidyverse)
library(flextable)
library(officer)
```

After confirming the libraries update the file directory.  

```
###--------------------------- Update with your Google Scholar ID ------------------------------###
myid <- "wUACzXkAAAAJ&hl"
```

Follow Google Scholar’s instructions for obtaining an ID:
>A primer on creating and modifying your Google Scholar account can be found at 
https://scholar.google.com/intl/en/scholar/citations.html.

```
###------------------------ Update the location of the supporting files-------------------------###
C:/Users/whowar/Desktop/biosketch/2021_01_WJH/positions-honors-nih.xlsx

```

That's all the changes you need. Now you can update data in the supporting files and generate your biosketch by simply selecting the blue 'Knit' button at the top left of the console pane. 

Of course you could put more stuff in the R Markdown template or improve the design, but this is the beauty of it, the data and tables are all modifyable. 

#### Current features

- Reads data from a local file (i.e., mydata.xlsx)
- Can add additional data from Google Scholar 
- Includes automated NIH-biosketch formatting  
- Can customize tables and data 
- Exports as a Word document (fully editable) 

#### Future features

New features may include reading the supporting files from a remote API (such as from orcid.org), streamlining code for efficiency, and other ideas that you come up with. 

#### Feedback

If you think you could have a use for `RmdNIHbio`, please do <a href="mailto:waylon.howard@seattlechildrens.org">let me know</a> or [update the code yourself](https://childrens-atlassian/bitbucket). Don't be shy!

#### Notes

Per typical - please don't look at the code too closely, it's hideous! This was done on and off over time without a large block of time so it needs to be cleaned up quite a bit. I'm completely open for input.
