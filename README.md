# JNLP Slave with Docker [![Docker Badge]][Docker Hub]

A JNLP Slave Docker image with docker and docker-compose installed. We use this with the Jenkins ECS plugin to
automatically provision Jenkins slaves which then can use Docker to run their jobs.

You can either connect via the Docker socket like this:

```sh
docker run -v /var/run/docker.sock:/var/run/docker.sock ninech/jnlp-slave-with-docker docker ps
```

Or better, connect to some external Docker deamon via TCP:

```sh
docker run -e DOCKER_HOST=dind ninech/jnlp-slave-with-docker docker ps
```

See the [docker-compose.yml](docker-compose.yml) file for reference.

[Docker Badge]: https://badgen.net/docker/pulls/devsisters/jnlp-slave-with-docker?icon=docker&label=pulls
[Docker Hub]: https://hub.docker.com/r/devsisters/jnlp-slave-with-docker/
