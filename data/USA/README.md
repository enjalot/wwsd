# USA Geometries

## States & Counties
Type: MultiPolygon  
Source: [U.S. Atlas](https://github.com/mbostock/us-atlas)  
[TopoJSON](us-named.topojson)  

## California Streams
Type: MultiLineString  
Source: [U.S. Atlas](https://github.com/mbostock/us-atlas)  

[TopoJSON](california-streams.topojson)  

```shell
# clone the us-atlas project and follow instructions for initializing
cd us-atlas
# download the river data
make shp/us/streams-unmerged.shp
# grab california's [region](http://www.horizon-systems.com/nhdplus/NHDPlusV2_data.php) and convert to GeoJSON
ogr2ogr -f GeoJSON topo/us-streams-unmerged-18.geojson shp/us/streams-unmerged.shp -where Region=18
# convert the geojson to topojson (this fails due to lack of memory if tried on the entire country)
geo2topo -o topo/us-streams-unmerged-18.topojson -p Name --no-pre-quantization --post-quantization=1e6 --simplify=7e-7 topo/us-streams-unmerged-18.geojson
```

## SF Election Precincts
Type: MultiPolygon & Tabular data
Source: [Original](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Election-Precincts-Zipped-Shapefile-Format-/w3ua-z2my)
[Processed](http://bl.ocks.org/rogerfischer/338b7fcd478eea7af0eec61f3c5e8c1b)

The SF precincts are split out into two files, one for the geometry and one for
some associated metadata. The two can be joined by the id of each feature.

[TopoJSON](sf-precincts.topojson)  
[CSV](sf-precincts.csv)  
