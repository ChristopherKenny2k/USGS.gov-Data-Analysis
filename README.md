# USGS.gov Earthquake Data Analysis

### Project Description

This project uses publicly available USGS.gov (United States Geological Survey) earthquake data. The USGS monitors and collectes data relating to seismic events around the globe. The main aim of this project is to analyse aspects of earthquakes/seismic events with a magnitude of more than 5.5 that have occured in the last 10 years. Through the use of python and the 'pandas' library, the data was analysed with the intention of identifying any interesting trends.

### Data Used

The python 'Requests' package was used to access the data through the USGS API. All seismic events with a magnitude of more than 5.5 (in the last 10 years) were collected through this request.

After loading this data, various operations were performed to reduce dimensionality and handle missing values. Irrelevant features were removed and other features were created.

By using the 'globe' package in python I was able to take the XY coordinate data for each seismic event and place them on a world map. The results of which show that almost all of the seismic events occur at the boundaries of tectonic plates.

Another features that I created was a 'magCat' features relating to the magnitude category of each seismic event. The Alaska Earthquake Center from the University of Alaska Fairbanks has a categorisation of earthquake levels using magnitude classes. The ranges for which are as follows. 
[Label : Magnitude]
- Minor: 3.0 - 3.9 (may be felt)
- Light: 4.0 - 4.9 (likely felt)
- Moderate: 5.0 - 5.9 (possible minor damage)
- Strong: 6.0 - 6.9 (possible moderate damage)
- Major: 7.0 - 7.9 (damage expected)
- Great: 8.0+ (significant damage expected)

### Some Intersting Findings

- Of the 4593 seismic events in my data, only 2 were not earthquakes. One was a nuclear explosion and the other was a volcanic eruption.
- 72.9% of onshore earthquakes occur at a depth of 0-70km
- 84.0% of offshore earthquakes occur at a depth of 0-70km.
- By generating a kernel density graph of the depths of onshore and offshore earthquakes we can see that a higher concentration of offshore earthquakes occur at shallower depths when compared to onshore earthquakes.
- A correlation coefficient of 0.106 indicated only a weak positive correlation exists between the depth of an earthquake and the magnitude of an earthquake.
