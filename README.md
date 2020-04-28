
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
on 2020-04-28 08:44:29. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-27 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-27 |   199,414 | 26,977 |    66,624 | 105,813 |
| Germany      | 2020-04-27 |   158,758 |  6,126 |   114,500 |  38,132 |
| China        | 2020-04-27 |    83,918 |  4,637 |    78,374 |     907 |
| Korea, South | 2020-04-27 |    10,752 |    244 |     8,854 |   1,654 |

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
| Spain          | 2020-04-27 |   229,422 | 23,521 |   120,832 |  85,069 |
| Italy          | 2020-04-27 |   199,414 | 26,977 |    66,624 | 105,813 |
| France         | 2020-04-27 |   165,963 | 23,327 |    46,293 |  96,343 |
| Germany        | 2020-04-27 |   158,758 |  6,126 |   114,500 |  38,132 |
| United Kingdom | 2020-04-27 |   158,348 | 21,157 |       807 | 136,384 |
| Turkey         | 2020-04-27 |   112,261 |  2,900 |    33,791 |  75,570 |
| Belgium        | 2020-04-27 |    46,687 |  7,207 |    10,878 |  28,602 |
| Netherlands    | 2020-04-27 |    38,440 |  4,534 |       117 |  33,789 |
| Switzerland    | 2020-04-27 |    29,164 |  1,665 |    22,200 |   5,299 |
| Portugal       | 2020-04-27 |    24,027 |    928 |     1,357 |  21,742 |
| Ireland        | 2020-04-27 |    19,648 |  1,102 |     9,233 |   9,313 |
| Sweden         | 2020-04-27 |    18,926 |  2,274 |     1,005 |  15,647 |
| Austria        | 2020-04-27 |    15,274 |    549 |    12,362 |   2,363 |
| Poland         | 2020-04-27 |    11,902 |    562 |     2,466 |   8,874 |
| Romania        | 2020-04-27 |    11,339 |    641 |     3,141 |   7,557 |
| Ukraine        | 2020-04-27 |     9,009 |    220 |       864 |   7,925 |
| Denmark        | 2020-04-27 |     8,896 |    427 |     6,148 |   2,321 |
| Norway         | 2020-04-27 |     7,599 |    205 |        32 |   7,362 |
| Czechia        | 2020-04-27 |     7,445 |    223 |     2,826 |   4,396 |
| Serbia         | 2020-04-27 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-27 |     4,695 |    193 |     2,500 |   2,002 |
| Luxembourg     | 2020-04-27 |     3,729 |     88 |     3,123 |     518 |

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
| US                 | 2020-04-27 |   988,197 | 56,259 |   111,424 | 820,514 |
| Brazil             | 2020-04-27 |    67,446 |  4,603 |    31,142 |  31,701 |
| Canada             | 2020-04-27 |    49,616 |  2,841 |    18,268 |  28,507 |
| Peru               | 2020-04-27 |    28,699 |    782 |     8,425 |  19,492 |
| Ecuador            | 2020-04-27 |    23,240 |    663 |     1,557 |  21,020 |
| Mexico             | 2020-04-27 |    15,529 |  1,434 |     9,086 |   5,009 |
| Chile              | 2020-04-27 |    13,813 |    198 |     7,327 |   6,288 |
| Dominican Republic | 2020-04-27 |     6,293 |    282 |       993 |   5,018 |
| Panama             | 2020-04-27 |     6,021 |    167 |       455 |   5,399 |
| Colombia           | 2020-04-27 |     5,597 |    253 |     1,210 |   4,134 |
| Argentina          | 2020-04-27 |     4,003 |    197 |     1,140 |   2,666 |

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
| Iran                 | 2020-04-27 |    91,472 |  5,806 |    70,933 | 14,733 |
| Saudi Arabia         | 2020-04-27 |    18,811 |    144 |     2,531 | 16,136 |
| Israel               | 2020-04-27 |    15,555 |    204 |     7,200 |  8,151 |
| Pakistan             | 2020-04-27 |    13,915 |    292 |     3,029 | 10,594 |
| Qatar                | 2020-04-27 |    11,244 |     10 |     1,066 | 10,168 |
| United Arab Emirates | 2020-04-27 |    10,839 |     82 |     2,090 |  8,667 |

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
| Russia       | 2020-04-27 |    87,147 |    794 |     7,346 | 79,007 |
| China        | 2020-04-27 |    83,918 |  4,637 |    78,374 |    907 |
| India        | 2020-04-27 |    29,451 |    939 |     7,137 | 21,375 |
| Japan        | 2020-04-27 |    14,153 |    385 |     1,899 | 11,869 |
| Korea, South | 2020-04-27 |    10,752 |    244 |     8,854 |  1,654 |
| Philippines  | 2020-04-27 |     7,777 |    511 |       932 |  6,334 |
| Australia    | 2020-04-27 |     6,721 |     83 |     5,588 |  1,050 |
| Malaysia     | 2020-04-27 |     5,820 |     99 |     3,957 |  1,764 |
| Thailand     | 2020-04-27 |     2,931 |     52 |     2,609 |    270 |

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
| South Africa | 2020-04-27 |     4,793 |     90 |     1,473 |  3,230 |
| Egypt        | 2020-04-27 |     4,782 |    337 |     1,236 |  3,209 |
| Morocco      | 2020-04-27 |     4,120 |    162 |       695 |  3,263 |
| Algeria      | 2020-04-27 |     3,517 |    432 |     1,558 |  1,527 |

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
