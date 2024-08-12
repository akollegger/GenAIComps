# Start Neo4j server

## Manual installation and start

### 1. Download Neo4j image

```bash
docker pull neo4j:5.20.0
```

### 2. Run Neo4j service

```bash
docker run \
    --restart always \
    --publish=7474:7474 --publish=7687:7687 \
    --env NEO4J_AUTH=neo4j/your_password \
    --volume=./data:/data \
    neo4j:5.22.0
```

Notes:
- `neo4j/yourpassword` is a username/password combination for the default `neo4j` user. Replace `your_password` with a password of your choosing
- `./data` should be replaced with a location 

## Using docker up

### 1. Set required environmental variables

```bash
export NEO4J_AUTH=neo4j/your_password
```

### 2. Start Neo4j service

```bash
docker compose up
```

## Appendix - Neo4j in Docker

- [Neo4j in Docker documentation](https://neo4j.com/docs/operations-manual/current/docker/introduction/)
- [Neo4j Tags on DockerHub](https://hub.docker.com/_/neo4j/tags)
