
# Visualizing the Corona (COVID-19) pandemic

## Basic idea

I generally think that the news do a good job in describing and
visualizing the corona pandemic. However, there are two things that I
believe are quite problematic and that I am missing the any news
coverage on the pandemic.

1.  Visualizations of the growth curves often log-transform the x-axis
    instead of showing the actual *exponential* growth.
2.  Visualizations never plot *total* cases against a) deaths, b)
    recovered, AND c) active cases.

With regard to the former, I recently wrote [this
blogpost](http://philippmasur.de/blog/2020/03/13/understanding-exponential-growth-the-corona-pandemic/)
that explains why exponential growth is so hard to grasp. With regard to
the latter, I believe that showing only the total cases growth curve can
be misleading or at least is not sufficient to understand the pandemic
and to judge whether certain measures work or not. Visualizations would
become a lot more informative, if we also look at the active cases
vs. recovered cases vs. deaths. Looking at all *four* curves
simultaneously, we see how well a country succeeds in stopping the
infections.

In what follows, I am using actual data on worldwide total infections,
death rates, and number of recoveries to produce more insightful
visualizations.

### Where does the data come frome?

The analyses and visualizations are based on the data provided by the
John Hopkins University in the [Official 2019 Novel Coronavirus COVID-19
(2019-nCoV) Data
Repository](https://github.com/CSSEGISandData/COVID-19). The same data
sets are used to constantly update this visual dashboard:
<https://coronavirus.jhu.edu/map.html>

### Will these figures be updated?

Yes, I will update these figures every morning. The last update was made
on 2020-03-18 07:51:30. The data of the John Hopkins University,
however, is always updated at 23:59. What you see is hence the situation
on 2020-03-17 at 23:59.

## The analyses

The following code downloads the data sets and transforms them directly
to be ready for the visualizations. Overall, the data is already in a
very tidy format. As I am not focusing on provinces, we only summarize
the cases across countries and dates (NOT provinces). That said, I
distinguish China and Hong Kong due to their different timelines in
responding to the virus outbreak.

``` r
library(tidyverse)
library(readr)

# Function to crawl data from the github repository
get_data <- function(url) {
  read_csv(url(url)) %>%
  select(-Lat, -Long) %>%
  rename(province = "Province/State",
         country = "Country/Region") %>%
  gather(date, type, -country, -province) %>%
  mutate(type = as.numeric(type),
         date = lubridate::mdy(date)) %>% 
  tbl_df
}

# Get total cases per country/region
cases <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Confirmed.csv" 

# Get number of deaths per country/region
deaths <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Deaths.csv" 

# Get number of recovered cases per country/region
recovered <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Recovered.csv" 

# Prepare data
d_cases <- get_data(cases) %>%
  rename(cases = type)
d_deaths <- get_data(deaths) %>%
  rename(deaths = type)
d_recovered <- get_data(recovered) %>%
  rename(recovered = type)

# Join data sets by country, province, and date
d <- d_cases %>%
  left_join(d_deaths) %>%
  left_join(d_recovered) 

# Distinguish Hong Kong and China
d$country[d$province=="Hong Kong"] <- "Hong Kong"

# Prepare data for visualization
data <- d %>%
  group_by(country, date) %>%
  summarize(cases = sum(cases),
            deaths = sum(deaths),
            recovered = sum(recovered)) %>%
  filter(country != "") %>%
  mutate(active = cases - (deaths + recovered)) %>%
  magrittr::set_colnames(c("country", "date", "total cases", "deaths", "recovered", "active")) %>%
  ungroup
```

### 1\. Most exemplary developments of the corona pandemic

In a first step, I am comparing China, South Korea, Italy, and Germany.
Why these four countries? These four countries are at different stages
during the corona pandemic. China was the first to experience the
outbreak and they have almost contained the spreading of the virus by
now. South Korea is close to containg the virus. Italy is experiencing
the second worst pandemic after China and drastic measures have been
taken. The virus has reached Germany considerably later, but the growth
rate is very steep. By comparing these countries, we can learn a lot
about “typical” growth rates and patterns.

``` r
# Current cases 
table <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country == "China" | country == "Germany" | 
         country == "Italy" | country == "Korea, South") %>%
  arrange(desc(`total cases`))
papaja::apa_table(table, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-2)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | total cases | deaths | recovered | active |
| :----------- | :--------: | ----------: | -----: | --------: | -----: |
| China        | 2020-03-17 |      80,896 |  3,226 |    68,710 |  8,960 |
| Italy        | 2020-03-17 |      31,506 |  2,503 |     2,941 | 26,062 |
| Germany      | 2020-03-17 |       9,257 |     24 |        67 |  9,166 |
| Korea, South | 2020-03-17 |       8,320 |     81 |     1,407 |  6,832 |

``` r
# Example plot for China, Germany, Italy and South Korea
data %>%
  filter(`total cases` >= 1) %>%
  filter(country == "China" | country == "Germany" | 
         country == "Italy" | country == "Korea, South") %>%
  mutate(country = factor(country, 
                          levels = c("China", "Korea, South", 
                                     "Italy", "Germany"))) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  scale_color_brewer(palette = "Set2") +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-3-1.png" width="100%" />

``` r

ggsave("figures/plot_1.png",
       width = 8,
       height = 7)
```

CHINA (upper left): The number of *total* confirmed cases is still
rising (pink), but only very slowly and almost comes to a halt. But, the
number of *active* cases (green) is declining steeply and at the same
time the number of *recovered* cases (blue) is increasing a lot, slowly
approximating the number of *total* cases. This is how it should look
like as this pattern shows that measures are working and the spreading
of the virus is stopping.

SOUTH KOREA (upper right): The number of *total* confirmed cases is
still rising (pink), but the growth rate slowly resembles a S-curve.
This is a good sign, because new infections are fewer. The number of
*active* cases (green) is hence starting to decline (since the 15th of
March) and at the same time the number of *recovered* cases (blue) is
starting to grow.

ITALY (lower left): the number of *total* confirmed cases is growing
exponentially. More importantly, the number of *active* cases is almost
equivalent to the number of *total* cases. The number of *recovered*
cases sadly equals the number of *deaths*. So far, we do not see
implications of the drastic measures taken by the Italian government.
Yet, recent analyses of the number of *total* cases suggest the curve is
slowly declining (which would be a sign of hope\!).

GERMANY (lower right): The number of *total* confirmed cases likewise
grows exponentially. Again (see Italy), the number of *active* cases is
practically equivalent to the number of *total* cases (so far, luckily
only few *deaths*, but also only few recovered).

**Conclusion:** As long as we do not see signs that the curves approach
a similar pattern as in China, the virus is still spreading
uncontrollably.

### 2\. Development in countries that reacted fast

Although the number of cases in these countries is small (a good
thing\!), we should look at the distributions of countries that reacted
fast and efficiently (e.g., Hong Kong, Taiwan, Singapore).

``` r
# Current cases 
table2 <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country == "Hong Kong" | 
         country == "Taiwan*" | 
         country == "Singapore") %>%
  arrange(desc(`total cases`))
papaja::apa_table(table2, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-4)

</caption>

<caption>

\*\*

</caption>

| country   |    date    | total cases | deaths | recovered | active |
| :-------- | :--------: | ----------: | -----: | --------: | -----: |
| Singapore | 2020-03-17 |         266 |      0 |       114 |    152 |
| Hong Kong | 2020-03-17 |         162 |      4 |        88 |     70 |
| Taiwan\*  | 2020-03-17 |          77 |      1 |        22 |     54 |

``` r
# Plot for Hong Kong, Taiwan, and Singapore 
data %>%
  filter(`total cases` >= 1) %>%
  filter(country == "Hong Kong" | 
         country == "Taiwan*" | 
         country == "Singapore") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-5-1.png" width="100%" />

``` r

ggsave("figures/plot_2.png",
       width = 8,
       height = 3)
```

We clearly see that the number of *active* cases is declining earlier.
At the same time the number of *total* cases increases not
exponentially\!

### The situation in Europe

A comparative plot of all countries with more than 500 confirmed total
cases.

``` r
europe <- c("Italy", "Spain", "Germany", "France", 
            "Switzerland", "United Kingdom", "Netherlands", 
            "Norway", "Austria", "Sweden", "Belgium", "Denmark")

# Current cases 
table3 <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country %in% europe) %>%
  arrange(desc(`total cases`))
papaja::apa_table(table3, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-6)

</caption>

<caption>

\*\*

</caption>

| country        |    date    | total cases | deaths | recovered | active |
| :------------- | :--------: | ----------: | -----: | --------: | -----: |
| Italy          | 2020-03-17 |      31,506 |  2,503 |     2,941 | 26,062 |
| Spain          | 2020-03-17 |      11,748 |    533 |     1,028 | 10,187 |
| Germany        | 2020-03-17 |       9,257 |     24 |        67 |  9,166 |
| France         | 2020-03-17 |       7,699 |    148 |        12 |  7,539 |
| Switzerland    | 2020-03-17 |       2,700 |     27 |         4 |  2,669 |
| United Kingdom | 2020-03-17 |       1,960 |     56 |        53 |  1,851 |
| Netherlands    | 2020-03-17 |       1,708 |     43 |         2 |  1,663 |
| Norway         | 2020-03-17 |       1,463 |      3 |         1 |  1,459 |
| Austria        | 2020-03-17 |       1,332 |      3 |         1 |  1,328 |
| Belgium        | 2020-03-17 |       1,243 |     10 |         1 |  1,232 |
| Sweden         | 2020-03-17 |       1,190 |      7 |         1 |  1,182 |
| Denmark        | 2020-03-17 |       1,024 |      4 |         1 |  1,019 |

``` r
data %>%
  filter(`total cases` >= 1) %>%
  filter(country %in% europe) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-7-1.png" width="100%" />

``` r

ggsave("figures/plot_3.png",
       width = 10,
       height = 6)
```

### USA and Canada

``` r
# Current cases 
table4 <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country == "US" | country == "Canada") %>%
  arrange(desc(`total cases`))
papaja::apa_table(table4, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-8)

</caption>

<caption>

\*\*

</caption>

| country |    date    | total cases | deaths | recovered | active |
| :------ | :--------: | ----------: | -----: | --------: | -----: |
| US      | 2020-03-17 |       6,421 |    108 |        17 |  6,296 |
| Canada  | 2020-03-17 |         478 |      5 |         9 |    464 |

``` r
data %>%
  filter(`total cases` >= 1) %>%
  filter(country == "US" | country == "Canada") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-9-1.png" width="100%" />

``` r

ggsave("figures/plot_4.png",
       width = 7,
       height = 3)
```

### Middle East

``` r
# Current cases 
table5 <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country %in% c("Iran", "Qatar", 
                        "Israel", "Pakistan")) %>%
  arrange(desc(`total cases`))
papaja::apa_table(table5, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-10)

</caption>

<caption>

\*\*

</caption>

| country  |    date    | total cases | deaths | recovered | active |
| :------- | :--------: | ----------: | -----: | --------: | -----: |
| Iran     | 2020-03-17 |      16,169 |    988 |     5,389 |  9,792 |
| Qatar    | 2020-03-17 |         439 |      0 |         4 |    435 |
| Israel   | 2020-03-17 |         337 |      0 |        11 |    326 |
| Pakistan | 2020-03-17 |         236 |      0 |         2 |    234 |

``` r
data %>%
  filter(country %in% c("Iran", "Qatar", 
                        "Israel", "Pakistan")) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-11-1.png" width="100%" />

``` r

ggsave("figures/plot_5.png",
       width = 8,
       height = 7)
```

### Asia

Plot for Asian countries with \> 500 cases.

``` r
# Current cases 
table6 <- data %>%
  filter(date == as.character(Sys.Date()-1)) %>%
  filter(country %in% c("China", "Korea, South", "Japan", "Malaysia")) %>%
  arrange(desc(`total cases`))
papaja::apa_table(table6, format = "html", digits = 0, align = c("l", "c", rep("r", 4)))
```

<caption>

(\#tab:unnamed-chunk-12)

</caption>

<caption>

\*\*

</caption>

| country      |    date    | total cases | deaths | recovered | active |
| :----------- | :--------: | ----------: | -----: | --------: | -----: |
| China        | 2020-03-17 |      80,896 |  3,226 |    68,710 |  8,960 |
| Korea, South | 2020-03-17 |       8,320 |     81 |     1,407 |  6,832 |
| Japan        | 2020-03-17 |         878 |     29 |       144 |    705 |
| Malaysia     | 2020-03-17 |         673 |      2 |        49 |    622 |

``` r
data %>%
  filter(country %in% c("China", "Korea, South", "Japan", "Malaysia")) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free_y") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-13-1.png" width="100%" />

``` r

ggsave("figures/plot_6.png",
       width = 8,
       height = 7)
```

Let me know if I should include any other countries in on this page.
