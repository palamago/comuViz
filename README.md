#comuViz
===========
Visualización de la cantidad de habitantes por comuna de la Ciudad Autónoma de Buenos Aires. 

*Nota: El demo 3D requiere tener instalado el plugin de Google Earth para el browser con el que se esté accediendo*

## Demos
* [Demo 3D](http://alanreid.com.ar/comuViz/3d/index.html) 

## Fuente de la información
* [GCBA Data](http://data.buenosaires.gob.ar/dataset/mapa-comunas) 
* [Censo 2010 (Indec)](http://www.censo2010.indec.gov.ar/resultadosdefinitivos.asp)


## Datos útiles

#### Comando para pasar el shapefile de las comunas a KML (usando GDAL):
```
ogr2ogr 
	-s_srs "+proj=tmerc +lat_0=-34.629269 +lon_0=-58.463300 +x_0=100000 +y_0=100000 +k=0.999998 +units=m +ellps=intl +a=6378388 +rf=297 +no_defs" 
	-t_srs "EPSG:4326" 
	-f "KML" 
	Comunas.kml Comunas.shp
```


#### Comando para pasar el shapefile de las comunas a GeoJSON (usando GDAL):
```
ogr2ogr 
	-s_srs "+proj=tmerc +lat_0=-34.629269 +lon_0=-58.463300 +x_0=100000 +y_0=100000 +k=0.999998 +units=m +ellps=intl +a=6378388 +rf=297 +no_defs" 
	-t_srs "EPSG:4326" 
	-f "GeoJSON" 
	Comunas.json Comunas.shp
```

## Autores
* Pablo Paladino ([@palamago](http://twitter.com/palamago))
* Alan Reid ([@alan_reid](http://twitter.com/alan_reid))

## Licencia
Este software es distribuído bajo la licencia Apache 2.0: http://www.apache.org/licenses/LICENSE-2.0
