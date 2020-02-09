# Docker https://www.docker.com/
# https://docs.docker.com/
# Hyper -V Container for creating linux containers

1) Carves up a computer into a sealed containers that run your code.
2) Gets the code to and from your computer
3) It builds a containers for you
4) It is social platform to find and share containers, which are different from virtual machines.


# Container
1) It is self contained sealed unit of software
2) Contains everyting required to run the code.
3) Includes batteries and OS
4) It includes:
   a) Codes 
   b) Configs
   c) Processes
   d) Networking
   e) Dependencies

# Docker Container
1) A client program
2) A server program that manages a linux system.
3) A program that builds container from code.
4) A service that distributes containers
5) A company that makes containers

1) Command : docker run hello-world
 Above output indicates that the docker is working fine.

Output :

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
1b930d010525: Pull complete
Digest: sha256:9572f7cdcee8591948c2963463447a53466950b3fc15a247fcad1917ca215a2f
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

 ----------------------------------------------------------------

2) Command: docker info

The above command gives the server side info about the docker

-----------------------------------------------------------------
# Docker Flow

1) Images

Command = docker images/docker image ls

Output:

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              fce289e99eb9        13 months ago       1.84kBREPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

# Running Comtainer
Command: docker run -ti <REPOSITORY_NAME>:<TAG>
eg: docker run -ti hello-world:latest bash

ti -- terminal Interactive

Command to list the Container:
docker container ls / docker ps 


Command for a stopped Conatainer:
docker ps -l --format=$FORMAT

Output:
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                   PORTS               NAMES
d90360cc6dd4        hello-world         "/hello"            2 hours ago         Exited (0) 2 hours ago                       great_wescoff

Commiting and creating a new image -->

1) docker commit e758f9fd8b12  -- e758f9fd8b12/Container id --OUTPUT:sha256:a16eeff5f29036c1c6e320258105087946e9e0716edb27afc5d5c521e59208e1
2) docker tag sha256:a16eeff5f29036c1c6e320258105087946e9e0716edb27afc5d5c521e59208e1 my-image -- Renaming the image

Another Way
1) docker commit 9b2d94a18f04 my-immage2
2) docker-images


