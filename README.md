
<!-- README.md is generated from README.Rmd. Please edit that file -->
dataplotr
=========

This package mainly contains wrapper functions for ggplot2.

Installation
------------

You can install dataplotr from github with:

``` r
# install.packages("devtools")
devtools::install_github("aotearoastats/dataplotr")
```

plot\_barplot
-------------

Plot\_barplot plots simple barplots with the option to add a grid. See `?plot_barplot` for documentation.

``` r
library(dataplotr)
library(dplyr)
iris.plot <- iris %>% 
  group_by(Species) %>% 
  summarize(Sepal.Length=mean(Sepal.Length))

plot_barplot(iris.plot,
             main_title="Sepal.Length by Species on the Iris Data Set",
             x_var = "Species",
             y_var = "Sepal.Length",
             fill_title = "Species",
             fill_vars = "Species",
             colour_vars = "rev(Species)")
```

![](README-plot_barplot_exampe-1.png)
