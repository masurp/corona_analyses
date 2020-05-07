
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
on 2020-05-07 15:32:45. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-06 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-06 |   214,457 | 29,684 |    93,245 | 91,528 |
| Germany      | 2020-05-06 |   168,162 |  7,275 |   139,900 | 20,987 |
| China        | 2020-05-06 |    83,970 |  4,637 |    78,929 |    404 |
| Korea, South | 2020-05-06 |    10,810 |    256 |     9,419 |  1,135 |

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
| Spain          | 2020-05-06 |   220,325 | 25,857 |   126,002 |  68,466 |
| Italy          | 2020-05-06 |   214,457 | 29,684 |    93,245 |  91,528 |
| United Kingdom | 2020-05-06 |   202,359 | 30,150 |       934 | 171,275 |
| France         | 2020-05-06 |   174,224 | 25,812 |    54,079 |  94,333 |
| Germany        | 2020-05-06 |   168,162 |  7,275 |   139,900 |  20,987 |
| Turkey         | 2020-05-06 |   131,744 |  3,584 |    78,202 |  49,958 |
| Belgium        | 2020-05-06 |    50,781 |  8,339 |    12,731 |  29,711 |
| Netherlands    | 2020-05-06 |    41,518 |  5,221 |       146 |  36,151 |
| Switzerland    | 2020-05-06 |    30,060 |  1,805 |    25,700 |   2,555 |
| Portugal       | 2020-05-06 |    26,182 |  1,089 |     2,076 |  23,017 |
| Sweden         | 2020-05-06 |    23,918 |  2,941 |     4,074 |  16,903 |
| Ireland        | 2020-05-06 |    22,248 |  1,375 |    17,110 |   3,763 |
| Austria        | 2020-05-06 |    15,684 |    608 |    13,639 |   1,437 |
| Poland         | 2020-05-06 |    14,740 |    733 |     4,655 |   9,352 |
| Romania        | 2020-05-06 |    14,107 |    864 |     5,788 |   7,455 |
| Ukraine        | 2020-05-06 |    13,184 |    327 |     2,097 |  10,760 |
| Denmark        | 2020-05-06 |    10,136 |    506 |     7,689 |   1,941 |
| Serbia         | 2020-05-06 |     9,791 |    203 |     1,971 |   7,617 |
| Norway         | 2020-05-06 |     7,996 |    216 |        32 |   7,748 |
| Czechia        | 2020-05-06 |     7,974 |    262 |     4,205 |   3,507 |
| Finland        | 2020-05-06 |     5,573 |    252 |     3,500 |   1,821 |
| Luxembourg     | 2020-05-06 |     3,851 |     98 |     3,452 |     301 |

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
| US                 | 2020-05-06 | 1,228,603 | 73,431 |   189,910 | 965,262 |
| Brazil             | 2020-05-06 |   126,611 |  8,588 |    51,370 |  66,653 |
| Canada             | 2020-05-06 |    64,694 |  4,366 |    28,184 |  32,144 |
| Peru               | 2020-05-06 |    54,817 |  1,533 |    17,527 |  35,757 |
| Ecuador            | 2020-05-06 |    31,881 |  1,618 |     3,433 |  26,830 |
| Mexico             | 2020-05-06 |    27,634 |  2,704 |    17,781 |   7,149 |
| Chile              | 2020-05-06 |    23,048 |    281 |    11,189 |  11,578 |
| Colombia           | 2020-05-06 |     8,959 |    397 |     2,148 |   6,414 |
| Dominican Republic | 2020-05-06 |     8,807 |    362 |     1,960 |   6,485 |
| Panama             | 2020-05-06 |     7,731 |    218 |       859 |   6,654 |
| Argentina          | 2020-05-06 |     5,208 |    273 |     1,524 |   3,411 |

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
| Iran                 | 2020-05-06 |   101,650 |  6,418 |    81,587 | 13,645 |
| Saudi Arabia         | 2020-05-06 |    31,938 |    209 |     6,783 | 24,946 |
| Pakistan             | 2020-05-06 |    24,073 |    564 |     6,464 | 17,045 |
| Qatar                | 2020-05-06 |    17,972 |     12 |     2,070 | 15,890 |
| Israel               | 2020-05-06 |    16,310 |    239 |    10,637 |  5,434 |
| United Arab Emirates | 2020-05-06 |    15,738 |    157 |     3,359 | 12,222 |

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
| Russia       | 2020-05-06 |   165,929 |  1,537 |    21,327 | 143,065 |
| China        | 2020-05-06 |    83,970 |  4,637 |    78,929 |     404 |
| India        | 2020-05-06 |    52,987 |  1,785 |    15,331 |  35,871 |
| Japan        | 2020-05-06 |    15,253 |    556 |     4,496 |  10,201 |
| Korea, South | 2020-05-06 |    10,810 |    256 |     9,419 |   1,135 |
| Philippines  | 2020-05-06 |    10,004 |    658 |     1,506 |   7,840 |
| Australia    | 2020-05-06 |     6,894 |     97 |     6,031 |     766 |
| Malaysia     | 2020-05-06 |     6,428 |    107 |     4,702 |   1,619 |
| Thailand     | 2020-05-06 |     2,989 |     55 |     2,761 |     173 |

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
| South Africa | 2020-05-06 |     7,808 |    153 |     3,153 |  4,502 |
| Egypt        | 2020-05-06 |     7,588 |    469 |     1,815 |  5,304 |
| Morocco      | 2020-05-06 |     5,408 |    183 |     2,017 |  3,208 |
| Algeria      | 2020-05-06 |     4,997 |    476 |     2,197 |  2,324 |

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
