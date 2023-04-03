# python-api-challenge

## WeatherPy
Once the list of cities was generated, I updated the code to parse the required weather information, after converting the API call results into a JSON. This was then appended into a list to track the city data, and was then converted into a dataframe. It was then exported into a CSV and read back in. A few scatter plots were created to show relationships between latitude and different weather variables.

Before computing linear regression for other relationships, I defined a function to create linear regression plots, based on variables x and y. This would shorten the code input for each required plot to fewer lines. As the plot labels were more unique to each plot, those were added in manually for each plot. Before creating those plots, I split the dataframe into 2 separate dataframes, Northern Hemisphere and Southern Hemisphere. Each plot was then calculated based on the data from the relevant hemisphere's dataframe.

## VacationPy
In VacationPy, I started by importing the city data from WeatherPy's output path. Sean Seaforth helped walk me through configuring the plot. 

I then created a new dataframe to house the city information for the cities that met the ideal weather condition criteria (a temperature between 21 and 27 C, wind speed less than 4.5 m/s and cloudiness of 0). This way, the original dataframe still exists if needed further on. This dataframe was then copied in another new dataframe called hotel_df. I then set it to only include the columns City, Country, Lat, Lng and Humidity, and entered a blank column for Hotel Name.

I then created an API request to Geoapify, to find the first hotel with 10,000 meters of the coordinates. Finally, I created a plot to show a map with points for each city, showing the hotel name and country when hovering over the point, still having the points change size based on humidity.
