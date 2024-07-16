# web-api-fastify-mongodb

Web App and REST API powered by Fastify, Docker and MongoDB

## Initialize Replica set

- Bash into one container: `docker exec -it mongo1 bash`
- Run `mongosh -u root -p example`
- Initiate the replica set using:

```javascript
rs.initiate(
  {
    _id: "rs0",
    version: 1,
    members: [
      { _id: 0, host: "mongo1:27017" },
      { _id: 1, host: "mongo2:27018" },
      { _id: 2, host: "mongo3:27019" }
    ]
  }
)
```

## TODO

- Write bash script to automate start mongo with replica set

## Links

- [MongoDB Replica Set with Docker-compose](https://medium.com/@JosephOjo/mongodb-replica-set-with-docker-compose-5ab95c02af0d)
