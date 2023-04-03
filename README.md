# python-api-challenge

## WeatherPy

## VacationPy
In VacationPy, I added the Geoviews library in the initial importing. From there, I imported the city data from WeatherPy's output path, and then used Geoviews to create points from the data. In doing so, I defined the dimensions based on the specific titling of the Latitude and Longitude columns, and set the Humidity to adjust the points' size. Sean Seaforth helped walk me through configuring the plot.

I then created a new dataframe to house the city information for the cities that met the ideal weather condition criteria (a temperature between 21 and 27 C, wind speed less than 4.5 m/s and cloudiness of 0). This way, the original dataframe still exists if needed further on. This dataframe was then copied in another new dataframe called hotel_df. I then set it to only include the columns City, Country, Lat, Lng and Humidity, and entered a blank column for Hotel Name.

I then created an API request to Geoapify, to find the first hotel with 10,000 meters of the coordinates.

Finally, I created a final plot to show a map with points for each city, showing the hotel name and country when hovering over the point.
