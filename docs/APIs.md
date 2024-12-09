## General Template
- GET /api/v1/{collection-code}_{type-code}_{variable-code}_{product-code}_{aggregation-code}_{period-code}_{percentile-code}_{scenario-code}_{model-code}_{model-calculation-code}_{statistic-code}/{geocode}

## Variable-specific

### Variables that should definitely be adopted.

#### CRU data set > timeseries > monthly > 1901-2022 > mean > model "ts4.07"
- tas // Average Mean Surface Air Temperature
  - https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tas_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json
- tasmax // Average Maximum Surface Air Temperature
	- https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tasmax_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json
- tasmin // Average Minimum Surface Air Temperature
	- https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tasmin_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json

#### ERA5 data set > timeseries
- cdd65 // Cooling Degree Days (ref-65°F)
	- ...
- hd35 // Number of Hot Days (Tmax > 35°C)
	- ...
- hd40 // Number of Hot Days (Tmax > 40°C)
	- ...
- hd42 // Number of Hot Days (Tmax > 42°C)
	- ...
- hdd65 // Heating degree days (ref-65°F)
	- ...
- hi35 // Number of Days with Heat Index > 35°C
	- ...
- hi37 // Number of Days with Heat Index > 37°C
	- ...
- hurs // Relative Humidity
	- ...
- prpercnt // Precipitation Percent Change
	- ...
- rx1day // Average Largest 1-Day Precipitation
	- ...
- rx5day // Average Largest 5-Day Cumulative Precipitation
	- ...
- tnn // Minimum of Daily Min-Temperature
	- ...
- tx84rr // Excess Mortality
	- ...

- https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tas_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json
- https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tasmax_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json
- https://cckpapi.worldbank.org/cckp/v1/cru-x0.5_timeseries_tasmin_timeseries_monthly_1901-2022_mean_historical_cru_ts4.07_mean/all_countries?_format=json

- txx // Maximum of Daily Max-Temperature
	- ...
