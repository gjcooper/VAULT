# Watercolours

An [[R]] package for providing colour palettes based on specific paintings by well known watercolur painting artists. The [home page](https://github.com/gjcooper/watercolours#readme)contains several examples of its use and images of each of the currently available palettes.

## Examples

``` r
library(ggplot2)
ggplot(diamonds, aes(color, fill = clarity)) +
  geom_bar() +
  scale_fill_watercolour(palette = "durer")
```


``` r
ggplot(mtcars, aes(disp, mpg, col = qsec)) +
  geom_point(size = 4) +
  scale_color_watercolour(type = "continuous")
```

### The available palettes are

Anders Zorn - [*Sommarnöje*](https://commons.wikimedia.org/wiki/File:Sommarn%C3%B6je_(1886),_akvarell_av_Anders_Zorn.jpg) (1886)

``` r
show_palette("zorn")
```

Fidelia Bridges - [*Calla Lilly*](https://commons.wikimedia.org/wiki/File:Brooklyn_Museum_-_Calla_Lily_-_Fidelia_Bridges_-_overall.jpg) (1875)

``` r
show_palette("bridges")
```

Dolla Richmond -[*Mount Egmont*](https://artsandculture.google.com/asset/mount-egmont/2AH3LhLcXldhDA)

``` r
show_palette("richmond")
```

Albrecht Durer - [*Wing of a Blue Roller*](https://commons.wikimedia.org/wiki/File:Duerer_wing_of_a_blue_roller.jpg)

``` r
show_palette("durer")
```

## Installation

You can install `watercolours` from github with:

``` r
devtools::install_github("gjcooper/watercolours")
```
