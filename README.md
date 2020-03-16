
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

# Get total cases per country/region
d.cases <- read.csv("data_corona.csv") %>% 
  select(-Lat, -Long) %>%
  gather(date, cases, -country, -province) %>%
  separate(date, c("x", "date"), sep = 1) %>%
  mutate(cases = as.numeric(cases),
         date = lubridate::mdy(date)) %>% 
  select(-x) %>%
  tbl_df

# Get number of deaths per country/region
d.deaths <- read.csv("data_deaths.csv") %>% 
  select(-Lat, -Long) %>%
  gather(date, deaths, -country, -province) %>%
  separate(date, c("x", "date"), sep = 1) %>%
  mutate(deaths = as.numeric(deaths),
         date = lubridate::mdy(date)) %>%
  select(-x) %>%
  tbl_df

# Get number of recovered cases per country/region
d.recovered <- read.csv("data_recovered.csv") %>% 
  select(-Lat, -Long) %>%
  gather(date, recovered, -country, -province) %>%
  separate(date, c("x", "date"), sep = 1) %>%
  mutate(recovered = as.numeric(recovered),
         date = lubridate::mdy(date)) %>% 
  select(-x) %>%
  tbl_df

# Join data sets by country, province, and date
d <- d.cases %>%
  left_join(d.deaths) %>%
  left_join(d.recovered) 


# Prepare data for visualization
data <- d %>%
  filter(province != "Hong Kong") %>%
  bind_rows(., d %>%
  filter(province == "Hong Kong") %>%
  mutate(country = recode(as.character(country), 
                          "China" = "Hong Kong"))) %>% 
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

<img src="README_files/figure-gfm/unnamed-chunk-1-1.png" width="100%" />

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

<img src="README_files/figure-gfm/unnamed-chunk-1-2.png" width="100%" />

``` r

ggsave("figures/plot_2.png",
       width = 10,
       height = 5)


# Plot for USA
data %>%
  filter(country == "US") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="README_files/figure-gfm/unnamed-chunk-1-3.png" width="100%" />

``` r

ggsave("figures/plot_3.png",
       width = 6,
       height = 4)

# Plot for Europe
data %>%
  filter(country == "Netherlands" |
         country == "Belgium" |
         country == "France" |
         country == "United Kingdom") %>%
  gather(key, value, -country, -date) %>%
  ggplot(aes(x = date, y = value, color = key)) +
  geom_line() +
  facet_wrap(~country, scales = "free") +
  theme_bw() +
  scale_color_brewer(palette = "Set2") +
  labs(x = "date", y = "cases", color = "")
```

<img src="README_files/figure-gfm/unnamed-chunk-1-4.png" width="100%" />

``` r

ggsave("figures/plot_4.png",
       width = 8,
       height = 7)
```
