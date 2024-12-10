### Code
1. Processing to make sure the data are matching the VIEWS country-month or country-year format
  + Confusion: What is the VIEWS country-month/country-year format? // VIEWS documentation, download exemplary data, try out’
  + Focus (P): country code convention // Mihai’s ingested manual: https://github.com/UppsalaConflictDataProgram/ingester3_loaders/blob/gadm_pg/Ingester3_documentation.ipynb.
  + Advice (P): Use viewser functions to process the data (checking for duplicates, converting country identifiers)
2. Ingestion
  + Actual ingestion does not need to be included, maybe play around with it



## Done

### GitHub
+ Set up the GitHub repository in a standard way

### Check variables to include
+ Check Garret's pgm variables against the ones available at the country-level on
+ Garret's variables:
  + main.py, rows 47 - 54: https://github.com/prio-data/climate_extremes/blob/main/main.py
  + All indicators at the pg-level: https://cds.climate.copernicus.eu/datasets/sis-extreme-indices-cmip6?tab=overview

### Code
1. API request to download the data
