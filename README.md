
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
on 2020-04-26 09:35:44. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-25 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-25 |   195,351 | 26,384 |    63,120 | 105,847 |
| Germany      | 2020-04-25 |   156,513 |  5,877 |   109,800 |  40,836 |
| China        | 2020-04-25 |    83,909 |  4,636 |    78,175 |   1,098 |
| Korea, South | 2020-04-25 |    10,728 |    242 |     8,717 |   1,769 |

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
| Spain          | 2020-04-25 |   223,759 | 22,902 |    95,708 | 105,149 |
| Italy          | 2020-04-25 |   195,351 | 26,384 |    63,120 | 105,847 |
| France         | 2020-04-25 |   161,644 | 22,648 |    45,372 |  93,624 |
| Germany        | 2020-04-25 |   156,513 |  5,877 |   109,800 |  40,836 |
| United Kingdom | 2020-04-25 |   149,569 | 20,381 |       774 | 128,414 |
| Turkey         | 2020-04-25 |   107,773 |  2,706 |    25,582 |  79,485 |
| Belgium        | 2020-04-25 |    45,325 |  6,917 |    10,417 |  27,991 |
| Netherlands    | 2020-04-25 |    37,384 |  4,424 |       102 |  32,858 |
| Switzerland    | 2020-04-25 |    28,894 |  1,599 |    21,300 |   5,995 |
| Portugal       | 2020-04-25 |    23,392 |    880 |     1,277 |  21,235 |
| Ireland        | 2020-04-25 |    18,561 |  1,063 |     9,233 |   8,265 |
| Sweden         | 2020-04-25 |    18,177 |  2,192 |     1,005 |  14,980 |
| Austria        | 2020-04-25 |    15,148 |    536 |    12,103 |   2,509 |
| Poland         | 2020-04-25 |    11,273 |    524 |     2,126 |   8,623 |
| Romania        | 2020-04-25 |    10,635 |    601 |     2,890 |   7,144 |
| Denmark        | 2020-04-25 |     8,643 |    418 |     5,858 |   2,367 |
| Ukraine        | 2020-04-25 |     8,125 |    201 |       782 |   7,142 |
| Norway         | 2020-04-25 |     7,499 |    201 |        32 |   7,266 |
| Czechia        | 2020-04-25 |     7,352 |    218 |     2,453 |   4,681 |
| Serbia         | 2020-04-25 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-25 |     4,475 |    186 |     2,500 |   1,789 |
| Luxembourg     | 2020-04-25 |     3,711 |     85 |     3,088 |     538 |

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
| US                 | 2020-04-25 |   938,154 | 53,755 |   100,372 | 784,027 |
| Brazil             | 2020-04-25 |    59,324 |  4,057 |    29,160 |  26,107 |
| Canada             | 2020-04-25 |    45,491 |  2,547 |    16,013 |  26,931 |
| Peru               | 2020-04-25 |    25,331 |    700 |     7,797 |  16,834 |
| Ecuador            | 2020-04-25 |    22,719 |    576 |     1,366 |  20,777 |
| Mexico             | 2020-04-25 |    13,842 |  1,305 |     7,149 |   5,388 |
| Chile              | 2020-04-25 |    12,858 |    181 |     6,746 |   5,931 |
| Dominican Republic | 2020-04-25 |     5,926 |    273 |       822 |   4,831 |
| Panama             | 2020-04-25 |     5,538 |    159 |       338 |   5,041 |
| Colombia           | 2020-04-25 |     5,142 |    233 |     1,067 |   3,842 |
| Argentina          | 2020-04-25 |     3,780 |    185 |     1,030 |   2,565 |

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
| Iran                 | 2020-04-25 |    89,328 |  5,650 |    68,193 | 15,485 |
| Saudi Arabia         | 2020-04-25 |    16,299 |    136 |     2,215 | 13,948 |
| Israel               | 2020-04-25 |    15,298 |    199 |     6,435 |  8,664 |
| Pakistan             | 2020-04-25 |    12,723 |    269 |     2,866 |  9,588 |
| United Arab Emirates | 2020-04-25 |     9,813 |     71 |     1,887 |  7,855 |
| Qatar                | 2020-04-25 |     9,358 |     10 |       929 |  8,419 |

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
| China        | 2020-04-25 |    83,909 |  4,636 |    78,175 |  1,098 |
| Russia       | 2020-04-25 |    74,588 |    681 |     6,250 | 67,657 |
| India        | 2020-04-25 |    26,283 |    825 |     5,939 | 19,519 |
| Japan        | 2020-04-25 |    13,231 |    360 |     1,656 | 11,215 |
| Korea, South | 2020-04-25 |    10,728 |    242 |     8,717 |  1,769 |
| Philippines  | 2020-04-25 |     7,294 |    494 |       792 |  6,008 |
| Australia    | 2020-04-25 |     6,694 |     80 |     4,223 |  2,391 |
| Malaysia     | 2020-04-25 |     5,742 |     98 |     3,762 |  1,882 |
| Thailand     | 2020-04-25 |     2,907 |     51 |     2,547 |    309 |

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
| South Africa | 2020-04-25 |     4,361 |     86 |     1,473 |  2,802 |
| Egypt        | 2020-04-25 |     4,319 |    307 |     1,114 |  2,898 |
| Morocco      | 2020-04-25 |     3,897 |    159 |       537 |  3,201 |
| Algeria      | 2020-04-25 |     3,256 |    419 |     1,479 |  1,358 |

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
