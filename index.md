---
layout: default
hv-loader:
  hv-chart-1: ["charts/conversion_map.html", "500"] 
  hv-chart-2: ["charts/social_conditions.html", "600"] # second argument is the desired height
  hv-chart-3: ["charts/interact_dashboard.html", "500"] # second argument is the desired height
---

## What is heat island?

Heat islands are urbanized areas that experience higher temperatures than outlying areas. It usually occurs when natural land cover is replaced with dense concentrations of pavement, buildings, and other surfaces that absorb and retain heat. Urban heat island effect increases energy costs, air pollution levels, and heat-related illness and mortality. It is a challenging urban problem not only impact sustainability and human health, but also reflects social, racial, and economic inequalities associated with disproportionate green spaces in cities.

Multiple studies of urban heat island indicate green space can mitigate urban heat island effect by creating cooling buffer zones, but little research conducted a quantitative analysis of the mitigating effect of converting vacant lands to green spaces. Thus, we examined the potential of converting paved areas and bare earth in vacant lands to green space and predict the mitigation effect with machine learning technology in this study. We also talked about the relationship between heat islands and socioeconomic conditions.

## How land cover make a difference?

### Land Surface Temperature VS. Land cover

We calcultaed land surface temperature of Philadelphia on August 26th in this year from Landsat Satellite Image, also imported the land cover data of philadelphia. The map of LST on the top shows the land surface temperature of Philadelphia, with range between 11°C and 35°C. The map on the bottom present land cover types across the city, with most tree canopies clustered in Pennypack Park, Wissahickon Valley Park, and Fairmount Park. Most land cover of other paved surfaces are industrial zones in the South Philadelphia West. 

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/LST.png)

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/LC.png)

### Heat Islands in Philadelphia

Census tracts whose temperature is higher than 26 degree centigrade are recognized as heat islands. Roads, bared earth and other paved surfaces of vacant lands in heat islands will be converted to tree canopy to see whether it can lead to a great difference. 

The census tracts with red boarder in the map are heat islands, under the context of land cover map, we found that urban heat islands always appear in areas with high density of buildings and low coverage of tree canopies. Also have a look to check whether you live in a heat island!

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/HI.png)

### Convert vacant lands to tree canopy

We did a Random Forest regression to explore the relationship between surface temperature and **land cover**. Based on the model, we convert roads, bare earth and other paved surfaces of vacant lands in heat islands to tree canopy with a specific conversion rate. You can see the change of temperature distribution by choosing 0%, 50% or 100% three level of conversion rate.

<div id="hv-chart-1"></div>

Found nothing changed? We have to admit color gradient change is invisible in this map. One possible reason is local mitigation might only be reduction of 1-2°C in the vacant land. In a large scale of city map, especially responding to the mean temperature of a tract, the minor change of surface temperature is hard to identify. To improve the visualization outcome, we will zoom in some typical vacant lands and visualized the change of temperature in a local scale. At the same time, we will provide quantitative change of data in text to correspond to the visualized data.

## Do rich and white people live in cooler places?

### Socioeconomic conditions of census tracts

Land surface temperature maybe also correlated to socieconomic conditions of census tracts, which introduces a problem about **Environmental justice**. Below are multiple maps of Socioeconomic conditions of census tracts. Those tracts with abnormal values are removed.

<div id="hv-chart-2"></div>

It seems that the sptial distribution type of proportion of white and median household income are similar, as well as spatial distribution type of percent of vacant house and percent of people under poverty are similar. The latter two are also similar to the median temperature distribution type. It shows that in the census tracts where have higher proportion of vacant house and higher percent of poverty people are cooler. The results are not consistent with our cognition and the conclusions of many literature researches. However, that's what happened in Philadelphia.

### Relationship between socioeconomic conditions and land cover.

Below is a scatter plot of between social conditions and land cover. You can change varibales of x-axis and y-axis, and explore the relationship between them. The color represents value of land surface temperature. The deeper the color, the higher the temperature. There is no apparent relationship between landcover types and socioeconomic conditions.

<div id="hv-chart-3"></div>


## Conclusion

By analyzing the satellite image, we found heat islands in Philadelphia. We also tried to convert vacant roads, bare earth and other paved surfaces to green space, in order to tackle the problem of Heat Island Effect problem. Due to the limitation of data, we didn’t find a relationship between land cover and land surface temperature in regression model, only find some positive correlation between land surface temperature and median household income with building as an important feature. In urban area, rich people may prefer to live in high rise apartment other than low density building areas., which explained why landcover has certain correlation with median household income. In the further research, we are going to expand our research object to other cities to make our study more comprehensive and the results more significant. In addition, to improve the model between land cover and median surface temperature, we will consider using mean temperature of each type of land cover as dependent variable to respond to variable of different types of land cover with other types of models.
