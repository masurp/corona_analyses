
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
on 2020-04-27 08:17:32. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-26 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-26 |   197,675 | 26,644 |    64,928 | 106,103 |
| Germany      | 2020-04-26 |   157,770 |  5,976 |   112,000 |  39,794 |
| China        | 2020-04-26 |    83,912 |  4,637 |    78,277 |     998 |
| Korea, South | 2020-04-26 |    10,738 |    243 |     8,764 |   1,731 |

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
| Spain          | 2020-04-26 |   226,629 | 23,190 |   117,727 |  85,712 |
| Italy          | 2020-04-26 |   197,675 | 26,644 |    64,928 | 106,103 |
| France         | 2020-04-26 |   162,220 | 22,890 |    45,681 |  93,649 |
| Germany        | 2020-04-26 |   157,770 |  5,976 |   112,000 |  39,794 |
| United Kingdom | 2020-04-26 |   154,037 | 20,794 |       778 | 132,465 |
| Turkey         | 2020-04-26 |   110,130 |  2,805 |    29,140 |  78,185 |
| Belgium        | 2020-04-26 |    46,134 |  7,094 |    10,785 |  28,255 |
| Netherlands    | 2020-04-26 |    38,040 |  4,491 |       117 |  33,432 |
| Switzerland    | 2020-04-26 |    29,061 |  1,610 |    21,800 |   5,651 |
| Portugal       | 2020-04-26 |    23,864 |    903 |     1,329 |  21,632 |
| Ireland        | 2020-04-26 |    19,262 |  1,087 |     9,233 |   8,942 |
| Sweden         | 2020-04-26 |    18,640 |  2,194 |     1,005 |  15,441 |
| Austria        | 2020-04-26 |    15,225 |    542 |    12,282 |   2,401 |
| Poland         | 2020-04-26 |    11,617 |    535 |     2,265 |   8,817 |
| Romania        | 2020-04-26 |    11,036 |    619 |     3,054 |   7,363 |
| Denmark        | 2020-04-26 |     8,773 |    422 |     5,994 |   2,357 |
| Ukraine        | 2020-04-26 |     8,617 |    209 |       840 |   7,568 |
| Norway         | 2020-04-26 |     7,527 |    201 |        32 |   7,294 |
| Czechia        | 2020-04-26 |     7,404 |    220 |     2,545 |   4,639 |
| Serbia         | 2020-04-26 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-26 |     4,576 |    190 |     2,500 |   1,886 |
| Luxembourg     | 2020-04-26 |     3,723 |     88 |     3,104 |     531 |

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
| US                 | 2020-04-26 |   965,785 | 54,881 |   106,988 | 803,916 |
| Brazil             | 2020-04-26 |    63,100 |  4,286 |    30,152 |  28,662 |
| Canada             | 2020-04-26 |    47,145 |  2,661 |    16,883 |  27,601 |
| Peru               | 2020-04-26 |    27,517 |    728 |     8,088 |  18,701 |
| Ecuador            | 2020-04-26 |    22,719 |    576 |     1,366 |  20,777 |
| Mexico             | 2020-04-26 |    14,677 |  1,351 |     8,354 |   4,972 |
| Chile              | 2020-04-26 |    13,331 |    189 |     7,024 |   6,118 |
| Dominican Republic | 2020-04-26 |     6,135 |    278 |       910 |   4,947 |
| Panama             | 2020-04-26 |     5,779 |    165 |       338 |   5,276 |
| Colombia           | 2020-04-26 |     5,379 |    244 |     1,133 |   4,002 |
| Argentina          | 2020-04-26 |     3,892 |    192 |     1,107 |   2,593 |

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
| Iran                 | 2020-04-26 |    90,481 |  5,710 |    69,657 | 15,114 |
| Saudi Arabia         | 2020-04-26 |    17,522 |    139 |     2,357 | 15,026 |
| Israel               | 2020-04-26 |    15,443 |    201 |     6,731 |  8,511 |
| Pakistan             | 2020-04-26 |    13,328 |    281 |     2,936 | 10,111 |
| United Arab Emirates | 2020-04-26 |    10,349 |     76 |     1,978 |  8,295 |
| Qatar                | 2020-04-26 |    10,287 |     10 |     1,012 |  9,265 |

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
| China        | 2020-04-26 |    83,912 |  4,637 |    78,277 |    998 |
| Russia       | 2020-04-26 |    80,949 |    747 |     6,767 | 73,435 |
| India        | 2020-04-26 |    27,890 |    881 |     6,523 | 20,486 |
| Japan        | 2020-04-26 |    13,441 |    372 |     1,809 | 11,260 |
| Korea, South | 2020-04-26 |    10,738 |    243 |     8,764 |  1,731 |
| Philippines  | 2020-04-26 |     7,579 |    501 |       862 |  6,216 |
| Australia    | 2020-04-26 |     6,714 |     83 |     5,541 |  1,090 |
| Malaysia     | 2020-04-26 |     5,780 |     98 |     3,862 |  1,820 |
| Thailand     | 2020-04-26 |     2,922 |     51 |     2,594 |    277 |

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
| South Africa | 2020-04-26 |     4,546 |     87 |     1,473 |  2,986 |
| Egypt        | 2020-04-26 |     4,534 |    317 |     1,176 |  3,041 |
| Morocco      | 2020-04-26 |     4,065 |    161 |       593 |  3,311 |
| Algeria      | 2020-04-26 |     3,382 |    425 |     1,508 |  1,449 |

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
