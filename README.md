API para consulta de cédulas SEP
===========

**URL**
```bash
GET https://cedulaprofesional.sep.gob.mx/cedula/buscaCedulaJson.action
```

**Parametros**
```json
{
    "json": {
        "maxResult": "",
        "nombre": "",
        "paterno": "",
        "materno": "",
        "idCedula": ""
    }
}
```
Propiedad|Tipo de datos|Descripcion
---|---|---
maxResult|string|Cantidad maxima de resultados retornados por el API
nombre|string|Nombre para realizar la busqueda. Opcional
paterno|string|Apellido paterno. Solo en caso de busqueda por nombre
materno|string|Apellido materno. Solo en caso de busqueda por nombre
idCedula|string|Numero de cedula profecional a buscar. Opcional

**Headers**
```json
{
    "Content-Type": "application/x-www-form-urlencoded; charset=utf-8"
}
```
| Nota: Si no se especifica el header el API no retorna datos

## Ejemplos

Busqueda por nombre
```curl
curl --location -g --request GET 'https://cedulaprofesional.sep.gob.mx/cedula/buscaCedulaJson.action?json={"maxResult":"1000","nombre":"ENRIQUE","paterno":"PEÑA","materno":"NIETO","idCedula":""}' \
--header 'Content-Type: application/x-www-form-urlencoded; charset=utf-8'
```
Busqueda de cedula por su numero
```curl
curl --location -g --request GET 'https://cedulaprofesional.sep.gob.mx/cedula/buscaCedulaJson.action?json={"maxResult":"1000","nombre":"","paterno":"","materno":"","idCedula":"10390826"}' \
--header 'Content-Type: application/x-www-form-urlencoded; charset=utf-8'
```

## Respuesta

```json
{
    "items": [
        {
            "anioreg": 1991,
            "carArea": null,
            "carCons": null,
            "carNivel": null,
            "carSarea": null,
            "curp": null,
            "desins": "UNIVERSIDAD PANAMERICANA",
            "foja": null,
            "idCedula": "1629426",
            "inscons": null,
            "insedo": null,
            "libro": null,
            "materno": "NIETO",
            "maternoM": null,
            "nombre": "ENRIQUE",
            "nombreM": null,
            "numero": null,
            "paterno": "PEÑA",
            "paternoM": null,
            "sexo": "1",
            "tipo": "C1",
            "titulo": "LICENCIATURA EN DERECHO"
        },
        {
            "anioreg": 2017,
            "carArea": null,
            "carCons": null,
            "carNivel": null,
            "carSarea": null,
            "curp": null,
            "desins": "INSTITUTO TECNOLÓGICO Y DE ESTUDIOS SUPERIORES DE MONTERREY",
            "foja": null,
            "idCedula": "10390826",
            "inscons": null,
            "insedo": null,
            "libro": null,
            "materno": "NIETO",
            "maternoM": null,
            "nombre": "ENRIQUE",
            "nombreM": null,
            "numero": null,
            "paterno": "PEÑA",
            "paternoM": null,
            "sexo": "1",
            "tipo": "C1",
            "titulo": "MAESTRÍA EN ADMINISTRACIÓN"
        }
    ],
    "filename": null,
    "idCedula": null,
    "idProfesionista": null,
    "sessionId": null,
    "theStream": null,
    "token": null,
    "urlVideo": null
}
```
