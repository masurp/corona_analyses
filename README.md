
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
on 2020-04-22 08:49:07. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-04-21 at 23:59:00. Also bear in mind that the
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

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered |  active |
| :----------- | :--------: | --------: | -----: | --------: | ------: |
| Italy        | 2020-04-21 |   183,957 | 24,648 |    51,600 | 107,709 |
| Germany      | 2020-04-21 |   148,291 |  5,033 |    95,200 |  48,058 |
| China        | 2020-04-21 |    83,853 |  4,636 |    77,799 |   1,418 |
| Korea, South | 2020-04-21 |    10,683 |    237 |     8,213 |   2,233 |

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
| Spain          | 2020-04-21 |   204,178 | 21,282 |    82,514 | 100,382 |
| Italy          | 2020-04-21 |   183,957 | 24,648 |    51,600 | 107,709 |
| France         | 2020-04-21 |   159,297 | 20,829 |    39,819 |  98,649 |
| Germany        | 2020-04-21 |   148,291 |  5,033 |    95,200 |  48,058 |
| United Kingdom | 2020-04-21 |   130,172 | 17,378 |       638 | 112,156 |
| Turkey         | 2020-04-21 |    95,591 |  2,259 |    14,918 |  78,414 |
| Belgium        | 2020-04-21 |    40,956 |  5,998 |     9,002 |  25,956 |
| Netherlands    | 2020-04-21 |    34,317 |  3,929 |        74 |  30,314 |
| Switzerland    | 2020-04-21 |    28,063 |  1,478 |    19,400 |   7,185 |
| Portugal       | 2020-04-21 |    21,379 |    762 |       917 |  19,700 |
| Ireland        | 2020-04-21 |    16,040 |    730 |     9,233 |   6,077 |
| Sweden         | 2020-04-21 |    15,322 |  1,765 |       550 |  13,007 |
| Austria        | 2020-04-21 |    14,873 |    491 |    10,971 |   3,411 |
| Poland         | 2020-04-21 |     9,856 |    401 |     1,297 |   8,158 |
| Romania        | 2020-04-21 |     9,242 |    498 |     2,153 |   6,591 |
| Denmark        | 2020-04-21 |     7,891 |    370 |     4,889 |   2,632 |
| Norway         | 2020-04-21 |     7,191 |    182 |        32 |   6,977 |
| Czechia        | 2020-04-21 |     7,033 |    201 |     1,753 |   5,079 |
| Serbia         | 2020-04-21 |     6,630 |    125 |       870 |   5,635 |
| Ukraine        | 2020-04-21 |     6,125 |    161 |       367 |   5,597 |
| Finland        | 2020-04-21 |     4,014 |    141 |     2,000 |   1,873 |
| Luxembourg     | 2020-04-21 |     3,618 |     78 |       670 |   2,870 |

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
| US                 | 2020-04-21 |   823,786 | 44,845 |    75,204 | 703,737 |
| Brazil             | 2020-04-21 |    43,079 |  2,741 |    22,991 |  17,347 |
| Canada             | 2020-04-21 |    39,401 |  1,908 |    13,188 |  24,305 |
| Peru               | 2020-04-21 |    17,837 |    484 |     6,982 |  10,371 |
| Chile              | 2020-04-21 |    10,832 |    147 |     4,969 |   5,716 |
| Ecuador            | 2020-04-21 |    10,398 |    520 |     1,207 |   8,671 |
| Mexico             | 2020-04-21 |     8,772 |    712 |     2,627 |   5,433 |
| Dominican Republic | 2020-04-21 |     5,044 |    245 |       463 |   4,336 |
| Panama             | 2020-04-21 |     4,658 |    136 |       204 |   4,318 |
| Colombia           | 2020-04-21 |     4,149 |    196 |       804 |   3,149 |
| Argentina          | 2020-04-21 |     3,031 |    147 |       840 |   2,044 |

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
| Iran                 | 2020-04-21 |    84,802 |  5,297 |    60,965 | 18,540 |
| Israel               | 2020-04-21 |    13,942 |    184 |     4,507 |  9,251 |
| Saudi Arabia         | 2020-04-21 |    11,631 |    109 |     1,640 |  9,882 |
| Pakistan             | 2020-04-21 |     9,565 |    201 |     2,073 |  7,291 |
| United Arab Emirates | 2020-04-21 |     7,755 |     46 |     1,443 |  6,266 |
| Qatar                | 2020-04-21 |     6,533 |      9 |       614 |  5,910 |

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
| China        | 2020-04-21 |    83,853 |  4,636 |    77,799 |  1,418 |
| Russia       | 2020-04-21 |    52,763 |    456 |     3,873 | 48,434 |
| India        | 2020-04-21 |    20,080 |    645 |     3,975 | 15,460 |
| Japan        | 2020-04-21 |    11,135 |    263 |     1,239 |  9,633 |
| Korea, South | 2020-04-21 |    10,683 |    237 |     8,213 |  2,233 |
| Philippines  | 2020-04-21 |     6,599 |    437 |       654 |  5,508 |
| Australia    | 2020-04-21 |     6,547 |     67 |     4,124 |  2,356 |
| Malaysia     | 2020-04-21 |     5,482 |     92 |     3,349 |  2,041 |
| Thailand     | 2020-04-21 |     2,811 |     48 |     2,108 |    655 |

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
| Egypt        | 2020-04-21 |     3,490 |    264 |       870 |  2,356 |
| South Africa | 2020-04-21 |     3,465 |     58 |     1,055 |  2,352 |
| Morocco      | 2020-04-21 |     3,209 |    145 |       393 |  2,671 |
| Algeria      | 2020-04-21 |     2,811 |    392 |     1,152 |  1,267 |

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
