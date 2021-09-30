# Simple Node 
[![Build Status](https://app.travis-ci.com/AntonioDaria/simple_node.svg?branch=master)](https://app.travis-ci.com/AntonioDaria/simple_node)
## Overview
This is a very simple, bare-bones NodeJS.
The purpose of this project is to demonstrate the use of Containers with Docker as well as setting up CI piplines with Travis CI.

Note that in the .travis.yml file Environment variables containing sensitive informations are used to interact with Dockerhub(see example below)
* push to docker: `push "$DOCKER_HUB_USER_NAME"/container_demo`

## Local Setup
* Install dependencies: `npm install`
* Run server: `node server.js`

## Container Setup
* Build image: `docker build .`
* Run container with image: `docker run {image_id}` where `image_id` can be retrieved by running `docker images` and found under the column `IMAGE ID`

## Push a docker image to Dockerhub
* tag image: `docker tag <image name> <Dockerhub UserName>/ <image name> .`
* connect to docker hub: `docker login --username=<Dockerhub username> .`
* push the image to docker hub: `docker push <Dockerhub username>/<image name> {image_id} `

## Container teardown
* Remove container: `docker kill {container_id}` where `container_id` can be retrieved by running `docker ps` and found under the column `CONTAINER ID`
