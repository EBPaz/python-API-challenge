# Project Title
Python API Challenge
Data Visualization Class, June 2023


## About
This project has two components, assessing weather types by latitude in WeatherPy and finding locations in the world that have great weather for vacations in VacationPy.

WeatherPy looks for correlations between weather data and latitude by utilizing a specific point in time. Weather data inclduing; maximum temperature, humidity, cloudiness and wind speed was collected at random from different latitudes via the Open Weather API. That data was then placed into a Dataframe with its corresponding city location. Scatter plots were created comparing latitude to each weather type. This data was then broken down further into weather type by hemisphere. Regression lines and r-values were computed for each plot by hemisphere and conclusions were made. 

VacationPy utilizes the weather dataframe we collected in WeatherPy. Uitlizing the geoviews application, cities were mapped with plot sizes increasing in relation to increasing humidity. That dataframe was then filtered to obtain ideal weather conditions and a new dataframe was created for cities with max temperatures between 65 to 75 degrees Fahrenheit as well as 55% to 60% humidity. The ideal weather data was run through the Geoapify API to obtain hotel names within 10,000 meters for each location. That data was also plotted on a world map using geoviews to indicate hotels to stay on vacation with great weather. 


## Getting Started / Installation
To be able to obtain, manipulate and run this data, you need to install the following applications.

WeatherPy:
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import requests
import time
from scipy.stats import linregress

from citipy import citipy
to find cities based on latitude and longitude

Import your OpenWeatherMap API key
from api_keys import weather_api_key
You must go to https://home.openweathermap.org/users/sign_up to sign up for an API key to gather data.


VacationPy:
import hvplot.pandas
import pandas as pd
import requests

Import your Geoapify API key
from api_keys import geoapify_key
You must go to https://www.geoapify.com/ to sign up for an API key to gather data. 


## Acknowledgments
https://stackoverflow.com/questions/34962104/how-can-i-use-the-apply-function-for-a-single-column
.apply function to change the Max Temp to Fahrenheit from Kelvin

linear regression equation taken from this example:
https://github.com/poonam-ux/Python_API_WeatherPy_VacationPy/blob/main/WeatherPy/WeatherPy.ipynb

https://www.geeksforgeeks.org/python-pandas-dataframe-copy-function/
to find the pandas copy function
