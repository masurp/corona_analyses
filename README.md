
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

The last update was made on 2020-12-22 15:49:00. The data of the John
Hopkins University, however, are always updated at 23:59. What you see
is hence the situation on 2020-12-21 at 23:59:00. Also bear in mind that
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
| US             | 2020-12-21 | 18,035,209.00 | 319,364.00 |         0.00 | 17,715,845.00 | 190,519.00 |
| India          | 2020-12-21 | 10,075,116.00 | 146,111.00 | 9,636,487.00 |    292,518.00 |  19,556.00 |
| Russia         | 2020-12-21 |  2,850,042.00 |  50,723.00 | 2,273,510.00 |    525,809.00 |  28,917.00 |
| France         | 2020-12-21 |  2,535,716.00 |  61,019.00 |   190,296.00 |  2,284,401.00 |   5,960.00 |
| United Kingdom | 2020-12-21 |  2,079,678.00 |  67,718.00 |     4,386.00 |  2,007,574.00 |  33,517.00 |
| Italy          | 2020-12-21 |  1,964,054.00 |  69,214.00 | 1,281,258.00 |    613,582.00 |  10,869.00 |
| Spain          | 2020-12-21 |  1,819,249.00 |  49,260.00 |   150,376.00 |  1,619,613.00 |  22,013.00 |
| Germany        | 2020-12-21 |  1,534,218.00 |  27,110.00 | 1,147,943.00 |    359,165.00 |  19,256.00 |
| Netherlands    | 2020-12-21 |    711,540.00 |  10,606.00 |     8,627.00 |    692,307.00 |  11,218.00 |

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
