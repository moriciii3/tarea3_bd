-- Integrantes --
Bruno Morici, ROL: 202373555-8
Martin Aranda, ROL: 202373021-1

--- Orden para probar la tarea ---
(1) Abrir Mongo App
(2) Mediante la WSL acceder a la carpeta de la tarea
(3) Ejecutar el comando "docker compose -f deploy-2023730211-2023735558.yml up -d"
(4) Correr todo el código del Notebook
(Opcional) Detener el bloque de la carga de datos, ya que gasta muchos recursos del PC
(5) Disfrutar ;)

--- Otras consideraciones ---

Modificamos levemente el compose que se nos entregó, esto debido a que generaba errores en la generación de los volúmenes de data, para ello utilizamos volúmenes de Docker en vez de bind mounts, con esto funciona bien.

Debido al excesivo peso del dataset entregado se subió a un drive para descargarlo posteriormente: https://drive.google.com/file/d/1P2NWF41B6LljOhB5t-6P3yVq4HGDUO0M/view?usp=sharing

Para que se pueda leer el dataset, este archivo uarxiv-202730211-2023735558.json se debe encontrar en la misma carpeta que el pymongo-2023730211-2023735558.ipynb para que se pueda realizar la lectura

Como abrir Mongo Shell mediante Docker:
docker exec -it mongo1 mongosh --port 30001

En la mongosh con el comando rs.status() se puede verificar la correcta inicialización de los contenedores con la arquitectura solicitada.
