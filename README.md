
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
on 2020-05-06 09:15:32. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-05 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-05 |   213,013 | 29,315 |    85,231 | 98,467 |
| Germany      | 2020-05-05 |   167,007 |  6,993 |   135,100 | 24,914 |
| China        | 2020-05-05 |    83,968 |  4,637 |    78,870 |    461 |
| Korea, South | 2020-05-05 |    10,806 |    255 |     9,333 |  1,218 |

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
| Spain          | 2020-05-05 |   219,329 | 25,613 |   123,486 |  70,230 |
| Italy          | 2020-05-05 |   213,013 | 29,315 |    85,231 |  98,467 |
| United Kingdom | 2020-05-05 |   196,243 | 29,501 |       926 | 165,816 |
| France         | 2020-05-05 |   170,687 | 25,537 |    52,842 |  92,308 |
| Germany        | 2020-05-05 |   167,007 |  6,993 |   135,100 |  24,914 |
| Turkey         | 2020-05-05 |   129,491 |  3,520 |    73,285 |  52,686 |
| Belgium        | 2020-05-05 |    50,509 |  8,016 |    12,441 |  30,052 |
| Netherlands    | 2020-05-05 |    41,286 |  5,185 |       139 |  35,962 |
| Switzerland    | 2020-05-05 |    30,009 |  1,795 |    25,400 |   2,814 |
| Portugal       | 2020-05-05 |    25,702 |  1,074 |     1,743 |  22,885 |
| Sweden         | 2020-05-05 |    23,216 |  2,854 |     4,074 |  16,288 |
| Ireland        | 2020-05-05 |    21,983 |  1,339 |    13,386 |   7,258 |
| Austria        | 2020-05-05 |    15,650 |    606 |    13,462 |   1,582 |
| Poland         | 2020-05-05 |    14,431 |    716 |     4,280 |   9,435 |
| Romania        | 2020-05-05 |    13,837 |    841 |     5,454 |   7,542 |
| Ukraine        | 2020-05-05 |    12,697 |    316 |     1,875 |  10,506 |
| Denmark        | 2020-05-05 |    10,019 |    503 |     7,492 |   2,024 |
| Serbia         | 2020-05-05 |     9,677 |    200 |     1,723 |   7,754 |
| Norway         | 2020-05-05 |     7,955 |    215 |        32 |   7,708 |
| Czechia        | 2020-05-05 |     7,896 |    257 |     4,006 |   3,633 |
| Finland        | 2020-05-05 |     5,412 |    246 |     3,500 |   1,666 |
| Luxembourg     | 2020-05-05 |     3,840 |     96 |     3,412 |     332 |

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
| US                 | 2020-05-05 | 1,204,351 | 71,064 |   189,791 | 943,496 |
| Brazil             | 2020-05-05 |   115,455 |  7,938 |    48,221 |  59,296 |
| Canada             | 2020-05-05 |    63,215 |  4,190 |    27,006 |  32,019 |
| Peru               | 2020-05-05 |    51,189 |  1,444 |    15,413 |  34,332 |
| Ecuador            | 2020-05-05 |    31,881 |  1,569 |     3,433 |  26,879 |
| Mexico             | 2020-05-05 |    26,025 |  2,507 |    16,810 |   6,708 |
| Chile              | 2020-05-05 |    22,016 |    275 |    10,710 |  11,031 |
| Colombia           | 2020-05-05 |     8,613 |    378 |     2,013 |   6,222 |
| Dominican Republic | 2020-05-05 |     8,480 |    354 |     1,905 |   6,221 |
| Panama             | 2020-05-05 |     7,523 |    210 |       823 |   6,490 |
| Argentina          | 2020-05-05 |     5,020 |    264 |     1,472 |   3,284 |

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
| Iran                 | 2020-05-05 |    99,970 |  6,340 |    80,475 | 13,155 |
| Saudi Arabia         | 2020-05-05 |    30,251 |    200 |     5,431 | 24,620 |
| Pakistan             | 2020-05-05 |    22,049 |    514 |     5,801 | 15,734 |
| Qatar                | 2020-05-05 |    17,142 |     12 |     1,924 | 15,206 |
| Israel               | 2020-05-05 |    16,289 |    238 |    10,465 |  5,586 |
| United Arab Emirates | 2020-05-05 |    15,192 |    146 |     3,153 | 11,893 |

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
| Russia       | 2020-05-05 |   155,370 |  1,451 |    19,865 | 134,054 |
| China        | 2020-05-05 |    83,968 |  4,637 |    78,870 |     461 |
| India        | 2020-05-05 |    49,400 |  1,693 |    14,142 |  33,565 |
| Japan        | 2020-05-05 |    15,253 |    556 |     4,496 |  10,201 |
| Korea, South | 2020-05-05 |    10,806 |    255 |     9,333 |   1,218 |
| Philippines  | 2020-05-05 |     9,684 |    637 |     1,408 |   7,639 |
| Australia    | 2020-05-05 |     6,875 |     97 |     5,975 |     803 |
| Malaysia     | 2020-05-05 |     6,383 |    106 |     4,567 |   1,710 |
| Thailand     | 2020-05-05 |     2,988 |     54 |     2,747 |     187 |

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
| South Africa | 2020-05-05 |     7,572 |    148 |     2,746 |  4,678 |
| Egypt        | 2020-05-05 |     7,201 |    452 |     1,730 |  5,019 |
| Morocco      | 2020-05-05 |     5,219 |    181 |     1,838 |  3,200 |
| Algeria      | 2020-05-05 |     4,838 |    470 |     2,067 |  2,301 |

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
