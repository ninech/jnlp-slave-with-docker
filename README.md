# JNLP Slave with Docker

A JNLP Slave Docker image with docker and docker-compose installed. We use this with the Jenkins ECS plugin to
automatically provision Jenkins slaves which then can use Docker to run their jobs.

Make sure to map the host's Docker socket into the container:

```sh
docker run -v /var/run/docker.sock:/var/run/docker.sock ninech/jnlp-slave-with-docker docker ps
```
