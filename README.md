
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
on 2020-04-16 08:03:58. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-15 at 23:59:00. Also bear in mind that the
reporting of cases is somewhat delayed so that it is very likely that
the actual numbers are higher.

## Visualizations

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

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Italy        | 2020-04-15 |   165,155 | 21,645 |    38,092 | 105,418 |
| Germany      | 2020-04-15 |   134,753 |  3,804 |    72,600 |  58,349 |
| China        | 2020-04-15 |    83,356 |  3,346 |    78,311 |   1,699 |
| Korea, South | 2020-04-15 |    10,591 |    225 |     7,616 |   2,750 |

<img src="figures/unnamed-chunk-2-1.png" width="100%" />

### 2\. Worldwide developments

#### Europe

<caption>

(\#tab:europe)

</caption>

<caption>

\*\*

</caption>

| country        |    date    | confirmed | deaths | recovered |  active |
| :------------- | :--------: | --------: | -----: | --------: | ------: |
| Spain          | 2020-04-15 |   177,644 | 18,708 |    70,853 |  88,083 |
| Italy          | 2020-04-15 |   165,155 | 21,645 |    38,092 | 105,418 |
| Germany        | 2020-04-15 |   134,753 |  3,804 |    72,600 |  58,349 |
| France         | 2020-04-15 |   134,582 | 17,188 |    31,470 |  85,924 |
| United Kingdom | 2020-04-15 |    99,483 | 12,894 |       368 |  86,221 |
| Turkey         | 2020-04-15 |    69,392 |  1,518 |     5,674 |  62,200 |
| Belgium        | 2020-04-15 |    33,573 |  4,440 |     7,107 |  22,026 |
| Netherlands    | 2020-04-15 |    28,316 |  3,145 |       304 |  24,867 |
| Switzerland    | 2020-04-15 |    26,336 |  1,239 |    15,400 |   9,697 |
| Portugal       | 2020-04-15 |    18,091 |    599 |       383 |  17,109 |
| Austria        | 2020-04-15 |    14,336 |    393 |     8,098 |   5,845 |
| Ireland        | 2020-04-15 |    12,547 |    444 |        77 |  12,026 |
| Sweden         | 2020-04-15 |    11,927 |  1,203 |       381 |  10,343 |
| Poland         | 2020-04-15 |     7,582 |    286 |       668 |   6,628 |
| Romania        | 2020-04-15 |     7,216 |    372 |     1,217 |   5,627 |
| Denmark        | 2020-04-15 |     6,876 |    309 |     2,925 |   3,642 |
| Norway         | 2020-04-15 |     6,740 |    150 |        32 |   6,558 |
| Czechia        | 2020-04-15 |     6,216 |    166 |       819 |   5,231 |
| Serbia         | 2020-04-15 |     4,873 |     99 |         0 |   4,774 |
| Ukraine        | 2020-04-15 |     3,764 |    108 |       143 |   3,513 |
| Luxembourg     | 2020-04-15 |     3,373 |     69 |       526 |   2,778 |
| Finland        | 2020-04-15 |     3,237 |     72 |       300 |   2,865 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<caption>

\*\*

</caption>

| country            |    date    | confirmed | deaths | recovered |  active |
| :----------------- | :--------: | --------: | -----: | --------: | ------: |
| US                 | 2020-04-15 |   636,350 | 28,326 |    52,096 | 555,928 |
| Brazil             | 2020-04-15 |    28,320 |  1,736 |    14,026 |  12,558 |
| Canada             | 2020-04-15 |    28,208 |  1,006 |     8,966 |  18,236 |
| Peru               | 2020-04-15 |    11,475 |    254 |     3,108 |   8,113 |
| Chile              | 2020-04-15 |     8,273 |     94 |     2,937 |   5,242 |
| Ecuador            | 2020-04-15 |     7,858 |    388 |       780 |   6,690 |
| Mexico             | 2020-04-15 |     5,399 |    406 |     2,125 |   2,868 |
| Dominican Republic | 2020-04-15 |     3,614 |    189 |       208 |   3,217 |
| Panama             | 2020-04-15 |     3,574 |     95 |        72 |   3,407 |
| Colombia           | 2020-04-15 |     3,105 |    131 |       452 |   2,522 |
| Argentina          | 2020-04-15 |     2,443 |    111 |       596 |   1,736 |

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<caption>

\*\*

</caption>

| country              |    date    | confirmed | deaths | recovered | active |
| :------------------- | :--------: | --------: | -----: | --------: | -----: |
| Iran                 | 2020-04-15 |    76,389 |  4,777 |    49,933 | 21,679 |
| Israel               | 2020-04-15 |    12,501 |    130 |     2,563 |  9,808 |
| Pakistan             | 2020-04-15 |     6,383 |    111 |     1,446 |  4,826 |
| Saudi Arabia         | 2020-04-15 |     5,862 |     79 |       931 |  4,852 |
| United Arab Emirates | 2020-04-15 |     5,365 |     33 |     1,034 |  4,298 |
| Qatar                | 2020-04-15 |     3,711 |      7 |       406 |  3,298 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia, Indonesia, Australia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| China        | 2020-04-15 |    83,356 |  3,346 |    78,311 |  1,699 |
| Russia       | 2020-04-15 |    24,490 |    198 |     1,986 | 22,306 |
| India        | 2020-04-15 |    12,322 |    405 |     1,432 | 10,485 |
| Korea, South | 2020-04-15 |    10,591 |    225 |     7,616 |  2,750 |
| Japan        | 2020-04-15 |     8,100 |    146 |       853 |  7,101 |
| Australia    | 2020-04-15 |     6,440 |     63 |     2,186 |  4,191 |
| Philippines  | 2020-04-15 |     5,453 |    349 |       353 |  4,751 |
| Malaysia     | 2020-04-15 |     5,072 |     83 |     2,647 |  2,342 |
| Thailand     | 2020-04-15 |     2,643 |     43 |     1,497 |  1,103 |

<img src="figures/asia-1.png" width="100%" />

### Africa

<caption>

(\#tab:unnamed-chunk-6)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| South Africa | 2020-04-15 |     2,506 |     34 |       410 |  2,062 |
| Egypt        | 2020-04-15 |     2,505 |    183 |       589 |  1,733 |
| Algeria      | 2020-04-15 |     2,160 |    336 |       708 |  1,116 |
| Morocco      | 2020-04-15 |     2,024 |    127 |       229 |  1,668 |

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
