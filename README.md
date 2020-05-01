
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
on 2020-05-01 08:33:32. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-30 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-30 |   205,463 | 27,967 |    75,945 | 101,551 |
| Germany      | 2020-04-30 |   163,009 |  6,623 |   123,500 |  32,886 |
| China        | 2020-04-30 |    83,956 |  4,637 |    78,523 |     796 |
| Korea, South | 2020-04-30 |    10,774 |    248 |     9,072 |   1,454 |

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
| Spain          | 2020-04-30 |   213,435 | 24,543 |   112,050 |  76,842 |
| Italy          | 2020-04-30 |   205,463 | 27,967 |    75,945 | 101,551 |
| United Kingdom | 2020-04-30 |   172,481 | 26,842 |       859 | 144,780 |
| France         | 2020-04-30 |   167,299 | 24,410 |    50,380 |  92,509 |
| Germany        | 2020-04-30 |   163,009 |  6,623 |   123,500 |  32,886 |
| Turkey         | 2020-04-30 |   120,204 |  3,174 |    48,886 |  68,144 |
| Belgium        | 2020-04-30 |    48,519 |  7,594 |    11,576 |  29,349 |
| Netherlands    | 2020-04-30 |    39,512 |  4,811 |       125 |  34,576 |
| Switzerland    | 2020-04-30 |    29,586 |  1,737 |    23,400 |   4,449 |
| Portugal       | 2020-04-30 |    25,045 |    989 |     1,519 |  22,537 |
| Sweden         | 2020-04-30 |    21,092 |  2,586 |     1,005 |  17,501 |
| Ireland        | 2020-04-30 |    20,612 |  1,232 |    13,386 |   5,994 |
| Austria        | 2020-04-30 |    15,452 |    584 |    12,907 |   1,961 |
| Poland         | 2020-04-30 |    12,877 |    644 |     3,236 |   8,997 |
| Romania        | 2020-04-30 |    12,240 |    717 |     4,017 |   7,506 |
| Ukraine        | 2020-04-30 |    10,406 |    261 |     1,238 |   8,907 |
| Denmark        | 2020-04-30 |     9,356 |    452 |     6,741 |   2,163 |
| Serbia         | 2020-04-30 |     9,009 |    179 |     1,343 |   7,487 |
| Norway         | 2020-04-30 |     7,738 |    210 |        32 |   7,496 |
| Czechia        | 2020-04-30 |     7,682 |    236 |     3,314 |   4,132 |
| Finland        | 2020-04-30 |     4,995 |    211 |     3,000 |   1,784 |
| Luxembourg     | 2020-04-30 |     3,784 |     90 |     3,213 |     481 |

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
| US                 | 2020-04-30 | 1,069,424 | 62,996 |   153,947 | 852,481 |
| Brazil             | 2020-04-30 |    87,187 |  6,006 |    35,935 |  45,246 |
| Canada             | 2020-04-30 |    54,457 |  3,310 |    21,424 |  29,723 |
| Peru               | 2020-04-30 |    36,976 |  1,051 |    10,405 |  25,520 |
| Ecuador            | 2020-04-30 |    24,934 |    900 |     1,558 |  22,476 |
| Mexico             | 2020-04-30 |    19,224 |  1,859 |    11,423 |   5,942 |
| Chile              | 2020-04-30 |    16,023 |    227 |     8,580 |   7,216 |
| Dominican Republic | 2020-04-30 |     6,972 |    301 |     1,301 |   5,370 |
| Panama             | 2020-04-30 |     6,532 |    188 |       576 |   5,768 |
| Colombia           | 2020-04-30 |     6,507 |    293 |     1,439 |   4,775 |
| Argentina          | 2020-04-30 |     4,428 |    218 |     1,256 |   2,954 |

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
| Iran                 | 2020-04-30 |    94,640 |  6,028 |    75,103 | 13,509 |
| Saudi Arabia         | 2020-04-30 |    22,753 |    162 |     3,163 | 19,428 |
| Pakistan             | 2020-04-30 |    16,817 |    385 |     4,315 | 12,117 |
| Israel               | 2020-04-30 |    15,946 |    222 |     8,561 |  7,163 |
| Qatar                | 2020-04-30 |    13,409 |     10 |     1,372 | 12,027 |
| United Arab Emirates | 2020-04-30 |    12,481 |    105 |     2,429 |  9,947 |

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
| Russia       | 2020-04-30 |   106,498 |  1,073 |    11,619 | 93,806 |
| China        | 2020-04-30 |    83,956 |  4,637 |    78,523 |    796 |
| India        | 2020-04-30 |    34,863 |  1,154 |     9,068 | 24,641 |
| Japan        | 2020-04-30 |    14,088 |    430 |     2,460 | 11,198 |
| Korea, South | 2020-04-30 |    10,774 |    248 |     9,072 |  1,454 |
| Philippines  | 2020-04-30 |     8,488 |    568 |     1,043 |  6,877 |
| Australia    | 2020-04-30 |     6,766 |     93 |     5,742 |    931 |
| Malaysia     | 2020-04-30 |     6,002 |    102 |     4,171 |  1,729 |
| Thailand     | 2020-04-30 |     2,954 |     54 |     2,684 |    216 |

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
| South Africa | 2020-04-30 |     5,647 |    103 |     2,073 |  3,471 |
| Egypt        | 2020-04-30 |     5,537 |    392 |     1,381 |  3,764 |
| Morocco      | 2020-04-30 |     4,423 |    170 |       984 |  3,269 |
| Algeria      | 2020-04-30 |     4,006 |    450 |     1,779 |  1,777 |

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
