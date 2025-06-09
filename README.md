Commands

docker ps - shows Containers
docker images - shows Images
docker build -t app_name_to_be_created Dockerfile_name
docker run app_name_created

Steps to Stop/Delete container
docker ps -a - shows all current stopped / exited / running
docker rmi -f containerid - to remove container
docker stop imageid
