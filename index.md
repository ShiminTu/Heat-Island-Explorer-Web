---
layout: default
altair-loader:
  altair-chart-1: "charts/measlesAltair.json"
hv-loader:
  hv-chart-1: ["charts/conversion_map.html", "500"] 
  hv-chart-2: ["charts/social_conditions.html", "700"] # second argument is the desired height
  hv-chart-3: ["charts/interact_dashboard.html", "700"] # second argument is the desired height
---

# Introduction!

【This single-page website demos how to display visualizations created with altair, hvplot, and folium.

For examples of how to use markdown to style text, see this [this page](./another-page.html).

## Land Surface Temperature and Land Cover

Below is a comparison chart of land surface temperature and land cover.

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/img/log.jpg

[explaination]. 

## Convert vacant lands to tree canopy

We can convert roads, bare earth and other paved areas to canopy. 

<div id="hv-chart-1"></div>

[explaination]. 

Land surface temperature maybe also correlated to socieconomic conditions of census tracts, which introduces a problem about **Environmental justice**.

## Social conditions in Philadelphia

Land surface temperature maybe also correlated to socieconomic conditions of census tracts, which introduces a problem about **Environmental justice**.

<div id="hv-chart-2"></div>

[explaination]. 

<br/>

## Relationship between social conditions and land cover.

Below is a scatter plot of ...

<div id="hv-chart-3"></div>


# conclusion
