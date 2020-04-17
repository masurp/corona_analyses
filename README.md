
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
on 2020-04-17 08:43:41. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-16 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-04-16 |   168,941 | 22,170 |    40,164 | 106,607 |
| Germany      | 2020-04-16 |   137,698 |  4,052 |    77,000 |  56,646 |
| China        | 2020-04-16 |    83,403 |  3,346 |    78,401 |   1,656 |
| Korea, South | 2020-04-16 |    10,613 |    229 |     7,757 |   2,627 |

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
| Spain          | 2020-04-16 |   184,948 | 19,315 |    74,797 |  90,836 |
| Italy          | 2020-04-16 |   168,941 | 22,170 |    40,164 | 106,607 |
| France         | 2020-04-16 |   147,091 | 17,941 |    33,327 |  95,823 |
| Germany        | 2020-04-16 |   137,698 |  4,052 |    77,000 |  56,646 |
| United Kingdom | 2020-04-16 |   104,145 | 13,759 |       375 |  90,011 |
| Turkey         | 2020-04-16 |    74,193 |  1,643 |     7,089 |  65,461 |
| Belgium        | 2020-04-16 |    34,809 |  4,857 |     7,562 |  22,390 |
| Netherlands    | 2020-04-16 |    29,383 |  3,327 |       311 |  25,745 |
| Switzerland    | 2020-04-16 |    26,732 |  1,281 |    15,900 |   9,551 |
| Portugal       | 2020-04-16 |    18,841 |    629 |       493 |  17,719 |
| Austria        | 2020-04-16 |    14,476 |    410 |     8,986 |   5,080 |
| Ireland        | 2020-04-16 |    13,271 |    486 |        77 |  12,708 |
| Sweden         | 2020-04-16 |    12,540 |  1,333 |       550 |  10,657 |
| Poland         | 2020-04-16 |     7,918 |    314 |       774 |   6,830 |
| Romania        | 2020-04-16 |     7,707 |    392 |     1,357 |   5,958 |
| Denmark        | 2020-04-16 |     7,074 |    321 |     3,203 |   3,550 |
| Norway         | 2020-04-16 |     6,896 |    152 |        32 |   6,712 |
| Czechia        | 2020-04-16 |     6,433 |    169 |       972 |   5,292 |
| Serbia         | 2020-04-16 |     5,318 |    103 |         0 |   5,215 |
| Ukraine        | 2020-04-16 |     4,161 |    116 |       186 |   3,859 |
| Luxembourg     | 2020-04-16 |     3,444 |     69 |       552 |   2,823 |
| Finland        | 2020-04-16 |     3,369 |     75 |     1,700 |   1,594 |

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
| US                 | 2020-04-16 |   667,801 | 32,916 |    54,703 | 580,182 |
| Canada             | 2020-04-16 |    30,808 |  1,257 |     9,698 |  19,853 |
| Brazil             | 2020-04-16 |    30,425 |  1,924 |    14,026 |  14,475 |
| Peru               | 2020-04-16 |    12,491 |    274 |     6,120 |   6,097 |
| Chile              | 2020-04-16 |     8,807 |    105 |     3,299 |   5,403 |
| Ecuador            | 2020-04-16 |     8,225 |    403 |       838 |   6,984 |
| Mexico             | 2020-04-16 |     5,847 |    449 |     2,125 |   3,273 |
| Dominican Republic | 2020-04-16 |     3,755 |    196 |       215 |   3,344 |
| Panama             | 2020-04-16 |     3,751 |    103 |        75 |   3,573 |
| Colombia           | 2020-04-16 |     3,233 |    144 |       550 |   2,539 |
| Argentina          | 2020-04-16 |     2,571 |    115 |       631 |   1,825 |

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
| Iran                 | 2020-04-16 |    77,995 |  4,869 |    52,229 | 20,897 |
| Israel               | 2020-04-16 |    12,758 |    142 |     2,818 |  9,798 |
| Pakistan             | 2020-04-16 |     6,919 |    128 |     1,645 |  5,146 |
| Saudi Arabia         | 2020-04-16 |     6,380 |     83 |       990 |  5,307 |
| United Arab Emirates | 2020-04-16 |     5,825 |     35 |     1,095 |  4,695 |
| Qatar                | 2020-04-16 |     4,103 |      7 |       415 |  3,681 |

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
| China        | 2020-04-16 |    83,403 |  3,346 |    78,401 |  1,656 |
| Russia       | 2020-04-16 |    27,938 |    232 |     2,304 | 25,402 |
| India        | 2020-04-16 |    13,430 |    448 |     1,768 | 11,214 |
| Korea, South | 2020-04-16 |    10,613 |    229 |     7,757 |  2,627 |
| Japan        | 2020-04-16 |     8,626 |    178 |       901 |  7,547 |
| Australia    | 2020-04-16 |     6,462 |     63 |     2,355 |  4,044 |
| Philippines  | 2020-04-16 |     5,660 |    362 |       435 |  4,863 |
| Malaysia     | 2020-04-16 |     5,182 |     84 |     2,766 |  2,332 |
| Thailand     | 2020-04-16 |     2,672 |     46 |     1,593 |  1,033 |

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
| Egypt        | 2020-04-16 |     2,673 |    196 |       596 |  1,881 |
| South Africa | 2020-04-16 |     2,605 |     48 |       903 |  1,654 |
| Morocco      | 2020-04-16 |     2,283 |    130 |       249 |  1,904 |
| Algeria      | 2020-04-16 |     2,268 |    348 |       783 |  1,137 |

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
