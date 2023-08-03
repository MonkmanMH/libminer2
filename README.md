
<!-- README.md is generated from README.Rmd. Please edit that file -->

# libminer2

<!-- badges: start -->
<!-- badges: end -->

The goal of libminer2 is to provide a summary of a user’s R libraries.
It’s a toy package developed in a workshop taught by Andy Teucher on
2023-08-03.

## Installation

You can install the development version of libminer2 from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("MonkmanMH/libminer2")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(libminer2)
## basic example code

lib_summary()
#>                                                               library
#> 1                                  C:/Program Files/R/R-4.3.1/library
#> 2                      C:/Users/marti/AppData/Local/R/win-library/4.3
#> 3 C:/Users/marti/AppData/Local/Temp/RtmpgncejI/temp_libpath4ae4691ad0
#>   n_packages
#> 1         30
#> 2        200
#> 3          1

# you can also ask it to calculate the sizes 

lib_summary(sizes = TRUE)
#>                                                               library
#> 1                                  C:/Program Files/R/R-4.3.1/library
#> 2                      C:/Users/marti/AppData/Local/R/win-library/4.3
#> 3 C:/Users/marti/AppData/Local/Temp/RtmpgncejI/temp_libpath4ae4691ad0
#>   n_packages  lib_size
#> 1         30  68858812
#> 2        200 614077127
#> 3          1     17125
```

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
summary(cars)
#>      speed           dist       
#>  Min.   : 4.0   Min.   :  2.00  
#>  1st Qu.:12.0   1st Qu.: 26.00  
#>  Median :15.0   Median : 36.00  
#>  Mean   :15.4   Mean   : 42.98  
#>  3rd Qu.:19.0   3rd Qu.: 56.00  
#>  Max.   :25.0   Max.   :120.00
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date. `devtools::build_readme()` is handy for this.
