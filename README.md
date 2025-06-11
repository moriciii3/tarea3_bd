-- Integrantes --
Bruno Morici, ROL: 202373555-8
Martin Aranda, ROL: 202373021-1

--- Orden para probar la tarea ---
(1) Abrir Mongo App
(2) Mediante la WSL acceder a la carpeta de la tarea
(3) Ejecutar el comando "docker compose up -d"
(4) Correr todo el código del Notebook
(Opcional) Detener el bloque de la carga de datos, ya que gasta muchos recursos del PC
(5) Disfrutar ;)

--- Otras consideraciones ---

Como abrir Mongo Shell mediante Docker:
docker exec -it mongo1 mongosh

En la mongosh con el comando rs.status() se puede verificar la correcta inicialización de los contenedores con la arquitectura solicitada.

La inicialización es automática mediante el docker compose, aquí creamos un contenedor llamado mongo-init que ejecuta el comando de inicialización de forma automática.

El docker compose entregado en la tarea no fue utilizado ya que generaba errores, pero realizamos la misma y exacta arquitectura maestro-esclavo con 1 primario (mongo1) y 2 secundarios (mongo2), los cuales son consistentes y comparten la misma data.

Para que se pueda leer el dataset, este archivo arxiv-metadata-oai-snapshot.json se debe encontrar en la misma carpeta que el notebook.ipynb para que se pueda realizar la lectura