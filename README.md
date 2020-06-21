# OSM GIS
This project utilizes open street maps (**OSM**) to build a geographic information system of different cities across the world. The GIS 
maps roads, buildings, geographical features, and any particular points of interest ie. restaurants, gas stations.
## Stack
Developed in C++ for front and backend. Utilized a wrapper EZGL library for graphics, built using the GTK library.
## How It Works
![](Demo%20Material/HowItWorks.gif)

## Notable Algorithms
### A*, Multi-destination A*, Multi-start A*
A* calculates the best route for driving (default route mode), Multi-Start/Destination A* is used for the uber pool feature. This feature allows the user to specify how far they are willing to walk to get picked up with a driver. 

The uber pool algorithm utilizes multi-destination A* to find all intersections within a range the user specifies (red) which multi-start A* finds all possible routes from those intersections to the final destination (blue). 

![](Demo%20Material/debug_walk_drive.PNG)

Joining the two routes together forms the best path with the walking portion highlighted in red and the driving route in blue.

![](Demo%20Material/uber_pool.PNG)

#### Performance of A* algorithms
The algorithms have been tested against thousands of scenarios for legality, performance (time complexity) and the optimality (how well is the calculated path compared to the known best path). The results for the test cases are below.

![](Demo%20Material/m3_results.PNG)

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
