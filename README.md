## Docker for Absolute Beginner HandsOn

1. Basic commands

Purpose | Command
------------- | -------------
  check version of docker | docker version 
  list of all running container |  docker ps 
  list of all (both running and stopped) container | docker ps -a 
  stop a running container | docker stop <container_id or container_name>
  remove a container | docker rm <container_id or container_name>
  pull a particular image from docker hub | docker pull <image_name>
  run a particular image | docker run <image_name> ; docker run --name webapp nginx:1.14-alpine 
  list of all images | docker images 
  remove a image |  docker rm <image_id or image_name> 
  remove all images | docker rmi -f `docker images -q` ; docker rmi `docker images -q` 
  stop all running container | docker stop `docker ps -q` 
  remove all running containers | docker rm `docker ps -q -a`
  remove all containers of a particular image |
  
