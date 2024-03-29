	$ docker ps -a  // status
	$ docker stop service_id  // stop
	$ docker rm service_id   //remove
	$ docker ps -a
	$ docker images


### Docker Compose
	$ docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d   // up docker compose
	$ docker-compose -f docker-compose.yml -f docker-compose.override.yml down    // down docker compose
	
#Docker Commands


### Example docker hub pull :

	$ docker run -d --hostname swn-rabbit --name swn-rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management

### Single Container

For aspnetcore app after adding docker file -- for single container add docker file build and run = create new container

	$ docker build -t aspnetapp .
 
	$ docker run -d -p 8080:80 --name myapp aspnetapp

 $ docker compose up

### This command run multiple container

Multi Container - docker-compose.yml

	$ docker-compose up
	$ docker-compose -f docker-compose.yaml -f docker-compose-infrastructure.yaml up --build


 $ DOCKER REMOVE ALL CONTAINER IMAGES PS -A

### POWERSHELL commands

https://blog.baudson.de/blog/stop-and-remove-all-docker-containers-and-images

### List all containers (only IDs)

 $ docker ps -aq

### Stop all running containers

 $ docker stop $(docker ps -aq)

### Remove all containers

 $ docker rm $(docker ps -aq)

### Remove all images

 $ docker rmi $(docker images -q)

### Remove all none images

 $ docker system prune

-- You can also run all with copy paste

 $ docker ps -aq

 $ docker stop $(docker ps -aq)

 $ docker rm $(docker ps -aq)

 $ docker rmi $(docker images -q) -f

 $ docker system prune

### Docker Compose Commands
Close all dockers and run with below command on that location;

	$ docker-compose -f docker-compose.yml -f docker-compose.override.yml up --build
 
	or
 
	$ docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
 
	$ docker-compose -f docker-compose.yml -f docker-compose.override.yml down
 
