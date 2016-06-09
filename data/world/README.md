# World Geometries

## Admin 0 Country Boundaries
Type: MultiPolygon  
Source: [geojson.xyz](http://geojson.xyz)  


download the geojson file
```shell
wget https://d2ad6b4ur7yvpq.cloudfront.net/naturalearth-3.3.0/ne_50m_admin_0_countries.geojson
```
convert the geojson to topojson (with simplification) and preserve a couple key properties
```shell
topojson -s 1e-6 ne_50m_admin_0_countries.geojson -p name -p pop_est -p continent -o ne_50m_admin_0_countries.topojson
```

## Populated Places Simple (Cities)
Type: Point  
Source: [geojson.xyz](http://geojson.xyz)  


download the geojson file
```shell
wget https://d2ad6b4ur7yvpq.cloudfront.net/naturalearth-3.3.0/ne_50m_populated_places_simple.geojson
```
convert the geojson to topojson and preserve only a couple key properties
```shell
topojson ne_50m_populated_places_simple.geojson -p name -p adm0name -o ne_50m_populated_places_simple.topojson
```

## Rivers & Lake centerlines
Type: LineString  
source: [geojson.xyz](http://geojson.xyz)


download the geojson file  
```shell
wget https://d2ad6b4ur7yvpq.cloudfront.net/naturalearth-3.3.0/ne_50m_rivers_lake_centerlines.geojson
```
convert the geojson to topojson and preserve only a couple key properties
```shell
topojson -s 1e-6 ne_50m_rivers_lake_centerlines.geojson -p name -p dissolve -p featureclass -o ne_50m_rivers_lake_centerlines.topojson
```

## File sizes
Notice how much smaller the topojson files are than the geojson:
| filesize | filename |
|----------|----------|
| 3.9M | ne_50m_admin_0_countries.geojson |
| 301K | ne_50m_admin_0_countries.topojson |
| 893K | ne_50m_populated_places_simple.geojson |
| 121K | ne_50m_populated_places_simple.topojson |
| 1.0M | ne_50m_rivers_lake_centerlines.geojson |
| 143K | ne_50m_rivers_lake_centerlines.topojson |
```
