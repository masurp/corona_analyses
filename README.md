
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
on 2020-04-21 07:36:43. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-20 at 23:59:00. Also bear in mind that the
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

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Italy        | 2020-04-20 |   181,228 | 24,114 |    48,877 | 108,237 |
| Germany      | 2020-04-20 |   147,065 |  4,862 |    91,500 |  50,703 |
| China        | 2020-04-20 |    83,817 |  4,636 |    77,745 |   1,436 |
| Korea, South | 2020-04-20 |    10,674 |    236 |     8,114 |   2,324 |

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
| Spain          | 2020-04-20 |   200,210 | 20,852 |    80,587 |  98,771 |
| Italy          | 2020-04-20 |   181,228 | 24,114 |    48,877 | 108,237 |
| France         | 2020-04-20 |   156,480 | 20,292 |    38,036 |  98,152 |
| Germany        | 2020-04-20 |   147,065 |  4,862 |    91,500 |  50,703 |
| United Kingdom | 2020-04-20 |   125,856 | 16,550 |       446 | 108,860 |
| Turkey         | 2020-04-20 |    90,980 |  2,140 |    13,430 |  75,410 |
| Belgium        | 2020-04-20 |    39,983 |  5,828 |     8,895 |  25,260 |
| Netherlands    | 2020-04-20 |    33,588 |  3,764 |       322 |  29,502 |
| Switzerland    | 2020-04-20 |    27,944 |  1,429 |    18,600 |   7,915 |
| Portugal       | 2020-04-20 |    20,863 |    735 |       610 |  19,518 |
| Ireland        | 2020-04-20 |    15,652 |    687 |        77 |  14,888 |
| Austria        | 2020-04-20 |    14,795 |    470 |    10,631 |   3,694 |
| Sweden         | 2020-04-20 |    14,777 |  1,580 |       550 |  12,647 |
| Poland         | 2020-04-20 |     9,593 |    380 |     1,133 |   8,080 |
| Romania        | 2020-04-20 |     8,936 |    478 |     2,017 |   6,441 |
| Denmark        | 2020-04-20 |     7,711 |    364 |     4,499 |   2,848 |
| Norway         | 2020-04-20 |     7,156 |    181 |        32 |   6,943 |
| Czechia        | 2020-04-20 |     6,900 |    194 |     1,559 |   5,147 |
| Serbia         | 2020-04-20 |     6,630 |    125 |       870 |   5,635 |
| Ukraine        | 2020-04-20 |     5,710 |    151 |       359 |   5,200 |
| Finland        | 2020-04-20 |     3,868 |     98 |     2,000 |   1,770 |
| Luxembourg     | 2020-04-20 |     3,558 |     75 |       637 |   2,846 |

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
| US                 | 2020-04-20 |   784,326 | 42,094 |    72,329 | 669,903 |
| Brazil             | 2020-04-20 |    40,743 |  2,587 |    22,130 |  16,026 |
| Canada             | 2020-04-20 |    37,657 |  1,725 |    12,543 |  23,389 |
| Peru               | 2020-04-20 |    16,325 |    445 |     6,968 |   8,912 |
| Chile              | 2020-04-20 |    10,507 |    139 |     4,676 |   5,692 |
| Ecuador            | 2020-04-20 |    10,128 |    507 |     1,150 |   8,471 |
| Mexico             | 2020-04-20 |     8,261 |    686 |     2,627 |   4,948 |
| Dominican Republic | 2020-04-20 |     4,964 |    235 |       416 |   4,313 |
| Panama             | 2020-04-20 |     4,467 |    126 |       165 |   4,176 |
| Colombia           | 2020-04-20 |     3,977 |    189 |       804 |   2,984 |
| Argentina          | 2020-04-20 |     2,941 |    136 |       737 |   2,068 |

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
| Iran                 | 2020-04-20 |    83,505 |  5,209 |    59,273 | 19,023 |
| Israel               | 2020-04-20 |    13,713 |    177 |     4,049 |  9,487 |
| Saudi Arabia         | 2020-04-20 |    10,484 |    103 |     1,490 |  8,891 |
| Pakistan             | 2020-04-20 |     8,418 |    176 |     1,970 |  6,272 |
| United Arab Emirates | 2020-04-20 |     7,265 |     43 |     1,360 |  5,862 |
| Qatar                | 2020-04-20 |     6,015 |      9 |       555 |  5,451 |

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
| China        | 2020-04-20 |    83,817 |  4,636 |    77,745 |  1,436 |
| Russia       | 2020-04-20 |    47,121 |    405 |     3,446 | 43,270 |
| India        | 2020-04-20 |    18,539 |    592 |     3,273 | 14,674 |
| Japan        | 2020-04-20 |    10,797 |    236 |     1,159 |  9,402 |
| Korea, South | 2020-04-20 |    10,674 |    236 |     8,114 |  2,324 |
| Australia    | 2020-04-20 |     6,547 |     67 |     4,124 |  2,356 |
| Philippines  | 2020-04-20 |     6,459 |    428 |       613 |  5,418 |
| Malaysia     | 2020-04-20 |     5,425 |     89 |     3,295 |  2,041 |
| Thailand     | 2020-04-20 |     2,792 |     47 |     1,999 |    746 |

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
| Egypt        | 2020-04-20 |     3,333 |    250 |       821 |  2,262 |
| South Africa | 2020-04-20 |     3,300 |     58 |     1,055 |  2,187 |
| Morocco      | 2020-04-20 |     3,046 |    143 |       350 |  2,553 |
| Algeria      | 2020-04-20 |     2,718 |    384 |     1,099 |  1,235 |

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
