# Working with spatial data for the web

![Working with spatial data](img/header.png)

## Introduction
This workshop is designed to help you learn how to learn when it comes to
working with geospatial data. The workshop has been split into three acts,
each focusing on a different zoom level, geographic area and technical tool.
The idea is that you develop the ability to work with geospatial data no matter where it covers
or what kind it is. To help you develop the confidence to visualize spatial data
from anywhere in the world we will repeat the following refrain throughout each
act:

**a) Inspect the data**  
We will go over how to orient ourselves and the data and how to read
GeoJSON/TopoJSON before we try to make the computer read it.  

**b) Get something on the screen**  
After we know the basics about our data we can put it on the screen in the form
of a simple map. Depending on what we want to do with it we may choose different
tools as starting points. You will have a better sense of which tools and how to
choose them after completing all three acts.  

---

This workshop is designed to be very hands-on, with many examples that can be
extended as exercises. It would be impossible to touch everything that we could
find [interesting in web mapping](https://hi.stamen.com/an-ode-to-d3-js-projections-9d6477d6da0b#.1hr10rltk).
The hope is that after going through these
three acts you will feel empowered to swap in your own data and add geo contexts
to your own data visualization projects!

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

I recommend reading [More than you ever wanted to know about GeoJSON](http://www.macwright.org/2015/03/23/geojson-second-bite.html)
before the workshop, we will cover the same stuff but its a concise overview and a great reference.

# Act I
_I've got the whole world, in my hands_

### Inspect the data: [World data files](data/world)  
* View each data file in a text editor.  
* Copy each data file into [geojson.io](http://geojson.io)  
* [Inspect the TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf).  
* Open the console. Poke around the loaded GeoJSON data to see how its structured. You can treat a FeatureCollection almost like any other array of objects you
visualize with d3.  
*  [Preview the TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63).  

### Leaflet
**Getting started**  
[<img src="https://gist.github.com/enjalot/208dd99b6ed6a424513524d963880700/raw/c026672c7dc702708f1d5a5ef5097da2e336dc20/thumbnail.png">](https://github.com/enjalot/wwsd/issues/1)

**Basic styling & interaction**  
[<img src="https://gist.githubusercontent.com/enjalot/0c8028933d402fb4823a5b0067b12a56/raw/2f8a6bb6ffd901059f95565f74175237a25d70fe/thumbnail.png">](https://github.com/enjalot/wwsd/issues/2)

### d3.js
**SVG Paths**  
[<img src="https://gist.githubusercontent.com/enjalot/6c13610b33ed9d3f5b052fa3fc20ba56/raw/95497d048c07a95148b0d629d9dd34362a10c48c/thumbnail.png">](https://github.com/enjalot/wwsd/issues/3)

**Rendering a map with d3 + GeoJSON + SVG**   
[<img src="https://gist.githubusercontent.com/enjalot/c069550b4fc4fb409430829f07bd78f2/raw/74dce341847482d9dfd387b2aa6127eab539c3ba/thumbnail.png">](https://github.com/enjalot/wwsd/issues/4)

**Rendering a map with d3 + TopoJSON + SVG**   
[<img src="https://gist.githubusercontent.com/enjalot/4a449bee40e7b74108de89e303a2a284/raw/09d140a991f7cbbe507b6d01086c2c6a3c79a90d/thumbnail.png">](https://github.com/enjalot/wwsd/issues/5)

**Mouse interactions with d3 + SVG**  
[<img src="https://gist.github.com/enjalot/b37e8dac613d0a39c5b4c2f0e13e1277/raw/c82cb9e878a20d632ce54700203dfb9070b12998/thumbnail.png">](https://github.com/enjalot/wwsd/issues/6)

**Zooming with d3**  
[<img src="https://gist.githubusercontent.com/mbostock/4987520/raw/2eb118ef3ac0869552c6ce5cb77c625c6558e5cb/thumbnail.png">](https://github.com/enjalot/wwsd/issues/7)


# Act II
_Fancy a cup of tea?_  

### Inspect the data
[UK (London) data files](data/UK)  
View each data file in a text editor.  
Copy each data file into [geojson.io](http://geojson.io)  
[Inspect the TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf)  
[Preview the TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63)  

### Mapbox-gl

**Getting started**  
[<img src="https://gist.github.com/enjalot/b81e02d752855d106f88a9c0e42e65a0/raw/f897bad8e804af7428c1d4419daca4f13e1cd2d3/thumbnail.png">](https://github.com/enjalot/wwsd/issues/8)


**Basic styling & interaction**  
[<img src="https://camo.githubusercontent.com/a0747cb59f501c6e675ccb21d04914a79ca31a38/68747470733a2f2f676973742e6769746875622e636f6d2f656e6a616c6f742f32316335356666313031323239656534366631323265623962643165346237372f7261772f326333646235363337613835373531616236353638636337386634623334636436663365323666322f7468756d626e61696c2e706e67">](https://github.com/enjalot/wwsd/issues/9)


### d3.js
**Leaflet SVG Overlay**  
[<img src="https://gist.githubusercontent.com/enjalot/eaf648eb5fd33a59b3865d8fc4f5eade/raw/4f59de7db1310a2c851c029054fa96b83dbfa495/thumbnail.png">](https://github.com/enjalot/wwsd/issues/10)

**Mapbox-gl SVG Overlay**

[<img src="https://gist.githubusercontent.com/enjalot/0d87f32a1ccb9a720d29ba74142ba365/raw/231cfdc132d214a7b7830173f33338ef236e6c1c/thumbnail.png">](https://github.com/enjalot/wwsd/issues/11)



# Act III
_Hella data_  

### Inspect the data
[USA (SF) data files](data/USA)
View each data file in a text editor.  
Copy each data file into [geojson.io](http://geojson.io)  
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
[Transitions & point-along-path]()
