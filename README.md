
<!-- README.md is generated from README.Rmd. Please edit that file -->

[![Travis build
status](https://travis-ci.org/datalorax/slidex.svg?branch=master)](https://travis-ci.org/datalorax/slidex)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/datalorax/slidex?branch=master&svg=true)](https://ci.appveyor.com/project/datalorax/slidex)
[![Coverage
status](https://codecov.io/gh/datalorax/slidex/branch/master/graph/badge.svg)](https://codecov.io/github/datalorax/slidex?branch=master)
[![CRAN
status](https://www.r-pkg.org/badges/version/slidex)](https://cran.r-project.org/package=slidex)

# slidex

This package is a work-in-progress, but is aimed at making the process
of converting Microsoft PowerPoint slides to beautiful HTML
[xaringan](https://github.com/yihui/xaringan) slides as seamless as
possible, maintaining tables,figures, links, and bulleted lists.

## Installation

The package is not yet on CRAN. Install the development version with

``` r
devtools::install_github("datalorax/slidex")
```

## Basic usage

At present, the package exports a single function, `convert_pptx`, which
takes two required argument: the `path` to the PPTX file (passed as a
string), and the `author` (also passed as a sting). For example:

``` r
library(slidex)
convert_pptx(path = "inst/examples/slidedemo.pptx",
             author = "Daniel Anderson")
```

You can optionally pass additional arguments, such as `theme` (see a
list of themes
[here](https://github.com/yihui/xaringan/tree/master/inst/rmarkdown/templates/xaringan/resources))
or a new
`title`.

![](https://github.com/datalorax/slidex/raw/master/docs/slidex-preview.gif)

## Suggested pacakges

Although not a dependency, the package functionally requires the
[xaringan](https://github.com/yihui/xaringan) package, and works best if
both the [knitr](https://github.com/yihui/knitr) and
[kableExtra](https://github.com/haozhu233/kableExtra) packages are
installed. Without the latter two, tables will not be produced, although
the code to create a dataframe from the tables will still be embedded.
