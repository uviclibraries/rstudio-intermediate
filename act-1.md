---
layout: default
title: 1-R Markdown
nav_order: 2
parent: Workshop Activities
---

# Generate Reports With R Markdown

<img>

Tips before you start. If you haven’t done so already, please do the following:
-   Pull up documentation for a function by executing `?function` in the Console.
-   Install LaTeX in RStudio:
    ```
    install.packages('tinytex')
    tinytex::install_tinytex()
    ```
-   [RMarkdown Cheat Sheet](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf){:target="_blank"}

We will create a report as a PDF file. The process is similar for html or docx documents.
-   Open RStudio, click **File -> New File -> RMarkdown...**
-   Enter title, author, and select the type of output format **PDF** and click **OK**
-   The Markdown document with some example code will appear on your Editor window.

    <img src="images/act-1/icon.png" alt="small icon" style="float:right;width:120px;">

-   Click the **Knit** icon in the toolbar (see right). A PDF file is now generated and saved to the current folder/directory.
-   Continue editing this R Markdown document for other Activities.
-   RStudio has a handy [cheat sheet for RMarkdown.](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf){:target="_blank"}

[NEXT STEP: Tests For Difference in Means (t-tests, ANOVA)](act-2.html){: .btn .btn-blue }
