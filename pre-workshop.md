---
layout: default
title: Pre-Workshop Activities
nav_order: 2
---
## Pre-Workshop Videos & Activities

This workshop is primarily hands-on practice with RStudio in order to learn to use key features of the software. To participate fully please do the following **before the workshop**:

### Download & Install R then RStudio

-   Mac Installation
    -   [Mac Installation Video](https://youtu.be/dRkAvBz9Ibc){:target="_blank"} (3 min)
        <iframe width="560" height="315" src="https://www.youtube.com/embed/dRkAvBz9Ibc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    -   [Mac R Download](https://bit.ly/dsc-r-mac){:target="_blank"}
    -   [RStudio Desktop Download](http://bit.ly/dsc-rstudio-down){:target="_blank"}
-   Windows Installation
    -   [Windows 10 Installation Video](https://youtu.be/HqrqRMnK4XA){:target="_blank"} (3 min)
        <iframe width="560" height="315" src="https://www.youtube.com/embed/HqrqRMnK4XA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    -   [Windows R Download](http://bit.ly/dsc-r-win){:target="_blank"}
    -   [RStudio Desktop Download](http://bit.ly/dsc-rstudio-down){:target="_blank"}
 
### Install RMarkdown and LaTeX

In this workshop, we will be using R Markdown documents to write our script and produce the outputs of our analysis. We will explain what R Markdown is in the first section of the workshop, but before we start, make sure you have the package downloaded. For that, open RStudio, and type in the console:
```
install.packages("rmarkdown")
```

R Markdown documents can be exported (or "knitted") into .html, .docx, or .pdf formats. However, to knit them into .pdf files, you also need to have LaTeX installed on your computer. LaTeX is a system for preparing documents, and it has its own language. Luckily, you won't need to learn LaTeX to use it with R Markdown, as R Markdown takes care of everything in the background. You just need to install it, which you can do if you type it in the console:

```
install.packages("tinytex")
tinytex::install_tinytex()
```
If you see the following message, enter 'N' and continue to the next step.
```
tinytex::install_tinytex()
Found '/usr/local/bin/tlmgr', which indicates a LaTeX distribution may have existed in the system.
Continue the installation anyway? (Y/N) N
```

If you want to know more about LaTeX, you can check our [Introduction to LaTeX](https://uviclibraries.github.io/latex/){:target="_blank"} workshop.

[NEXT STEP: Introduction to Hands-On Activities](activities-intro.html){: .btn .btn-blue }
