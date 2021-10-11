# Docker

Docker is an open platform for developing, shipping, and running the applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.  

You can manage your infrastructure in the same way you manage your applications by taking advantages of docker methodlogies for shipping, testing and deploying you can significantly reduce the delay between writing code and running it in production.

## What is a container?  
A container is simply another process on your machine that has been isolated from all other processes on the host machine. That isolation leverages kernel namespaces and cgroups, features that have been in Linux for a long time. Docker has worked to make these capabilities approachable and easy to use.

How Docker is Working:

namespacing: Isolate the resources per process.

control groups or cgroups: Limit the amount used per process.

Docker technology uses the Linux kernel and features of the kernel, like Cgroups and namespaces, to segregate processes so that they can run independently. 

This independence is the intention of containers the ability to run multiple processes and application separately from one to another to make better use of your infrastructure.

Cgroups allow you to allocate resources from the underlying host machine — such as CPU time, system memory, network bandwidth, or combinations of these resources — among user-defined groups of tasks(processes) running on a system.


## Docker daemon:
	
Docker Daemon is a server which interacts with the operating system and performs all kind of services.

Docker Daemon listens and receive REST API request and performs the operation after communicated with docker components and services.

Docker daemon creating and managing the docker images, containers, networks and volumes.

## Docker Volumes:
	
Docker Volumes are the best way to store the persistent data that your application consume and create. 
	

## Docker Registry:
	
A Docker Registry is the remote location where Docker Images are stored. You push images to a registry and pull images from a registry. You can host your own registry or use a provider’s registry.


## Docker HUB:

Docker Hub is the largest registry of Docker images. It’s also the default registry. You can find images and store your own images on Docker Hub for free.

## Docker Repository: 
	
A Docker Repository is a collection of Docker images with the same name and different tags. The tag is the identifier for the image.


## Docker Engine:

Docker Engine or Docker is the base engine installed on your host machine to build and run containers using Docker components and services.
	 

## Docker Machine:

Docker Machine is a tool that lets you install Docker Engine on virtual hosts.

Docker Machine enables you to provision multiple remote Docker hosts on various flavors of Linux.

Docker Machine is a tool for provisioning and managing your Dockerized hosts (hosts with Docker Engine on them)

Docker Machine has its own command line client docker-machine and the Docker Engine client, docker. You can use Machine to install Docker Engine on one or more virtual systems. These virtual systems can be local (as when you use Machine to install and run Docker Engine in VirtualBox on Mac or Windows) or remote (as when you use Machine to provision Dockerized hosts on cloud providers). The Dockerized hosts themselves can be thought of, and are sometimes referred to as, managed “machines”.

## Docker Image:

A Docker Image is a file of instructions which is used to create Containers.

	
## Docker File

A DockerFile is a text document that contains all the commands a user could call on the command line to assemble an image.
Docker can build images automatically by reading the instructions from a Dockerfile.  
The docker build command builds an image from a Dockerfile and a context. The build’s context is the set of files at a specified location PATH or URL.

## Docker Compose

Docker Compose is used for running multiple containers as a single service. Here, containers run in isolation but can interact with each other
All Docker Compose files are YAML files. In Docker Compose, a user can start all the services (containers) using a single command

For example:

If you have an application which requires NGINX server and Redis database, you can create a Docker Compose file which can run both the containers as a service without the need to start each one separately
	
## Docker Compose Commands:

All the docker compose command
# docker-compose 

Run the docker image command
# docker-compose up

Rebuild the docker compose
#docker-compose up --build

	
	
Management Commands:
  builder     Manage builds
  config      Manage Docker configs
  container   Manage containers
  engine      Manage the docker engine
  image       Manage images
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes


## Docker Installation on CentOS 7.x

Remove if there are any previous version of docker packages
	#yum remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine
	
Setup docker repository

	#yum install -y yum-utils device-mapper-persistent-data lvm2
	#yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

Install docker community edition

	#yum install -y docker-ce docker-ce-cli containerd.io

  
## Docker Swarm

## Computer Cluster:

A computer cluster is a single logical unit consisting of multiple computers that are linked through a LAN. The networked computers essentially act as a single, much more powerful machine. A computer cluster provides much faster processing speed, larger storage capacity, better data integrity, superior reliability and wider availability of resources. 	
	
## Docker Swarm:
	
	Container orchestration tool.

Basics:
		Platform-the software that makes Docker containers possible
		Engine-client-server app (CE or Enterprise)
		Client-handles Docker CLI so you can communicate with the Daemon
		Daemon-Docker server that manages key things	
		Volumes-persistent data storage
		Registry-remote image storage
		Docker Hub-default and largest Docker Registry
		Repository-collection of Docker images, e.g. Alpine
	
Scaling:

		Networking-connect containers together
		Compose-time saver for multi-container apps
		Swarm-orchestrates container deployment
		Services-containers in production
		
docker swarm init --advertise-addr


To add a worker to this swarm, run the following command:

   docker swarm join --token SWMTKN-1-1k42ab37rrbz9fhjyfeu5cobh83cub4j94elot48slsapsurva-evsixoxk72f2b3s0tet77qt8l 192.168.118.128:2377
  
  
firewall-cmd --permanent --add-port=100/tcp
firewall-cmd --reload

To add a manager to this swarm, run 'docker swarm join-token manager' and follow the instructions.
