## General Template
- GET /api/v1/{collection-code}_{type-code}_{variable-code}_{product-code}_{aggregation-code}_{period-code}_{percentile-code}_{scenario-code}_{model-code}_{model-calculation-code}_{statistic-code}/{geocode}

## Variable-specific

### Variables that should definitely be adopted.

#### CRU data set > timeseries > monthly > 1901-2022 > mean > model "ts4.07"
- API Structure: https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_{variable_name}_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json

- tas // Average Mean Surface Air Temperature
- tasmax // Average Maximum Surface Air Temperature
- tasmin // Average Minimum Surface Air Temperature

#### ERA5 data set > timeseries > monthly > 1950-2023 > mean > model "era5" > model label "x0.25"
- API Structure: https://cckpapi.worldbank.org/cckp/v1/era5-x0.25_timeseries_{variable_name}_timeseries_monthly_1950-2023_mean_historical_era5_x0.25_mean/all_countries?_format=json

- cdd65 // Cooling Degree Days (ref-65°F)
- hd35 // Number of Hot Days (Tmax > 35°C)
- hd40 // Number of Hot Days (Tmax > 40°C)
- hd42 // Number of Hot Days (Tmax > 42°C)
- hdd65 // Heating degree days (ref-65°F)
- hi35 // Number of Days with Heat Index > 35°C
- hi37 // Number of Days with Heat Index > 37°C
- hurs // Relative Humidity
- prpercnt // Precipitation Percent Change
- rx1day // Average Largest 1-Day Precipitation
- rx5day // Average Largest 5-Day Cumulative Precipitation
- tnn // Minimum of Daily Min-Temperature
- tx84rr // Excess Mortality
- txx // Maximum of Daily Max-Temperature

### Variables that should probably be adopted (all ERA5).
- API Structure: https://cckpapi.worldbank.org/cckp/v1/era5-x0.25_timeseries_{variable_name}_timeseries_monthly_1950-2023_mean_historical_era5_x0.25_mean/all_countries?_format=json

- pr // Precipitation // G: "Total wet day precipitation" // similar, not identical to existing "pr" variable // This variable is average precipitation over a given time // Potentially also includes smaller variation of rain below 1mm
- hd30 // Number of Hot Days (Tmax > 30°C) //  G: - // Overlaping with existing hd35, hd40, hd42
- hd45 // Number of Hot Days (Tmax > 45°C) // G: - // Only daily maximum temperature per month/year.
- hd50 // Number of Hot Days (Tmax > 50°C) // G: - // Only daily maximum temperature per month/year.
- hi39 // Number of Days with Heat Index > 39°C // Did not include variable that was available
- hi41 // Number of Days with Heat Index > 41°C // G: - // Did not include variable that was available
- r50mm // Number of Days with Precipitation >50mm // G: - // Only "Very heavy precipitation days" = days with more than 20mm
- r95ptot // Precipitation amount during wettest days //  G: - // Did not include identical variable "Very wet day precipitation"
- tr23 // Number of Tropical Nights (T-min > 23°C) // [Very similar to "tr"]
- tr26 // Number of Tropical Nights (T-min > 26°C) // [Very similar to "tr"]
- tr29 // Number of Tropical Nights (T-min > 29°C) // [Very similar to "tr"]
- tr32 // Number of Tropical Nights (T-min > 32°C) // [Very similar to "tr"]

### Variables should probably NOT be adopted (all ERA5)
- API Structure: https://cckpapi.worldbank.org/cckp/v1/era5-x0.25_timeseries_{variable_name}_timeseries_monthly_1950-2023_mean_historical_era5_x0.25_mean/all_countries?_format=json

- fd // Number of Frost Days (Tmin < 0°C) // G: Almost identical variable // G: count variable // Here: Average over time, i.e. data period. Smoothed-out, long-term perspective of Frost Days; Less interesting for forecasting.
- id // Number of Ice Days (Tmax < 0°C) // G: Almost identical variable // G: count variable // Here: Average over time, i.e. data period. Smoothed-out, long-term perspective of Ice Days; Less interesting for forecasting.
- tx84rr // Excess Mortality // ERROR: API IS EMPTY
