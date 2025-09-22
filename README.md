| command  | Description |
| ------------- | ------------- |
| **docker version** | Output of information |
| **docker ps -a** | Displaying information about all containers |
| **docker images** | Displaying a list of images |
| **docker rm \<name>** | Deleting a container |
| **docker rm -f $(docker ps -aq)** | Forced deletion |
| **docker container prune** | Deleting all stopped containers |
| **docker container inspect \<name>** | Getting information |
| **docker stop <name> ~ docker kill \<name>** | Container stop |
| **docker exec -it \<name> bash** | Connecting to a container |
| **docker run \<name>** | Creating a container |
| **docker run -it \<name>** | Switching to interactive mode |
| **docker run -d \<name>** | Running in the background |
| **docker run -d --name \<cast_name> \<name>** | Assign a name|
| **docker run -p <external_port>:<container_port> \<name>** | Port mapping |
| **docker run -v <local_path>:<container_path> \<name>** | Volume mapping |
| **docker run --rm \<name>** | Automatic deletion |



#### Long commands
```shell
docker run \
  --name my_nginx \
  -v ${PWD}:/home \
  -p 8080:80 \
  -d \
  --rm \
  nginx
```