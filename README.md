
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
on 2020-04-23 07:59:01. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-22 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-22 |   187,327 | 25,085 |    54,543 | 107,699 |
| Germany      | 2020-04-22 |   150,648 |  5,279 |    99,400 |  45,969 |
| China        | 2020-04-22 |    83,868 |  4,636 |    77,861 |   1,371 |
| Korea, South | 2020-04-22 |    10,694 |    238 |     8,277 |   2,179 |

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
| Spain          | 2020-04-22 |   208,389 | 21,717 |    85,915 | 100,757 |
| Italy          | 2020-04-22 |   187,327 | 25,085 |    54,543 | 107,699 |
| France         | 2020-04-22 |   157,125 | 21,373 |    41,326 |  94,426 |
| Germany        | 2020-04-22 |   150,648 |  5,279 |    99,400 |  45,969 |
| United Kingdom | 2020-04-22 |   134,638 | 18,151 |       683 | 115,804 |
| Turkey         | 2020-04-22 |    98,674 |  2,376 |    16,477 |  79,821 |
| Belgium        | 2020-04-22 |    41,889 |  6,262 |     9,433 |  26,194 |
| Netherlands    | 2020-04-22 |    35,032 |  4,068 |       101 |  30,863 |
| Switzerland    | 2020-04-22 |    28,268 |  1,509 |    19,900 |   6,859 |
| Portugal       | 2020-04-22 |    21,982 |    785 |     1,143 |  20,054 |
| Ireland        | 2020-04-22 |    16,671 |    769 |     9,233 |   6,669 |
| Sweden         | 2020-04-22 |    16,004 |  1,937 |       550 |  13,517 |
| Austria        | 2020-04-22 |    14,925 |    510 |    11,328 |   3,087 |
| Poland         | 2020-04-22 |    10,169 |    426 |     1,513 |   8,230 |
| Romania        | 2020-04-22 |     9,710 |    524 |     2,406 |   6,780 |
| Denmark        | 2020-04-22 |     8,108 |    384 |     5,276 |   2,448 |
| Norway         | 2020-04-22 |     7,338 |    187 |        32 |   7,119 |
| Czechia        | 2020-04-22 |     7,132 |    208 |     1,989 |   4,935 |
| Serbia         | 2020-04-22 |     6,630 |    125 |       870 |   5,635 |
| Ukraine        | 2020-04-22 |     6,592 |    174 |       424 |   5,994 |
| Finland        | 2020-04-22 |     4,129 |    149 |     2,000 |   1,980 |
| Luxembourg     | 2020-04-22 |     3,654 |     80 |       711 |   2,863 |

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
| US                 | 2020-04-22 |   839,675 | 46,583 |    77,366 | 715,726 |
| Brazil             | 2020-04-22 |    45,757 |  2,906 |    25,318 |  17,533 |
| Canada             | 2020-04-22 |    41,648 |  2,075 |    14,454 |  25,119 |
| Peru               | 2020-04-22 |    19,250 |    530 |     7,027 |  11,693 |
| Chile              | 2020-04-22 |    11,296 |    160 |     5,386 |   5,750 |
| Ecuador            | 2020-04-22 |    10,850 |    537 |     1,262 |   9,051 |
| Mexico             | 2020-04-22 |     9,501 |    857 |     2,627 |   6,017 |
| Dominican Republic | 2020-04-22 |     5,300 |    260 |       581 |   4,459 |
| Panama             | 2020-04-22 |     4,821 |    141 |       231 |   4,449 |
| Colombia           | 2020-04-22 |     4,356 |    206 |       870 |   3,280 |
| Argentina          | 2020-04-22 |     3,144 |    152 |       872 |   2,120 |

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
| Iran                 | 2020-04-22 |    85,996 |  5,391 |    63,113 | 17,492 |
| Israel               | 2020-04-22 |    14,498 |    189 |     5,215 |  9,094 |
| Saudi Arabia         | 2020-04-22 |    12,772 |    114 |     1,812 | 10,846 |
| Pakistan             | 2020-04-22 |    10,076 |    212 |     2,156 |  7,708 |
| United Arab Emirates | 2020-04-22 |     8,238 |     52 |     1,546 |  6,640 |
| Qatar                | 2020-04-22 |     7,141 |     10 |       689 |  6,442 |

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
| China        | 2020-04-22 |    83,868 |  4,636 |    77,861 |  1,371 |
| Russia       | 2020-04-22 |    57,999 |    513 |     4,420 | 53,066 |
| India        | 2020-04-22 |    21,370 |    681 |     4,370 | 16,319 |
| Japan        | 2020-04-22 |    11,512 |    281 |     1,356 |  9,875 |
| Korea, South | 2020-04-22 |    10,694 |    238 |     8,277 |  2,179 |
| Philippines  | 2020-04-22 |     6,710 |    446 |       693 |  5,571 |
| Australia    | 2020-04-22 |     6,547 |     67 |     4,124 |  2,356 |
| Malaysia     | 2020-04-22 |     5,532 |     93 |     3,452 |  1,987 |
| Thailand     | 2020-04-22 |     2,826 |     49 |     2,352 |    425 |

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
| Egypt        | 2020-04-22 |     3,659 |    276 |       935 |  2,448 |
| South Africa | 2020-04-22 |     3,635 |     65 |     1,055 |  2,515 |
| Morocco      | 2020-04-22 |     3,446 |    149 |       417 |  2,880 |
| Algeria      | 2020-04-22 |     2,910 |    402 |     1,204 |  1,304 |

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
