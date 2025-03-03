# NICAR-spatial-analysis
Hands on materials for 2025 Spatial analysis using geographical Census data class

## Software requirements
- Python 3
- Jupyter notebook
- pandas
- geopandas
- matplotlib

Sample pip installation:
```
pip install notebook pandas geopandas matplotlib
```

## Example spatial analyses

These are not the exercises we are completing today, but are some examples of real-world analyses that these and similar techniques can be used for.

### Drug overdose mapping

#### [Pandemic, homelessness brought record overdose calls in Minneapolis](https://www2.startribune.com/pandemic-homelessness-brought-record-overdose-calls-in-minneapolis/600094050/)  
*Minnesota Star Tribune, 2021*

[<img style="width: 300px;" alt="A screenshot of a map with colored hex bins showing the count of suspected drug overdoses." src="/images/strib-overdose-map.png">](https://www2.startribune.com/pandemic-homelessness-brought-record-overdose-calls-in-minneapolis/600094050/)

Sometimes, traditional boundaries like neighborhoods may be too coarse or not comparable enough to each other for the story you are trying to tell.

This analysis took geocoded EMS calls related to suspected drug overdoses and placed each into hexagonal bins generated to show spatial clusters that were more localized than whole neighborhoods.

The hex bins were generated using QGIS's "Create Grid Layer" function and exported as a shapefile. The rest of the analysis was done with geopandas.


## Alternate sources for Census geographic data

### Census Reporter

"[Census Reporter](https://censusreporter.org/) is an independent project to make it easier for journalists to write stories using information from the U.S. Census bureau. Place profiles and comparison pages provide a friendly interface for navigating data, including visualizations for a more useful first look."

### IPUMS/NHGIS

"[IPUMS USA](https://usa.ipums.org/usa/) collects, preserves and harmonizes U.S. census microdata and provides easy access to this data with enhanced documentation. Data includes decennial censuses from 1790 to 2010 and American Community Surveys (ACS) from 2000 to the present."

International data also available, though it varies considerably by country.

"The [National Historical Geographic Information System](https://www.nhgis.org/) (NHGIS) provides easy access to summary tables and time series of population, housing, agriculture, and economic data, along with GIS-compatible mapping files, for years from 1790 through the present and for all levels of U.S. census geography, including states, counties, tracts, and blocks."

The amount of historical data available from the NHGIS project, based at the University of Minnesota, is truly staggering. However, using NHGIS data requires more attention to what variables and geographies have changed over time.