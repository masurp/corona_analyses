
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

!!!!!!!!! THE DATA ARE NO LONGER UPDATED ON THE JOHN HOPKINS UNIVERSIY DATA REPOSITORY !!!!!!!!


Yes, I will update these figures every morning. The last update was made
on 2020-03-31 18:24:38. The data of the John Hopkins University,
however, are always updated at 23:59. What you see is hence the
situation on 2020-03-30 at 23:59:00. Also bear in mind that the
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

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| Italy        | 2020-03-30 |   101,739 | 11,591 |    14,620 | 75,528 |
| China        | 2020-03-30 |    82,198 |  3,308 |    75,923 |  2,967 |
| Germany      | 2020-03-30 |    66,885 |    645 |    13,500 | 52,740 |
| Korea, South | 2020-03-30 |     9,661 |    158 |     5,228 |  4,275 |

<img src="figures/unnamed-chunk-2-1.png" width="100%" />

### 2\. Worldwide developments

#### Europe

<caption>

(\#tab:europe)

</caption>

<caption>

\*\*

</caption>

| country        |    date    | confirmed | deaths | recovered | active |
| :------------- | :--------: | --------: | -----: | --------: | -----: |
| Italy          | 2020-03-30 |   101,739 | 11,591 |    14,620 | 75,528 |
| Spain          | 2020-03-30 |    87,956 |  7,716 |    16,780 | 63,460 |
| Germany        | 2020-03-30 |    66,885 |    645 |    13,500 | 52,740 |
| France         | 2020-03-30 |    45,170 |  3,030 |     7,964 | 34,176 |
| United Kingdom | 2020-03-30 |    22,453 |  1,411 |       171 | 20,871 |
| Switzerland    | 2020-03-30 |    15,922 |    359 |     1,823 | 13,740 |
| Belgium        | 2020-03-30 |    11,899 |    513 |     1,527 |  9,859 |
| Netherlands    | 2020-03-30 |    11,817 |    865 |       253 | 10,699 |
| Turkey         | 2020-03-30 |    10,827 |    168 |       162 | 10,497 |
| Austria        | 2020-03-30 |     9,618 |    108 |       636 |  8,874 |
| Portugal       | 2020-03-30 |     6,408 |    140 |        43 |  6,225 |
| Norway         | 2020-03-30 |     4,445 |     32 |        12 |  4,401 |
| Sweden         | 2020-03-30 |     4,028 |    146 |        16 |  3,866 |
| Czechia        | 2020-03-30 |     3,001 |     23 |        25 |  2,953 |
| Ireland        | 2020-03-30 |     2,910 |     54 |         5 |  2,851 |
| Denmark        | 2020-03-30 |     2,755 |     77 |        73 |  2,605 |

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<caption>

(\#tab:unnamed-chunk-3)

</caption>

<caption>

\*\*

</caption>

| country |    date    | confirmed | deaths | recovered |  active |
| :------ | :--------: | --------: | -----: | --------: | ------: |
| US      | 2020-03-30 |   161,807 |  2,978 |     5,644 | 153,185 |
| Canada  | 2020-03-30 |     7,398 |     80 |       466 |   6,852 |
| Brazil  | 2020-03-30 |     4,579 |    159 |       120 |   4,300 |

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<caption>

\*\*

</caption>

| country  |    date    | confirmed | deaths | recovered | active |
| :------- | :--------: | --------: | -----: | --------: | -----: |
| Iran     | 2020-03-30 |    41,495 |  2,757 |    13,911 | 24,827 |
| Israel   | 2020-03-30 |     4,695 |     16 |       161 |  4,518 |
| Pakistan | 2020-03-30 |     1,717 |     21 |        76 |  1,620 |
| Qatar    | 2020-03-30 |       693 |      1 |        51 |    641 |

<img src="figures/middleeast-1.png" width="100%" />

#### Asia

<caption>

(\#tab:unnamed-chunk-5)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | confirmed | deaths | recovered | active |
| :----------- | :--------: | --------: | -----: | --------: | -----: |
| China        | 2020-03-30 |    82,198 |  3,308 |    75,923 |  2,967 |
| Korea, South | 2020-03-30 |     9,661 |    158 |     5,228 |  4,275 |
| Malaysia     | 2020-03-30 |     2,626 |     37 |       479 |  2,110 |
| Japan        | 2020-03-30 |     1,866 |     54 |       424 |  1,388 |

<img src="figures/asia-1.png" width="100%" />
