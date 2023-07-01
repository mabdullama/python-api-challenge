# python-api-challenge

# Part 1: Weather Analysis

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


# Part 2: Hotel Finder

This repository contains a Python script for finding hotels near cities based on specific weather conditions. The script utilizes the Geoapify API to search for hotels within a certain radius of latitude and longitude coordinates.

## Dependencies and Setup

The following dependencies are required to run the script:

- hvplot
- pandas
- requests

## Load the Data

The script loads a CSV file created in a previous step (Part 1) called "cities.csv". The CSV file contains weather data for various cities.

## Step 1: Create a Map

The script creates a map that displays a point for every city in the DataFrame. The size of the point represents the humidity level of each city. The map is generated using the `hvplot` library and visualized using the OSM (OpenStreetMap) tiles.

## Step 2: Narrow Down the Data

The script narrows down the DataFrame to find cities that meet specific weather conditions. It filters cities based on maximum temperature, cloudiness, and wind speed criteria. Null values are dropped from the narrowed DataFrame.

## Step 3: Create a New DataFrame for Hotels

A new DataFrame called `hotel_df` is created to store information about the hotels. It includes columns for city, country, coordinates, humidity, and hotel name. The "Hotel Name" column is initially empty.

## Step 4: Find Hotels Using the Geoapify API

For each city in the `hotel_df` DataFrame, the script uses the Geoapify API to find the first hotel located within 10,000 meters of the city's coordinates. The API request includes parameters such as limit, radius, and API key. The hotel name is stored in the "Hotel Name" column of the `hotel_df` DataFrame.







