# What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

![Equator](Images/equatorsign.png)


## Part I - WeatherPy

In this example, you'll be creating a Python script to visualise the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilising a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

Your first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot add a sentence or too explaining what the code is and analysing.

Your second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots explain what the linear regression is modelling such as any relationships you notice and any other analysis you may have.

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* Create a heat map that displays the humidity for every city from the part I of the homework.

  ![heatmap](Images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

### Copyright

© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.

## **Summary**:
## **Languages used**:
- Python

## **Python Packages Used**:
- Pandas
- Matplotlib
- citipy
- requests
- json
- numpy
- spicy
- random
- pprint
- gmaps
  
## **Conclusions**
- We can see from the analysis that as latitude approaches 0 (the equator), the temperature increases. With high correlation values for both southern and northen hemispheres, suggesting our conclusion may be true.
- We can also see that when latitude is 0, the humidty is higher than it is at other latitude values. With very weak correlation values for both northern and southern hemispheres, suggesting our conclusion may be false.
- From the analysis, wind speed appears to approach 0 as latitude approaches 0. With very weak correlation values for both northern and southern hemispheres, suggesting our conclusion may be false.

## **Screenshots**
## **Latitude Vs Temperature**
![Latitude Vs Temp](/WeatherPy/Lat_VS_Temp.png)

## **Latitude Vs Temperature (Southern Hemisphere)**
![Latitude Vs Temp (Southern)](/WeatherPy/Latitude_Vs_Temp(Southern).png)

## **Latitude Vs Temperature (Northern Hemisphere)**
![Lat Vs Temp](/WeatherPy/Latitude_Vs_Temp(Northen).png)

## **Latitude Vs Humidity**
![Latitude Vs Humidity](/WeatherPy/Latitude_Vs_Humidity.png)

## **Latitude Vs Windspeed**
![Latitude Vs WindSpeed](/WeatherPy/Latitude_Vs_WindSpeed.png)

## **Latitude Vs Cloudiness**
![Latitude Vs Cloudiness](/WeatherPy/Latitude_Vs_Cloudiness.png)

## **Running the jupyter notebooks**
1. Before running any of the jupyter notebooks please install needed packages running the following code in the terminal.
         
        pip install pandas
        pip install citipy
        pip install requests
        pip install json
        pip install matplotlib
        pip install numpy
        pip install pprint
        pip install spicy
        pip install gmaps

Or run this code in the first Jupyter Notebook

        ! pip install --user pandas
        ! pip install --user citipy
        ! pip install --user requests
        ! pip install --user json
        ! pip install --user matplotlib
        ! pip install --user numpy
        ! pip install --user spicy
        ! pip install --user pprint
        ! pip install --user gmaps
1. Sign up to [Open Weather API](https://openweathermap.org/api) and insert your API key in the *api_keys.py* .
   
2. Sign up to [Google Places API](https://developers.google.com/maps/documentation/places/web-service/overview) and insert your API key in the *api_keys.py*.
   
3. Run the file *WeatherPy.ipynb.ipynb* (This may take up to 10 min)

4. **Note: There is a bug in the gmaps module itself that causes the map to not load. A solution to this is to open a new jupter notebook and rerun the code.**

    Run the file *VacationPy.ipynb* 
