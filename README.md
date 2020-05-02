
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
on 2020-05-02 09:03:00. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-01 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-01 |   207,428 | 28,236 |    78,249 | 100,943 |
| Germany      | 2020-05-01 |   164,077 |  6,736 |   126,900 |  30,441 |
| China        | 2020-05-01 |    83,959 |  4,637 |    78,573 |     749 |
| Korea, South | 2020-05-01 |    10,780 |    250 |     9,123 |   1,407 |

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
| Spain          | 2020-05-01 |   213,435 | 24,543 |   112,050 |  76,842 |
| Italy          | 2020-05-01 |   207,428 | 28,236 |    78,249 | 100,943 |
| United Kingdom | 2020-05-01 |   178,685 | 27,583 |       892 | 150,210 |
| France         | 2020-05-01 |   167,305 | 24,628 |    51,124 |  91,553 |
| Germany        | 2020-05-01 |   164,077 |  6,736 |   126,900 |  30,441 |
| Turkey         | 2020-05-01 |   122,392 |  3,258 |    53,808 |  65,326 |
| Belgium        | 2020-05-01 |    49,032 |  7,703 |    11,892 |  29,437 |
| Netherlands    | 2020-05-01 |    39,989 |  4,909 |       138 |  34,942 |
| Switzerland    | 2020-05-01 |    29,705 |  1,754 |    23,900 |   4,051 |
| Portugal       | 2020-05-01 |    25,351 |  1,007 |     1,647 |  22,697 |
| Sweden         | 2020-05-01 |    21,520 |  2,653 |     1,005 |  17,862 |
| Ireland        | 2020-05-01 |    20,833 |  1,265 |    13,386 |   6,182 |
| Austria        | 2020-05-01 |    15,531 |    589 |    13,110 |   1,832 |
| Poland         | 2020-05-01 |    13,105 |    651 |     3,491 |   8,963 |
| Romania        | 2020-05-01 |    12,567 |    744 |     4,328 |   7,495 |
| Ukraine        | 2020-05-01 |    10,861 |    272 |     1,413 |   9,176 |
| Denmark        | 2020-05-01 |     9,509 |    460 |     6,924 |   2,125 |
| Serbia         | 2020-05-01 |     9,009 |    179 |     1,343 |   7,487 |
| Norway         | 2020-05-01 |     7,783 |    210 |        32 |   7,541 |
| Czechia        | 2020-05-01 |     7,737 |    240 |     3,372 |   4,125 |
| Finland        | 2020-05-01 |     5,051 |    218 |     3,000 |   1,833 |
| Luxembourg     | 2020-05-01 |     3,802 |     92 |     3,213 |     497 |

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
| US                 | 2020-05-01 | 1,103,461 | 64,943 |   164,015 | 874,503 |
| Brazil             | 2020-05-01 |    92,202 |  6,412 |    38,039 |  47,751 |
| Canada             | 2020-05-01 |    56,343 |  3,537 |    22,764 |  30,042 |
| Peru               | 2020-05-01 |    40,459 |  1,124 |    11,129 |  28,206 |
| Ecuador            | 2020-05-01 |    26,336 |  1,063 |     1,913 |  23,360 |
| Mexico             | 2020-05-01 |    20,739 |  1,972 |    12,377 |   6,390 |
| Chile              | 2020-05-01 |    17,008 |    234 |     9,018 |   7,756 |
| Dominican Republic | 2020-05-01 |     7,288 |    313 |     1,387 |   5,588 |
| Colombia           | 2020-05-01 |     7,006 |    314 |     1,551 |   5,141 |
| Panama             | 2020-05-01 |     6,720 |    192 |       622 |   5,906 |
| Argentina          | 2020-05-01 |     4,532 |    225 |     1,292 |   3,015 |

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
| Iran                 | 2020-05-01 |    95,646 |  6,091 |    76,318 | 13,237 |
| Saudi Arabia         | 2020-05-01 |    24,097 |    169 |     3,555 | 20,373 |
| Pakistan             | 2020-05-01 |    18,114 |    417 |     4,715 | 12,982 |
| Israel               | 2020-05-01 |    16,101 |    225 |     9,156 |  6,720 |
| Qatar                | 2020-05-01 |    14,096 |     12 |     1,436 | 12,648 |
| United Arab Emirates | 2020-05-01 |    13,038 |    111 |     2,543 | 10,384 |

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
| Russia       | 2020-05-01 |   114,431 |  1,169 |    13,220 | 100,042 |
| China        | 2020-05-01 |    83,959 |  4,637 |    78,573 |     749 |
| India        | 2020-05-01 |    37,257 |  1,223 |    10,007 |  26,027 |
| Japan        | 2020-05-01 |    14,305 |    455 |     2,975 |  10,875 |
| Korea, South | 2020-05-01 |    10,780 |    250 |     9,123 |   1,407 |
| Philippines  | 2020-05-01 |     8,772 |    579 |     1,084 |   7,109 |
| Australia    | 2020-05-01 |     6,778 |     93 |     5,775 |     910 |
| Malaysia     | 2020-05-01 |     6,071 |    103 |     4,210 |   1,758 |
| Thailand     | 2020-05-01 |     2,960 |     54 |     2,719 |     187 |

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
| South Africa | 2020-05-01 |     5,951 |    116 |     2,382 |  3,453 |
| Egypt        | 2020-05-01 |     5,895 |    406 |     1,460 |  4,029 |
| Morocco      | 2020-05-01 |     4,569 |    171 |     1,083 |  3,315 |
| Algeria      | 2020-05-01 |     4,154 |    453 |     1,821 |  1,880 |

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
