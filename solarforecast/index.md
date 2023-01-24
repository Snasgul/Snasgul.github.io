# Solarforecast
 
The goal is to make accurate solar energy production forecasts, by using cloud cover forecasts in 2D at the beginning. Creating a clear sky model and a cloud model is currently the best option.

The clear sky model considers the entry angle in the earths atmosphere (Airmass) and the entry angle to the solar cells, witch is calculated by knowing the exact position of the sun with the [astropy](https://github.com/astropy/astropy) package using location and time. For a proof of concept only a clear sky model will be implemented in its simplest form.
The clear sky model should also concider the occlusion of the sun by elavations of the surrounding terrain by using a height map.

The cloud model is much more complicated. The ideas range from machine learning to raytracing. Maybe a combination of both is the most accurate model. The inputs are: Airmass, Cloud thickness, albedo map, a reflection model. The model will not only use datapoints at the exact location, but also around the point. The further away the point, the less the weight is.
