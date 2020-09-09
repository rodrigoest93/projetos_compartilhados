TurnOver v2
================
Rafael Barbosa & Rodrigo Almeida
06/04/2020

``` r
require(tidyverse)
require(kabl)

dados <- read.csv(file = "data/turnover-data-set.csv")

dados %>% 
  head %>% 
  knitr::kable()
```

|      stag | event | gender | age | industry        | profession | traffic     | coach | head\_gender | greywage | way | extraversion | independ | selfcontrol | anxiety | novator |
| --------: | ----: | :----- | --: | :-------------- | :--------- | :---------- | :---- | :----------- | :------- | :-- | -----------: | -------: | ----------: | ------: | ------: |
|  7.030801 |     1 | m      |  35 | Banks           | HR         | rabrecNErab | no    | f            | white    | bus |          6.2 |      4.1 |         5.7 |     7.1 |     8.3 |
| 22.965092 |     1 | m      |  33 | Banks           | HR         | empjs       | no    | m            | white    | bus |          6.2 |      4.1 |         5.7 |     7.1 |     8.3 |
| 15.934292 |     1 | f      |  35 | PowerGeneration | HR         | rabrecNErab | no    | m            | white    | bus |          6.2 |      6.2 |         2.6 |     4.8 |     8.3 |
| 15.934292 |     1 | f      |  35 | PowerGeneration | HR         | rabrecNErab | no    | m            | white    | bus |          5.4 |      7.6 |         4.9 |     2.5 |     6.7 |
|  8.410678 |     1 | m      |  32 | Retail          | Commercial | youjs       | yes   | f            | white    | bus |          3.0 |      4.1 |         8.0 |     7.1 |     3.7 |
|  8.969199 |     1 | f      |  42 | manufacture     | HR         | empjs       | yes   | m            | white    | bus |          6.2 |      6.2 |         4.1 |     5.6 |     6.7 |
