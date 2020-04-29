# TSPPD-Mapper
This project utilizes open street maps (**OSM**) to build a geographic information system of different cities across the world. The GIS 
maps roads, buildings, geographical features, and any particular points of interest ie. restaurants, gas stations.
## How It Works
![](Demo%20Material/HowItWorks.gif)
## Stack
Developed in C++ for front and backend. Utilized EZGL library for graphics.
## Notable Algorithms
### R Trees
R Trees were utilized to spatially organize geographical data to improve responsiveness and reduce FPS lag. Utilizing R Trees enables specific filtering of data to only display and access points that belong on the user's visible screen. 

The GIF on the left illusrates the GIS **before** the R Tree implementation and on the right is **After** 
 <img src="Demo%20Material/NoRtreeGif.gif" width="425"/>  <img src="Demo%20Material/RTreeGif.gif" width="425"/>
 
The improvements range from 100x to 10000x faster depending on how zoomed in the map is, with a higher zoom yielding a larger filter resulting more noticable improvement. 
![](Demo%20Material/RTreeGraph.PNG)

## Additional Features
1) Uber Pool Mode
2) Dark Mode
3) Building Toggles
4) Full mouse control
5) Scalable code to display any city 
6) Search menu for intersections
## Uber Pool Mode
The user can specify how far/long they are willing to walk and the GIS will find the most optimal destination for pickup.
![](Demo%20Material/mapper_walk_drive_route.PNG)
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
