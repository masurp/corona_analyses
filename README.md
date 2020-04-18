
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
on 2020-04-18 09:53:37. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-17 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-17 |   172,434 | 22,745 |    42,727 | 106,962 |
| Germany      | 2020-04-17 |   141,397 |  4,352 |    83,114 |  53,931 |
| China        | 2020-04-17 |    83,760 |  4,636 |    77,552 |   1,572 |
| Korea, South | 2020-04-17 |    10,635 |    230 |     7,829 |   2,576 |

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
| Spain          | 2020-04-17 |   190,839 | 20,002 |    74,797 |  96,040 |
| Italy          | 2020-04-17 |   172,434 | 22,745 |    42,727 | 106,962 |
| France         | 2020-04-17 |   149,130 | 18,703 |    35,006 |  95,421 |
| Germany        | 2020-04-17 |   141,397 |  4,352 |    83,114 |  53,931 |
| United Kingdom | 2020-04-17 |   109,769 | 14,607 |       394 |  94,768 |
| Turkey         | 2020-04-17 |    78,546 |  1,769 |     8,631 |  68,146 |
| Belgium        | 2020-04-17 |    36,138 |  5,163 |     7,961 |  23,014 |
| Netherlands    | 2020-04-17 |    30,619 |  3,471 |       315 |  26,833 |
| Switzerland    | 2020-04-17 |    27,078 |  1,327 |    16,400 |   9,351 |
| Portugal       | 2020-04-17 |    19,022 |    657 |       519 |  17,846 |
| Austria        | 2020-04-17 |    14,595 |    431 |     9,704 |   4,460 |
| Ireland        | 2020-04-17 |    13,980 |    530 |        77 |  13,373 |
| Sweden         | 2020-04-17 |    13,216 |  1,400 |       550 |  11,266 |
| Poland         | 2020-04-17 |     8,379 |    332 |       866 |   7,181 |
| Romania        | 2020-04-17 |     8,067 |    411 |     1,508 |   6,148 |
| Denmark        | 2020-04-17 |     7,268 |    336 |     3,571 |   3,361 |
| Norway         | 2020-04-17 |     6,937 |    161 |        32 |   6,744 |
| Czechia        | 2020-04-17 |     6,549 |    173 |     1,174 |   5,202 |
| Serbia         | 2020-04-17 |     5,690 |    110 |       534 |   5,046 |
| Ukraine        | 2020-04-17 |     4,662 |    125 |       246 |   4,291 |
| Finland        | 2020-04-17 |     3,489 |     82 |     1,700 |   1,707 |
| Luxembourg     | 2020-04-17 |     3,480 |     72 |       579 |   2,829 |

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
| US                 | 2020-04-17 |   699,706 | 36,773 |    58,545 | 604,388 |
| Brazil             | 2020-04-17 |    33,682 |  2,141 |    14,026 |  17,515 |
| Canada             | 2020-04-17 |    32,813 |  1,354 |    10,545 |  20,914 |
| Peru               | 2020-04-17 |    13,489 |    300 |     6,541 |   6,648 |
| Chile              | 2020-04-17 |     9,252 |    116 |     3,621 |   5,515 |
| Ecuador            | 2020-04-17 |     8,450 |    421 |       838 |   7,191 |
| Mexico             | 2020-04-17 |     6,297 |    486 |     2,125 |   3,686 |
| Dominican Republic | 2020-04-17 |     4,126 |    200 |       268 |   3,658 |
| Panama             | 2020-04-17 |     4,016 |    109 |        98 |   3,809 |
| Colombia           | 2020-04-17 |     3,439 |    153 |       634 |   2,652 |
| Argentina          | 2020-04-17 |     2,669 |    123 |       666 |   1,880 |

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
| Iran                 | 2020-04-17 |    79,494 |  4,958 |    54,064 | 20,472 |
| Israel               | 2020-04-17 |    12,982 |    151 |     3,126 |  9,705 |
| Saudi Arabia         | 2020-04-17 |     7,142 |     87 |     1,049 |  6,006 |
| Pakistan             | 2020-04-17 |     7,025 |    135 |     1,765 |  5,125 |
| United Arab Emirates | 2020-04-17 |     6,302 |     37 |     1,188 |  5,077 |
| Qatar                | 2020-04-17 |     4,663 |      7 |       464 |  4,192 |

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
| China        | 2020-04-17 |    83,760 |  4,636 |    77,552 |  1,572 |
| Russia       | 2020-04-17 |    32,008 |    273 |     2,590 | 29,145 |
| India        | 2020-04-17 |    14,352 |    486 |     2,041 | 11,825 |
| Korea, South | 2020-04-17 |    10,635 |    230 |     7,829 |  2,576 |
| Japan        | 2020-04-17 |     9,787 |    190 |       935 |  8,662 |
| Australia    | 2020-04-17 |     6,522 |     66 |     3,808 |  2,648 |
| Philippines  | 2020-04-17 |     5,878 |    387 |       487 |  5,004 |
| Malaysia     | 2020-04-17 |     5,251 |     86 |     2,967 |  2,198 |
| Thailand     | 2020-04-17 |     2,700 |     47 |     1,689 |    964 |

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
| Egypt        | 2020-04-17 |     2,844 |    205 |       646 |  1,993 |
| South Africa | 2020-04-17 |     2,783 |     50 |       903 |  1,830 |
| Morocco      | 2020-04-17 |     2,564 |    135 |       281 |  2,148 |
| Algeria      | 2020-04-17 |     2,418 |    364 |       846 |  1,208 |

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
