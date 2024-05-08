---
title:  "Docker Cheatsheet"
date:   2024-04-30 9:00:00 # 4/3 10:20-
layout: page
#
# toc: true
# categories:
---

Want to share a few useful docker commands.

```bash
# list running dockers
docker ps

# pull docker image from docker hub
docker pull hello-world
docker run hello-world

# build docker image
docker build -t my-image .

# run a container w a specific port mapping
docker run -d -p 8080:80 my-image

# view container logs
docker logs container_id

# check docker configurations (ie. port, firewall)
docker inspect container_id

# stop/remove container logs
docker stop container_id #stop container
docker rm container_id # remove stopped container

# restart docker command
docker restart container_id [container...]

# stop the running docker compose services
docker-compose down
docker-compose down -v #  removes all volumes associated with the containers, including the node_modules volume. This ensures that any updates to your package.json file are reflected.

# make changes to docker-compose.yaml and start the docker services
docker-compose up -d


# hot reload docker and nextjs config
# https://jameschambers.co.uk/nextjs-hot-reload-docker-development
docker-compose up -d --build

# access docker terminal
docker exec -it container_id /bin/bash

# show docker images and tags
docker images
docker run -p 8000:8000 perplexica-perplexica-backend:latest

# run container detached mode - run in background and don't block the terminal
docker run -d -p 8000:8000 perplexica-perplexica-backend:latest

# docker build image
docker build -f app.dockerfile -t frontend:latest .

# remove unused docker iamges
docker image prune
docker image prune -a
docker image

```
