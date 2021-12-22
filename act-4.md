---
layout: default
title: 4-RShiny (Optional)
nav_order: 5
parent: Workshop Activities
---

# OPTIONAL: Interactive Data Dashboard With RShiny

<img>

In this activity, we build a data visualization dashboard with the package `shiny`

1.  **Introduction**

    -   Install the package:
    
        ```
        install.packages("shiny")
        library(shiny)
        ```
    
    -   Shiny apps are contained in a single script app.R which has three components:
    
        -   A user interface (ui) that contains the layout of the Shiny dashboard
        -   A server (server) that contains the code to manipulate data and create graphs
        -   A function to combine these two previous components
            
            <img>
        
        The Shiny package contains a few examples which display both the dashboards and the app.R scripts to create them. In practice, we don’t need to display the actual script as a part of the dashboard. Let’s give each of these a try. Exit each Shiny app by closing its window or hitting Escape on the keyboard.
        
        ```
        runExample("01_hello")
        runExample("02_text")
        ```
    
    -   Create a new `app.R` file containing this basic setup:
        
        ```
        library(shiny)
        
        # Define UI ----
        ui <- fluidPage(
        
        )
        
        # Define server logic ----
        server <- function(input, output) {
        
        }
        
        # Run the app ----
        shinyApp(ui = ui, server = server)
        ```

2.  **Build a user interface**

    -   We will build a basic dashboard to display data from the Life Expectancy dataset.
    -   First, add a few elements to the user interface: a title panel on the top, a sidebar panel on the left, a main panel on the right.
    
        ```
        ui <- fluidPage(
            titlePanel("WHO Life Expectancy"),
            
            sidebarLayout(
                sidebarPanel(
                    h3("This is the sidebar title"),
                    p("This is the sidebar body")
                    ),
                    mainPanel("This is the main panel, draw graphs here")
                )
            )
        ```
        
        Click on Run App or run runapp() command to start the application.
    
    -   The sidebar is often used for choosing inputs for the graphs. Here we will choose the year of the data (2015, 2010, or 2005). Based on this selection, we will filter the Life Expectancy dataset by the selected year.
        
        ```
        ui <- fluidPage(
            titlePanel("WHO Life Expectancy"),
            
            sidebarLayout(
                sidebarPanel(
                    selectInput("year",
                                label = "Choose a year to display",
                                choices = list("2015",
                                               "2010",
                                               "2005"),
                                selected = "2015"
                    ),
                    mainPanel("This is the main panel, draw graphs here")
                )
            )
        ```
        **DOUBLE CHECK CODE**
        
        Run the app to see what it now looks like.
        
    -   Add t **NEEDS WORK**
    -   Get the 95% confidence interval for the coefficient estimates.
        
        ```
        confint(lm_schooling)
        ```

    -   Linear regression makes several assumptions about the data:

        _Linearity of the data & constant variance:_ we want to check the Residuals vs Fitted plot for no pattern, the red line should be fairly flat, the points should be equally scattered.
        
        ```
        plot(lm_schooling, 1)
        ```
        
        _Normality:_ points should be close to the line in the Normal Q-Q plot.
        
        ```
        plot(lm_schooling, 2)
        ```
        
        Overall the assumptions are met. However, there are a few outliers seen in the Schooling vs. Life expectancy plot. We may want to examine these data points in further analysis.

3.  **NEEDS TEXT**

    -   We want to expand our model to consider an additional factor, BMI.
        
        ```
        plot(select(life_expectancy_2015, one_of(c("Life expectancy", "BMI", "Schooling"))))
        ```
        
        From the plot, BMI doesn’t look as good as Schooling as a predictor of Life expectancy. But we will go ahead and fit a multiple regression model to have a concrete result.
        
    -   Create a multiple linear regression model where the response variable is Life expectancy and the independent variables are BMI and Schooling. The model can be written as:
        Life expectancy = slope_1 * BMI + slope_2 * Schooling + intercept
        
        **In R:**
        
        ```
        lm_multiple <- lm(life_expectancy_2015$`Life expectancy` ~ life_expectancy_2015$Schooling + life_expectancy_2015$BMI, data=life_expectancy_2015)
        summary(lm_multiple)
        ```
        
        <img>
        
        As we thought, BMI is not a significant variable with a p-value of 0.234. The model is still significant however, with p-value of 2.2e^-16, because Schooling is included. We conclude that the simple regression model adequately fits the data. For the sake of completeness, the multiple regression model can be written as:
        
        Life expectancy = 2.16981 * Schooling + 0.02442 * GDP + 42.57196
        
    -   Similar to the simple model, this command produces graphs to check the model assumptions.
        
        ```
        plot(lm_multiple)
        ```

4.  Conduct a single or multiple regression analysis with other variables of your choosing. Make a scatter plot to visualize their linear relationship, build a model and assess the results. Let the instructors know if you need help!

[NEXT STEP: Earn a Workshop Badge](informal-credentials.html){: .btn .btn-blue }
