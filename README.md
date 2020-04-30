
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
how many tests were conducted. South Korea, for example, has tested \>
270,000 people, which amounts to more than 5,200 tests per million
inhabitants. The numbers in South Korea are hence more trustworthy than
the numbers of all other countries. A high diagnostic capacity at scale
is hence key to epidemic control as it provides us with precise
estimates and growth rate predictions (for more information on this, see
[this
article](https://www.sciencemag.org/news/2020/03/coronavirus-cases-have-dropped-sharply-south-korea-whats-secret-its-success?fbclid=IwAR3BnhqQMxCdu8-fQelEkWIDQn-j9UASV773Xl-WbIy8l7M5ZVSQpHFgkL8)
in Science). For this reasons, I believe that the value of these
visualization lies NOT in comparing the actual numbers, but in
understanding the patterns that emerge by comparing all four curves.

Furthermore, I would like to emphasize that I am not an expert on
epidemology or virus outbreaks and I am not working in the health
sector. On this page, I am only visualizing the data by the John Hopkins
University in a different way that most news or other outlets do.
Reliance on the these visualizations for medical guidance or use of
these visualization in commerce is strictly prohibited.

#### Will these figures be updated?

Yes, I will update these figures every morning. The last update was made
on 2020-04-30 08:24:31. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-29 at 23:59:00. Also bear in mind that the
reporting of cases is somewhat delayed so that it is very likely that
the actual numbers are higher.

## Visualizations

If you are interested in the R code, please see the
[README.rmd](https://github.com/masurp/corona_analyses/blob/master/README.rmd).

### 1\. Analyzing China, South Korea, Italy, and Germany

In a first step, I am comparing China, South Korea, Italy, and Germany.
Why these countries? These countries are at very different stages or
show very different developments (in terms of size and patterns). China,
for example, was the first to experience the outbreak and they seem to
have contained the spreading of the virus by now. South Korea is
similarly controlling the virus outbreak (the pattern follows China).
Italy has been experiencing one of the worst outbreaks and drastic
measures have been taken, we see the first signs that it slowly gets
better. The virus has reached Germany considerably later. Although the
growth rate was very steep in the beginning, it now starts to follow the
pattern of China and South Korea.

<caption>

(\#tab:example)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Italy        | 2020-04-29 |   203,591 | 27,682 |    71,252 | 104,657 |
| Germany      | 2020-04-29 |   161,539 |  6,467 |   120,400 |  34,672 |
| China        | 2020-04-29 |    83,944 |  4,637 |    78,474 |     833 |
| Korea, South | 2020-04-29 |    10,765 |    247 |     9,059 |   1,459 |

<img src="figures/unnamed-chunk-2-1.png" width="100%" />

### 2\. Worldwide developments

#### Europe

<caption>

(\#tab:europe)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country        |    date    | confirmed | deaths | recovered |  active |
| :------------- | :--------: | --------: | -----: | --------: | ------: |
| Spain          | 2020-04-29 |   236,899 | 24,275 |   132,929 |  79,695 |
| Italy          | 2020-04-29 |   203,591 | 27,682 |    71,252 | 104,657 |
| France         | 2020-04-29 |   166,543 | 24,121 |    49,118 |  93,304 |
| United Kingdom | 2020-04-29 |   166,441 | 26,166 |       857 | 139,418 |
| Germany        | 2020-04-29 |   161,539 |  6,467 |   120,400 |  34,672 |
| Turkey         | 2020-04-29 |   117,589 |  3,081 |    44,040 |  70,468 |
| Belgium        | 2020-04-29 |    47,859 |  7,501 |    11,283 |  29,075 |
| Netherlands    | 2020-04-29 |    38,998 |  4,727 |       119 |  34,152 |
| Switzerland    | 2020-04-29 |    29,407 |  1,716 |    22,600 |   5,091 |
| Portugal       | 2020-04-29 |    24,505 |    973 |     1,470 |  22,062 |
| Sweden         | 2020-04-29 |    20,302 |  2,462 |     1,005 |  16,835 |
| Ireland        | 2020-04-29 |    20,253 |  1,190 |    13,386 |   5,677 |
| Austria        | 2020-04-29 |    15,402 |    580 |    12,779 |   2,043 |
| Poland         | 2020-04-29 |    12,640 |    624 |     3,025 |   8,991 |
| Romania        | 2020-04-29 |    11,978 |    693 |     3,569 |   7,716 |
| Ukraine        | 2020-04-29 |     9,866 |    250 |     1,103 |   8,513 |
| Denmark        | 2020-04-29 |     9,206 |    443 |     6,558 |   2,205 |
| Norway         | 2020-04-29 |     7,710 |    207 |        32 |   7,471 |
| Czechia        | 2020-04-29 |     7,579 |    227 |     3,108 |   4,244 |
| Serbia         | 2020-04-29 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-29 |     4,906 |    206 |     2,800 |   1,900 |
| Luxembourg     | 2020-04-29 |     3,769 |     89 |     3,134 |     546 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country            |    date    | confirmed | deaths | recovered |  active |
| :----------------- | :--------: | --------: | -----: | --------: | ------: |
| US                 | 2020-04-29 | 1,039,909 | 60,967 |   120,720 | 858,222 |
| Brazil             | 2020-04-29 |    79,685 |  5,513 |    34,132 |  40,040 |
| Canada             | 2020-04-29 |    52,865 |  3,155 |    20,327 |  29,383 |
| Peru               | 2020-04-29 |    33,931 |    943 |    10,037 |  22,951 |
| Ecuador            | 2020-04-29 |    24,675 |    883 |     1,557 |  22,235 |
| Mexico             | 2020-04-29 |    17,799 |  1,732 |    11,423 |   4,644 |
| Chile              | 2020-04-29 |    14,885 |    216 |     8,057 |   6,612 |
| Dominican Republic | 2020-04-29 |     6,652 |    293 |     1,228 |   5,131 |
| Panama             | 2020-04-29 |     6,378 |    178 |       527 |   5,673 |
| Colombia           | 2020-04-29 |     6,207 |    278 |     1,411 |   4,518 |
| Argentina          | 2020-04-29 |     4,285 |    214 |     1,192 |   2,879 |

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country              |    date    | confirmed | deaths | recovered | active |
| :------------------- | :--------: | --------: | -----: | --------: | -----: |
| Iran                 | 2020-04-29 |    93,657 |  5,957 |    73,791 | 13,909 |
| Saudi Arabia         | 2020-04-29 |    21,402 |    157 |     2,953 | 18,292 |
| Israel               | 2020-04-29 |    15,834 |    215 |     8,233 |  7,386 |
| Pakistan             | 2020-04-29 |    15,525 |    343 |     3,425 | 11,757 |
| Qatar                | 2020-04-29 |    12,564 |     10 |     1,243 | 11,311 |
| United Arab Emirates | 2020-04-29 |    11,929 |     98 |     2,329 |  9,502 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia, Indonesia, Australia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| Russia       | 2020-04-29 |    99,399 |    972 |    10,286 | 88,141 |
| China        | 2020-04-29 |    83,944 |  4,637 |    78,474 |    833 |
| India        | 2020-04-29 |    33,062 |  1,079 |     8,437 | 23,546 |
| Japan        | 2020-04-29 |    13,895 |    413 |     2,368 | 11,114 |
| Korea, South | 2020-04-29 |    10,765 |    247 |     9,059 |  1,459 |
| Philippines  | 2020-04-29 |     8,212 |    558 |     1,023 |  6,631 |
| Australia    | 2020-04-29 |     6,752 |     91 |     5,715 |    946 |
| Malaysia     | 2020-04-29 |     5,945 |    100 |     4,087 |  1,758 |
| Thailand     | 2020-04-29 |     2,947 |     54 |     2,665 |    228 |

<img src="figures/asia-1.png" width="100%" />

#### Africa

<caption>

(\#tab:unnamed-chunk-6)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| South Africa | 2020-04-29 |     5,350 |    103 |     2,073 |  3,174 |
| Egypt        | 2020-04-29 |     5,268 |    380 |     1,335 |  3,553 |
| Morocco      | 2020-04-29 |     4,321 |    168 |       928 |  3,225 |
| Algeria      | 2020-04-29 |     3,848 |    444 |     1,702 |  1,702 |

<img src="figures/africa-1.png" width="100%" />

### 3\. Alternative visualizations

One thing that is constantly debatted is how to visualize growth (of
total confirmed cases) at all. Log-transform the y-axis or not? Plot
against the date? Plot against days after 100th case? Plot something
entirely different?

Here, I would like to explain some differences between visualizations
that have been used in the media. All of them are helpful in their own
regard.

1.  LEFT: Here, I plotted total cases against days after the 100th cases
    *without* logarithmizing the y-axis.

2.  MIDDLE: The y-axis is logarithmized. This figure is often shown in
    the news.

3.  RIGHT: New cases per 7 days (y-axis) are plotted against total cases
    (x-axis), both axes are logarithmized (Idea explained in this
    [video](https://www.youtube.com/watch?v=54XLXg4fYsc).

We see clearly that each plot has benefits and weaknesses. The first
example provides perhaps the best comparison of the total numbers and
shows quite drastically how exponential growth curves look likes.
S-curves represent positive developments towards a slower growth. Yet,
changes are barely identifiable. The second example makes the actual
growth more comparable and by logarithmizing the y-axsis, we can
actually see changes in the growth. Here, it seesm that most countries
are actually starting to slow the growth. Finally, the last example is
hard to understand generally, but it shows best whether some sort of
measure is working. The curve needs to sink drastically, otherwise, the
growth is continuing uncontrollibly.

<img src="figures/unnamed-chunk-7-1.png" width="100%" />
