# Working with spatial data for the web

![Working with spatial data](img/header.png)

## Introduction

This workshop is designed to be very hands-on, with many examples that can be
extended as exercises. It would be impossible to touch everything that we could
find [interesting in web mapping](https://hi.stamen.com/an-ode-to-d3-js-projections-9d6477d6da0b#.1hr10rltk),
so the hope is that after going through these three acts you will feel empowered
to swap in your own data and leverage [hundreds of examples](http://blockbuilder.org/search#api=geo.path) in your own data visualization projects!

## Tools

This workshop will cover the following Javascript libraries, by the end you will have had
hands on experience with each one. We will see first-hand which tool is best for the
job in different situations.

* [Leaflet](http://leafletjs.com)
* [Mapbox-gl](https://www.mapbox.com/mapbox-gl-js/examples/)
* [d3.js](http://d3js.org)
* [turf.js](http://turfjs.org/)


# Act I: fundamentals
_I've got the whole world, in my hands_

This first part of the workshop will focus on understanding the data and quickly getting something on the screen.

## Data

First things first we will play with basic GeoJSON on [geojson.io](http://geojson.io) to get an intuitive sense for spatial data.
We can look at [this example](http://blockbuilder.org/enjalot/9a51c6ef89a3625684bf) to get a relative sense for the "size" of a degree in longitude and latitude.  
[<img src="https://gist.github.com/enjalot/9a51c6ef89a3625684bf/raw/da78aefb6caca640fbad4432e6c7f2c4ba2cbf0f/thumbnail.png">](http://blockbuilder.org/enjalot/9a51c6ef89a3625684bf)

We will use a set of pre-prepared datasets designed to cover a variety of locations and scales (world-wide
down to city level) in the workshop so that you don't feel confined to one geographic area
while practicing. Each data folder contains a README that describes where the
data comes from and how it was processed:

[World data files](data/world)  
[UK (London) data files](data/UK)  
[USA (SF) data files](data/USA)

We will explore the three basic GeoJSON data types with these files:  
* Polygons - Administrative boundaries (e.g. countries, states and counties)
* Lines - Roads, Routes and Rivers
* Points - Cities, Subway stations

You can find the commands we used to process and convert the data in each folder.
If you want to convert your own spatial data you may want to start with
[Mapshaper](http://www.mapshaper.org/) before getting into command line tools.

I recommend reading [More than you ever wanted to know about GeoJSON](http://www.macwright.org/2015/03/23/geojson-second-bite.html)
before the workshop, we will cover the same stuff but its a concise overview and a great reference.


### Leaflet
**[1) Getting started with Leaflet](https://github.com/enjalot/wwsd/issues/1)**  
[<img src="https://gist.github.com/enjalot/208dd99b6ed6a424513524d963880700/raw/c026672c7dc702708f1d5a5ef5097da2e336dc20/thumbnail.png">](https://github.com/enjalot/wwsd/issues/1)

**[2) Basic styling & interaction](https://github.com/enjalot/wwsd/issues/2)**  
[<img src="https://gist.githubusercontent.com/enjalot/0c8028933d402fb4823a5b0067b12a56/raw/2f8a6bb6ffd901059f95565f74175237a25d70fe/thumbnail.png">](https://github.com/enjalot/wwsd/issues/2)

### Mapbox-gl

**[3) Getting started with Mapbox-gl](https://github.com/enjalot/wwsd/issues/3)**  
[<img src="https://gist.github.com/enjalot/b81e02d752855d106f88a9c0e42e65a0/raw/f897bad8e804af7428c1d4419daca4f13e1cd2d3/thumbnail.png">](https://github.com/enjalot/wwsd/issues/8)

**[4) Basic styling & interaction](https://github.com/enjalot/wwsd/issues/4)**  
[<img src="https://camo.githubusercontent.com/a0747cb59f501c6e675ccb21d04914a79ca31a38/68747470733a2f2f676973742e6769746875622e636f6d2f656e6a616c6f742f32316335356666313031323239656534366631323265623962643165346237372f7261772f326333646235363337613835373531616236353638636337386634623334636436663365323666322f7468756d626e61696c2e706e67">](https://github.com/enjalot/wwsd/issues/9)


# Act II: d3.js
_Data driven_  

This second part of the workshop will focus on understanding projections and using them
with [d3](http://d3js.org) to render custom data-driven maps.

## Projections
[Map projections](https://en.wikipedia.org/wiki/Map_projection) are an important concept, and we need at least a basic grasp
of how they work to make the kinds of [custom maps](https://hi.stamen.com/an-ode-to-d3-js-projections-9d6477d6da0b#.bemxsm2j1) we'd like to with d3.  
[<img src="https://gist.github.com/enjalot/b3dcf273c3c6d56411b6/raw/d01821a6ae8e6e78681984fdfc52aa7f2fa4eb14/thumbnail.png">](https://hi.stamen.com/an-ode-to-d3-js-projections-9d6477d6da0b#.bemxsm2j1)

One point we need to emphasize is that projections introduce distortion,
to get a sense for how different projections distort the geometry of the earth play with [this example](http://blockbuilder.org/enjalot/bd552e711b8325c64729):  
[<img src="https://gist.github.com/enjalot/bd552e711b8325c64729/raw/0c08b1ff1f690f12d476de724ac8a8084a137567/thumbnail.png">](http://blockbuilder.org/enjalot/bd552e711b8325c64729)  
A fun modification using images to show distortion:  
[<img src="https://gist.github.com/enjalot/5233898432653069ea8e/raw/96143ed7dd56e0a576e91b1362e16442d5f9f77b/thumbnail.png">](http://blockbuilder.org/enjalot/5233898432653069ea8e)  
And a [gratuitous animation](http://blockbuilder.org/enjalot/27969219a945e2bd20dc) with a particularly interesting projection.

If you want to understand projections from a fundamental level, checkout this [thorough presentation](http://lyzidiamond.com/geodesy-pt-1/#0) on where projections come from.


## Rendering with d3.js

**[5) SVG Paths](https://github.com/enjalot/wwsd/issues/5)**  
[<img src="https://gist.githubusercontent.com/enjalot/6c13610b33ed9d3f5b052fa3fc20ba56/raw/95497d048c07a95148b0d629d9dd34362a10c48c/thumbnail.png">](https://github.com/enjalot/wwsd/issues/5)

**[6) Rendering a map with d3 projections](https://github.com/enjalot/wwsd/issues/46)**   
[<img src="https://gist.githubusercontent.com/enjalot/c069550b4fc4fb409430829f07bd78f2/raw/74dce341847482d9dfd387b2aa6127eab539c3ba/thumbnail.png">](https://github.com/enjalot/wwsd/issues/6)

**[7) Mouse interactions with d3 + SVG](https://github.com/enjalot/wwsd/issues/7)**  
[<img src="https://gist.github.com/enjalot/b37e8dac613d0a39c5b4c2f0e13e1277/raw/c82cb9e878a20d632ce54700203dfb9070b12998/thumbnail.png">](https://github.com/enjalot/wwsd/issues/7)

**[8) Data lookups](https://github.com/enjalot/wwsd/issues/8)**  
[<img src="https://gist.github.com/enjalot/f071fe9f332c62cb7bcad13ae5d645d8/raw/9d153c338e5c793107c2bba894c956cd592eee67/thumbnail.png">](https://github.com/enjalot/wwsd/issues/8)

### Advanced d3.js usage

**[9) Zooming with d3](https://github.com/enjalot/wwsd/issues/9)**  
[<img src="https://gist.githubusercontent.com/mbostock/4987520/raw/2eb118ef3ac0869552c6ce5cb77c625c6558e5cb/thumbnail.png">](https://github.com/enjalot/wwsd/issues/9)

**[10) Leaflet SVG Overlay](https://github.com/enjalot/wwsd/issues/10)**  
[<img src="https://gist.githubusercontent.com/enjalot/eaf648eb5fd33a59b3865d8fc4f5eade/raw/4f59de7db1310a2c851c029054fa96b83dbfa495/thumbnail.png">](https://github.com/enjalot/wwsd/issues/10)

**[11) Mapbox-gl SVG Overlay](https://github.com/enjalot/wwsd/issues/11)**

[<img src="https://gist.githubusercontent.com/enjalot/0d87f32a1ccb9a720d29ba74142ba365/raw/231cfdc132d214a7b7830173f33338ef236e6c1c/thumbnail.png">](https://github.com/enjalot/wwsd/issues/11)


# Act III: performance
_Hella data_  

This part of the workshop will focus on how we can render our maps with better performance.
We can utilize an extension of GeoJSON called [TopoJSON](https://github.com/mbostock/topojson) as well as other rendering techniques like using the [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API).

### TopoJSON
[TopoJSON](https://github.com/mbostock/topojson) is an extension of GeoJSON that encodes topology. One of the biggest benefits of this is
that file sizes can be significantly smaller.

A couple tools that can be used to orient yourself with TopoJSON files:
[Inspect TopoJSON](http://blockbuilder.org/enjalot/63d06e2ccadad0cb30dc5f920efd1cdf)  
[Preview TopoJSON](http://blockbuilder.org/enjalot/fe2a8ee0ad59a58ce295f035419d9e63)  


**[12) Rendering a map with d3 + TopoJSON + SVG](https://github.com/enjalot/wwsd/issues/12)**  
[<img src="https://gist.githubusercontent.com/enjalot/4a449bee40e7b74108de89e303a2a284/raw/09d140a991f7cbbe507b6d01086c2c6a3c79a90d/thumbnail.png">](https://github.com/enjalot/wwsd/issues/12)

### Canvas
[Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) is an HTML5 API for drawing pixel based images in the browser with Javascript.
It is possible to render lots of data quicker with canvas than SVG, but it is less convenient for interaction.

**[13) Rendering with d3 + Canvas](https://github.com/enjalot/wwsd/issues/13)**  
[<img src="https://gist.github.com/enjalot/f6ac38e86de3e7d4cbe109ed601fa6d7/raw/64141ff1ccc42e112fd1f17c713f5d424a7f9a82/thumbnail.png">](https://github.com/enjalot/wwsd/issues/13)

**[14) Zooming with Canvas](https://github.com/enjalot/wwsd/issues/13)**  
[<img src="https://gist.githubusercontent.com/mbostock/4987520/raw/2eb118ef3ac0869552c6ce5cb77c625c6558e5cb/thumbnail.png">](https://github.com/enjalot/wwsd/issues/14)

**[15) Mapbox-gl Canvas Overlay](https://github.com/enjalot/wwsd/issues/13)**  
[<img src="https://gist.github.com/enjalot/7e1c6eda09fb3c8cb64453a79e760f25/raw/d0006272e088f9a7012fbbd85c6594c47ea9d8e3/thumbnail.png">](https://github.com/enjalot/wwsd/issues/15)

## turf.js

[TurfJS](http://turfjs.org) is a Javascript library for geospatial calculations and analysis.
It provides many features which can come in handy when dealing with spatial data.

**[16) Measuring areas and lengths]()**  
[<img src="https://gist.github.com/enjalot/7e1c6eda09fb3c8cb64453a79e760f25/raw/d0006272e088f9a7012fbbd85c6594c47ea9d8e3/thumbnail.png">](https://github.com/enjalot/wwsd/issues/16)

**[17) Buffering and contracting features]()**  
[<img src="https://gist.github.com/enjalot/397af58276d926193d28b8023b2400f2/raw/53ceb523af4237bb5b464e2475a968c716300545/thumbnail.png"](https://github.com/enjalot/wwsd/issues/17)

# Encore: advanced techniques
We may not have time to explore these examples in depth, but they should provide
inspiration and exercises for those who wish to venture deeper into the technical
possibilities of the tools covered in this workshop.

**It's a map, sort of**  
Using geospatial properties or locations to add context:  
[Circle counties](http://bl.ocks.org/mbostock/4206975)  
Try doing this with the [world populations](http://enjalot.github.io/wwsd/data/world/ne_50m_admin_0_countries.topojson)
You can calculate the centroids of each country using d3 or turf. [Example answer](http://blockbuilder.org/eesur/14e16ab00342ea44e46f3fa45a2bbf08)

**Advanced canvas interaction**   
[Selecting countries on a canvas globe](http://bl.ocks.org/syntagmatic/6645345)  

**Clipping**  
[Clipping geometry data](http://blockbuilder.org/mbostock/6301872)  
[Clipping raster tiles](http://bl.ocks.org/enjalot/985de8fcd65d37583949edbf280f2632)  

**Animated paths**  
[Timer & Mapbox-gl](http://bl.ocks.org/enjalot/4ff31e96860f38d4fd58)  
[Transitions & Canvas](http://blockbuilder.org/rveciana/502db152b70cddfd554e9d48ee23e279)
[Point-along-path & SVG]()
