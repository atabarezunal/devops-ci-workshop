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

