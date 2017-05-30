
<!-- README.md is generated from README.Rmd. Please edit that file -->
colformat
=========

[![Travis-CI Build Status](https://travis-ci.org/hadley/colformat.svg?branch=master)](https://travis-ci.org/hadley/colformat)

colformat provides tools for styling columns of data, artfully using colour and unicode characters to

Installation
------------

``` r
# install.packages("devtools")
devtools::install_github("hadley/colformat")
```

Usage
-----

colformat is not designed for end-users but will eventually be incorporated in packages like [tibble](http://tibble.tidyverse.org).

``` r
library(colformat)

x <- 123456789 * (10 ^ c(1, -3, -5, NA, -8, -10))
colformat(x)
#>           title
#> 1234567890     
#>     123457     
#>       1235     
#>         NA     
#>          1.23  
#>          0.0123
```

If you render this in a console that supports colour, you'll see something that looks like this:

<img src="man/figures/colours.png" width="200px" />

Inspirations
------------

-   [TextPlots](https://github.com/sunetos/TextPlots.jl) for use of Braille characters

-   [spark](https://github.com/holman/spark) for use of block characters.

The earliest use of unicode characters to generate sparklines appears to be [from 2009](https://blog.jonudell.net/2009/01/13/fuel-prices-and-pageviews/).

Exercising these ideas to their fullest requires a font with good support for block drawing characters. [PragamataPro](https://www.fsd.it/shop/fonts/pragmatapro/) is one such font.
