## Docker for Absolute Beginner HandsOn

1. Basic commands - Images and Containers

Purpose | Command
------------- | -------------
  Check version of docker | docker version 
  List of all running container |  docker ps 
  List of ids of all running container | docker ps -q
  List of all (both running and stopped) container | docker ps -a 
  Stop a running container | docker stop <container_id or container_name>
  Remove a container | docker rm <container_id or container_name>
  Removing multiple container | docker rm <list of container_id or container_name separated by space>
  Stop all running container | docker stop \`docker ps -q\` 
  Remove all running containers | docker rm \`docker ps -q -a\`
  List of all images | docker images 
  Pull a particular image | docker pull <image_name>
  Run a particular image | docker run <image_name> <br/> docker run --name webapp nginx:1.14-alpine 
  Remove a image |  docker rm <image_id or image_name> 
  Remove all images | docker rmi -f \`docker images -q\` <br/> docker rmi \`docker images -q\` 
  Remove all containers of a particular image |
  
