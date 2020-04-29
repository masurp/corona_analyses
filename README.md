
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
on 2020-04-29 08:16:55. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-28 at 23:59:00. Also bear in mind that the
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

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Italy        | 2020-04-28 |   201,505 | 27,359 |    68,941 | 105,205 |
| Germany      | 2020-04-28 |   159,912 |  6,314 |   117,400 |  36,198 |
| China        | 2020-04-28 |    83,940 |  4,637 |    78,422 |     881 |
| Korea, South | 2020-04-28 |    10,761 |    246 |     8,922 |   1,593 |

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
| Spain          | 2020-04-28 |   232,128 | 23,822 |   123,903 |  84,403 |
| Italy          | 2020-04-28 |   201,505 | 27,359 |    68,941 | 105,205 |
| France         | 2020-04-28 |   169,053 | 23,694 |    47,775 |  97,584 |
| United Kingdom | 2020-04-28 |   162,350 | 21,745 |       813 | 139,792 |
| Germany        | 2020-04-28 |   159,912 |  6,314 |   117,400 |  36,198 |
| Turkey         | 2020-04-28 |   114,653 |  2,992 |    38,809 |  72,852 |
| Belgium        | 2020-04-28 |    47,334 |  7,331 |    10,943 |  29,060 |
| Netherlands    | 2020-04-28 |    38,612 |  4,582 |       117 |  33,913 |
| Switzerland    | 2020-04-28 |    29,264 |  1,699 |    22,600 |   4,965 |
| Portugal       | 2020-04-28 |    24,322 |    948 |     1,389 |  21,985 |
| Ireland        | 2020-04-28 |    19,877 |  1,159 |     9,233 |   9,485 |
| Sweden         | 2020-04-28 |    19,621 |  2,355 |     1,005 |  16,261 |
| Austria        | 2020-04-28 |    15,357 |    569 |    12,580 |   2,208 |
| Poland         | 2020-04-28 |    12,218 |    596 |     2,655 |   8,967 |
| Romania        | 2020-04-28 |    11,616 |    663 |     3,404 |   7,549 |
| Ukraine        | 2020-04-28 |     9,410 |    239 |       992 |   8,179 |
| Denmark        | 2020-04-28 |     9,049 |    434 |     6,313 |   2,302 |
| Norway         | 2020-04-28 |     7,660 |    206 |        32 |   7,422 |
| Czechia        | 2020-04-28 |     7,504 |    227 |     2,948 |   4,329 |
| Serbia         | 2020-04-28 |     6,630 |    125 |       870 |   5,635 |
| Finland        | 2020-04-28 |     4,740 |    199 |     2,800 |   1,741 |
| Luxembourg     | 2020-04-28 |     3,741 |     89 |     3,123 |     529 |

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
| US                 | 2020-04-28 | 1,012,582 | 58,355 |   115,936 | 838,291 |
| Brazil             | 2020-04-28 |    73,235 |  5,083 |    32,544 |  35,608 |
| Canada             | 2020-04-28 |    51,150 |  2,983 |    19,231 |  28,936 |
| Peru               | 2020-04-28 |    31,190 |    854 |     9,179 |  21,157 |
| Ecuador            | 2020-04-28 |    24,258 |    871 |     1,557 |  21,830 |
| Mexico             | 2020-04-28 |    16,752 |  1,569 |    11,423 |   3,760 |
| Chile              | 2020-04-28 |    14,365 |    207 |     7,710 |   6,448 |
| Dominican Republic | 2020-04-28 |     6,416 |    286 |     1,165 |   4,965 |
| Panama             | 2020-04-28 |     6,021 |    167 |       455 |   5,399 |
| Colombia           | 2020-04-28 |     5,949 |    269 |     1,268 |   4,412 |
| Argentina          | 2020-04-28 |     4,127 |    207 |     1,162 |   2,758 |

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
| Iran                 | 2020-04-28 |    92,584 |  5,877 |    72,439 | 14,268 |
| Saudi Arabia         | 2020-04-28 |    20,077 |    152 |     2,784 | 17,141 |
| Israel               | 2020-04-28 |    15,728 |    210 |     7,746 |  7,772 |
| Pakistan             | 2020-04-28 |    14,612 |    312 |     3,233 | 11,067 |
| Qatar                | 2020-04-28 |    11,921 |     10 |     1,134 | 10,777 |
| United Arab Emirates | 2020-04-28 |    11,380 |     89 |     2,181 |  9,110 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia, Indonesia, Australia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| Russia       | 2020-04-28 |    93,558 |    867 |     8,456 | 84,235 |
| China        | 2020-04-28 |    83,940 |  4,637 |    78,422 |    881 |
| India        | 2020-04-28 |    31,324 |  1,008 |     7,747 | 22,569 |
| Japan        | 2020-04-28 |    13,736 |    394 |     1,899 | 11,443 |
| Korea, South | 2020-04-28 |    10,761 |    246 |     8,922 |  1,593 |
| Philippines  | 2020-04-28 |     7,958 |    530 |       975 |  6,453 |
| Australia    | 2020-04-28 |     6,744 |     89 |     5,665 |    990 |
| Malaysia     | 2020-04-28 |     5,851 |    100 |     4,032 |  1,719 |
| Thailand     | 2020-04-28 |     2,938 |     54 |     2,652 |    232 |

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
| Egypt        | 2020-04-28 |     5,042 |    359 |     1,304 |  3,379 |
| South Africa | 2020-04-28 |     4,996 |     93 |     2,073 |  2,830 |
| Morocco      | 2020-04-28 |     4,252 |    165 |       778 |  3,309 |
| Algeria      | 2020-04-28 |     3,649 |    437 |     1,651 |  1,561 |

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
