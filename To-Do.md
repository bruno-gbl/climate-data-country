## Final points
2. Country IDs
  + Coordinate with Jim for a qualified decision on how to deal with lack of data on older geographic entities, like pre 2011 Sudan.
2. Ommitted territories
  + Figure out, whether there is a way to not omit the data from the smaller autonomous regions etc. that do not exist in VIEWS, like Åland, Antigua etc.
  + Arguably most relevant case: Is Greenland coded as part of Denmark in VIEWS?
3. Ingestion
  + Propose code for ingestion.
4. Decision on variables
  + Coordinate with Paola which variables should be adopted and which should be ommitted.
4. Hand-In
  + Transfer code to Jim.


## Done

### GitHub
+ Set up the GitHub repository in a standard way

### Check variables to include
+ Check Garret's pgm variables against the ones available at the country-level on
+ Garret's variables:
  + main.py, rows 47 - 54: https://github.com/prio-data/climate_extremes/blob/main/main.py
  + All indicators at the pg-level: https://cds.climate.copernicus.eu/datasets/sis-extreme-indices-cmip6?tab=overview

### Code
+ API request to download the data
+ Tranform individual JSON files into one unitary dataframe
+ Insert month_id column
+ Prepare decision on c_id column.
