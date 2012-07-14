


Comando para pasar el shapefile de las comunas a KML:
ogr2ogr 
	-s_srs "+proj=tmerc +lat_0=-34.629717 +lon_0=-58.462700 +x_0=100000 +y_0=100000 +k=0.999998 +units=m +ellps=intl +a=6378388 +rf=297 +no_defs" 
	-t_srs "EPSG:4326" 
	-f "KML" 
	Comunas.kml Comunas.shp


Comando para pasar el shapefile de las comunas a GeoJSON:
ogr2ogr 
	-s_srs "+proj=tmerc +lat_0=-34.629717 +lon_0=-58.462700 +x_0=100000 +y_0=100000 +k=0.999998 +units=m +ellps=intl +a=6378388 +rf=297 +no_defs" 
	-t_srs "EPSG:4326" 
	-f "GeoJSON" 
	Comunas.json Comunas.shp


