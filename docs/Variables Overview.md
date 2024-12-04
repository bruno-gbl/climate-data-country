## Ressources
- [Data Download API, WorldBank](https://climateknowledgeportal.worldbank.org/download-data#htab-1497)
- [Data Catalogue, Worldbank](https://climateknowledgeportal.worldbank.org/download-data#htab-1499)
- [Variable List (p. 10 ff.), Worldbank](https://climateknowledgeportal.worldbank.org/media/document/metatag.pdf)
- [Climate-data-project, Notion](https://www.notion.so/Climate-data-ingestion-bab76c3ef377496787583f53fdbdba76?pvs=4)

- [Documentation, climate data ingestion, Notion](https://www.notion.so/VIEWS-PIN-CRAF-D-8e9666d1bbaa455ead5608c7f256a354?pvs=4)
- [Documentation, Ingester3, GitHub](https://github.com/UppsalaConflictDataProgram/ingester3_loaders/blob/gadm_pg/Ingester3_documentation.ipynb)
- Examples: [Folder, GitHub](https://github.com/UppsalaConflictDataProgram/ingester3_loaders)
	- [WDI, Malika, GitHub](https://github.com/UppsalaConflictDataProgram/ingester3_loaders/blob/main/WDI_master/World_bank_loader.ipynb)
 	- [KCMD, Maxine, GitHub](https://github.com/UppsalaConflictDataProgram/ingester3_loaders/blob/main/mig_loaders/KCMD_loader.ipynb)
  	- [ACLED, GitHub](https://github.com/UppsalaConflictDataProgram/ingester3_loaders/blob/gadm_pg/ACLED_loader.ipynb)


---

## New variables: World Bank @country Level, not covered by Garrett's PRIO-GRID variables

### Variables that should definitely be adopted.
- tas
	- Average Mean Surface Air Temperature
   	- G: Only relative temperature variables
- tasmax
	- Average Maximum Surface Air Temperature
	- G: Only relative temperature variables
- tasmin
	- Average Minimum Surface Air Temperature
 	- G: Only relative temperature variables
- cdd65
	- Cooling Degree Days (ref-65°F)
 	- G: -
- hd35
	- Number of Hot Days (Tmax > 35°C)
 	- G: - // Only daily maximum temperature per month/year.
- hd40
	- Number of Hot Days (Tmax > 40°C)
	- G: - // Only daily maximum temperature per month/year.
- hd42
	- Number of Hot Days (Tmax > 42°C)
	- G: - // Only daily maximum temperature per month/year.
- hdd65
	- Heating degree days (ref-65°F)
	- G: -
- hi35
	- Number of Days with Heat Index > 35°C
	- G: - // Did not include variable that was available
- hi37
	- Number of Days with Heat Index > 37°C
	- G: - // Did not include variable that was available
- hurs
	- Relative Humidity
	- G: -
- prpercnt
	- Precipitation Percent Change
 	- G: - // Only absolute values.
- rx1day
	- Average Largest 1-Day Precipitation
	- G: -	
- rx5day
	- Average Largest 5-Day Cumulative Precipitation
	- G: -	
- tnn
	- Minimum of Daily Min-Temperature
 	- G: -
- tx84rr
	- Excess Mortality
	- G: -
- txx
	- Maximum of Daily Max-Temperature
	- G: -	

### Variables that should probably be adopted.
- pr
	- Precipitation
	- G: "Total wet day precipitation" // similar, not identical // This variable is average precipitation over a given time // Potentially also includes smaller variation of rain below 1mm
- hd30
	- Number of Hot Days (Tmax > 30°C)
	- G: - // Only daily maximum temperature per month/year.
- hd45
	- Number of Hot Days (Tmax > 45°C)
	- G: - // Only daily maximum temperature per month/year.	
- hd50
	- Number of Hot Days (Tmax > 50°C)
	- G: - // Only daily maximum temperature per month/year.	
- hi39
	- Number of Days with Heat Index > 39°C
	- G: - // Did not include variable that was available	
- hi41
	- Number of Days with Heat Index > 41°C
	- G: - // Did not include variable that was available	
- r50mm
	- Number of Days with Precipitation >50mm
	- G: - // Only "Very heavy precipitation days" = days with more than 20mm
- r95ptot
	- Precipitation amount during wettest days
	- G: - // Did not include identical variable "Very wet day precipitation"
- tr23
	- Number of Tropical Nights (T-min > 23°C)
	- [Very similar to "tr"]	
- tr26
	- Number of Tropical Nights (T-min > 26°C)
	- [Very similar to "tr"]	
- tr29
	- Number of Tropical Nights (T-min > 29°C)
	- [Very similar to "tr"]	
- tr32
	- Number of Tropical Nights (T-min > 32°C)
	- [Very similar to "tr"]	

### Variables that should probably not be adopted.
- fd
	- Number of Frost Days (Tmin < 0°C)
	- G: Almost identical variable // G: count variable // Here: Average over time, i.e. data period. Smoothed-out, long-term perspective of Frost Days; Less interesting for forecasting.	
- id
	- Number of Ice Days (Tmax < 0°C)
	- G: Almost identical variable // G: count variable // Here: Average over time, i.e. data period. Smoothed-out, long-term perspective of Ice Days; Less interesting for forecasting.	

### Variables that should definitely not be adopted.
- cdd
	- Maximum number of consecutive dry days
	- G: Identical variable
- csdi
	- Cold Spell Duration Index
	- Only annual data
- cwd
	- Max Number of Consecutive Wet Days
	- G: Identical variable
- gslend
	- Growing Season Length End
	- G: Identical variable
- gslstart
	- Growing Season Length Start
	- G: Identical variable
- r20mm
	- Number of Days with Precipitation >20mm
	- G: Identical variable // "Very heavy precipitation days" = days with more than 20mm
- sd
	- Number of Summer Days (Tmax > 25°C)
	- G: Identical variable.
- tr
	- Number of Tropical Nights (T-min > 20°C)
	- G: Identical Variable
- wsdi
	- Warm Spell Duration Index
	- Only annual data

----

## Variables used by Garrett on the PRIO-Grid Level

### Used by Garret
- Cold days
- Cold nights
- Consecutive dry days
- Consecutive wet days
- Diurnal temperature range
- Frost days
- Growing season length
- Heavy precipitation days
- Ice days
- Maximum 1-day precipitation
- Maximum 5-day precipitation
- Maximum value of daily maximum temperature
- Maximum value of daily minimum temperature
- Minimum value of daily maximum temperature
- Minimum value of daily minimum temperature
- Number of wet days
- Simple daily intensity index
- Summer days
- Total wet day precipitation
- Tropical nights
- Very heavy precipitation days
- Warm days
- Warm nights

### Further existing variables on the Climate Data Store site
- Cold spell duration index
- Extremely wet day precipitation
- Very wet day precipitation
- Warm spell duration index
- Heat index
- Humidex
- Indoor universal thermal climate index
- Wet-bulb temperature
- Indoor wet-bulb globe temperature

-----------------------

## Archive

### Taken from his GitHub main.py file
- **"consecutive_dry_days"**
- **"consecutive_wet_days"**
- **"diurnal_temperature_range"**
- **"frost_days"**
- **"growing_season_length"**
- **"heavy_precipitation_days"**
- **"ice_days"**
- **"maximum_1_day_precipitation"**
- **"maximum_5_day_precipitation"**
- **"maximum_value_of_daily_maximum_temperature"**
- **"minimum_value_of_daily_maximum_temperature"**
- **"maximum_value_of_daily_minimum_temperature"**
- **"minimum_value_of_daily_minimum_temperature"**
- **"number_of_wet_days"**
- **"simple_daily_intensity_index"**
- **"summer_days"**
- **"total_wet_day_precipitation"**
- **"tropical_nights"**
- **"very_heavy_precipitation_days"**
- **"cold_days"**
- **"cold_nights"**
- **"warm_days"**
- **"warm_nights"**

### Taken from Paola's Website
- **Cold days**
	- %
	- Percentage of days with maximum temperature below the corresponding calendar day 10th percentile of maximum temperature for a 5-day moving window in the base period. The ETCCDI short name for this variable is "TX10p".
- **Cold nights**
	- %
	- Percentage of days with minimum temperature below the corresponding calendar day 10th percentile of minimum temperature for a 5-day moving window in the base period. The ETCCDI short name for this variable is "TN10p".
- Cold spell duration index
	- day
	- Annual count of days with at least 6 consecutive days when daily minimum temperature is below the calendar day 10th percentile of minimum temperature centered on a 5-day sliding window during the base period. The ETCCDI short name for this variable is "CSDI".
- **Consecutive dry days**
	- day
	- Maximum number of days in a row with precipitation below 1 mm in a year. If a dry spell does not end in a particular year and spans a period longer than 1 year (as may happen in very dry regions), then CDD is not reported for that year and the accumulated dry days are carried forward to the year when the spell ends. The ETCCDI short name for this variable is "CDD".
- **Consecutive wet days**
	- day
	- Maximum number of days in a row with precipitation above 1 mm in a year. If a wet spell does not end in a particular year and spans a period longer than 1 year (as may happen in very wet regions), then it is not reported for that year and the accumulated wet days are carried forward to the year when the spell ends. The ETCCDI short name for this variable is "CWD".
- **Diurnal temperature range**
	- °C
	- Annual mean of the daily difference between minimum and maximum temperature. The ETCCDI short name for this variable is "DTR".
- Extremely wet day precipitation
	- mm
	- Total annually summed precipitation on days with more daily precipitation than the 99th daily precipitation percentile on wet days in the base period. Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "R99p".
- **Frost days**
	- day
	- Annual count of days when daily minimum temperature < 0°C. The ETCCDI short name for this variable is "FD".
- **Growing season length**
	- day
	- Annual (January 1st to December 31st in the northern hemisphere and July 1st to June 30th in the southern hemisphere) count of days between first period of at least 6 days with daily mean temperature above 5°C and first period after July 1st (northern hemisphere) or January 1st (southern hemisphere) of at least 6 days with daily mean temperature below 5°C. The ETCCDI short name for this variable is "GSL".
- **Heavy precipitation days**
	- day
	- Number of days per year with 10 mm or more precipitation. Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "R10mm".
- **Ice days**
	- day
	- Annual count of days when daily maximum temperature < 0°C. The ETCCDI short name for this variable is "ID".
- **Maximum 1-day precipitation**
	- mm
	- Maximum precipitation on a single day in period (year or month). Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "Rx1day".
- **Maximum 5-day precipitation**
	- mm
	- Maximum precipitation in five consecutive days in the given period (month or year). Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "Rx5day".
- **Maximum value of daily maximum temperature**
	- °C
	- Maximum of daily maximum temperature in period (year or month). The ETCCDI short name for this variable is "TXx".
- **Maximum value of daily minimum temperature**
	- °C
	- Maximum of daily minimum temperature in the period (year or month). The ETCCDI short name for this variable is "TNx".
- **Minimum value of daily maximum temperature**
	- °C
	- Minimum of daily maximum temperature in period (year or month). The ETCCDI short name for this variable is "TXn".
- **Minimum value of daily minimum temperature**
	- °C
	- Minimum of daily minimum temperature in the period (year or month). The ETCCDI short name for this variable is "TNn".
- **Number of wet days**
	- day
	- Number of days per year with 1 mm or more precipitation. Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "R1mm".
- **Simple daily intensity index**
	- mm/day
	- Total annually summed precipitation on wet days (days with >= 1mm), divided by total number of wet days. Precipitation is the deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "SDII".
- **Summer days**
	- day
	- Annual count of days when daily maximum temperature > 25°C. The ETCCDI short name for this variable is "SU".
- **Total wet day precipitation**
	- mm
	- Total annually summed precipitation on days with precipitation > 1mm. Precipitation is the deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "PRCPTOT".
- **Tropical nights**
	- day
	- Annual count of days when daily minimum temperature > 20°C. The ETCCDI short name for this variable is "TR".
- **Very heavy precipitation days**
	- day
	- Number of days per year with 20 mm or more precipitation. Precipitation is deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "R20mm".
- Very wet day precipitation
	- mm
	- Total annually summed precipitation on days with more daily precipitation than the 95th daily precipitation percentile on wet days in the base period. Precipitation is the deposition of water on the Earth's surface, either rain, snow, ice or hail. The ETCCDI short name for this variable is "R95p".
- **Warm days**
	- %
	- Percentage of days with maximum temperature above the corresponding calendar day 90th percentile of maximum temperature for a 5-day moving window in the base period. The ETCCDI short name for this variable is "TX90p".
- **Warm nights**
	- %
	- Percentage of days with minimum temperature above the corresponding calendar day 90th percentile of minimum temperature for a 5-day moving window in the base period. The ETCCDI short name for this variable is "TN90p".
- Warm spell duration index
	- day
	- Annual count of days with at least 6 consecutive days when daily maximum temperature is above the calendar day 90th percentile of maximum temperature centered on a 5-day sliding window during the base period. The ETCCDI short name for this variable is "WSDI".


#### HSI variables
- Heat index
	- °C
	- Heat index is a heat stress indicator used by the US National Oceanic and Atmospheric Administration (NOAA) National Weather Service for issuing heat warnings. It is calculated using multiple linear regression based on daily maximum temperature and relative humidity (calculated from daily mean specific humidity and surface pressure).
- Humidex
	- °C
	- Humidex is a heat stress indicator used by Canadian meteorological services. It is calculated as linear combination of daily maximum temperature and vapour pressure (calculated from daily mean specific humidity and surface pressure).
- Indoor universal thermal climate index
	- °C
	- The indoor universal thermal climate index is defined as the air temperature of a reference outdoor environment that would elicit in the human body the same physiological model’s response (sweat production, shivering, skin wettedness, skin blood flow and rectal, mean skin and face temperatures) as the actual environment. Here, a polynomial approximation based on near-surface air temperature, solar radiation, vapor pressure, and wind speed is used for calculating the universal thermal climate index. In the present dataset, the influence of solar radiation and wind speed is not considered, and the universal thermal climate index is calculated from near-surface air temperature and vapor pressure solely, thus representing indoor conditions.
- Wet-bulb temperature
	- °C
	- The wet-bulb temperature index is a heat stress indicator that indicates the human cooling capacity through sweating. It is calculated from the equivalent potential temperature based on daily maximum temperature and water vapour mixing ratio (calculated from daily mean specific humidity and surface pressure).
- Indoor wet-bulb globe temperature
	- °C
	- Indoor wet-bulb globe temperature is a heat stress indicator that is calculated as weighted mean of wet-bulb temperature, globe temperature, and daily maximum temperature. In the present dataset, the influence of solar radiation and wind speed is not considered and wet-bulb globe temperature is calculated as weighted mean of wet-bulb temperature and daily maximum temperature (neglecting globe temperature). It thus represents indoor conditions.

