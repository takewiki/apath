# apath

[Path component](https://github.com/protyze/aframe-alongpath-component) for [aframer](http://aframer.john-coene.com/)

## Installation

``` r
# install.packages("devtools")
devtools::install_github("JohnCoene/apath")
```

## Example

``` r
library(aframer)
library(acurve)
library(apath)

embed_aframe(
  a_scene(
    a_dependency(),
    acurve_dependency(),
    apath_dependency(),
    a_curve(
      id = "track1",
      a_curve_point(position = "-2 2 -3"),
      a_curve_point(position = "0 1 -3"),
      a_curve_point(position = "2 2 -3")
    ),
    a_box(
      alongpath = opts_aframe(
        curve = "#track1",
        dur = 5000,
        loop = TRUE
      ), 
      color = "blue"
    )
  )
)
```

