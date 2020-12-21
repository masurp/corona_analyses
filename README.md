
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

The last update was made on 2020-12-21 11:34:34. The data of the John
Hopkins University, however, are always updated at 23:59. What you see
is hence the situation on 2020-12-20 at 23:59:00. Also bear in mind that
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

| country        |    date    |     confirmed |     deaths |    recovered |        active | new\_cases |
| :------------- | :--------: | ------------: | ---------: | -----------: | ------------: | ---------: |
| US             | 2020-12-20 | 17,844,690.00 | 317,668.00 |         0.00 | 17,527,022.00 | 189,099.00 |
| India          | 2020-12-20 | 10,055,560.00 | 145,810.00 | 9,606,111.00 |    303,639.00 |  24,337.00 |
| Russia         | 2020-12-20 |  2,821,125.00 |  50,242.00 | 2,253,826.00 |    517,057.00 |  28,510.00 |
| France         | 2020-12-20 |  2,529,756.00 |  60,665.00 |   189,638.00 |  2,279,453.00 |  12,799.00 |
| United Kingdom | 2020-12-20 |  2,046,161.00 |  67,503.00 |     4,375.00 |  1,974,283.00 |  36,084.00 |
| Italy          | 2020-12-20 |  1,953,185.00 |  68,799.00 | 1,261,626.00 |    622,760.00 |  15,102.00 |
| Spain          | 2020-12-20 |  1,797,236.00 |  48,926.00 |   150,376.00 |  1,597,934.00 |       0.00 |
| Germany        | 2020-12-20 |  1,514,962.00 |  26,400.00 | 1,123,725.00 |    364,837.00 |   6,444.00 |
| Netherlands    | 2020-12-20 |    700,322.00 |  10,578.00 |     8,589.00 |    681,155.00 |  13,072.00 |

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
