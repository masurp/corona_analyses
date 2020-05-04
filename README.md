
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
on 2020-05-04 07:31:36. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-03 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-03 |   210,717 | 28,884 |    81,654 | 100,179 |
| Germany      | 2020-05-03 |   165,664 |  6,866 |   130,600 |  28,198 |
| China        | 2020-05-03 |    83,964 |  4,637 |    78,684 |     643 |
| Korea, South | 2020-05-03 |    10,801 |    252 |     9,217 |   1,332 |

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
| Spain          | 2020-05-03 |   217,466 | 25,264 |   118,902 |  73,300 |
| Italy          | 2020-05-03 |   210,717 | 28,884 |    81,654 | 100,179 |
| United Kingdom | 2020-05-03 |   187,842 | 28,520 |       901 | 158,421 |
| France         | 2020-05-03 |   168,925 | 24,900 |    50,885 |  93,140 |
| Germany        | 2020-05-03 |   165,664 |  6,866 |   130,600 |  28,198 |
| Turkey         | 2020-05-03 |   126,045 |  3,397 |    63,151 |  59,497 |
| Belgium        | 2020-05-03 |    49,906 |  7,844 |    12,309 |  29,753 |
| Netherlands    | 2020-05-03 |    40,769 |  5,072 |       138 |  35,559 |
| Switzerland    | 2020-05-03 |    29,905 |  1,762 |    24,500 |   3,643 |
| Portugal       | 2020-05-03 |    25,282 |  1,043 |     1,689 |  22,550 |
| Sweden         | 2020-05-03 |    22,317 |  2,679 |     1,005 |  18,633 |
| Ireland        | 2020-05-03 |    21,506 |  1,303 |    13,386 |   6,817 |
| Austria        | 2020-05-03 |    15,597 |    598 |    13,228 |   1,771 |
| Poland         | 2020-05-03 |    13,693 |    678 |     3,945 |   9,070 |
| Romania        | 2020-05-03 |    13,163 |    790 |     4,869 |   7,504 |
| Ukraine        | 2020-05-03 |    11,913 |    288 |     1,548 |  10,077 |
| Denmark        | 2020-05-03 |     9,721 |    484 |     7,183 |   2,054 |
| Serbia         | 2020-05-03 |     9,464 |    193 |     1,551 |   7,720 |
| Norway         | 2020-05-03 |     7,847 |    211 |        32 |   7,604 |
| Czechia        | 2020-05-03 |     7,781 |    248 |     3,587 |   3,946 |
| Finland        | 2020-05-03 |     5,254 |    230 |     3,000 |   2,024 |
| Luxembourg     | 2020-05-03 |     3,824 |     96 |     3,379 |     349 |

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
| US                 | 2020-05-03 | 1,158,040 | 67,682 |   180,152 | 910,206 |
| Brazil             | 2020-05-03 |   101,826 |  7,051 |    42,991 |  51,784 |
| Canada             | 2020-05-03 |    60,504 |  3,795 |    24,921 |  31,788 |
| Peru               | 2020-05-03 |    45,928 |  1,286 |    13,550 |  31,092 |
| Ecuador            | 2020-05-03 |    29,538 |  1,564 |     3,300 |  24,674 |
| Mexico             | 2020-05-03 |    23,471 |  2,154 |    13,447 |   7,870 |
| Chile              | 2020-05-03 |    19,663 |    260 |    10,041 |   9,362 |
| Dominican Republic | 2020-05-03 |     7,954 |    333 |     1,606 |   6,015 |
| Colombia           | 2020-05-03 |     7,668 |    340 |     1,722 |   5,606 |
| Panama             | 2020-05-03 |     7,090 |    197 |       641 |   6,252 |
| Argentina          | 2020-05-03 |     4,783 |    246 |     1,354 |   3,183 |

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
| Iran                 | 2020-05-03 |    97,424 |  6,203 |    78,422 | 12,799 |
| Saudi Arabia         | 2020-05-03 |    27,011 |    184 |     4,134 | 22,693 |
| Pakistan             | 2020-05-03 |    20,084 |    457 |     5,114 | 14,513 |
| Israel               | 2020-05-03 |    16,208 |    232 |     9,749 |  6,227 |
| Qatar                | 2020-05-03 |    15,551 |     12 |     1,664 | 13,875 |
| United Arab Emirates | 2020-05-03 |    14,163 |    126 |     2,763 | 11,274 |

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
| Russia       | 2020-05-03 |   134,687 |  1,280 |    16,639 | 116,768 |
| China        | 2020-05-03 |    83,964 |  4,637 |    78,684 |     643 |
| India        | 2020-05-03 |    42,505 |  1,391 |    11,775 |  29,339 |
| Japan        | 2020-05-03 |    14,877 |    487 |     3,981 |  10,409 |
| Korea, South | 2020-05-03 |    10,801 |    252 |     9,217 |   1,332 |
| Philippines  | 2020-05-03 |     9,223 |    607 |     1,214 |   7,402 |
| Australia    | 2020-05-03 |     6,822 |     95 |     5,849 |     878 |
| Malaysia     | 2020-05-03 |     6,298 |    105 |     4,413 |   1,780 |
| Thailand     | 2020-05-03 |     2,969 |     54 |     2,739 |     176 |

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
| South Africa | 2020-05-03 |     6,783 |    131 |     2,549 |  4,103 |
| Egypt        | 2020-05-03 |     6,465 |    429 |     1,562 |  4,474 |
| Morocco      | 2020-05-03 |     4,903 |    174 |     1,438 |  3,291 |
| Algeria      | 2020-05-03 |     4,474 |    463 |     1,936 |  2,075 |

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
