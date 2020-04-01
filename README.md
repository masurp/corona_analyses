
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
on 2020-04-01 08:31:30. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-03-31 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-03-31 |   105,792 | 12,428 |    15,729 | 77,635 |
| China        | 2020-03-31 |    82,279 |  3,309 |    76,206 |  2,764 |
| Germany      | 2020-03-31 |    71,808 |    775 |    16,100 | 54,933 |
| Korea, South | 2020-03-31 |     9,786 |    162 |     5,408 |  4,216 |

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
| Italy          | 2020-03-31 |   105,792 | 12,428 |    15,729 | 77,635 |
| Spain          | 2020-03-31 |    95,923 |  8,464 |    19,259 | 68,200 |
| Germany        | 2020-03-31 |    71,808 |    775 |    16,100 | 54,933 |
| France         | 2020-03-31 |    52,827 |  3,532 |     9,513 | 39,782 |
| United Kingdom | 2020-03-31 |    25,481 |  1,793 |       179 | 23,509 |
| Switzerland    | 2020-03-31 |    16,605 |    433 |     1,823 | 14,349 |
| Turkey         | 2020-03-31 |    13,531 |    214 |       243 | 13,074 |
| Belgium        | 2020-03-31 |    12,775 |    705 |     1,696 | 10,374 |
| Netherlands    | 2020-03-31 |    12,667 |  1,040 |       253 | 11,374 |
| Austria        | 2020-03-31 |    10,180 |    128 |     1,095 |  8,957 |
| Portugal       | 2020-03-31 |     7,443 |    160 |        43 |  7,240 |
| Norway         | 2020-03-31 |     4,641 |     39 |        13 |  4,589 |
| Sweden         | 2020-03-31 |     4,435 |    180 |        16 |  4,239 |
| Czechia        | 2020-03-31 |     3,308 |     31 |        45 |  3,232 |
| Ireland        | 2020-03-31 |     3,235 |     71 |         5 |  3,159 |
| Denmark        | 2020-03-31 |     3,039 |     90 |        77 |  2,872 |

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
| US      | 2020-03-31 |   188,172 |  3,873 |     7,024 | 177,275 |
| Canada  | 2020-03-31 |     8,527 |    101 |     1,592 |   6,834 |
| Brazil  | 2020-03-31 |     5,717 |    201 |       127 |   5,389 |

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
| Iran     | 2020-03-31 |    44,605 |  2,898 |    14,656 | 27,051 |
| Israel   | 2020-03-31 |     5,358 |     20 |       224 |  5,114 |
| Pakistan | 2020-03-31 |     1,938 |     26 |        76 |  1,836 |
| Qatar    | 2020-03-31 |       781 |      2 |        62 |    717 |

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
| China        | 2020-03-31 |    82,279 |  3,309 |    76,206 |  2,764 |
| Korea, South | 2020-03-31 |     9,786 |    162 |     5,408 |  4,216 |
| Malaysia     | 2020-03-31 |     2,766 |     43 |       537 |  2,186 |
| Japan        | 2020-03-31 |     1,953 |     56 |       424 |  1,473 |

<img src="figures/asia-1.png" width="100%" />

### 3\. Alternative visualizations

One thing that is constantly debatted is how to visualize growth at all.
Log-transform the y-axis or not? Plot against the date? Plot against
days after 100th case? Plot something entirely different?

Here, I would like to explain some differences between visualizations
that have been used in the media. All of them are helpful in their own
regard.

1.  LEFT: Here, I plotted total cases against days after the 100th cases
    *without* logarithmizing the y-axis.

2.  MIDDLE: The y-axis is logarithmized. This figure is often shown in
    the news.

3.  RIGHT: New cases per 7 days (y-axis) are plotted against total cases
    (x-axis), both axes are logarithmized.

We see clearly that each plot has benefits and weaknesses. The first
example provides perhaps the best comparison of the total numbers and
shows quite drastically how exponential growth looks likes. S-curves
represent positive developments towars a slower growth. Yet, changes are
barely identifiable. The second example makes the actual growth more
comparable and by logarithmizing the y-axsis, we can actually see
changes in the growth. Here, it seesm that most countries are actually
starting to slow the growth. Finally, the last example is hard to
understand generally, but it shows best whether some sort of measure is
working. The curve needs to sink drastically, otherwise, the growth is
continuing uncontrollibly.

<img src="figures/unnamed-chunk-6-1.png" width="100%" />
