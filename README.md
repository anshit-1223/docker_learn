Commands

docker ps - shows Containers
docker images - shows Images
docker build -t app_name_to_be_created Dockerfile_name
docker run app_name_created

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