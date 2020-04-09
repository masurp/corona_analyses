
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
on 2020-04-09 07:37:29. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-08 at 23:59:00. Also bear in mind that the
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

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| Italy        | 2020-04-08 |   139,422 | 17,669 |    26,491 | 95,262 |
| Germany      | 2020-04-08 |   113,296 |  2,349 |    46,300 | 64,647 |
| China        | 2020-04-08 |    82,809 |  3,337 |    77,567 |  1,905 |
| Korea, South | 2020-04-08 |    10,384 |    200 |     6,776 |  3,408 |

<img src="figures/unnamed-chunk-2-1.png" width="100%" />

### 2\. Worldwide developments

#### Europe

<caption>

(\#tab:europe)

</caption>

<caption>

\*\*

</caption>

| country        |    date    | confirmed | deaths | recovered | active |
| :------------- | :--------: | --------: | -----: | --------: | -----: |
| Spain          | 2020-04-08 |   148,220 | 14,792 |    48,021 | 85,407 |
| Italy          | 2020-04-08 |   139,422 | 17,669 |    26,491 | 95,262 |
| France         | 2020-04-08 |   113,959 | 10,887 |    21,452 | 81,620 |
| Germany        | 2020-04-08 |   113,296 |  2,349 |    46,300 | 64,647 |
| United Kingdom | 2020-04-08 |    61,474 |  7,111 |       345 | 54,018 |
| Turkey         | 2020-04-08 |    38,226 |    812 |     1,846 | 35,568 |
| Belgium        | 2020-04-08 |    23,403 |  2,240 |     4,681 | 16,482 |
| Switzerland    | 2020-04-08 |    23,280 |    895 |     9,800 | 12,585 |
| Netherlands    | 2020-04-08 |    20,682 |  2,255 |       272 | 18,155 |
| Portugal       | 2020-04-08 |    13,141 |    380 |       196 | 12,565 |
| Austria        | 2020-04-08 |    12,942 |    273 |     4,512 |  8,157 |
| Sweden         | 2020-04-08 |     8,419 |    687 |       205 |  7,527 |
| Norway         | 2020-04-08 |     6,086 |    101 |        32 |  5,953 |
| Ireland        | 2020-04-08 |     6,074 |    235 |        25 |  5,814 |
| Denmark        | 2020-04-08 |     5,597 |    218 |     1,763 |  3,616 |
| Czechia        | 2020-04-08 |     5,312 |     99 |       233 |  4,980 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<caption>

\*\*

</caption>

| country |    date    | confirmed | deaths | recovered |  active |
| :------ | :--------: | --------: | -----: | --------: | ------: |
| US      | 2020-04-08 |   429,052 | 14,695 |    23,559 | 390,798 |
| Canada  | 2020-04-08 |    19,141 |    407 |     4,154 |  14,580 |
| Brazil  | 2020-04-08 |    16,170 |    819 |       127 |  15,224 |

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<caption>

\*\*

</caption>

| country  |    date    | confirmed | deaths | recovered | active |
| :------- | :--------: | --------: | -----: | --------: | -----: |
| Iran     | 2020-04-08 |    64,586 |  3,993 |    29,812 | 30,781 |
| Israel   | 2020-04-08 |     9,404 |     73 |       801 |  8,530 |
| Pakistan | 2020-04-08 |     4,263 |     61 |       467 |  3,735 |
| Qatar    | 2020-04-08 |     2,210 |      6 |       178 |  2,026 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| China        | 2020-04-08 |    82,809 |  3,337 |    77,567 |  1,905 |
| Korea, South | 2020-04-08 |    10,384 |    200 |     6,776 |  3,408 |
| Japan        | 2020-04-08 |     4,257 |     93 |       622 |  3,542 |
| Malaysia     | 2020-04-08 |     4,119 |     65 |     1,487 |  2,567 |

<img src="figures/asia-1.png" width="100%" />

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

<img src="figures/unnamed-chunk-6-1.png" width="100%" />
