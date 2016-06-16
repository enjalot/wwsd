# Working with spatial data for the web

## Introduction
This workshop is designed to help you learn how to learn when it comes to
working with geospatial data. The workshop has been split into three acts,
each focusing on a different zoom level and geographic area. The idea is that
you develop the ability to work with geospatial data no matter where it covers
or what kind it is. To help you develop the confidence to tackle spatial data
from anywhere in the world we will repeat the following refrain throughout each
act:

**a) Inspect the data**  
We will go over how to orient ourselves and the data and how to read
GeoJSON/TopoJSON before we try to make the computer read it.  

**b) Get something on screen**  
After we know the basics about our data we can put it on the screen in the form
of a simple map. Depending on what we want to do with it we may choose different
tools as starting points. You will have a better sense of which tools and how to
choose them after completing all three acts.  

**c) Line things up**  
One of the major concepts in cartography is that of Layers. This concept can be
extended in various ways when making data-driven maps. We will practice several
different techniques for lining up data visualizations with geographic context.  

**d) Customize**  
The reason you are probably trying to learn this is so you can make rich,
powerful and custom visualizations. Each tool we will use has its own
possibilities (and constraints) when it comes to customization. You should have
a strong sense for whats possible and how to go deeper at the end of this
workshop.  

**e) Interaction**  
Each tool we will use can be used for designing interaction with our
maps and visualizations. We will take a look at the interaction capabilities and
explore some of the possibilities in each act.  

---

This workshop is designed to be very hands-on, with many examples that can be
extended as exercises. It would be impossible to touch everything that we could
find interesting in web mapping. The hope is that after going through these
three acts you will feel empowered to swap in your own data and add geo contexts
to your own data visualization projects!

An important thing to note about this workshop: It will not show you how to find
and process geospatial data. There is more and more open data coming online from
every level of government (and private organizations), learning how to search
for good, complete and relevant data is a challenge unto itself. This workshop
assumes you have data in GeoJSON format (if you have it in some other common  
format like SHP it is trivial to convert). You should have a better sense of how
to validate data you have found and make sure its the real deal before you get
too far into building your data visualization.

# Data
The data used in the following examples is all contained in this repository. The
datasets are designed to cover a variety of locations and scales (world-wide
down to city level) so that you don't feel confined to one geographic area
while practicing. Each data folder contains a README that describes where the
data comes from and how it was processed.

## [World data files](data/world)  
## [UK (London) data files](data/UK)  
## [USA (SF) data files](data/USA)

We will explore the three basic GeoJSON data types with these files:  
* Polygons - Administrative boundaries (e.g. countries, states and counties)
* Lines - Roads, Routes and Rivers
* Points - Cities, Subway stations


# Act I
_I've got the whole world, in my hands_

### Inspect the data
[World data files](data/world)  
View each data file in a text editor.  
Copy each data file into [geojson.io](http://geojson.io).  
[Inspect the TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf).  
Open the console. Poke around the loaded TopoJSON and GeoJSON data to see how its structured.
You can treat a FeatureCollection almost like any other array of objects you
visualize with d3.  
[Preview the TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63).  

### Leaflet
**Getting started**  
[Example #1]()


**Basic styling**  


**Basic interaction**  


Resources: leaflet docs

### d3.js
**SVG Paths**  

resources:
MDN

**Rendering a map with SVG**   

[Projections](http://bl.ocks.org/enjalot/bd552e711b8325c64729)

Resources:  
D3 docs: [d3.geo.path](https://github.com/d3/d3/wiki/Geo-Paths)  
Tutorial: [lets make a map](https://bost.ocks.org/mike/map/)  

**Mouse interactions with SVG**  


**Zooming with SVG**  
[Mike's examples](http://blockbuilder.org/search#text=zoom;user=mbostock;api=geo.path)
[State grid minimap](http://bl.ocks.org/enjalot/1919bd8c2f574caa17ba)

Resources:
example search


# Act II
_Fancy a cup of tea?_  

### Inspect the data
[UK (London) data files](data/UK)  
View each data file in a text editor.  
Copy each data file into [geojson.io](http://geojson.io).  
[Inspect the TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf)  
[Preview the TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63)  

### Mapbox-gl

**Getting started**  


**Basic styling**  


**Basic interaction**  

resources:
mapbox-gl docs
mapbox-gl examples
[fitBounds](https://www.mapbox.com/mapbox-gl-js/example/fitbounds/)


### d3.js
**Leaflet SVG Overlay**  

resources: d3 leaflet, dots on a map

**Mapbox-gl SVG Overlay**

resources: dots on a map


# Act III
_Hella data_  

### Inspect the data
[USA (SF) data files](data/USA)
View each data file in a text editor.  
Copy each data file into [geojson.io](http://geojson.io).  
[Inspect the TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf)  
[Preview the TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63)  

### d3.js

**Rendering with Canvas**  
CA counties

**Data lookups**  
[SF Precincts](http://blockbuilder.org/enjalot/f071fe9f332c62cb7bcad13ae5d645d8)

### turf.js
**Measuring**  
CA counties + CA rivers
**Intersections**  
CA counties + CA rivers
**Buffering**  
CA rivers

Resources:  
[TurfJS Docs](http://turfjs.org/docs/)  

# Encore
We may not have time to explore these examples in depth, but they should provide
inspiration and exercises for those who wish to venture deeper into the technical
possibilities of the tools covered in this workshop.

**It's a map, sort of**  
Using geospatial properties or locations to add context:  
[Circle counties](http://bl.ocks.org/mbostock/4206975)  
Try doing this with the [world populations](http://enjalot.github.io/wwsd/data/world/ne_50m_admin_0_countries.topojson)

**Advanced canvas interaction**   
[Selecting countries on a canvas globe](http://bl.ocks.org/syntagmatic/6645345)  

**Clipping**  
[Clipping geometry data](http://blockbuilder.org/mbostock/6301872)  
[Clipping raster tiles](http://bl.ocks.org/enjalot/985de8fcd65d37583949edbf280f2632)  

**Animated paths**  
[Timer & Mapbox-gl](http://bl.ocks.org/enjalot/4ff31e96860f38d4fd58)  
