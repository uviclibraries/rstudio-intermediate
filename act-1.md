---
layout: default
title: 1-R Markdown
nav_order: 2
parent: Workshop Activities
---

# Generate Reports With R Markdown

Tips before you start. If you haven’t done so already, please do the following:
-   Pull up documentation for a function by executing `?function` in the Console.
-   Install LaTeX in RStudio:
    ```
    install.packages('tinytex')
    tinytex::install_tinytex()
    ```

1. Read parts 1 - 6 of the [RMarkdown Cheat Sheet](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf){:target="_blank"}
2. For the rest of the workshop, we will save our code on a R Markdown file. Let's create this file in RStudio. The steps are similar to described in the cheatsheet.
-   Open RStudio, click **File -> New File -> RMarkdown...**
-   Enter title, author, and select the type of output format **PDF** and click **OK**
-   After creating your R Markdown file, you must save it. Click **File -> Save As ->...** Enter the filename and make sure to remember where you saved it.
-   The Markdown document with some example code will appear on your Editor window.

    <img src="images/act-1/icon.png" alt="small icon" style="float:right;width:120px;">

-   Click the **Knit** icon in the toolbar (see right). A PDF file is now generated and saved to the current folder/directory.
-   Continue editing this R Markdown document for other Activities.

[NEXT STEP: Tests For Difference in Means (t-tests, ANOVA)](act-2.html){: .btn .btn-blue }
