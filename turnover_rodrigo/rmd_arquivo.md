TurnOver v2
================
Rafael Barbosa & Rodrigo Almeida
06/04/2020

# Pacotes do R

``` r
require(tidyverse)
require(kableExtra)

dados <- read.csv(file = "data/turnover-data-set.csv")

dados %>% 
  head %>% 
  kbl %>% 
  kable_styling(bootstrap_options = c("striped", "hover", "condensed", "responsive"))
```

<table class="table table-striped table-hover table-condensed table-responsive" style="margin-left: auto; margin-right: auto;">

<thead>

<tr>

<th style="text-align:right;">

stag

</th>

<th style="text-align:right;">

event

</th>

<th style="text-align:left;">

gender

</th>

<th style="text-align:right;">

age

</th>

<th style="text-align:left;">

industry

</th>

<th style="text-align:left;">

profession

</th>

<th style="text-align:left;">

traffic

</th>

<th style="text-align:left;">

coach

</th>

<th style="text-align:left;">

head\_gender

</th>

<th style="text-align:left;">

greywage

</th>

<th style="text-align:left;">

way

</th>

<th style="text-align:right;">

extraversion

</th>

<th style="text-align:right;">

independ

</th>

<th style="text-align:right;">

selfcontrol

</th>

<th style="text-align:right;">

anxiety

</th>

<th style="text-align:right;">

novator

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:right;">

7.030801

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:right;">

35

</td>

<td style="text-align:left;">

Banks

</td>

<td style="text-align:left;">

HR

</td>

<td style="text-align:left;">

rabrecNErab

</td>

<td style="text-align:left;">

no

</td>

<td style="text-align:left;">

f

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

4.1

</td>

<td style="text-align:right;">

5.7

</td>

<td style="text-align:right;">

7.1

</td>

<td style="text-align:right;">

8.3

</td>

</tr>

<tr>

<td style="text-align:right;">

22.965092

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:right;">

33

</td>

<td style="text-align:left;">

Banks

</td>

<td style="text-align:left;">

HR

</td>

<td style="text-align:left;">

empjs

</td>

<td style="text-align:left;">

no

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

4.1

</td>

<td style="text-align:right;">

5.7

</td>

<td style="text-align:right;">

7.1

</td>

<td style="text-align:right;">

8.3

</td>

</tr>

<tr>

<td style="text-align:right;">

15.934292

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

f

</td>

<td style="text-align:right;">

35

</td>

<td style="text-align:left;">

PowerGeneration

</td>

<td style="text-align:left;">

HR

</td>

<td style="text-align:left;">

rabrecNErab

</td>

<td style="text-align:left;">

no

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

2.6

</td>

<td style="text-align:right;">

4.8

</td>

<td style="text-align:right;">

8.3

</td>

</tr>

<tr>

<td style="text-align:right;">

15.934292

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

f

</td>

<td style="text-align:right;">

35

</td>

<td style="text-align:left;">

PowerGeneration

</td>

<td style="text-align:left;">

HR

</td>

<td style="text-align:left;">

rabrecNErab

</td>

<td style="text-align:left;">

no

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

5.4

</td>

<td style="text-align:right;">

7.6

</td>

<td style="text-align:right;">

4.9

</td>

<td style="text-align:right;">

2.5

</td>

<td style="text-align:right;">

6.7

</td>

</tr>

<tr>

<td style="text-align:right;">

8.410678

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:right;">

32

</td>

<td style="text-align:left;">

Retail

</td>

<td style="text-align:left;">

Commercial

</td>

<td style="text-align:left;">

youjs

</td>

<td style="text-align:left;">

yes

</td>

<td style="text-align:left;">

f

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

3.0

</td>

<td style="text-align:right;">

4.1

</td>

<td style="text-align:right;">

8.0

</td>

<td style="text-align:right;">

7.1

</td>

<td style="text-align:right;">

3.7

</td>

</tr>

<tr>

<td style="text-align:right;">

8.969199

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

f

</td>

<td style="text-align:right;">

42

</td>

<td style="text-align:left;">

manufacture

</td>

<td style="text-align:left;">

HR

</td>

<td style="text-align:left;">

empjs

</td>

<td style="text-align:left;">

yes

</td>

<td style="text-align:left;">

m

</td>

<td style="text-align:left;">

white

</td>

<td style="text-align:left;">

bus

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

6.2

</td>

<td style="text-align:right;">

4.1

</td>

<td style="text-align:right;">

5.6

</td>

<td style="text-align:right;">

6.7

</td>

</tr>

</tbody>

</table>

# Introdução ao TurnOver
