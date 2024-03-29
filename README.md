# Cassandra Docker playground

## Getting Started

While in project dir copy example env file to .env
```
cp .env_example .env
docker-compose up
```
To check that both nodes are up and running execute
```
docker exec -it cas2 nodetool status
docker exec -it cas2 nodetool status
```
Both should have IP assigned and status `UN` (Up and Normal)

To get into CQL shell
```
docker exec -it cas2  cqlsh
```

`connect.py` contain example of connection Python outside of docker to Cassandra inside docker

### Prerequisites

Have installed and running docker

### Troubleshooting

Before you even start, make sure you set up the Docker Memory to at least 4GB otherwise the container can exit with the error code 137.
