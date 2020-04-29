# TSPPD-Mapper
This project utilizes open street maps (**OSM**) to build a geographic information system of different cities across the world. The GIS 
maps roads, buildings, geographical features, and any particular points of interest ie. restaurants, gas stations.
## Stack
Developed in C++ for front and backend. Utilized EZGL library for graphics.
## Notable Algorithms
R Trees were utilized to spatially organize geographical data to improve responsiveness and reduce FPS lag. Utilizing R Trees enables specific filtering of data to only display and access points that belong on the user's visible screen. The improvements range from 100x to 1000x faster depending on how zoomed in the map is, with a higher zoom yielding a larger filter resulting more noticable improvement. 

The GIF on the left illusrates the GIS **before** the R Tree implementation and on the right is **After** 
 <img src="Demo%20Material/NoRtreeGif.gif" width="425"/>  <img src="Demo%20Material/RTreeGif.gif" width="425"/>

## Additional Features
1) Dark Mode
2) Building Toggles
3) Full mouse control
4) Scalable code to display any city 
5) Search menu for intersections
6) Route calculations for the fastest path to destination
7) Route instructions
## Dark Mode
![](Demo%20Material/mapper_toronto_darkmode.PNG)
## Building Toggle
![](Demo%20Material/mapper_toronto_darkmode_buildingstoggle.PNG)
## Cities
Any city can be loaded provided the osm.bin file is installed
### Toronto, Canada
![](Demo%20Material/mapper_toronto.PNG)
### London, England
![](Demo%20Material/mapper_london.PNG)
### New York, USA
![](Demo%20Material/mapper_NY.PNG)
