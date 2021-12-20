---
layout: default
hv-loader:
  hv-chart-1: ["charts/conversion_map.html", "500"] 
  hv-chart-2: ["charts/social_conditions.html", "600"] # second argument is the desired height
  hv-chart-3: ["charts/interact_dashboard.html", "500"] # second argument is the desired height
---

## What is heat island ?

Heat islands are urbanized areas that experience higher temperatures than outlying areas. It usually occurs when natural land cover is replaced with dense concentrations of pavement, buildings, and other surfaces that absorb and retain heat. Urban heat island effect increases energy costs, air pollution levels, and heat-related illness and mortality. It is a challenging urban problem not only impact sustainability and human health, but also reflects social, racial, and economic inequalities associated with disproportionate green spaces in cities.

Multiple studies of urban heat island indicate green space can mitigate urban heat island effect by creating cooling buffer zones, but little research conducted a quantitative analysis of the mitigating effect of converting vacant lands to green spaces. Thus, we examined the potential of converting paved areas and bare earth in vacant lands to green space and predict the mitigation effect with machine learning technology in this study. We also talked about the relationship between heat islands and socioeconomic conditions.

## Land Surface Temperature and Land Cover

We calcultaed land surface temperature of Philadelphia on August 26th in this year from Landsat Satellite Image, also imported the land cover data of philadelphia. AS maps below show,....

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/LST.png)

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/LC.png)

Census tracts whose temperature is higher than 26 degree centigrade are recognized as heat islands. Roads, bared earth and other paved surfaces of vacant lands in heat islands will be converted to tree canopy to see whether it can lead to a great difference. 

The census tracts with read boarder in the map are heat islands, have a look to check whether you live in a heat island!

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/HI.png)

## Convert vacant lands to tree canopy

We did a Random Forest regression to explore the relationship between surface temperature and **land cover**. Based on the model, we convert roads, bare earth and other paved surfaces of vacant lands in heat islands to tree canopy with a specific conversion rate. You can see the change of temperature distribution by choosing 0%, 50% or 100% three level of conversion rate.

<div id="hv-chart-1"></div>

Found nothing changed? Yes, in this project, even though we convert all vacant roads, bare earth and othering paved surfaces in heat islands, the land surface temperature of heat island won't have a visible decrease. In a conclusion, it's useless to only change the land cover type in vacant lands. In the urban planning, some of paved surfaces which have a function now should be converted to green space.

## Socioeconomic conditions of census tracts in Philadelphia

Land surface temperature maybe also correlated to socieconomic conditions of census tracts, which introduces a problem about **Environmental justice**. Below are multiple maps of Socioeconomic conditions of census tracts. Those tracts with abnormal values are removed.

<div id="hv-chart-2"></div>

[explaination]. 

<br/>

## Relationship between socioeconomic conditions and land cover.

Below is a scatter plot of between social conditions and land cover. You can change varibales of x-axis and y-axis, and explore the relationship between them. The color represents value of land surface temperature. The deeper the color, the higher the temperature.

<div id="hv-chart-3"></div>


## Results
