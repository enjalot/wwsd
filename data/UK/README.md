# UK Geometries

## Counties (Local Authority Districts)
Type: MultiPolygon  
Source: http://martinjc.github.io/UK-GeoJSON/  

[GeoJSON](counties.geojson)  
[TopoJSON](counties.topojson)  

These files came preprocessed (GeoJSON and TopoJSON)

NOTE:  
```
"counties" in the United Kingdom are not really straightforward. There seem to be a few different ways
to subdivide England, and counties don't cover all of the country. For the purpose of our workshop,
we just want some more detailed administrative boundaries somewhere besides San Francisco. If you are
interested in getting into the finer points, see these links:  
```
https://en.wikipedia.org/wiki/Subdivisions_of_England  
http://gis.stackexchange.com/questions/132105/where-could-i-find-geojson-data-for-all-counties-of-the-uk  


## Tube lines
Type: MultiLineString  
Source: https://github.com/oobrien/vis [specifically](https://github.com/oobrien/vis/blob/master/tube/data/tfl_lines.json)  

[GeoJSON](london_tube.geojson)  
[TopoJSON](london_tube.topojson)  

Download the geojson file from the link and rename to `london_tube.geojson`.
convert the geojson to topojson and preserve only a couple key properties:
```shell
geo2topo london_tube.geojson -p id -p lines -o london_tube.topojson
```


## Tube stations
Type: Point  
Source: https://github.com/oobrien/vis [specifically](https://github.com/oobrien/vis/blob/master/tube/data/tfl_stations.json)  

[GeoJSON](london_stations.geojson)  
[TopoJSON](london_stations.topojson)  

Download the geojson file from the link and rename to `london_tube.geojson`.  
convert the geojson to topojson and preserve only a couple key properties:  
```shell
geo2topo london_stations.geojson -p id -p name -p lines -o london_stations.topojson
```
