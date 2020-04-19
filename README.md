
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
on 2020-04-19 12:15:53. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-18 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-18 |   175,925 | 23,227 |    44,927 | 107,771 |
| Germany      | 2020-04-18 |   143,342 |  4,459 |    85,400 |  53,483 |
| China        | 2020-04-18 |    83,787 |  4,636 |    77,614 |   1,537 |
| Korea, South | 2020-04-18 |    10,653 |    232 |     7,937 |   2,484 |

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
| Spain          | 2020-04-18 |   191,726 | 20,043 |    74,797 |  96,886 |
| Italy          | 2020-04-18 |   175,925 | 23,227 |    44,927 | 107,771 |
| France         | 2020-04-18 |   149,149 | 19,345 |    36,587 |  93,217 |
| Germany        | 2020-04-18 |   143,342 |  4,459 |    85,400 |  53,483 |
| United Kingdom | 2020-04-18 |   115,314 | 15,498 |       414 |  99,402 |
| Turkey         | 2020-04-18 |    82,329 |  1,890 |    10,453 |  69,986 |
| Belgium        | 2020-04-18 |    37,183 |  5,453 |     8,348 |  23,382 |
| Netherlands    | 2020-04-18 |    31,766 |  3,613 |       317 |  27,836 |
| Switzerland    | 2020-04-18 |    27,404 |  1,368 |    17,100 |   8,936 |
| Portugal       | 2020-04-18 |    19,685 |    687 |       610 |  18,388 |
| Ireland        | 2020-04-18 |    14,758 |    571 |        77 |  14,110 |
| Austria        | 2020-04-18 |    14,671 |    443 |    10,214 |   4,014 |
| Sweden         | 2020-04-18 |    13,822 |  1,511 |       550 |  11,761 |
| Poland         | 2020-04-18 |     8,742 |    347 |       981 |   7,414 |
| Romania        | 2020-04-18 |     8,418 |    421 |     1,730 |   6,267 |
| Denmark        | 2020-04-18 |     7,437 |    346 |     4,031 |   3,060 |
| Norway         | 2020-04-18 |     7,036 |    164 |        32 |   6,840 |
| Czechia        | 2020-04-18 |     6,606 |    181 |     1,227 |   5,198 |
| Serbia         | 2020-04-18 |     5,994 |    117 |       637 |   5,240 |
| Ukraine        | 2020-04-18 |     5,106 |    133 |       275 |   4,698 |
| Finland        | 2020-04-18 |     3,681 |     90 |     1,700 |   1,891 |
| Luxembourg     | 2020-04-18 |     3,537 |     72 |       601 |   2,864 |

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
| US                 | 2020-04-18 |   732,197 | 38,664 |    64,840 | 628,693 |
| Brazil             | 2020-04-18 |    36,658 |  2,354 |    14,026 |  20,278 |
| Canada             | 2020-04-18 |    34,355 |  1,399 |    10,964 |  21,992 |
| Peru               | 2020-04-18 |    14,420 |    348 |     6,684 |   7,388 |
| Chile              | 2020-04-18 |     9,730 |    126 |     4,035 |   5,569 |
| Ecuador            | 2020-04-18 |     9,022 |    456 |     1,008 |   7,558 |
| Mexico             | 2020-04-18 |     6,875 |    546 |     2,125 |   4,204 |
| Dominican Republic | 2020-04-18 |     4,335 |    217 |       312 |   3,806 |
| Panama             | 2020-04-18 |     4,210 |    116 |       122 |   3,972 |
| Colombia           | 2020-04-18 |     3,439 |    153 |       634 |   2,652 |
| Argentina          | 2020-04-18 |     2,758 |    129 |       685 |   1,944 |

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
| Iran                 | 2020-04-18 |    80,868 |  5,031 |    55,987 | 19,850 |
| Israel               | 2020-04-18 |    13,265 |    164 |     3,456 |  9,645 |
| Saudi Arabia         | 2020-04-18 |     8,274 |     92 |     1,329 |  6,853 |
| Pakistan             | 2020-04-18 |     7,638 |    143 |     1,832 |  5,663 |
| United Arab Emirates | 2020-04-18 |     6,302 |     37 |     1,188 |  5,077 |
| Qatar                | 2020-04-18 |     5,008 |      8 |       510 |  4,490 |

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
| China        | 2020-04-18 |    83,787 |  4,636 |    77,614 |  1,537 |
| Russia       | 2020-04-18 |    36,793 |    313 |     3,057 | 33,423 |
| India        | 2020-04-18 |    15,722 |    521 |     2,463 | 12,738 |
| Korea, South | 2020-04-18 |    10,653 |    232 |     7,937 |  2,484 |
| Japan        | 2020-04-18 |    10,296 |    222 |     1,069 |  9,005 |
| Australia    | 2020-04-18 |     6,547 |     67 |     4,124 |  2,356 |
| Philippines  | 2020-04-18 |     6,087 |    397 |       516 |  5,174 |
| Malaysia     | 2020-04-18 |     5,305 |     88 |     3,102 |  2,115 |
| Thailand     | 2020-04-18 |     2,733 |     47 |     1,787 |    899 |

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
| South Africa | 2020-04-18 |     3,034 |     52 |       903 |  2,079 |
| Egypt        | 2020-04-18 |     3,032 |    224 |       701 |  2,107 |
| Morocco      | 2020-04-18 |     2,685 |    137 |       314 |  2,234 |
| Algeria      | 2020-04-18 |     2,534 |    367 |       894 |  1,273 |

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
