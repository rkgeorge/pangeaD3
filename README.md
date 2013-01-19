pangeaD3
========

Pangea animation using D3 Orthographic projection
Tectonic Plate motion simulation using D3
Data is from http://www.gplates.org/ under creative commons license
http://www.gps.caltech.edu/~gurnis/GPlates/License_Caltech_Global_201129.html

Time series data was exported as .shp and then converted to geoJson using ogr2ogr.These GeoJson files were compacted into TopoJson format using the <a href="https://github.com/mbostock/topojson/wiki" target="_blank">topojson</a> node.js tool.

Example:
	From .shp to GeoJson
		ogr2ogr -f GeoJSON step_000.0.json  reconstructed_0.00Ma.shp

	From GeoJson to TopoJson
		topojson -s 25 --force-clockwise true -o topostep_000.json    step_000.json
