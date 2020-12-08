
# Visualizing the Corona (COVID-19) pandemic

#### Where does the data come frome?

The analyses and visualizations are based on the data provided by the
John Hopkins University in the [Official 2019 Novel Coronavirus COVID-19
(2019-nCoV) Data
Repository](https://github.com/CSSEGISandData/COVID-19). The same data
sets are used to constantly update this visual dashboard:
<https://coronavirus.jhu.edu/map.html>

**IMPORTANT DISCLAIMER:** Although I do believe that these data help us
to understand the pandemic, they are nonetheless very imprecise. When we
want to make sense of positive test results (i.e., total cases and in
the long run mortality rates and recovering processes), we need to know
how many tests were conducted (for more information on this, see [this
article](https://www.sciencemag.org/news/2020/03/coronavirus-cases-have-dropped-sharply-south-korea-whats-secret-its-success?fbclid=IwAR3BnhqQMxCdu8-fQelEkWIDQn-j9UASV773Xl-WbIy8l7M5ZVSQpHFgkL8)
in Science).

Furthermore, I would like to emphasize that I am not an expert on
epidemology or virus outbreaks and I am not working in the health
sector. On this page, I am only visualizing the data by the John Hopkins
University. Reliance on the these visualizations for medical guidance or
use of these visualization in commerce is strictly prohibited.

#### Will these figures be updated?

The last update was made on 2020-12-08 08:41:36. The data of the John
Hopkins University, however, are always updated at 23:59. What you see
is hence the situation on 2020-12-07 at 23:59:00. Also bear in mind that
the reporting of cases is somewhat delayed so that it is very likely
that the actual numbers are higher.

## Visualizations

If you are interested in the R code, please see the
[README.rmd](https://github.com/masurp/corona_analyses/blob/master/README.rmd).

### 1\. Examplary patterns

<caption>

(\#tab:unnamed-chunk-2)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country        |    date    |     confirmed |     deaths |    recovered |       active | new\_cases |
| :------------- | :--------: | ------------: | ---------: | -----------: | -----------: | ---------: |
| US             | 2020-12-07 | 14,949,299.00 | 283,703.00 | 5,714,557.00 | 8,951,039.00 | 192,299.00 |
| India          | 2020-12-07 |  9,703,770.00 | 140,958.00 | 9,178,946.00 |   383,866.00 |  26,567.00 |
| Russia         | 2020-12-07 |  2,466,961.00 |  43,122.00 | 1,939,393.00 |   484,446.00 |  27,798.00 |
| France         | 2020-12-07 |  2,349,059.00 |  55,613.00 |   175,919.00 | 2,117,527.00 |   3,411.00 |
| Italy          | 2020-12-07 |  1,742,557.00 |  60,606.00 |   933,132.00 |   748,819.00 |  13,679.00 |
| United Kingdom | 2020-12-07 |  1,742,525.00 |  61,531.00 |     3,747.00 | 1,677,247.00 |  14,774.00 |
| Spain          | 2020-12-07 |  1,702,328.00 |  46,646.00 |   150,376.00 | 1,505,306.00 |  17,681.00 |
| Germany        | 2020-12-07 |  1,200,006.00 |  19,434.00 |   888,701.00 |   291,871.00 |   5,456.00 |
| Netherlands    | 2020-12-07 |    573,750.00 |   9,786.00 |     7,341.00 |   556,623.00 |   7,122.00 |

<img src="figures/unnamed-chunk-3-1.png" width="100%" />

### 2\. Comparing visualizations

### Total cases

One thing that is constantly debatted is how to visualize the growth of
total confirmed cases at all. Log-transform the y-axis or not? Plot
against the date? Plot against days after 100th case? Plot something
entirely different?

Here, I would like to explain some differences between visualizations
that have been used in the media or on Twitter. All of them are helpful
in their own regard.

1.  LEFT: Here, I plotted total cases against days after the 100th cases
    *without* logarithmizing the y-axis.

2.  MIDDLE: The y-axis is logarithmized. This figure is often shown in
    the news.

3.  RIGHT: New cases per 7 days (y-axis) are plotted against total cases
    (x-axis), both axes are logarithmized (Idea explained in this
    [video](https://www.youtube.com/watch?v=54XLXg4fYsc)).

<img src="figures/unnamed-chunk-4-1.png" width="100%" />

*Note:* Green = USA, Blue = Italy, Red = Germany, Pink = Austria, Orange
= United Kingdom

#### Daily new cases

Another visualization that is often used is based on changes in daily
new cases (here averaged cross one or two weeks).

##### Europe

<img src="figures/unnamed-chunk-5-1.png" width="100%" />

##### America

<img src="figures/unnamed-chunk-6-1.png" width="100%" />

##### Middle East

<img src="figures/unnamed-chunk-7-1.png" width="100%" />

##### Asia

<img src="figures/unnamed-chunk-8-1.png" width="100%" />

##### Africa

<img src="figures/unnamed-chunk-9-1.png" width="100%" />
