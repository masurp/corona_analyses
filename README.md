
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
on 2020-04-25 09:14:24. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-24 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-24 |   192,994 | 25,969 |    60,498 | 106,527 |
| Germany      | 2020-04-24 |   154,999 |  5,760 |   109,800 |  39,439 |
| China        | 2020-04-24 |    83,899 |  4,636 |    78,109 |   1,154 |
| Korea, South | 2020-04-24 |    10,718 |    240 |     8,635 |   1,843 |

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
| Spain          | 2020-04-24 |   219,764 | 22,524 |    92,355 | 104,885 |
| Italy          | 2020-04-24 |   192,994 | 25,969 |    60,498 | 106,527 |
| France         | 2020-04-24 |   159,952 | 22,279 |    44,271 |  93,402 |
| Germany        | 2020-04-24 |   154,999 |  5,760 |   109,800 |  39,439 |
| United Kingdom | 2020-04-24 |   144,640 | 19,567 |       724 | 124,349 |
| Turkey         | 2020-04-24 |   104,912 |  2,600 |    21,737 |  80,575 |
| Belgium        | 2020-04-24 |    44,293 |  6,679 |    10,122 |  27,492 |
| Netherlands    | 2020-04-24 |    36,729 |  4,304 |       102 |  32,323 |
| Switzerland    | 2020-04-24 |    28,677 |  1,589 |    21,000 |   6,088 |
| Portugal       | 2020-04-24 |    22,797 |    854 |     1,228 |  20,715 |
| Ireland        | 2020-04-24 |    18,184 |  1,014 |     9,233 |   7,937 |
| Sweden         | 2020-04-24 |    17,567 |  2,152 |     1,005 |  14,410 |
| Austria        | 2020-04-24 |    15,071 |    530 |    11,872 |   2,669 |
| Poland         | 2020-04-24 |    10,892 |    494 |     1,944 |   8,454 |
| Romania        | 2020-04-24 |    10,417 |    567 |     2,817 |   7,033 |
| Denmark        | 2020-04-24 |     8,408 |    403 |     5,715 |   2,290 |
| Ukraine        | 2020-04-24 |     8,125 |    201 |       782 |   7,142 |
| Norway         | 2020-04-24 |     7,463 |    199 |        32 |   7,232 |
| Czechia        | 2020-04-24 |     7,273 |    214 |     2,371 |   4,688 |
| Serbia         | 2020-04-24 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-24 |     4,395 |    177 |     2,500 |   1,718 |
| Luxembourg     | 2020-04-24 |     3,695 |     85 |     3,007 |     603 |

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
| US                 | 2020-04-24 |   905,358 | 51,949 |    99,079 | 754,330 |
| Brazil             | 2020-04-24 |    54,043 |  3,704 |    27,655 |  22,684 |
| Canada             | 2020-04-24 |    44,054 |  2,384 |    15,149 |  26,521 |
| Ecuador            | 2020-04-24 |    22,719 |    576 |     1,366 |  20,777 |
| Peru               | 2020-04-24 |    21,648 |    634 |     7,496 |  13,518 |
| Chile              | 2020-04-24 |    12,306 |    174 |     6,327 |   5,805 |
| Mexico             | 2020-04-24 |    11,633 |  1,069 |     2,627 |   7,937 |
| Dominican Republic | 2020-04-24 |     5,749 |    267 |       763 |   4,719 |
| Panama             | 2020-04-24 |     5,338 |    154 |       319 |   4,865 |
| Colombia           | 2020-04-24 |     4,881 |    225 |     1,003 |   3,653 |
| Argentina          | 2020-04-24 |     3,607 |    176 |       976 |   2,455 |

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
| Iran                 | 2020-04-24 |    88,194 |  5,574 |    66,599 | 16,021 |
| Saudi Arabia         | 2020-04-24 |    15,102 |    127 |     2,049 | 12,926 |
| Israel               | 2020-04-24 |    15,058 |    194 |     6,003 |  8,861 |
| Pakistan             | 2020-04-24 |    11,940 |    253 |     2,755 |  8,932 |
| United Arab Emirates | 2020-04-24 |     9,281 |     64 |     1,760 |  7,457 |
| Qatar                | 2020-04-24 |     8,525 |     10 |       809 |  7,706 |

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
| China        | 2020-04-24 |    83,899 |  4,636 |    78,109 |  1,154 |
| Russia       | 2020-04-24 |    68,622 |    615 |     5,568 | 62,439 |
| India        | 2020-04-24 |    24,530 |    780 |     5,498 | 18,252 |
| Japan        | 2020-04-24 |    12,829 |    345 |     1,530 | 10,954 |
| Korea, South | 2020-04-24 |    10,718 |    240 |     8,635 |  1,843 |
| Philippines  | 2020-04-24 |     7,192 |    477 |       762 |  5,953 |
| Australia    | 2020-04-24 |     6,677 |     79 |     4,124 |  2,474 |
| Malaysia     | 2020-04-24 |     5,691 |     96 |     3,663 |  1,932 |
| Thailand     | 2020-04-24 |     2,907 |     51 |     2,547 |    309 |

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
| South Africa | 2020-04-24 |     4,220 |     79 |     1,473 |  2,668 |
| Egypt        | 2020-04-24 |     4,092 |    294 |     1,075 |  2,723 |
| Morocco      | 2020-04-24 |     3,758 |    158 |       486 |  3,114 |
| Algeria      | 2020-04-24 |     3,127 |    415 |     1,408 |  1,304 |

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
