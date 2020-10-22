
# Visualizing the Corona (COVID-19) pandemic

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
how many tests were conducted (for more information on this, see [this
article](https://www.sciencemag.org/news/2020/03/coronavirus-cases-have-dropped-sharply-south-korea-whats-secret-its-success?fbclid=IwAR3BnhqQMxCdu8-fQelEkWIDQn-j9UASV773Xl-WbIy8l7M5ZVSQpHFgkL8)
in Science).

Furthermore, I would like to emphasize that I am not an expert on
epidemology or virus outbreaks and I am not working in the health
sector. On this page, I am only visualizing the data by the John Hopkins
University. Reliance on the these visualizations for medical guidance or
use of these visualization in commerce is strictly prohibited.

#### Will these figures be updated?

The last update was made on 2020-10-22 08:49:39. The data of the John
Hopkins University, however, are always updated at 23:59. What you see
is hence the situation on 2020-10-21 at 23:59:00. Also bear in mind that
the reporting of cases is somewhat delayed so that it is very likely
that the actual numbers are higher.

## Visualizations

If you are interested in the R code, please see the
[README.rmd](https://github.com/masurp/corona_analyses/blob/master/README.rmd).

### 1\. Examplary patterns

<caption>

(\#tab:unnamed-chunk-2)

</caption>

<div data-custom-style="Table Caption">

\*\*

</div>

| country        |    date    |    confirmed |     deaths |    recovered |       active | new\_cases |
| :------------- | :--------: | -----------: | ---------: | -----------: | -----------: | ---------: |
| US             | 2020-10-21 | 8,336,031.00 | 222,176.00 | 3,323,354.00 | 4,790,501.00 |  62,735.00 |
| India          | 2020-10-21 | 7,651,107.00 | 115,914.00 | 6,795,103.00 |   740,090.00 |       0.00 |
| Brazil         | 2020-10-21 | 5,298,772.00 | 155,403.00 | 4,526,393.00 |   616,976.00 |  24,818.00 |
| Russia         | 2020-10-21 | 1,438,219.00 |  24,786.00 | 1,091,264.00 |   322,169.00 |  15,444.00 |
| Spain          | 2020-10-21 | 1,005,295.00 |  34,366.00 |   150,376.00 |   820,553.00 |  16,973.00 |
| United Kingdom | 2020-10-21 |   792,194.00 |  44,248.00 |     2,636.00 |   745,310.00 |  26,707.00 |
| Italy          | 2020-10-21 |   449,648.00 |  36,832.00 |   257,374.00 |   155,442.00 |  15,199.00 |
| Germany        | 2020-10-21 |   397,922.00 |   9,911.00 |   304,173.00 |    83,838.00 |  12,331.00 |
| China          | 2020-10-21 |    91,044.00 |   4,739.00 |    85,899.00 |       406.00 |      22.00 |

<img src="figures/unnamed-chunk-3-1.png" width="100%" />

### 2\. Worldwide developments

#### Europe

<img src="figures/europe_plot-1.png" width="100%" />

#### North, Middle and South America

<img src="figures/northamerica-1.png" width="100%" />

#### Middle East

<img src="figures/middleeast-1.png" width="100%" />

#### Asia, Indonesia, Australia

<img src="figures/asia-1.png" width="100%" />

#### Africa

<img src="figures/africa-1.png" width="100%" />

### 3\. Alternative visualizations

### Total cases

One thing that is constantly debatted is how to visualize the growth of
total confirmed cases at all. Log-transform the y-axis or not? Plot
against the date? Plot against days after 100th case? Plot something
entirely different?

Here, I would like to explain some differences between visualizations
that have been used in the media or on Twitter. All of them are helpful
in their own regard.

1.  LEFT: Here, I plotted total cases against days after the 100th cases
    *without* logarithmizing the y-axis.

2.  MIDDLE: The y-axis is logarithmized. This figure is often shown in
    the news.

3.  RIGHT: New cases per 7 days (y-axis) are plotted against total cases
    (x-axis), both axes are logarithmized (Idea explained in this
    [video](https://www.youtube.com/watch?v=54XLXg4fYsc)).

We see clearly that each plot has benefits and weaknesses. The first
example provides perhaps the best comparison of the total numbers and
shows quite drastically how exponential growth curves look likes (bear
in mind that I cut off the growth curve of the US, which actually
extends to more than 1,5 million cases. I did this to make the other
growth curves visible). S-curves represent positive developments towards
a slower growth. Yet, changes are barely identifiable.

The second example makes the actual growth more comparable and by
logarithmizing the y-axsis, we can actually see changes in the growth.
Here, it seems that most countries are actually starting to slow the
growth. Yet, the huge difference between e.g., Austria and the US is not
as visible as in the first plot.

Finally, the last example is a bit harder to understand, but it shows
best whether some sort of measure is working. The curve needs to sink
drastically, otherwise, the growth is continuing uncontrollibly.

<img src="figures/unnamed-chunk-8-1.png" width="100%" />

#### Daily new cases

Another visualization that is often used is based on changes in daily
new cases (here averaged cross one or two weeks).

##### Europe

<img src="figures/unnamed-chunk-9-1.png" width="100%" />

##### America

<img src="figures/unnamed-chunk-10-1.png" width="100%" />

##### Middle East

<img src="figures/unnamed-chunk-11-1.png" width="100%" />

##### Asia

<img src="figures/unnamed-chunk-12-1.png" width="100%" />

##### Africa

<img src="figures/unnamed-chunk-13-1.png" width="100%" />
