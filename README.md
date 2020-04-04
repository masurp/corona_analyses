
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
on 2020-04-04 09:54:14. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-03 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-03 |   119,827 | 14,681 |    19,758 | 85,388 |
| Germany      | 2020-04-03 |    91,159 |  1,275 |    24,575 | 65,309 |
| China        | 2020-04-03 |    82,511 |  3,326 |    76,760 |  2,425 |
| Korea, South | 2020-04-03 |    10,062 |    174 |     6,021 |  3,867 |

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
| Italy          | 2020-04-03 |   119,827 | 14,681 |    19,758 | 85,388 |
| Spain          | 2020-04-03 |   119,199 | 11,198 |    30,513 | 77,488 |
| Germany        | 2020-04-03 |    91,159 |  1,275 |    24,575 | 65,309 |
| France         | 2020-04-03 |    65,202 |  6,520 |    14,135 | 44,547 |
| United Kingdom | 2020-04-03 |    38,689 |  3,611 |       208 | 34,870 |
| Turkey         | 2020-04-03 |    20,921 |    425 |       484 | 20,012 |
| Switzerland    | 2020-04-03 |    19,606 |    591 |     4,846 | 14,169 |
| Belgium        | 2020-04-03 |    16,770 |  1,143 |     2,872 | 12,755 |
| Netherlands    | 2020-04-03 |    15,821 |  1,490 |       260 | 14,071 |
| Austria        | 2020-04-03 |    11,524 |    168 |     2,022 |  9,334 |
| Portugal       | 2020-04-03 |     9,886 |    246 |        68 |  9,572 |
| Sweden         | 2020-04-03 |     6,131 |    358 |       205 |  5,568 |
| Norway         | 2020-04-03 |     5,370 |     59 |        32 |  5,279 |
| Ireland        | 2020-04-03 |     4,273 |    120 |         5 |  4,148 |
| Czechia        | 2020-04-03 |     4,091 |     53 |        72 |  3,966 |
| Denmark        | 2020-04-03 |     3,946 |    139 |     1,287 |  2,520 |

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
| US      | 2020-04-03 |   275,586 |  7,087 |     9,707 | 258,792 |
| Canada  | 2020-04-03 |    12,437 |    179 |     2,175 |  10,083 |
| Brazil  | 2020-04-03 |     9,056 |    359 |       127 |   8,570 |

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
| Iran     | 2020-04-03 |    53,183 |  3,294 |    17,935 | 31,954 |
| Israel   | 2020-04-03 |     7,428 |     40 |       403 |  6,985 |
| Pakistan | 2020-04-03 |     2,686 |     40 |       126 |  2,520 |
| Qatar    | 2020-04-03 |     1,075 |      3 |        93 |    979 |

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
| China        | 2020-04-03 |    82,511 |  3,326 |    76,760 |  2,425 |
| Korea, South | 2020-04-03 |    10,062 |    174 |     6,021 |  3,867 |
| Malaysia     | 2020-04-03 |     3,333 |     53 |       827 |  2,453 |
| Japan        | 2020-04-03 |     2,617 |     63 |       514 |  2,040 |

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
