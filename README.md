API para consulta de cédulas SEP
===========

API para consulta de cédulas profesionales de la SEP

http://search.sep.gob.mx/solr/cedulasCore/select?fl=%2A%2Cscore&q=enrique+pena+nieto&start=0&rows=100&facet=true&indent=on&wt=json

```
{
  "responseHeader":{
    "status":0,
    "QTime":1,
    "params":{
      "facet":"true",
      "indent":"on",
      "wt":"json",
      "rows":"100",
      "fl":"*,score",
      "start":"0",
      "q":"enrique pena nieto"}},
  "response":{"numFound":153546,"start":0,"maxScore":3.4999735,"docs":[
      {
        "nombre":"ENRIQUE",
        "id":"1629426|C1",
        "numCedula":"1629426",
        "titulo":"LICENCIATURA EN DERECHO",
        "genero":"1",
        "institucion":"UNIVERSIDAD PANAMERICANA",
        "materno":"NIETO",
        "anioRegistro":1991,
        "tipo":"C1",
        "paterno":"PEÑA",
        "timestamp":"2015-01-22T09:14:58.313Z",
        "score":3.4999735},
	...
```
