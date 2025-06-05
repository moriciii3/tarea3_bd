Como abrir Mongo Shell mediante Docker:
docker exec -it arxiv_db1 mongosh

Como inicializar los contenedores primarios y los dos secundarios:
rs.initiate({
  _id: "rs0",
  members: [
    { _id: 0, host: "arxiv_db1:27017" },
    { _id: 1, host: "arxiv_db2:27017" },
    { _id: 2, host: "arxiv_db3:27017" }
  ]
})