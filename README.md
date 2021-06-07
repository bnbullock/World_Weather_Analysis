# Planning My Trip with Google Maps

## Project Overview

To design a "PlanMyTrip" application that allows users to filter destinations based on temperature preferences. Once a temperature range has been selected by a client, this is used to identify potential destinations of travel and nearby accomodation choices. From the destination list, the client will choose a city to travel to along with a four-city travel itinerary. With the use of different Application Programming Interfaces(APIs), a marker map showing the four cities will be created along with a travel route map showing three different methods of transportation  - driving(yellow), bicycling(green) and walking(blue). Each transportation method is colour coded, as above, for ease of view on the itinerary map.

- Deliverables:
  1. Connect using OpenWeatherMap, retrieve weather data and export the results in a CSV file.
  2. Create a client travel map with various destinations and nearby hotels using Google Maps. 
  3. Create a four-city travel itinerary and associated marker map with Google Maps.

## Resources
- Current Weather Data: Open Weather API
- Google Maps REST APIs: Places API, Directions API, Javascript API
- Data files created from above APIs: WeatherPy_Database.csv, WeatherPy_vacation.csv
- Software: Python 3.7.10, Visual Studio Code 1.56.2, Jupyter Notebook Server 6.3.0

## Results

### Analyze database of Cities and Retrieve Weather Details

Current weather data is extracted using the Openweather API and attached to a number of cities in our database. The information is formatted correctly and saved as shown in the dataframe below.

![City Destinations](Weather_Database/City_Destinations.png)


### Provide Suitable Destination Choices

 The client is able to enter 2 values into a input request that allows a minimum and maximum temperature range to be determined. The system then goes out and searches all destinations currently in the database that have a current acceptable temperature that suits the client's needs. The following is a sample list of destinations with a minimum value of 55 degrees and a maximum of 85 degrees F.

![Hotel Destinations](Vacation_Search/Hotel_Destinations.png)

The total destination cities are then presented on a map and displayed for the client to review. Using the customary Google Maps interface the client is able to narrow down the travel destination and also determine which cities they would like to be part of their four city travel itinerary.

![Gmap Hotels](Vacation_Search/WeatherPy_vacation_map.png)


### Prepare Itinerary and Map results

Once the client has chosen a specific destination, they are then able to enter their itinerary choices into the application. The information is entered into input request windows with starting location, 1st city, 2nd city, 3rd city that the client would like to visit locally as part of their itinerary. The following is an example of the dataframe produced and the resultant google map produced by the software. In this particular example we have prepared a destination of Northan, England along with Horsham, Great Yarmouth and Rottingdean as the four city itinerary for travelling. Once the user enters the ciites a dataframe is produces specifically for their choices and the route map also prepared as shown below.
 
![Four Cities](Vacation_Itinerary/four_city_dataframe.png)

The travel paths information depicted have specific colours for a different transportation methods that the client might want to use. Driving is in yellow, the bicycling routes are shown in green and the walking paths are shown in blue.

![Travelling England](Vacation_Itinerary/WeatherPy_travel_map.png)

Below, we have also produced an individual map with simple markers for the client to review with individual markes assigned to each city stop along the four city itinerary as chosen by the client.

![England Markers](Vacation_Itinerary/WeatherPy_travel_map_markers.png)

## Overall Summary

In summary we are able to provide the client with real-time information to make a very informed decision. Also, the code is repeatable and provides the user with many different itinerary choices for temperature and ciites to visit. Both of these values are entered by the client and the application can present the results in a manner that allows the client to choose a suitable destination of travel.