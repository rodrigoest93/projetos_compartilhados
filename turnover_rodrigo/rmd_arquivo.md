TurnOver v2
================
**Autores:** Rodrigo Almeida & Rafael Barbosa | **Data:**
06/04/2020

![Image of
Yaktocat](https://www.nvoip.com.br/wp-content/uploads/2018/09/turnover_face.png)

## 1\. Introdução ao TurnOver

  - Escrever algo aqui sobre o TurnOver

## 2\. R e Rstudio

<p align="center">

<img alt="decision_tree" src="images/r_and_rstudio.png" alt="drawing" width="400" height="200"/>
<br> <em> <span>Disponível
<a href="https://bcrf.biochem.wisc.edu/all-tutorials/tutorial-materials-r-rstudio/">aqui</a></span>
</em>

</p>

  - Escrever algo aqui sobre o R e o Rstudio

### 2.1. Pacotes utilizados

``` r
require(tidyverse)
require(kableExtra)
```

### 2.2. Importação dos dados

  - Escrever algo?

<!-- end list -->

``` r
dados <- read.csv(file = "data/turnover-data-set.csv")

dados %>% 
  head %>% 
  kbl %>% 
  kable_classic(full_width = T, html_font = "Arial") %>% 
  kable_styling(bootstrap_options = c("striped", "hover", "condensed", "responsive", position = "center"))
```

<table class=" lightable-classic table table-striped table-hover table-condensed table-responsive" style="font-family: Arial; margin-left: auto; margin-right: auto; margin-left: auto; margin-right: auto;">

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

### 2.3. Glossário das variáveis

  - **stag**: experiência (em anos ou meses)
  - **event**: demitido ou não
  - **gender**: gênero
  - **age**: idade
  - **industry**: tipo de indústria
  - **profession**: setor em que trabalha
  - **traffic**: meio em que o candidato se candidatou
  - **coach**: presença de um **buddy**
  - **head\_gender**: gênero do seu **buddy**
  - **greywage**: algo relacionado com taxas para o governo
  - **way**: meio de transporte para o trabalho
  - **extraversion**, **independ**, **selfcontrol**, **anxiety**,
    **novator**: Escala de teste Big5

## 3\. Análise Exploratória de Dados

### 3.1. Estrutura dos dados

<p align="center">

<img alt="decision_tree" src="images/exploratory.jpg" alt="drawing" width="600" height="400"/>
<br> <em> <span>Foto por
<a href="https://unsplash.com/@marcobias?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Marco
Biasibetti</a> em
<a href="https://unsplash.com/s/photos/explorator?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>
</em>

</p>

``` r
dados %>% 
  str %>% 
  kbl %>% 
  kable_classic(full_width = T, html_font = "Arial") %>% 
  kable_styling(bootstrap_options = c("striped", "hover", "condensed", "responsive", position = "center"))
```

    ## 'data.frame':    1129 obs. of  16 variables:
    ##  $ stag        : num  7.03 22.97 15.93 15.93 8.41 ...
    ##  $ event       : int  1 1 1 1 1 1 1 1 1 1 ...
    ##  $ gender      : chr  "m" "m" "f" "f" ...
    ##  $ age         : num  35 33 35 35 32 42 42 28 29 30 ...
    ##  $ industry    : chr  "Banks" "Banks" "PowerGeneration" "PowerGeneration" ...
    ##  $ profession  : chr  "HR" "HR" "HR" "HR" ...
    ##  $ traffic     : chr  "rabrecNErab" "empjs" "rabrecNErab" "rabrecNErab" ...
    ##  $ coach       : chr  "no" "no" "no" "no" ...
    ##  $ head_gender : chr  "f" "m" "m" "m" ...
    ##  $ greywage    : chr  "white" "white" "white" "white" ...
    ##  $ way         : chr  "bus" "bus" "bus" "bus" ...
    ##  $ extraversion: num  6.2 6.2 6.2 5.4 3 6.2 6.2 3.8 8.6 5.4 ...
    ##  $ independ    : num  4.1 4.1 6.2 7.6 4.1 6.2 6.2 5.5 6.9 5.5 ...
    ##  $ selfcontrol : num  5.7 5.7 2.6 4.9 8 4.1 4.1 8 2.6 3.3 ...
    ##  $ anxiety     : num  7.1 7.1 4.8 2.5 7.1 5.6 5.6 4 4 7.9 ...
    ##  $ novator     : num  8.3 8.3 8.3 6.7 3.7 6.7 6.7 4.4 7.5 8.3 ...

<table class=" lightable-classic table table-striped table-hover table-condensed table-responsive" style="font-family: Arial; margin-left: auto; margin-right: auto; margin-left: auto; margin-right: auto;">

<tbody>

<tr>

</tr>

</tbody>

</table>
