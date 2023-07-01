# python-api-challenge

# Weather Analysis

This repository contains a Python script for analyzing weather data using the OpenWeatherMap API. The script retrieves weather data for a list of randomly generated cities and performs various analyses and visualizations.

## Dependencies and Setup

The following dependencies are required to run the script:

- matplotlib
- pandas
- numpy
- requests
- time
- datetime
- scipy


## Generate the Cities List

The script uses the `citipy` library to generate a list of cities based on randomly generated latitude and longitude coordinates. The latitude and longitude ranges are specified, and the script identifies the nearest city for each coordinate pair.

## Retrieve Weather Data

The script utilizes the OpenWeatherMap API to retrieve weather data for the generated cities. It makes API requests for each city and extracts relevant weather information such as temperature, humidity, cloudiness, wind speed, and country. The retrieved data is stored in a pandas DataFrame for further analysis.

## Create Plots to Showcase the Relationship Between Weather Variables and Latitude

The script creates scatter plots to visualize the relationship between weather variables and latitude. It includes the following plots:

- Latitude vs. Temperature
- Latitude vs. Humidity
- Latitude vs. Cloudiness
- Latitude vs. Wind Speed

The plots are generated using matplotlib and saved as PNG images in the `output_data` directory.

## Compute Linear Regression for Each Relationship

The script performs linear regression analysis on the relationships between weather variables and latitude. It calculates the regression line and displays the equation along with the R-value on the plots.

## Conclusion

This script provides a comprehensive analysis of weather data by retrieving, analyzing, and visualizing the relationship between weather variables and latitude. The generated plots and regression analysis can help in understanding the impact of latitude on various weather factors.



