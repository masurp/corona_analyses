
# Visualizing the Corona (COVID-19) pandemic

## Basic idea

I generally think that the news do a good job in describing and
visualizing the corona pandemic. However, there are two things that I
believe are quite problematic and that I am missing the any news
coverage on the pandemic.

1.  Visualizations of the growth curves often log-transform the x-axis
    instead of showing the actual *exponential* growth.
2.  Visualizations almost never plot *total* cases against a) deaths, b)
    recovered, AND c) active cases.

With regard to the former, I recently wrote [this
blogpost](http://philippmasur.de/blog/2020/03/13/understanding-exponential-growth-the-corona-pandemic/)
that explains why exponential growth is so hard to grasp. With regard to
the latter, I believe that visualizations would become a bit more
informative if we plot total cases, active cases, recovered cases, and
deaths. If we plot all *four* curves simultaneously, patterns emerge
that might tell us something about the “phase”" that a country is it. We
may also see whether a country succeeds in stopping the infections (BUT:
see disclaimer further below\!). In what follows, I am using the data on
worldwide total infections, death rates, and number of recoveries to
produce these (potentially) a bit more insightful visualizations.

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
how many tests were conducted. For example, Italy has an unusually high
mortality rate at this moment (\~8%). However, Italy ran only \~150k
tests. The real rate of infections is probably much higher, implying a
lower mortality rate. South Korea, in contrast, has tested \> 270,000
people, which amounts to more than 5,200 tests per million inhabitants —
more tests than any other country\! A high diagnostic capacity at scale
is hence key to epidemic control as it provides us with precise
estimates and growth rate predictions (for more information on this, see
[this
article](https://www.sciencemag.org/news/2020/03/coronavirus-cases-have-dropped-sharply-south-korea-whats-secret-its-success?fbclid=IwAR3BnhqQMxCdu8-fQelEkWIDQn-j9UASV773Xl-WbIy8l7M5ZVSQpHFgkL8)
in Science). For this reasons, I believe that the value of these
visualization lies NOT in comparing the actual numbers, but in the
understanding the patterns that emerge by comparing all four curves.

Furthermore, I would like to emphasize that I am not an expert on
epidemology or virus outbreaks and I am not working in the health
sector. On this page, I am only visualizing the data by the John Hopkins
University in a different way that most news or other outlets do.
Reliance on the these visualizations for medical guidance or use of
these visualization in commerce is strictly prohibited.

#### Will these figures be updated?

Yes, I will update these figures every morning. The last update was made
on 2020-03-24 07:55:11. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-03-23 at 23:59:00. Also bear in mind that the
reporting of cases is somewhat delayed so that it is very likely that
the actual numbers are higher.

## Visualizations

Note: I am not focusing on provinces, I hence only summarize across
countries and dates. That said, I distinguish China and Hong Kong due to
their different timelines in responding to the virus outbreak.

If you are interested in the R code, please see the
[README.rmd](https://github.com/masurp/corona_analyses/blob/master/README.rmd).

### 1\. Analyzing China, South Korea, Italy, and Germany

In a first step, I am comparing China, South Korea, Italy, and Germany.
Why these countries? These four countries are at very different stages.
China was the first to experience the outbreak and they have almost
contained the spreading of the virus by now. South Korea is starting to
control the virus outbreak. Italy is currently experiencing one of the
worst outbreaks and drastic measures have been taken in the last weeks.
The virus has reached Germany considerably later, but the growth rate is
very steep at this moment.

<caption>

(\#tab:example)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | total cases | deaths | recovered | active |
| :----------- | :--------: | ----------: | -----: | --------: | -----: |
| China        | 2020-03-23 |      81,122 |  3,270 |    72,714 |  5,138 |
| Italy        | 2020-03-23 |      59,138 |  5,476 |     7,024 | 46,638 |
| Germany      | 2020-03-23 |      24,873 |     94 |       266 | 24,513 |
| Korea, South | 2020-03-23 |       8,897 |    104 |     2,909 |  5,884 |

<img src="figures/unnamed-chunk-2-1.png" width="100%" />

CHINA (upper left): The number of *total* confirmed cases is still
rising (pink), but only very slowly and almost comes to a halt. The
number of *active* cases (green) is declining steeply and at the same
time the number of *recovered* cases (blue) is increasing a lot, slowly
approximating the number of *total* cases. This is how it should look
like as this pattern shows that measures are working and the spreading
of the virus is stopping.

SOUTH KOREA (upper right): The number of *total* confirmed cases is
still rising (pink), but the growth rate slowly resembles an S-curve.
This is a good sign, because new infections are fewer. The number of
*active* cases (green) is hence starting to decline (although it
recently started to grow again) and at the same time the number of
*recovered* cases (blue) is starting to grow.

ITALY (lower left): The number of *total* confirmed cases is still
growing exponentially. More importantly, the number of *active* cases is
almost equivalent to the number of *total* cases. The number of
*recovered* cases sadly equals the number of *deaths*. So far, we do not
see implications of the drastic measures taken by the Italian
government.

GERMANY (lower right): The number of *total* confirmed cases likewise
grows exponentially. Again, the number of *active* cases is practically
equivalent to the number of *total* cases.

### 2\. Worldwide developments

#### Europe

Countries with more than \~500 confirmed total cases.

<caption>

(\#tab:europe)

</caption>

<caption>

\*\*

</caption>

| country        |    date    | total cases | deaths | recovered | active |
| :------------- | :--------: | ----------: | -----: | --------: | -----: |
| Italy          | 2020-03-23 |      59,138 |  5,476 |     7,024 | 46,638 |
| Spain          | 2020-03-23 |      28,768 |  1,772 |     2,575 | 24,421 |
| Germany        | 2020-03-23 |      24,873 |     94 |       266 | 24,513 |
| France         | 2020-03-23 |      16,044 |    674 |     2,200 | 13,170 |
| Switzerland    | 2020-03-23 |       7,245 |     98 |       131 |  7,016 |
| United Kingdom | 2020-03-23 |       5,741 |    282 |        67 |  5,392 |
| Netherlands    | 2020-03-23 |       4,216 |    180 |         2 |  4,034 |
| Belgium        | 2020-03-23 |       3,401 |     75 |       263 |  3,063 |
| Austria        | 2020-03-23 |       3,244 |     16 |         9 |  3,219 |
| Norway         | 2020-03-23 |       2,383 |      7 |         1 |  2,375 |
| Sweden         | 2020-03-23 |       1,934 |     21 |        16 |  1,897 |
| Portugal       | 2020-03-23 |       1,600 |     14 |         5 |  1,581 |
| Denmark        | 2020-03-23 |       1,514 |     13 |         1 |  1,500 |
| Turkey         | 2020-03-23 |       1,236 |     30 |         0 |  1,206 |
| Czechia        | 2020-03-23 |       1,120 |      1 |         6 |  1,113 |
| Ireland        | 2020-03-23 |         906 |      4 |         5 |    897 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<caption>

\*\*

</caption>

| country |    date    | total cases | deaths | recovered | active |
| :------ | :--------: | ----------: | -----: | --------: | -----: |
| Brazil  | 2020-03-23 |       1,593 |     25 |         2 |  1,566 |
| Canada  | 2020-03-23 |       1,470 |     21 |        10 |  1,439 |
| US      | 2020-03-23 |          NA |     NA |        NA |     NA |

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

Countries in the middle east with \> 400 cases.

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<caption>

\*\*

</caption>

| country  |    date    | total cases | deaths | recovered | active |
| :------- | :--------: | ----------: | -----: | --------: | -----: |
| Iran     | 2020-03-23 |      21,638 |  1,685 |     7,931 | 12,022 |
| Israel   | 2020-03-23 |       1,071 |      1 |        37 |  1,033 |
| Pakistan | 2020-03-23 |         776 |      5 |         5 |    766 |
| Qatar    | 2020-03-23 |         494 |      0 |        33 |    461 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia

Asian countries with \> 500 cases.

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | total cases | deaths | recovered | active |
| :----------- | :--------: | ----------: | -----: | --------: | -----: |
| China        | 2020-03-23 |      81,122 |  3,270 |    72,714 |  5,138 |
| Korea, South | 2020-03-23 |       8,897 |    104 |     2,909 |  5,884 |
| Malaysia     | 2020-03-23 |       1,306 |     10 |       139 |  1,157 |
| Japan        | 2020-03-23 |       1,086 |     40 |       235 |    811 |

<img src="figures/asia-1.png" width="100%" />
