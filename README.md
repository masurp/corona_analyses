
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
on 2020-04-15 08:18:40. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-14 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-14 |   162,488 | 21,067 |    37,130 | 104,291 |
| Germany      | 2020-04-14 |   131,359 |  3,294 |    68,200 |  59,865 |
| China        | 2020-04-14 |    83,306 |  3,345 |    78,200 |   1,761 |
| Korea, South | 2020-04-14 |    10,564 |    222 |     7,534 |   2,808 |

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
| Spain          | 2020-04-14 |   172,541 | 18,056 |    67,504 |  86,981 |
| Italy          | 2020-04-14 |   162,488 | 21,067 |    37,130 | 104,291 |
| France         | 2020-04-14 |   131,361 | 15,748 |    29,098 |  86,515 |
| Germany        | 2020-04-14 |   131,359 |  3,294 |    68,200 |  59,865 |
| United Kingdom | 2020-04-14 |    94,845 | 12,129 |       323 |  82,393 |
| Turkey         | 2020-04-14 |    65,111 |  1,403 |     4,799 |  58,909 |
| Belgium        | 2020-04-14 |    31,119 |  4,157 |     6,868 |  20,094 |
| Netherlands    | 2020-04-14 |    27,580 |  2,955 |       297 |  24,328 |
| Switzerland    | 2020-04-14 |    25,936 |  1,174 |    13,700 |  11,062 |
| Portugal       | 2020-04-14 |    17,448 |    567 |       347 |  16,534 |
| Austria        | 2020-04-14 |    14,226 |    384 |     7,633 |   6,209 |
| Ireland        | 2020-04-14 |    11,479 |    406 |        25 |  11,048 |
| Sweden         | 2020-04-14 |    11,445 |  1,033 |       381 |  10,031 |
| Poland         | 2020-04-14 |     7,202 |    263 |       618 |   6,321 |
| Romania        | 2020-04-14 |     6,879 |    351 |     1,051 |   5,477 |
| Denmark        | 2020-04-14 |     6,706 |    299 |     2,689 |   3,718 |
| Norway         | 2020-04-14 |     6,623 |    139 |        32 |   6,452 |
| Czechia        | 2020-04-14 |     6,111 |    161 |       642 |   5,308 |
| Serbia         | 2020-04-14 |     4,465 |     94 |         0 |   4,371 |
| Ukraine        | 2020-04-14 |     3,372 |     98 |       119 |   3,155 |
| Luxembourg     | 2020-04-14 |     3,307 |     67 |       500 |   2,740 |
| Finland        | 2020-04-14 |     3,161 |     64 |       300 |   2,797 |

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
| US                 | 2020-04-14 |   607,670 | 25,832 |    47,763 | 534,075 |
| Canada             | 2020-04-14 |    27,034 |    899 |     8,210 |  17,925 |
| Brazil             | 2020-04-14 |    25,262 |  1,532 |     3,046 |  20,684 |
| Peru               | 2020-04-14 |    10,303 |    230 |     2,869 |   7,204 |
| Chile              | 2020-04-14 |     7,917 |     92 |     2,646 |   5,179 |
| Ecuador            | 2020-04-14 |     7,603 |    369 |       696 |   6,538 |
| Mexico             | 2020-04-14 |     5,014 |    332 |     1,964 |   2,718 |
| Panama             | 2020-04-14 |     3,472 |     94 |        61 |   3,317 |
| Dominican Republic | 2020-04-14 |     3,286 |    183 |       162 |   2,941 |
| Colombia           | 2020-04-14 |     2,979 |    127 |       354 |   2,498 |
| Argentina          | 2020-04-14 |     2,277 |    102 |       559 |   1,616 |

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
| Iran                 | 2020-04-14 |    74,877 |  4,683 |    48,129 | 22,065 |
| Israel               | 2020-04-14 |    12,046 |    123 |     2,195 |  9,728 |
| Pakistan             | 2020-04-14 |     5,837 |     96 |     1,378 |  4,363 |
| Saudi Arabia         | 2020-04-14 |     5,369 |     73 |       889 |  4,407 |
| United Arab Emirates | 2020-04-14 |     4,933 |     28 |       933 |  3,972 |
| Qatar                | 2020-04-14 |     3,428 |      7 |       373 |  3,048 |

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
| China        | 2020-04-14 |    83,306 |  3,345 |    78,200 |  1,761 |
| Russia       | 2020-04-14 |    21,102 |    170 |     1,694 | 19,238 |
| India        | 2020-04-14 |    11,487 |    393 |     1,359 |  9,735 |
| Korea, South | 2020-04-14 |    10,564 |    222 |     7,534 |  2,808 |
| Japan        | 2020-04-14 |     7,645 |    143 |       799 |  6,703 |
| Australia    | 2020-04-14 |     6,415 |     62 |     2,186 |  4,167 |
| Philippines  | 2020-04-14 |     5,223 |    335 |       295 |  4,593 |
| Malaysia     | 2020-04-14 |     4,987 |     82 |     2,478 |  2,427 |
| Thailand     | 2020-04-14 |     2,613 |     41 |     1,405 |  1,167 |

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
| South Africa | 2020-04-14 |     2,415 |     27 |       410 |  1,978 |
| Egypt        | 2020-04-14 |     2,350 |    178 |       589 |  1,583 |
| Algeria      | 2020-04-14 |     2,070 |    326 |       691 |  1,053 |
| Morocco      | 2020-04-14 |     1,888 |    126 |       217 |  1,545 |

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
