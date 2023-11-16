---
title: "Data Products Project: MTCar Data"
author: "Author: Isaac G. Veras"
date: "October 05, 2023"
output: ioslides_presentation
---

```{r setup, include = FALSE}
knitr::opts_chunk$set(echo = FALSE)
```

## Understanding Gas Mileage

Using the `mtcars` dataset we plotted, we can try to understand the relationship of factors to fuel consumption (`mpg`).

The weight (`wt`) versus the mileage (`mpg`) along the x/y axes. The number of cylinders (`cyl`) as colors and the amount of power (`hp`) as the size of an individual point on the graph.

## Visualizing the MTCar Data:

```{r plot, warning = FALSE}
suppressPackageStartupMessages(library(plotly))
plot_ly(
        data  = mtcars,
        x     = ~wt,
        y     = ~mpg,
        color = ~as.factor(cyl),
        size  = ~hp,
        text  = ~paste("Weight: ", wt, '<br>MPG:', mpg),
        type  = "scatter",
        mode  = "markers"
) %>%
        layout(title = "MTCar Data")
```
![1](https://github.com/i544c/Data_Products_Project2/assets/104391905/4360badf-f2d1-4635-baaa-0039afdb92fd)


![2](https://github.com/i544c/Data_Products_Project2/assets/104391905/9bec5c3c-f163-4c1f-9ef9-08a94738152c)


![3](https://github.com/i544c/Data_Products_Project2/assets/104391905/251462b7-99a8-4eef-a368-060273cc790d)


