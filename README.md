
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
on 2020-05-08 09:28:52. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-05-07 at 23:59:00. Also bear in mind that the
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
| Italy        | 2020-05-07 |   215,858 | 29,958 |    96,276 | 89,624 |
| Germany      | 2020-05-07 |   169,430 |  7,392 |   141,700 | 20,338 |
| China        | 2020-05-07 |    83,975 |  4,637 |    78,977 |    361 |
| Korea, South | 2020-05-07 |    10,822 |    256 |     9,484 |  1,082 |

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
| Spain          | 2020-05-07 |   221,447 | 26,070 |   128,511 |  66,866 |
| Italy          | 2020-05-07 |   215,858 | 29,958 |    96,276 |  89,624 |
| United Kingdom | 2020-05-07 |   207,977 | 30,689 |       970 | 176,318 |
| France         | 2020-05-07 |   174,918 | 25,990 |    55,191 |  93,737 |
| Germany        | 2020-05-07 |   169,430 |  7,392 |   141,700 |  20,338 |
| Turkey         | 2020-05-07 |   133,721 |  3,641 |    82,984 |  47,096 |
| Belgium        | 2020-05-07 |    51,420 |  8,415 |    12,980 |  30,025 |
| Netherlands    | 2020-05-07 |    41,973 |  5,306 |       147 |  36,520 |
| Switzerland    | 2020-05-07 |    30,126 |  1,810 |    25,900 |   2,416 |
| Portugal       | 2020-05-07 |    26,715 |  1,105 |     2,258 |  23,352 |
| Sweden         | 2020-05-07 |    24,623 |  3,040 |     4,971 |  16,612 |
| Ireland        | 2020-05-07 |    22,385 |  1,403 |    17,110 |   3,872 |
| Austria        | 2020-05-07 |    15,752 |    609 |    13,698 |   1,445 |
| Poland         | 2020-05-07 |    15,047 |    755 |     4,862 |   9,430 |
| Romania        | 2020-05-07 |    14,499 |    888 |     6,144 |   7,467 |
| Ukraine        | 2020-05-07 |    13,691 |    340 |     2,396 |  10,955 |
| Denmark        | 2020-05-07 |    10,281 |    514 |     7,907 |   1,860 |
| Serbia         | 2020-05-07 |     9,848 |    206 |     2,160 |   7,482 |
| Norway         | 2020-05-07 |     8,034 |    217 |        32 |   7,785 |
| Czechia        | 2020-05-07 |     8,031 |    270 |     4,371 |   3,390 |
| Finland        | 2020-05-07 |     5,673 |    255 |     3,500 |   1,918 |
| Luxembourg     | 2020-05-07 |     3,859 |    100 |     3,505 |     254 |

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
| US                 | 2020-05-07 | 1,257,023 | 75,662 |   195,036 | 986,325 |
| Brazil             | 2020-05-07 |   135,773 |  9,190 |    55,350 |  71,233 |
| Canada             | 2020-05-07 |    66,201 |  4,541 |    29,260 |  32,400 |
| Peru               | 2020-05-07 |    58,526 |  1,627 |    18,388 |  38,511 |
| Ecuador            | 2020-05-07 |    30,298 |  1,654 |     3,433 |  25,211 |
| Mexico             | 2020-05-07 |    29,616 |  2,961 |    17,781 |   8,874 |
| Chile              | 2020-05-07 |    24,581 |    285 |    11,664 |  12,632 |
| Colombia           | 2020-05-07 |     9,456 |    407 |     2,300 |   6,749 |
| Dominican Republic | 2020-05-07 |     9,095 |    373 |     2,064 |   6,658 |
| Panama             | 2020-05-07 |     7,868 |    225 |       886 |   6,757 |
| Argentina          | 2020-05-07 |     5,371 |    282 |     1,601 |   3,488 |

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
| Iran                 | 2020-05-07 |   103,135 |  6,486 |    82,744 | 13,905 |
| Saudi Arabia         | 2020-05-07 |    33,731 |    219 |     7,798 | 25,714 |
| Pakistan             | 2020-05-07 |    24,644 |    585 |     6,464 | 17,595 |
| Qatar                | 2020-05-07 |    18,890 |     12 |     2,286 | 16,592 |
| Israel               | 2020-05-07 |    16,381 |    240 |    10,873 |  5,268 |
| United Arab Emirates | 2020-05-07 |    16,240 |    165 |     3,572 | 12,503 |

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
| Russia       | 2020-05-07 |   177,160 |  1,625 |    23,803 | 151,732 |
| China        | 2020-05-07 |    83,975 |  4,637 |    78,977 |     361 |
| India        | 2020-05-07 |    56,351 |  1,889 |    16,776 |  37,686 |
| Japan        | 2020-05-07 |    15,477 |    577 |     4,918 |   9,982 |
| Korea, South | 2020-05-07 |    10,822 |    256 |     9,484 |   1,082 |
| Philippines  | 2020-05-07 |    10,343 |    685 |     1,618 |   8,040 |
| Australia    | 2020-05-07 |     6,913 |     97 |     6,078 |     738 |
| Malaysia     | 2020-05-07 |     6,467 |    107 |     4,776 |   1,584 |
| Thailand     | 2020-05-07 |     2,992 |     55 |     2,772 |     165 |

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
| South Africa | 2020-05-07 |     8,232 |    161 |     3,153 |  4,918 |
| Egypt        | 2020-05-07 |     7,981 |    482 |     1,887 |  5,612 |
| Morocco      | 2020-05-07 |     5,548 |    183 |     2,179 |  3,186 |
| Algeria      | 2020-05-07 |     5,182 |    483 |     2,323 |  2,376 |

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
