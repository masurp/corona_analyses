
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
on 2020-04-24 07:41:57. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-23 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-23 |   189,973 | 25,549 |    57,576 | 106,848 |
| Germany      | 2020-04-23 |   153,129 |  5,575 |   103,300 |  44,254 |
| China        | 2020-04-23 |    83,884 |  4,636 |    77,983 |   1,265 |
| Korea, South | 2020-04-23 |    10,708 |    240 |     8,501 |   1,967 |

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
| Spain          | 2020-04-23 |   213,024 | 22,157 |    89,250 | 101,617 |
| Italy          | 2020-04-23 |   189,973 | 25,549 |    57,576 | 106,848 |
| France         | 2020-04-23 |   159,460 | 21,889 |    42,762 |  94,809 |
| Germany        | 2020-04-23 |   153,129 |  5,575 |   103,300 |  44,254 |
| United Kingdom | 2020-04-23 |   139,246 | 18,791 |       712 | 119,743 |
| Turkey         | 2020-04-23 |   101,790 |  2,491 |    18,491 |  80,808 |
| Belgium        | 2020-04-23 |    42,797 |  6,490 |     9,800 |  26,507 |
| Netherlands    | 2020-04-23 |    35,921 |  4,192 |       101 |  31,628 |
| Switzerland    | 2020-04-23 |    28,496 |  1,549 |    20,600 |   6,347 |
| Portugal       | 2020-04-23 |    22,353 |    820 |     1,201 |  20,332 |
| Ireland        | 2020-04-23 |    17,607 |    794 |     9,233 |   7,580 |
| Sweden         | 2020-04-23 |    16,755 |  2,021 |       550 |  14,184 |
| Austria        | 2020-04-23 |    15,002 |    522 |    11,694 |   2,786 |
| Poland         | 2020-04-23 |    10,511 |    454 |     1,740 |   8,317 |
| Romania        | 2020-04-23 |    10,096 |    545 |     2,478 |   7,073 |
| Denmark        | 2020-04-23 |     8,271 |    394 |     5,573 |   2,304 |
| Norway         | 2020-04-23 |     7,401 |    194 |        32 |   7,175 |
| Czechia        | 2020-04-23 |     7,187 |    210 |     2,152 |   4,825 |
| Ukraine        | 2020-04-23 |     7,170 |    187 |       504 |   6,479 |
| Serbia         | 2020-04-23 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-23 |     4,284 |    172 |     2,000 |   2,112 |
| Luxembourg     | 2020-04-23 |     3,665 |     83 |       728 |   2,854 |

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
| US                 | 2020-04-23 |   869,170 | 49,954 |    80,203 | 739,013 |
| Brazil             | 2020-04-23 |    50,036 |  3,331 |    26,573 |  20,132 |
| Canada             | 2020-04-23 |    43,285 |  2,240 |    14,761 |  26,284 |
| Peru               | 2020-04-23 |    20,914 |    572 |     7,422 |  12,920 |
| Chile              | 2020-04-23 |    11,812 |    168 |     5,804 |   5,840 |
| Mexico             | 2020-04-23 |    11,633 |  1,069 |     2,627 |   7,937 |
| Ecuador            | 2020-04-23 |    11,183 |    560 |     1,328 |   9,295 |
| Dominican Republic | 2020-04-23 |     5,543 |    265 |       581 |   4,697 |
| Panama             | 2020-04-23 |     5,166 |    146 |       271 |   4,749 |
| Colombia           | 2020-04-23 |     4,561 |    215 |       927 |   3,419 |
| Argentina          | 2020-04-23 |     3,435 |    165 |       919 |   2,351 |

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
| Iran                 | 2020-04-23 |    87,026 |  5,481 |    64,843 | 16,702 |
| Israel               | 2020-04-23 |    14,803 |    192 |     5,611 |  9,000 |
| Saudi Arabia         | 2020-04-23 |    13,930 |    121 |     1,925 | 11,884 |
| Pakistan             | 2020-04-23 |    11,155 |    237 |     2,527 |  8,391 |
| United Arab Emirates | 2020-04-23 |     8,756 |     56 |     1,637 |  7,063 |
| Qatar                | 2020-04-23 |     7,764 |     10 |       750 |  7,004 |

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
| China        | 2020-04-23 |    83,884 |  4,636 |    77,983 |  1,265 |
| Russia       | 2020-04-23 |    62,773 |    555 |     4,891 | 57,327 |
| India        | 2020-04-23 |    23,077 |    721 |     5,012 | 17,344 |
| Japan        | 2020-04-23 |    12,368 |    328 |     1,494 | 10,546 |
| Korea, South | 2020-04-23 |    10,708 |    240 |     8,501 |  1,967 |
| Philippines  | 2020-04-23 |     6,981 |    462 |       722 |  5,797 |
| Australia    | 2020-04-23 |     6,661 |     75 |     4,124 |  2,462 |
| Malaysia     | 2020-04-23 |     5,603 |     95 |     3,542 |  1,966 |
| Thailand     | 2020-04-23 |     2,839 |     50 |     2,430 |    359 |

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
| South Africa | 2020-04-23 |     3,953 |     75 |     1,473 |  2,405 |
| Egypt        | 2020-04-23 |     3,891 |    287 |     1,004 |  2,600 |
| Morocco      | 2020-04-23 |     3,568 |    155 |       456 |  2,957 |
| Algeria      | 2020-04-23 |     3,007 |    407 |     1,355 |  1,245 |

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
