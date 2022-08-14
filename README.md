# Python-API-Challenge
In this challenge, I was tasked with taking a look at how the weather changes as you get closer to the equator; as well as creating a heatmap that shows humidity levels of random locations around the world, and hotels in ten or less regions that match specific parameters for planning future vacations.

## Part I - WeatherPy
In [WeatherPy]('../WeatherPy.ipynb'), a Python script was created to visualize the weather of 600+ cities across the world of varying distances from the equator. To accomplish this, [citipy]('https://pypi.org/project/citipy/'), and the [OpenWeatherMap API]('https://openweathermap.org/api') were used to create a representative model of weather across the globe's cities.

Scatter plots were created to showcase the following relationships:
- [Temperature (F) vs. Latitude]('images/lat_vs_temp.png')
- [Humidity (%) vs. Latitude]('images/lat_vs_humid.jpg')
- [Cloudiness (%) vs. Latitude]('images/lat_vs_cloud.png')
- [Wind Speed (mph) vs. Latitude]('images/lat_vs_wind.png')

Then a linear regression analysis was done to determine each realationship, except this time they were separated into northern and southern hemispheres:
- [Northern Hemisphere - Temperature (F) vs. Latitude]('images/north_temp_regress.png')
- [Southern Hemisphere - Temperature (F) vs. Latitude]('images/south_temp_regress.png')
- [Northern Hemisphere - Humidity (%) vs. Latitude]('images/north_humid_regress.png')
- [Southern Hemisphere - Humidity (%) vs. Latitude]('images/south_humid_regress.png')
- [Northern Hemisphere - Cloudiness (%) vs. Latitude]('images/north_cloud_regress.png')
- [Southern Hemisphere - Cloudiness (%) vs. Latitude]('images/south_cloud_regress.png')
- [Northern Hemisphere - Wind Speed (mph) vs. Latitude]('images/north_wind_regress.png')
- [Southern Hemisphere - Wind Speed (mph) vs. Latitude]('images/south_wind_regress.png')

After each pair of plots there is a short explanation of what the linear regression is modeling, and any notable findings.


## Part II - VacationPy

In [VacationPy]('VacationPy.ipynb'), the weather data from part I was used to plan future vacation using gmaps and the Google Places API.

- A heat map displaying humidity for every city from part I was created
![humidity heatmap]('images/humidity_heatmap.png')

- The DataFrames scope was narrowed down to only include ideal weather conditions

- Google Places API was used to find the first hotel for each city located within 5000 meters of the given coordinates.

- The hotels were then plotted on top of the humidity heatmap; each pin contains the hotel name, city, and country.
![hotel_and_humidity_heatmap]('images/hotel_and_humidity_heatmap.png')
