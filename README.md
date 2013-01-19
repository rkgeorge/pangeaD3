pangeaD3
========

Pangea animation using D3 Orthographic projection.

Demo: <a href="http://www.web-maps.com/pangea/" target="_blank">http://www.web-maps.com/pangea/</a>

Tectonic Plate motion simulation
 
Data is from http://www.gplates.org/ under creative commons license
http://www.gps.caltech.edu/~gurnis/GPlates/License_Caltech_Global_201129.html

1) Time series data was exported as .shp from <a href="http://www.gplates.org/" target="_blank">GPlates 1.2.0.</a> 

2) Converted to GeoJson using <a href="http://www.gdal.org/ogr2ogr.html" target="_blank">ogr2ogr.</a> 

3) GeoJson files were compacted into TopoJson format using the <a href="https://github.com/mbostock/topojson/wiki" target="_blank">topojson</a> node.js tool.

Example:

	From .shp to GeoJson
		ogr2ogr -f GeoJSON step_000.0.json  reconstructed_0.00Ma.shp

	From GeoJson to TopoJson using -simplification of 25 
		topojson -s 25 --force-clockwise true -o topostep_000.json    step_000.json

This provides very good compression: 2.89Mb GeoJson to 340KB TopoJson
