
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
on 2020-04-12 22:42:51. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-11 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-11 |   152,271 | 19,468 |    32,534 | 100,269 |
| Germany      | 2020-04-11 |   124,908 |  2,736 |    57,400 |  64,772 |
| China        | 2020-04-11 |    83,014 |  3,343 |    77,877 |   1,794 |
| Korea, South | 2020-04-11 |    10,480 |    211 |     7,243 |   3,026 |

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
| Spain          | 2020-04-11 |   163,027 | 16,606 |    59,109 |  87,312 |
| Italy          | 2020-04-11 |   152,271 | 19,468 |    32,534 | 100,269 |
| France         | 2020-04-11 |   130,727 | 13,851 |    26,663 |  90,213 |
| Germany        | 2020-04-11 |   124,908 |  2,736 |    57,400 |  64,772 |
| United Kingdom | 2020-04-11 |    79,874 |  9,892 |       622 |  69,360 |
| Turkey         | 2020-04-11 |    52,167 |  1,101 |     2,965 |  48,101 |
| Belgium        | 2020-04-11 |    28,018 |  3,346 |     5,986 |  18,686 |
| Switzerland    | 2020-04-11 |    25,107 |  1,036 |    12,100 |  11,971 |
| Netherlands    | 2020-04-11 |    24,571 |  2,653 |       291 |  21,627 |
| Portugal       | 2020-04-11 |    15,987 |    470 |       266 |  15,251 |
| Austria        | 2020-04-11 |    13,806 |    337 |     6,604 |   6,865 |
| Sweden         | 2020-04-11 |    10,151 |    887 |       381 |   8,883 |
| Ireland        | 2020-04-11 |     8,928 |    320 |        25 |   8,583 |
| Norway         | 2020-04-11 |     6,409 |    119 |        32 |   6,258 |
| Poland         | 2020-04-11 |     6,356 |    208 |       375 |   5,773 |
| Denmark        | 2020-04-11 |     6,191 |    260 |     2,111 |   3,820 |
| Romania        | 2020-04-11 |     5,990 |    291 |       758 |   4,941 |
| Czechia        | 2020-04-11 |     5,831 |    129 |       411 |   5,291 |
| Serbia         | 2020-04-11 |     3,380 |     74 |         0 |   3,306 |
| Luxembourg     | 2020-04-11 |     3,270 |     62 |       500 |   2,708 |
| Finland        | 2020-04-11 |     2,905 |     49 |       300 |   2,556 |
| Ukraine        | 2020-04-11 |     2,511 |     73 |        79 |   2,359 |

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
| US                 | 2020-04-11 |   526,396 | 20,463 |    31,270 | 474,663 |
| Canada             | 2020-04-11 |    23,316 |    654 |     6,589 |  16,073 |
| Brazil             | 2020-04-11 |    20,727 |  1,124 |       173 |  19,430 |
| Ecuador            | 2020-04-11 |     7,257 |    315 |       411 |   6,531 |
| Chile              | 2020-04-11 |     6,927 |     73 |     1,864 |   4,990 |
| Peru               | 2020-04-11 |     6,848 |    181 |     1,739 |   4,928 |
| Mexico             | 2020-04-11 |     3,844 |    233 |       633 |   2,978 |
| Panama             | 2020-04-11 |     2,974 |     74 |        17 |   2,883 |
| Dominican Republic | 2020-04-11 |     2,759 |    135 |       108 |   2,516 |
| Colombia           | 2020-04-11 |     2,709 |    100 |       214 |   2,395 |
| Argentina          | 2020-04-11 |     1,975 |     83 |       440 |   1,452 |

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
| Iran                 | 2020-04-11 |    70,029 |  4,357 |    41,947 | 23,725 |
| Israel               | 2020-04-11 |    10,743 |    101 |     1,341 |  9,301 |
| Pakistan             | 2020-04-11 |     5,011 |     86 |       762 |  4,163 |
| Saudi Arabia         | 2020-04-11 |     4,033 |     52 |       720 |  3,261 |
| United Arab Emirates | 2020-04-11 |     3,736 |     20 |       588 |  3,128 |
| Qatar                | 2020-04-11 |     2,728 |      6 |       247 |  2,475 |

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
| China        | 2020-04-11 |    83,014 |  3,343 |    77,877 |  1,794 |
| Russia       | 2020-04-11 |    13,584 |    106 |     1,045 | 12,433 |
| Korea, South | 2020-04-11 |    10,480 |    211 |     7,243 |  3,026 |
| India        | 2020-04-11 |     8,446 |    288 |       969 |  7,189 |
| Australia    | 2020-04-11 |     6,303 |     57 |     1,806 |  4,440 |
| Japan        | 2020-04-11 |     6,005 |     99 |       762 |  5,144 |
| Malaysia     | 2020-04-11 |     4,530 |     73 |     1,995 |  2,462 |
| Philippines  | 2020-04-11 |     4,428 |    247 |       157 |  4,024 |
| Thailand     | 2020-04-11 |     2,518 |     35 |     1,135 |  1,348 |

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
| South Africa | 2020-04-11 |     2,028 |     25 |       410 |  1,593 |
| Egypt        | 2020-04-11 |     1,939 |    146 |       426 |  1,367 |
| Algeria      | 2020-04-11 |     1,825 |    275 |       460 |  1,090 |
| Morocco      | 2020-04-11 |     1,545 |    111 |       146 |  1,288 |

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
