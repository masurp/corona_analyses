
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
on 2020-05-05 07:54:09. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-04 at 23:59:00. Also bear in mind that the
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

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| Italy        | 2020-05-04 |   211,938 | 29,079 |    82,879 | 99,980 |
| Germany      | 2020-05-04 |   166,152 |  6,993 |   132,700 | 26,459 |
| China        | 2020-05-04 |    83,966 |  4,637 |    78,792 |    537 |
| Korea, South | 2020-05-04 |    10,804 |    254 |     9,283 |  1,267 |

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
| Spain          | 2020-05-04 |   218,011 | 25,428 |   121,343 |  71,240 |
| Italy          | 2020-05-04 |   211,938 | 29,079 |    82,879 |  99,980 |
| United Kingdom | 2020-05-04 |   191,832 | 28,809 |       910 | 162,113 |
| France         | 2020-05-04 |   169,583 | 25,204 |    51,476 |  92,903 |
| Germany        | 2020-05-04 |   166,152 |  6,993 |   132,700 |  26,459 |
| Turkey         | 2020-05-04 |   127,659 |  3,461 |    68,166 |  56,032 |
| Belgium        | 2020-05-04 |    50,267 |  7,924 |    12,378 |  29,965 |
| Netherlands    | 2020-05-04 |    40,968 |  5,098 |       138 |  35,732 |
| Switzerland    | 2020-05-04 |    29,981 |  1,784 |    25,200 |   2,997 |
| Portugal       | 2020-05-04 |    25,524 |  1,063 |     1,712 |  22,749 |
| Sweden         | 2020-05-04 |    22,721 |  2,769 |     4,074 |  15,878 |
| Ireland        | 2020-05-04 |    21,772 |  1,319 |    13,386 |   7,067 |
| Austria        | 2020-05-04 |    15,621 |    600 |    13,316 |   1,705 |
| Poland         | 2020-05-04 |    14,006 |    698 |     4,095 |   9,213 |
| Romania        | 2020-05-04 |    13,512 |    818 |     5,269 |   7,425 |
| Ukraine        | 2020-05-04 |    12,331 |    303 |     1,619 |  10,409 |
| Denmark        | 2020-05-04 |     9,868 |    493 |     7,284 |   2,091 |
| Serbia         | 2020-05-04 |     9,557 |    197 |     1,574 |   7,786 |
| Norway         | 2020-05-04 |     7,904 |    214 |        32 |   7,658 |
| Czechia        | 2020-05-04 |     7,819 |    252 |     3,807 |   3,760 |
| Finland        | 2020-05-04 |     5,327 |    240 |     3,500 |   1,587 |
| Luxembourg     | 2020-05-04 |     3,828 |     96 |     3,405 |     327 |

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
| US                 | 2020-05-04 | 1,180,375 | 68,922 |   187,180 | 924,273 |
| Brazil             | 2020-05-04 |   108,620 |  7,367 |    45,815 |  55,438 |
| Canada             | 2020-05-04 |    61,957 |  4,003 |    26,030 |  31,924 |
| Peru               | 2020-05-04 |    47,372 |  1,344 |    14,427 |  31,601 |
| Ecuador            | 2020-05-04 |    31,881 |  1,569 |     3,433 |  26,879 |
| Mexico             | 2020-05-04 |    24,905 |  2,271 |    13,447 |   9,187 |
| Chile              | 2020-05-04 |    20,643 |    270 |    10,415 |   9,958 |
| Dominican Republic | 2020-05-04 |     8,235 |    346 |     1,771 |   6,118 |
| Colombia           | 2020-05-04 |     7,973 |    358 |     1,807 |   5,808 |
| Panama             | 2020-05-04 |     7,197 |    200 |       641 |   6,356 |
| Argentina          | 2020-05-04 |     4,887 |    260 |     1,442 |   3,185 |

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
| Iran                 | 2020-05-04 |    98,647 |  6,277 |    79,379 | 12,991 |
| Saudi Arabia         | 2020-05-04 |    28,656 |    191 |     4,476 | 23,989 |
| Pakistan             | 2020-05-04 |    20,941 |    476 |     5,635 | 14,830 |
| Israel               | 2020-05-04 |    16,246 |    235 |    10,064 |  5,947 |
| Qatar                | 2020-05-04 |    16,191 |     12 |     1,810 | 14,369 |
| United Arab Emirates | 2020-05-04 |    14,730 |    137 |     2,966 | 11,627 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia, Indonesia, Australia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Russia       | 2020-05-04 |   145,268 |  1,356 |    18,095 | 125,817 |
| China        | 2020-05-04 |    83,966 |  4,637 |    78,792 |     537 |
| India        | 2020-05-04 |    46,437 |  1,566 |    12,847 |  32,024 |
| Japan        | 2020-05-04 |    15,078 |    536 |     4,156 |  10,386 |
| Korea, South | 2020-05-04 |    10,804 |    254 |     9,283 |   1,267 |
| Philippines  | 2020-05-04 |     9,485 |    623 |     1,315 |   7,547 |
| Australia    | 2020-05-04 |     6,847 |     96 |     5,887 |     864 |
| Malaysia     | 2020-05-04 |     6,353 |    105 |     4,484 |   1,764 |
| Thailand     | 2020-05-04 |     2,987 |     54 |     2,740 |     193 |

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
| South Africa | 2020-05-04 |     7,220 |    138 |     2,746 |  4,336 |
| Egypt        | 2020-05-04 |     6,813 |    436 |     1,632 |  4,745 |
| Morocco      | 2020-05-04 |     5,053 |    179 |     1,653 |  3,221 |
| Algeria      | 2020-05-04 |     4,648 |    465 |     1,998 |  2,185 |

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
