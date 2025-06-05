Como abrir Mongo Shell mediante Docker:
docker exec -it mongo1 mongosh

Como inicializar los contenedores primarios y los dos secundarios:
rs.initiate({
  _id: "rs0",
  members: [
    { _id: 0, host: "mongo1:27017" },
    { _id: 1, host: "mongo2:27017" },
    { _id: 2, host: "mongo3:27017" }
  ]
})