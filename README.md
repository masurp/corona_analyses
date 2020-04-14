
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
on 2020-04-14 08:10:15. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-13 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-13 |   159,516 | 20,465 |    35,435 | 103,616 |
| Germany      | 2020-04-13 |   130,072 |  3,194 |    64,300 |  62,578 |
| China        | 2020-04-13 |    83,213 |  3,345 |    78,039 |   1,829 |
| Korea, South | 2020-04-13 |    10,537 |    217 |     7,447 |   2,873 |

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
| Spain          | 2020-04-13 |   170,099 | 17,756 |    64,727 |  87,616 |
| Italy          | 2020-04-13 |   159,516 | 20,465 |    35,435 | 103,616 |
| France         | 2020-04-13 |   137,875 | 14,986 |    28,001 |  94,888 |
| Germany        | 2020-04-13 |   130,072 |  3,194 |    64,300 |  62,578 |
| United Kingdom | 2020-04-13 |    89,570 | 11,347 |       304 |  77,919 |
| Turkey         | 2020-04-13 |    61,049 |  1,296 |     3,957 |  55,796 |
| Belgium        | 2020-04-13 |    30,589 |  3,903 |     6,707 |  19,979 |
| Netherlands    | 2020-04-13 |    26,710 |  2,833 |       295 |  23,582 |
| Switzerland    | 2020-04-13 |    25,688 |  1,138 |    13,700 |  10,850 |
| Portugal       | 2020-04-13 |    16,934 |    535 |       277 |  16,122 |
| Austria        | 2020-04-13 |    14,041 |    368 |     7,343 |   6,330 |
| Sweden         | 2020-04-13 |    10,948 |    919 |       381 |   9,648 |
| Ireland        | 2020-04-13 |    10,647 |    365 |        25 |  10,257 |
| Poland         | 2020-04-13 |     6,934 |    245 |       487 |   6,202 |
| Romania        | 2020-04-13 |     6,633 |    331 |       914 |   5,388 |
| Norway         | 2020-04-13 |     6,603 |    134 |        32 |   6,437 |
| Denmark        | 2020-04-13 |     6,513 |    285 |     2,403 |   3,825 |
| Czechia        | 2020-04-13 |     6,059 |    143 |       519 |   5,397 |
| Serbia         | 2020-04-13 |     4,054 |     85 |         0 |   3,969 |
| Luxembourg     | 2020-04-13 |     3,292 |     69 |       500 |   2,723 |
| Ukraine        | 2020-04-13 |     3,102 |     93 |        97 |   2,912 |
| Finland        | 2020-04-13 |     3,064 |     59 |       300 |   2,705 |

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
| US                 | 2020-04-13 |   580,619 | 23,529 |    43,482 | 513,608 |
| Canada             | 2020-04-13 |    25,679 |    779 |     7,758 |  17,142 |
| Brazil             | 2020-04-13 |    23,430 |  1,328 |       173 |  21,929 |
| Peru               | 2020-04-13 |     9,784 |    216 |     2,642 |   6,926 |
| Ecuador            | 2020-04-13 |     7,529 |    355 |       597 |   6,577 |
| Chile              | 2020-04-13 |     7,525 |     82 |     2,367 |   5,076 |
| Mexico             | 2020-04-13 |     4,661 |    296 |     1,843 |   2,522 |
| Panama             | 2020-04-13 |     3,400 |     87 |        29 |   3,284 |
| Dominican Republic | 2020-04-13 |     3,167 |    177 |       152 |   2,838 |
| Colombia           | 2020-04-13 |     2,852 |    112 |       319 |   2,421 |
| Argentina          | 2020-04-13 |     2,208 |     97 |       515 |   1,596 |

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
| Iran                 | 2020-04-13 |    73,303 |  4,585 |    45,983 | 22,735 |
| Israel               | 2020-04-13 |    11,586 |    116 |     1,855 |  9,615 |
| Pakistan             | 2020-04-13 |     5,496 |     93 |     1,095 |  4,308 |
| Saudi Arabia         | 2020-04-13 |     4,934 |     65 |       805 |  4,064 |
| United Arab Emirates | 2020-04-13 |     4,521 |     25 |       852 |  3,644 |
| Qatar                | 2020-04-13 |     3,231 |      7 |       334 |  2,890 |

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
| China        | 2020-04-13 |    83,213 |  3,345 |    78,039 |  1,829 |
| Russia       | 2020-04-13 |    18,328 |    148 |     1,470 | 16,710 |
| Korea, South | 2020-04-13 |    10,537 |    217 |     7,447 |  2,873 |
| India        | 2020-04-13 |    10,453 |    358 |     1,181 |  8,914 |
| Japan        | 2020-04-13 |     7,370 |    123 |       784 |  6,463 |
| Australia    | 2020-04-13 |     6,351 |     61 |     1,806 |  4,484 |
| Philippines  | 2020-04-13 |     4,932 |    315 |       242 |  4,375 |
| Malaysia     | 2020-04-13 |     4,817 |     77 |     2,276 |  2,464 |
| Thailand     | 2020-04-13 |     2,579 |     40 |     1,288 |  1,251 |

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
| South Africa | 2020-04-13 |     2,272 |     27 |       410 |  1,835 |
| Egypt        | 2020-04-13 |     2,190 |    164 |       589 |  1,437 |
| Algeria      | 2020-04-13 |     1,983 |    313 |       601 |  1,069 |
| Morocco      | 2020-04-13 |     1,763 |    126 |       203 |  1,434 |

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
