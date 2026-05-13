# Correcciones

**Integrantes:**

* Alejandro Tabarez Rodriguez
* Jeronimo Tabares Gallego

## Error 1

* **Archivo:** `app.py`
* **Problema:** El endpoint `/` devolvía `"status": "ok"` en vez de `"status": "running"`
* **Solución:** Cambié `"ok"` por `"running"` en la función `home()`

## Error 2

* **Archivo:** `app.py`
* **Problema:** El endpoint `/health` no tenía el campo `uptime_seconds`
* **Solución:** Importé `time`, creé la variable `start_time` y agregué `uptime_seconds` en la respuesta JSON

## Error 3

* **Archivo:** `app.py`
* **Problema:** El endpoint estaba definido como `/metric` y los tests esperaban `/metrics`
* **Solución:** Cambié la ruta de `/metric` a `/metrics` y renombré la función a `metrics()`

## Error 4

* **Archivo:** `app.py`
* **Problema:** La aplicación estaba configurada para ejecutarse en el puerto `5001`
* **Solución:** Cambié `port=5001` por `port=5000` en `app.run()`

## Error 5

* **Archivo:** `requirements.txt`
* **Problema:** El archivo requirements.txt no incluía pytest
* **Solución:** Agregué pytest al archivo para que también se instale automáticamente en el pipeline

## Error 6 
* **Archivo:** 'docker-compose.yml'
* **Problema:** El mapeo de puertos estaba incorrecto 5000:5001
* **Solución:** Cambié el mapeo a 5000:5000

## Error 7
* **Archivo:** 'app.py'
* **Problema:** El puerto estaba incorrecto 5000:5001
* **Solución:** Cambié el puerto a 5000:5000

## Error 8
* **Archivo:** 'app.py'
* **Problema:** La ruta tenia un error de sintaxis , /metric 
* **Solución:** Cambié la ruta : /metrics

## Error 9 (optimización)
* **Archivo:** 'Dockerfile'
* **Solución:** Cambié la python:3.11-slim

## Error 8
* **Archivo:** 'app.py'
* **Problema:** El endpoint /metrics devolvía contenido con tipo text/html, pero Prometheus espera text/plain
* **Solución:** Importé Response desde Flask y configuré el endpoint /metrics para responder con mimetype='text/plain'
