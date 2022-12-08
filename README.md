# The `rpart` package <img src="man/figures/rpart.png" alt="Rpart logo" style="float:right;height:232.25px" align="right" height="232.25"/>

[![CRAN_STATUS_BADGE](http://www.r-pkg.org/badges/version/rpart)](https://CRAN.R-project.org/package=rpart) [![Downloads](http://cranlogs.r-pkg.org/badges/rpart)](https://CRAN.R-project.org/package=rpart) [![Travis-CI Build Status](https://travis-ci.org/bethatkinson/rpart.svg?branch=master)](https://travis-ci.org/bethatkinson/rpart)

## Pkgdown Website

Original package Github link: <https://github.com/bethatkinson/rpart>

Deployed website link:

5 customizations to website: (1) Bootswatch theme (lux), (2) Code font (Roboto Mono), (3) Navigation bar height (100px), (4) Navigation bar structure, (5) Color for syntax highlighting (breeze-light).

This package is called rpart and is by Terry Therneau, Beth Atkinson, and Brian Ripley. The pkgdown website was created by Carly Lupton Brantner. This package is described more by the authors in the below overview. Exported functions include rpart, which fits a regression tree; prune, which prunes the tree; print, which prints the Rpart object; and printcp, which displays a CP table for an Rpart object. An example of the rpart function is below.

## Overview

The `rpart` code builds classification or regression models of a very general structure using a two stage procedure; the resulting models can be represented as binary trees. The package implements many of the ideas found in the CART (Classification and Regression Trees) book and programs of Breiman, Friedman, Olshen and Stone. Because CART is the trademarked name of a particular software implementation of these ideas and `tree` was used for the Splus routines of Clark and Pregibon, a different acronym - Recursive PARTitioning or rpart - was chosen.

## Example

```{r}
set.seed(10)
fit <- rpart(mpg ~ factor(cyl) + disp + hp + drat + wt + factor(gear),
             data = mtcars)
par(mfrow = c(1,2), xpd = NA) # otherwise on some devices the text is clipped
plot(fit)
text(fit, use.n = TRUE)
```
