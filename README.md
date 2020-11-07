## Docker for Absolute Beginner HandsOn

#### 1. Basic commands - Images and Containers

Purpose | Command
------------- | -------------
  Check version of docker | docker version 
  List of all running container |  docker ps 
  List of ids of all running container | docker ps -q
  List of all (both running and stopped) container | docker ps -a 
  Details of a container | docker inspect <container_name>
  Logs of a container | docker logs <container_name>
  Stop a running container | docker stop <container_id or container_name>
  Remove a container | docker rm <container_id or container_name>
  Removing multiple container | docker rm <list of container_id or container_name separated by space>
  Stop all running container | docker stop \`docker ps -q\` 
  Remove all running containers | docker rm \`docker ps -q -a\`
  List of all images | docker images 
  Pull a particular image | docker pull <image_name>
  Run a particular image | <ol><li>docker run <image_name></li> <li>docker run --name <container_name> <image_name></li></ol> 
  Remove a image |  docker rm <image_id or image_name> 
  Remove all images | <ol><li>docker rmi -f \`docker images -q\` </li><li> docker rmi \`docker images -q\`</li></ol> 
  Remove all containers of a particular image |
  
#### 2. Docker run
   
   There are 2 modes of running a docker image<br/>
   1. attach (default) - which executes the docker image in foreground but doesnot accept user interaction
   2. detach - runs docker image in background
   
   Attach Mode : 
   
  Command | Working
  ------------- | -------------
  docker run --name <container_name><image_name> | Creates the container with the name specified and starts executing it in foreground
  docker run --name <container_name><image_name>  | Accepts user input but doesn't provide an interactive terminal
  docker run -it --name <container_name><image_name> | Creates the container with the name specified and starts executing it in foreground.Accepts user input by provide an interactive terminal
  
  Detach Mode :
  
  Command | Working
  ------------- | -------------
  docker run -d <image_name> | Creates the container with random name and starts executing it in background
  docker exec <container_name or container_id> <command> | Execute a particular command on the detached container if required
  
  Port Mapping :
  
  - Used to redirect a container to a different port 
  - Used when user create multiple instances of a single image
  
  Command | Working
  ------------- | -------------
  docker run -P <image_name> | -P runs the application in a random port
  docker run -p <redirect_port>:<default_port> <image_name> | -p redirects the application to a specific port
  

  Volume : 
  - used to create a persistance volume of the data's stored in the container
  
  Command | Working
  ------------- | -------------
 docker run -v  /root/<any_folder_name>:<path_of_data's_in_image> | creates a path with given folder name in root and persist the data
 
 
 #### 3. Docker images
 
  
