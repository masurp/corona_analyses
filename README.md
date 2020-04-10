
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
on 2020-04-10 09:38:17. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-09 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-09 |   143,626 | 18,279 |    28,470 | 96,877 |
| Germany      | 2020-04-09 |   118,181 |  2,607 |    52,407 | 63,167 |
| China        | 2020-04-09 |    82,883 |  3,339 |    77,679 |  1,865 |
| Korea, South | 2020-04-09 |    10,423 |    204 |     6,973 |  3,246 |

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
| Spain          | 2020-04-09 |   153,222 | 15,447 |    52,165 | 85,610 |
| Italy          | 2020-04-09 |   143,626 | 18,279 |    28,470 | 96,877 |
| France         | 2020-04-09 |   118,781 | 12,228 |    23,413 | 83,140 |
| Germany        | 2020-04-09 |   118,181 |  2,607 |    52,407 | 63,167 |
| United Kingdom | 2020-04-09 |    65,872 |  7,993 |       359 | 57,520 |
| Turkey         | 2020-04-09 |    42,282 |    908 |     2,142 | 39,232 |
| Belgium        | 2020-04-09 |    24,983 |  2,523 |     5,164 | 17,296 |
| Switzerland    | 2020-04-09 |    24,051 |    948 |    10,600 | 12,503 |
| Netherlands    | 2020-04-09 |    21,903 |  2,403 |       278 | 19,222 |
| Portugal       | 2020-04-09 |    13,956 |    409 |       205 | 13,342 |
| Austria        | 2020-04-09 |    13,244 |    295 |     5,240 |  7,709 |
| Sweden         | 2020-04-09 |     9,141 |    793 |       205 |  8,143 |
| Ireland        | 2020-04-09 |     6,574 |    263 |        25 |  6,286 |
| Norway         | 2020-04-09 |     6,211 |    108 |        32 |  6,071 |
| Denmark        | 2020-04-09 |     5,830 |    237 |     1,883 |  3,710 |
| Czechia        | 2020-04-09 |     5,569 |    112 |       301 |  5,156 |

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
| US      | 2020-04-09 |   461,437 | 16,478 |    25,410 | 419,549 |
| Canada  | 2020-04-09 |    20,654 |    503 |     5,162 |  14,989 |
| Brazil  | 2020-04-09 |    18,092 |    950 |       173 |  16,969 |

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
| Iran     | 2020-04-09 |    66,220 |  4,110 |    32,309 | 29,801 |
| Israel   | 2020-04-09 |     9,968 |     86 |     1,011 |  8,871 |
| Pakistan | 2020-04-09 |     4,489 |     65 |       572 |  3,852 |
| Qatar    | 2020-04-09 |     2,376 |      6 |       206 |  2,164 |

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
| China        | 2020-04-09 |    82,883 |  3,339 |    77,679 |  1,865 |
| Korea, South | 2020-04-09 |    10,423 |    204 |     6,973 |  3,246 |
| Japan        | 2020-04-09 |     4,667 |     94 |       632 |  3,941 |
| Malaysia     | 2020-04-09 |     4,228 |     67 |     1,608 |  2,553 |

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
