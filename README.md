# Heat Island Explore Web

## Member
Hui Tian, Shimin Tu 

## Project Theme
Urban heat island effect is that cities are hotter than rural areas due to more concentrated human activities, which greatly impairs the lives and health of residents. Nowadays it is found that temperatures also vary widely across the city. Since green spaces can absorb the heat and decrease the effect of urban heat islands effectively, in the final project, we are going to model the relationship between green spaces and temperature, and investigate the positive impacts of converting vacant lots in cities to green spaces.

## Data
1. Urban Heat Island in Philadelphia:
Manage satellite imagery (lansat) data with ArcGIS or Use dataset from
https://www.phila.gov/2019-07-16-heat-vulnerability-index-highlights-city-hot-spots/ 
2. Tree map
PPR Tree Canopy - Datasets - OpenDataPhilly or
Green space data, collected by analysing satellite imagery with NDVI. 
3. Vacant lots data
https://phl.carto.com/api/v2/sql?q=SELECT+*+FROM+vacant_lot_cleanups&filename= vacant_lot_cleanups&format=geojson&skipfields=cartodb_id

## Method
- Build analysis units: neighborhoods or census tracts.
- Build a model to find a correlation between surface temperature and tree canopy and
shrub/ lawn cover.
- Use the model to predict the reduction effect on prospective vacant lands which have
potential to become green space.
- Create charts of positive effects at different conversion rates in an interactive map.

## Output
1. [code](https://github.com/ShiminTu/Heat-Island-Explorer-Web/blob/main/HeatIslandExplore.ipynb)
2. [explanatory documentation ](https://github.com/ShiminTu/Heat-Island-Explorer-Web/blob/main/Vacant_lands_Reduce_Heatisland_Effect.docx)
3. [interative web]()
