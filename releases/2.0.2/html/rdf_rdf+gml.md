```
@prefix locn: <http://w3.org/ns/locn#> .
@prefix geosparql: <http://www.opengis.net/ont/geosparql#> .
@prefix sf: <http://www.opengis.net/ont/sf#> .

<ex:a> a locn:Location ;
  locn:geometry [ a sf:Point;
                    geosparql:asGML "<gml:Point srsName="http://www.opengis.net/def/crs/OGC/1.3/CRS84">
                                       <gml:coordinates>
	                                     -0.001475, 51.477811
                                       </gml:coordinates>
			                         </gml:Point>"^^<geosparql:gmlLiteral> ] .
```
