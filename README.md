
<!-- README.md is generated from README.Rmd. Please edit that file -->

# processmapR <a href="https://bupaverse.github.io/processmapR/"><img src="man/figures/logo.png" align="right" height="50" /></a>

<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/processmapR)](https://CRAN.R-project.org/package=processmapR)
[![GitHub
version](https://img.shields.io/badge/GitHub-0.5.2-blue)](https://github.com/bupaverse/processmapR)
[![R-CMD-check](https://github.com/bupaverse/processmapR/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/bupaverse/processmapR/actions/workflows/R-CMD-check.yaml)
[![codecov](https://codecov.io/gh/bupaverse/processmapR/branch/master/graph/badge.svg)](https://app.codecov.io/gh/bupaverse/processmapR?branch=master)
[![Lifecycle:
stable](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable)
<!-- badges: end -->

**processmapR** is a [`R`](https://www.r-project.org/) package for
creating process maps. Part of the [bupaR](https://www.bupar.net/)
eco-system for business process analysis.

## Installation

You can install **processmapR** from [CRAN](https://cran.r-project.org/)
with:

``` r
install.packages("processmapR")
```

### Development Version

You can install the development version of **processmapR** from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("bupaverse/processmapR")
```

## Example

The [bupaR Documentation](https://bupar.net/processmaps.html) website
contains more details on creating process maps using **processmapR**.

``` r
library(processmapR)
#> 
#> Attaching package: 'processmapR'
#> The following object is masked from 'package:stats':
#> 
#>     frequency
library(bupaR)
#> 
#> Attaching package: 'bupaR'
#> The following object is masked from 'package:stats':
#> 
#>     filter
#> The following object is masked from 'package:utils':
#> 
#>     timestamp

# Process map
patients %>%
  process_map()
```

![process map](man/figures/README-example1-1.png)

``` r
# Dotted chart
patients %>%
  dotted_chart(x = "absolute", sort = "start")
```

<img src="man/figures/README-example2-1.png" width="100%" />
