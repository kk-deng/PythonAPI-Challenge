# World Weather Analysis - An API Application
A python project was built to analyze the weather of 500+ cities in the world of varying distance from the equator.

## Background

This script generates data of 500+ cities with following info:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

And linear regression was applied for the above info in Northern and Southern Hemispheres.

*Analyzed cities on the world map:*
<img src="https://github.com/kk-deng/PythonAPI-Challenge/blob/main/Images/worldmap.png?raw=true" border="0">

## Observations and Insights

1. From the graph of max temp and latitude, we can see that there is a strong relationship (r = -0.87271) between northern hemisphere latitude and max temp. The max temp will likely decrease 1 F degree per degree latitude in the northern hemisphere.

<img src="https://github.com/kk-deng/PythonAPI-Challenge/blob/main/Images/Linear_1.png?raw=true" border="0">


2. From the cloudiness graph, there is no significant correlation between cloudiness and latitude. Most cities have either higher (close to 100%) cloud covered or lower (close to 0%).

3. There is no strong relationship between wind speed and latitude too. Most cities have a wind speed lower than 20 mph all over the world.

4. We can see the most cities have higher humidity as shown below. This script got the random latitudes and longtitudes between (-90 to 90) and (-180 to 180). However, the **main defect** of this theoretical assumption is that **most area on the earth is covered by ocean where has much fewer cities than the continents**. ``citipy`` only get the closest city of the random coordinates. When it comes to the ocean coordinates, all cities along the coastline would be collected into the dataframe. Those cities are highly humid **due to the ocean currents**, resulting in the relatively higher humidity scatter points in this dataset.
<img src="https://github.com/kk-deng/PythonAPI-Challenge/blob/main/Images/Fig_2.png?raw=true" border="0">

**A world map of all analyzed cities** is shown in the notebook and readme file to prove this analysis. 

5. A correlation matrix was generated. Most columns have not strong relationship with each other. However, the Max temp shows a correlated relationship with Latitude (r = -0.67468).
