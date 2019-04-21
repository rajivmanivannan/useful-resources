# Docker Commands

## ORCHESTRATE

* Initialize swarm mode and listen on a specific interface

``` bash
docker swarm init --advertise-addr 10.1.0.2
```

* Join an existing swarm as a manager node

``` bash
docker swarm join --token <manager-token> 10.1.0.2:2377
```

* Join an existing swarm as a worker node

``` bash
docker swarm join --token <worker-token> 10.1.0.2:2377
```

* List the nodes participating in a swarm

``` bash
docker node ls
```

* Create a service from an image exposed on a specific port and deploy 3 instances

``` bash
docker service create --replicas 3 -p 80:80 --name web nginx
```

* List the services running in a swarm

``` bash
docker service ls
```

* Scale a service

``` bash
docker service scale web=5
```

* List the tasks of a service

``` bash
docker service ps web
```

-- -- --

## BUILD

* Build an image from the Dockerfile in the current directory and tag the image

``` bash
docker build -t myapp:1.0 .
```

* List all images that are locally stored with the Docker engine

``` bash
docker images
```

* Delete an image from the local image store

``` bash
docker rmi alpine:3.4
```

-- -- --

## SHIP

* Pull an image from a registry

``` bash
docker pull alpine:3.4
```

* Retag a local image with a new image name and tag

``` bash
docker tag alpine:3.4 myrepo/myalpine:3.4
```

* Log in to a registry (the Docker Hub by default)

``` bash
docker login my.registry.com:8000
```

* Push an image to a registry

``` bash
docker push myrepo/myalpine:3.4
```

-- -- --

## RUN

``` bash
docker run
-- rm remove container automatically after it exits
-it connect the container to terminal
--name web name the container
-p 5000:80 expose port 5000 externally and map to port 80
-v ~/dev:/code create a host mapped volume inside the container
alpine:3.4 the image from which the container is instantiated
/bin/sh the command to run inside the container
```

* Stop a running container through SIGTERM

``` bash
docker stop web
```

* Stop a running container through SIGKILL

``` bash
docker kill web
```

* Create an overlay network and specify a subnet

``` bash
docker network create --subnet 10.1.0.0/24 --gateway 10.1.0.1 -d overlay mynet
```

* List the networks

``` bash
docker network ls
```

* List the running containers

``` bash
docker ps
```

* Delete all running and stopped containers

``` bash
docker rm -f $(docker ps -aq)
```

* Create a new bash process inside the container and connect it to the terminal

``` bash
docker exec -it web bash
```

* Print the last 100 lines of a container’s logs

``` bash
docker logs --tail 100 web
```

-- -- --