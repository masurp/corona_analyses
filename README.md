
# Visualizing total cases against a) active cases, b) deaths, and c) recovered cases

The analysis detailed below uses data taken from the official 2019 Novel
Coronavirus COVID-19 (2019-nCoV) Data Repository by Johns Hopkins CSSE:
<https://github.com/CSSEGISandData/COVID-19>

All three data sets can be downloaded here:
<https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series>

The same data sets are used to update this visual dashboard:
<https://coronavirus.jhu.edu/map.html>

## More information:

I have explained the meaning of these plots in the following
Twitter-Thread:
<https://twitter.com/MasurPhil/status/1239630219922804736>

``` r
library(tidyverse)
library(readr)

# Get total cases per country/region
d.cases <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Confirmed.csv" 

d.cases <- read_csv(url(d.cases)) %>%
  select(-Lat, -Long) %>%
  rename(province = "Province/State",
         country = "Country/Region") %>%
  gather(date, cases, -country, -province) %>%
  mutate(cases = as.numeric(cases),
         date = lubridate::mdy(date)) %>% 
  tbl_df

# Get number of deaths per country/region
d.deaths <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Deaths.csv" 

d.deaths <- read_csv(url(d.deaths)) %>%
  select(-Lat, -Long) %>%
  rename(province = "Province/State",
         country = "Country/Region") %>%
  gather(date, deaths, -country, -province) %>%
  mutate(deaths = as.numeric(deaths),
         date = lubridate::mdy(date)) %>%
  tbl_df

# Get number of recovered cases per country/region
d.recovered <- "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Recovered.csv" 

d.recovered <- read_csv(url(d.recovered)) %>%
  select(-Lat, -Long) %>%
  rename(province = "Province/State",
         country = "Country/Region") %>%
  gather(date, recovered, -country, -province) %>%
  mutate(recovered = as.numeric(recovered),
         date = lubridate::mdy(date)) %>% 
  tbl_df

# Join data sets by country, province, and date
d <- d.cases %>%
  left_join(d.deaths) %>%
  left_join(d.recovered) 

d$country[d$province=="Hong Kong"] <- "Hong Kong"

# Prepare data for visualization
data <- d %>%
  group_by(country, date) %>%
  summarize(cases = sum(cases),
            deaths = sum(deaths),
            recovered = sum(recovered)) %>%
  filter(country != "") %>%
  mutate(active = cases - (deaths + recovered)) %>%
  magrittr::set_colnames(c("country", "date", "total cases", "deaths", "recovered", "active"))


# Plot for China, Germany, Italy and Iran (first figure in Twitter-Thread)
data %>%
  filter(country == "China" | country == "Germany" | 
         country == "Italy" | country == "Iran") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  scale_color_brewer(palette = "Set2") +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-1-1.png" width="100%" />

``` r

ggsave("figures/plot_1.png",
       width = 8,
       height = 7)


# Plot for Hong Kong, Taiwan, and Singapore (Second figure in Twitter-Thread)
data %>%
  filter(country == "Hong Kong" | country == "Taiwan*" | country == "Singapore") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-1-2.png" width="100%" />

``` r

ggsave("figures/plot_2.png",
       width = 10,
       height = 5)


## North America
# Plot for USA and Canada, 
data %>%
  filter(country == "US" | country == "Canada") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-1-3.png" width="100%" />

``` r

ggsave("figures/plot_3.png",
       width = 6,
       height = 4)

## Europe
# Plot for European countries with > 500 total cases
data %>%
  filter(country %in% c("Italy", "Spain", "Germany", "France", "Switzerland", "United Kingdom", "Netherlands", "Norway", "Austria", "Sweden", "Belgium", "Denmark")) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-1-4.png" width="100%" />

``` r

ggsave("figures/plot_4.png",
       width = 15,
       height = 9)

## Asia
# Plot for Asian countries with > 500 cases
data %>%
  filter(country %in% c("China", "Korea, South", "Japan", "Malaysia")) %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="figures/unnamed-chunk-1-5.png" width="100%" />

``` r

ggsave("figures/plot_5.png",
       width = 8,
       height = 7)
```
