## Creating a docker image

- To create a docker image, create a file names 'Dockerfile'(case sensitive)
- select the required image from base_image : select the base image from https://hub.docker.com/explore

## Deploying flask application in docker


Docker Image --> install python3, install pip3, copy source code, install python modules, expose port, make container executable

make a new docker image

use python image


run docker image : docker build -t flaskapp:latest

## Docker file

1. Create a file named Dockerfile
2.  #RUN gets executed while building the image and CMD gets executed after the image gets created.

    docker build /location
    docker build -t myimage1:tag #-t can be used for adding a name and tag

Docker image : blueprint of your container
Images are constructed in layers
base layer(ubuntu)
software files ....

3. docker run -it -d -p 5000:5000 flaskapp
it : interactive
-d : no idea
-p : open port(docker port: flask port)

4. remove an imgae
docker rmi imageID

5. stop a container
docker stop containerID

6. list all the containers
docker ps



build image to create the container
container is a running instance of a docker image
------------------------------------------------------------------------
###VM vs container
VM has a complete OS on it.
hardware is virtualized using a software called hypervisor.
It uses the system from the host server.

Container virtualizes the operating system. There is no hypervisor and no virtual machines.
It can boot-up instantly.

pull a dockerfile from docker hub
- docker pull python
