
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
on 2020-05-10 09:35:27. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-09 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-09 |   218,268 | 30,395 |   103,031 | 84,842 |
| Germany      | 2020-05-09 |   171,324 |  7,549 |   143,300 | 20,475 |
| China        | 2020-05-09 |    83,990 |  4,637 |    79,127 |    226 |
| Korea, South | 2020-05-09 |    10,874 |    256 |     9,610 |  1,008 |

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
| Spain          | 2020-05-09 |   223,578 | 26,478 |   133,952 |  63,148 |
| Italy          | 2020-05-09 |   218,268 | 30,395 |   103,031 |  84,842 |
| United Kingdom | 2020-05-09 |   216,525 | 31,662 |     1,001 | 183,862 |
| France         | 2020-05-09 |   176,782 | 26,313 |    56,148 |  94,321 |
| Germany        | 2020-05-09 |   171,324 |  7,549 |   143,300 |  20,475 |
| Turkey         | 2020-05-09 |   137,115 |  3,739 |    89,480 |  43,896 |
| Belgium        | 2020-05-09 |    52,596 |  8,581 |    13,411 |  30,604 |
| Netherlands    | 2020-05-09 |    42,581 |  5,441 |       149 |  36,991 |
| Switzerland    | 2020-05-09 |    30,251 |  1,830 |    26,400 |   2,021 |
| Portugal       | 2020-05-09 |    27,406 |  1,126 |     2,499 |  23,781 |
| Sweden         | 2020-05-09 |    25,921 |  3,220 |     4,971 |  17,730 |
| Ireland        | 2020-05-09 |    22,760 |  1,446 |    17,110 |   4,204 |
| Austria        | 2020-05-09 |    15,833 |    615 |    13,928 |   1,290 |
| Poland         | 2020-05-09 |    15,651 |    785 |     5,437 |   9,429 |
| Romania        | 2020-05-09 |    15,131 |    939 |     6,912 |   7,280 |
| Ukraine        | 2020-05-09 |    14,710 |    376 |     2,909 |  11,425 |
| Denmark        | 2020-05-09 |    10,517 |    526 |     8,291 |   1,700 |
| Serbia         | 2020-05-09 |    10,032 |    215 |     2,732 |   7,085 |
| Norway         | 2020-05-09 |     8,099 |    219 |        32 |   7,848 |
| Czechia        | 2020-05-09 |     8,095 |    276 |     4,447 |   3,372 |
| Finland        | 2020-05-09 |     5,880 |    265 |     4,000 |   1,615 |
| Luxembourg     | 2020-05-09 |     3,877 |    101 |     3,550 |     226 |

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
| US                 | 2020-05-09 | 1,309,550 | 78,795 |   212,534 | 1,018,221 |
| Brazil             | 2020-05-09 |   156,061 | 10,656 |    61,685 |    83,720 |
| Canada             | 2020-05-09 |    68,918 |  4,823 |    31,262 |    32,833 |
| Peru               | 2020-05-09 |    65,015 |  1,814 |    20,246 |    42,955 |
| Mexico             | 2020-05-09 |    33,460 |  3,353 |    21,824 |     8,283 |
| Ecuador            | 2020-05-09 |    29,071 |  1,717 |     3,433 |    23,921 |
| Chile              | 2020-05-09 |    27,219 |    304 |    12,667 |    14,248 |
| Colombia           | 2020-05-09 |    10,495 |    445 |     2,569 |     7,481 |
| Dominican Republic | 2020-05-09 |     9,882 |    385 |     2,584 |     6,913 |
| Panama             | 2020-05-09 |     8,282 |    237 |     4,501 |     3,544 |
| Argentina          | 2020-05-09 |     5,776 |    300 |     1,728 |     3,748 |

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
| Iran                 | 2020-05-09 |   106,220 |  6,589 |    85,064 | 14,567 |
| Saudi Arabia         | 2020-05-09 |    37,136 |    239 |    10,144 | 26,753 |
| Pakistan             | 2020-05-09 |    28,736 |    636 |     7,809 | 20,291 |
| Qatar                | 2020-05-09 |    21,331 |     13 |     2,449 | 18,869 |
| United Arab Emirates | 2020-05-09 |    17,417 |    185 |     4,295 | 12,937 |
| Israel               | 2020-05-09 |    16,454 |    247 |    11,376 |  4,831 |

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
| Russia       | 2020-05-09 |   198,676 |  1,827 |    31,916 | 164,933 |
| China        | 2020-05-09 |    83,990 |  4,637 |    79,127 |     226 |
| India        | 2020-05-09 |    62,808 |  2,101 |    19,301 |  41,406 |
| Japan        | 2020-05-09 |    15,663 |    607 |     5,906 |   9,150 |
| Korea, South | 2020-05-09 |    10,874 |    256 |     9,610 |   1,008 |
| Philippines  | 2020-05-09 |    10,610 |    704 |     1,842 |   8,064 |
| Australia    | 2020-05-09 |     6,939 |     97 |     6,141 |     701 |
| Malaysia     | 2020-05-09 |     6,589 |    108 |     4,929 |   1,552 |
| Thailand     | 2020-05-09 |     3,004 |     56 |     2,787 |     161 |

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
| South Africa | 2020-05-09 |     9,420 |    186 |     3,983 |  5,251 |
| Egypt        | 2020-05-09 |     8,964 |    514 |     2,002 |  6,448 |
| Morocco      | 2020-05-09 |     5,910 |    186 |     2,461 |  3,263 |
| Algeria      | 2020-05-09 |     5,558 |    494 |     2,546 |  2,518 |

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
