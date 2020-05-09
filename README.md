
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
on 2020-05-09 17:10:20. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-08 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-08 |   217,185 | 30,201 |    99,023 | 87,961 |
| Germany      | 2020-05-08 |   170,588 |  7,510 |   141,700 | 21,378 |
| China        | 2020-05-08 |    83,976 |  4,637 |    78,993 |    346 |
| Korea, South | 2020-05-08 |    10,840 |    256 |     9,568 |  1,016 |

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
| Spain          | 2020-05-08 |   222,857 | 26,299 |   131,148 |  65,410 |
| Italy          | 2020-05-08 |   217,185 | 30,201 |    99,023 |  87,961 |
| United Kingdom | 2020-05-08 |   212,629 | 31,316 |       997 | 180,316 |
| France         | 2020-05-08 |   176,202 | 26,233 |    55,892 |  94,077 |
| Germany        | 2020-05-08 |   170,588 |  7,510 |   141,700 |  21,378 |
| Turkey         | 2020-05-08 |   135,569 |  3,689 |    86,396 |  45,484 |
| Belgium        | 2020-05-08 |    52,011 |  8,521 |    13,201 |  30,289 |
| Netherlands    | 2020-05-08 |    42,292 |  5,377 |       147 |  36,768 |
| Switzerland    | 2020-05-08 |    30,207 |  1,823 |    26,100 |   2,284 |
| Portugal       | 2020-05-08 |    27,268 |  1,114 |     2,422 |  23,732 |
| Sweden         | 2020-05-08 |    25,265 |  3,175 |     4,971 |  17,119 |
| Ireland        | 2020-05-08 |    22,541 |  1,429 |    17,110 |   4,002 |
| Austria        | 2020-05-08 |    15,774 |    614 |    13,836 |   1,324 |
| Poland         | 2020-05-08 |    15,366 |    776 |     5,184 |   9,406 |
| Romania        | 2020-05-08 |    14,811 |    923 |     6,423 |   7,465 |
| Ukraine        | 2020-05-08 |    14,195 |    361 |     2,706 |  11,128 |
| Denmark        | 2020-05-08 |    10,416 |    522 |     8,125 |   1,769 |
| Serbia         | 2020-05-08 |     9,943 |    209 |     2,453 |   7,281 |
| Czechia        | 2020-05-08 |     8,077 |    273 |     4,413 |   3,391 |
| Norway         | 2020-05-08 |     8,070 |    218 |        32 |   7,820 |
| Finland        | 2020-05-08 |     5,738 |    260 |     4,000 |   1,478 |
| Luxembourg     | 2020-05-08 |     3,871 |    100 |     3,526 |     245 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country            |    date    | confirmed | deaths | recovered |    active |
| :----------------- | :--------: | --------: | -----: | --------: | --------: |
| US                 | 2020-05-08 | 1,283,929 | 77,180 |   198,993 | 1,007,756 |
| Brazil             | 2020-05-08 |   146,894 | 10,017 |    59,297 |    77,580 |
| Canada             | 2020-05-08 |    67,674 |  4,697 |    30,239 |    32,738 |
| Peru               | 2020-05-08 |    61,847 |  1,714 |    19,012 |    41,121 |
| Mexico             | 2020-05-08 |    31,522 |  3,160 |    20,314 |     8,048 |
| Ecuador            | 2020-05-08 |    28,818 |  1,704 |     3,433 |    23,681 |
| Chile              | 2020-05-08 |    25,972 |    294 |    12,160 |    13,518 |
| Colombia           | 2020-05-08 |    10,051 |    428 |     2,424 |     7,199 |
| Dominican Republic | 2020-05-08 |     9,376 |    380 |     2,286 |     6,710 |
| Panama             | 2020-05-08 |     8,070 |    231 |       886 |     6,953 |
| Argentina          | 2020-05-08 |     5,611 |    293 |     1,659 |     3,659 |

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
| Iran                 | 2020-05-08 |   104,691 |  6,541 |    83,837 | 14,313 |
| Saudi Arabia         | 2020-05-08 |    35,432 |    229 |     9,120 | 26,083 |
| Pakistan             | 2020-05-08 |    26,435 |    599 |     7,530 | 18,306 |
| Qatar                | 2020-05-08 |    20,201 |     12 |     2,370 | 17,819 |
| United Arab Emirates | 2020-05-08 |    16,793 |    174 |     3,837 | 12,782 |
| Israel               | 2020-05-08 |    16,436 |    245 |    11,229 |  4,962 |

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
| Russia       | 2020-05-08 |   187,859 |  1,723 |    26,608 | 159,528 |
| China        | 2020-05-08 |    83,976 |  4,637 |    78,993 |     346 |
| India        | 2020-05-08 |    59,695 |  1,985 |    17,887 |  39,823 |
| Japan        | 2020-05-08 |    15,575 |    590 |     5,146 |   9,839 |
| Korea, South | 2020-05-08 |    10,840 |    256 |     9,568 |   1,016 |
| Philippines  | 2020-05-08 |    10,463 |    696 |     1,734 |   8,033 |
| Australia    | 2020-05-08 |     6,918 |     97 |     6,122 |     699 |
| Malaysia     | 2020-05-08 |     6,535 |    107 |     4,864 |   1,564 |
| Thailand     | 2020-05-08 |     3,000 |     55 |     2,784 |     161 |

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
| South Africa | 2020-05-08 |     8,895 |    178 |     3,153 |  5,564 |
| Egypt        | 2020-05-08 |     8,476 |    503 |     1,945 |  6,028 |
| Morocco      | 2020-05-08 |     5,711 |    186 |     2,324 |  3,201 |
| Algeria      | 2020-05-08 |     5,369 |    488 |     2,467 |  2,414 |

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
shows quite drastically how exponential growth curves look likes (bear
in mind that I cut off the growth curve of the US, which actually
extends to more than 1 million cases. I did this to make the other
growth curves more identifiable). S-curves represent positive
developments towards a slower growth. Yet, changes are barely
identifiable. The second example makes the actual growth more comparable
and by logarithmizing the y-axsis, we can actually see changes in the
growth. Here, it seesm that most countries are actually starting to slow
the growth. Finally, the last example is hard to understand generally,
but it shows best whether some sort of measure is working. The curve
needs to sink drastically, otherwise, the growth is continuing
uncontrollibly.

<img src="figures/unnamed-chunk-7-1.png" width="100%" />
