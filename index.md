---
title       : Iris Analysis
subtitle    : 
author      : Jordan Cheah
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
ext_widgets: {rCharts: [libraries/nvd3]}
---

## Iris Analysis

This simple program accepts a species of iris, and then display the histogram of sepal length of the iris reactively, i.e. instantly, without the Submit button.

## Data

The data set iris is used in this exercise.

---

## Input: Species

An input box pre-populated with 3 species of iris
* setosa
* versicolor
* virginica

For this exercise, a sample image of iris is also displayed on the side panel.

---

## Ouput: Histogram

A histogram that shows the distribution of Sepal Length for the species.


## How to implement in slidify/R

This code in ui.R creates the input box:
* selectInput("Species", "Choose a species:", choices = c("setosa", "versicolor", "virginica"))

This code in server.R creates a vector of numbers for the selected species:
* Sepal_Length <- iris[iris$Species==input$Species,1]

The vector is then passed to hist to create the histogram:
* hist(Sepal_Length, col = 'skyblue', border = 'white')

---
## Sample embedded R Codes in slidify




```r
1+2
```

```
## [1] 3
```

```r
c(1:10)
```

```
##  [1]  1  2  3  4  5  6  7  8  9 10
```
