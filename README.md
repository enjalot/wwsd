# Introduction
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

[World data files](data/world)  
[UK (London) data files](data/UK)  
[USA (SF) data files](data/USA)

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
Whats up with this [TopoJSON stuff]()

### Leaflet
Getting started  
[Start]()
[Finish]()

Basic styling  
[Start]()
[Finish]()

Basic interaction  
[Start]()
[Finish]()

Resources: leaflet docs

### d3.js
SVG Paths
[Start]()
[Finish]()

Rendering a map with SVG  
[Start]()
[Finish]()

Mouse interactions with SVG

Zooming with SVG


Resources:
d3 docs
example search


# Act II
_Fancy a cup of tea?_

### Inspect the data

### Mapbox-gl

Getting started  
[Start]()
[Finish]()

Basic styling  
[Start]()
[Finish]()

Basic interaction  
[Start]()
[Finish]()

resources:
mapbox-gl docs
mapbox-gl examples


### d3.js
Leaflet SVG Overlay  
[Start]()
[Finish]()

resources: d3 leaflet, dots on a map

Mapbox-gl SVG Overlay
[Start]()
[Finish]()
resources: dots on a map



# Act III
_Hella data_

### d3.js


Rendering with Canvas
CA counties

(advanced)
Clipping

Kai's color lookup for canvas interaction

Animated paths

# Encore
We may not have time to explore these examples in depth, but they should provide
inspiration and exercises for those who wish to venture deeper into the technical
possibilities of the tools covered in this workshop.
