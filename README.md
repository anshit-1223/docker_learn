Commands

docker ps - shows Containers
docker images - shows Images
docker build -t app_name_to_be_created Dockerfile_name
docker run app_name_created

docker restart containerid

to connect running container
docker exec -it containerid commands
OR
docker exec -it containername bash

Steps to Stop/Delete container
docker ps -a - shows all current stopped / exited / running
docker rmi -f containerid - to remove container
docker stop imageid


DOCKER FILE ARCHITECTURE

FROM - Base Image 
WORKDIR - directory where code to be kept and later executed
COPY - copy source code to workdir
RUN - command to compile the code
CMD - command to run the compiled code


DOCKER NETWORKING

SEVEN TYPES OF NETWORKS -
Host
Bridge(default)
User Defined Bridge (Custom)
None
MACVLAN (Docker Swarm) outdated
IPVLAN
Overlay

Netowrking Commands 

docker network ls
docker network create -d bridge

//to pull mysql image
docker run --name mysql --network mynetwork -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=devops -d mysql  

//to run flask app in backend
docker run -d -p 5000:5000 --network mynetwork -e MYSQL_HOST=mysql -e MYSQL_USER=root -e MYSQL_PASSWORD=root -e MYSQL_DB=devops two-tier-flask-app:latest