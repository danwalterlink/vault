---
id: u8jrckr6ky7grwd5ip2sfoa
title: Docker
desc: ''
updated: 1633199319598
created: 1633199319598
---
ctrl+p, ctrl+q escapes the container without stopping it!

et started with containers

This guide assumes you have a working installation of Docker. To check your Docker install, run the following command:

## Check that you have a working install

$ docker info
If you get docker: command not found or something like /var/lib/docker/repositories: permission deniedyou may have an incomplete Docker installation or insufficient privileges to access Docker on your machine. Please
Additionally, depending on your Docker system configuration, you may be required to preface each dockercommand with sudo. To avoid having to use sudo with the docker command, your system administrator can create a Unix group called docker and add users to it.
For more information about installing Docker or sudo configuration, refer to the installation instructions for your operating system.
Download a pre-built image

## Download an ubuntu image

$ docker pull ubuntu
This will find the ubuntu image by name on Docker Hub and download it from Docker Hub to a local image cache.
Note: When the image has successfully downloaded, you will see a 12 character hash 539c0211cd76: Download complete which is the short form of the image ID. These short image IDs are the first 12 characters of the full image ID - which can be found using docker inspect or docker images --no-trunc=true
Note: if you are using a remote Docker daemon, such as Boot2Docker, then do not type the sudo before the docka111er commands shown in the documentation’s examples.
Running an interactive shell

# Run an interactive shell in the ubuntu image,

# allocate a tty, attach stdin and stdout

# To detach the tty without exiting the shell,

# use the escape sequence Ctrl-p + Ctrl-q

# note: This will continue to exist in a stopped state once exited (see "docker ps -a")

$ docker run -i -t ubuntu /bin/bash
Bind Docker to another host/port or a Unix socket

Warning: Changing the default docker daemon binding to a TCP port or Unix docker user group will increase your security risks by allowing non-root users to gain root access on the host. Make sure you control access to docker. If you are binding to a TCP port, anyone with access to that port has full Docker access; so it is not advisable on an open network.
With -H it is possible to make the Docker daemon to listen on a specific IP and port. By default, it will listen on unix:///var/run/docker.sock to allow only local connections by the root user. You could set it to 0.0.0.0:2375 or a specific host IP to give access to everybody, but that is not recommended because then it is trivial for someone to gain root access to the host where the daemon is running.
Similarly, the Docker client can use -H to connect to a custom port.
\-H accepts host and port assignment in the following format:
tcp://[host][:port]`or`unix://path
For example:

- tcp://host:2375 -> TCP connection on host:2375
- unix://path/to/socket -> Unix socket located at path/to/socket
  \-H, when empty, will default to the same value as when no -H was passed in.
  \-H also accepts short form for TCP bindings:
  host[:port]`or`:port
  Run Docker in daemon mode:
  $ sudo <path to>/docker -H 0.0.0.0:5555 -d &
  Download an ubuntu image:
  $ docker -H :5555 pull ubuntu
  You can use multiple -H, for example, if you want to listen on both TCP and a Unix socket

# Run docker in daemon mode

$ sudo <path to>/docker -H tcp://127.0.0.1:2375 -H unix:///var/run/docker.sock -d &

# Download an ubuntu image, use default Unix socket

$ docker pull ubuntu

# OR use the TCP port

$ docker -H tcp://127.0.0.1:2375 pull ubuntu
Starting a long-running worker process

# Start a very useful long-running process

$ JOB=$(docker run -d ubuntu /bin/sh -c "while true; do echo Hello world; sleep 1; done")

# Collect the output of the job so far

$ docker logs $JOB

# Kill the job

$ docker kill $JOB
Listing containers

$ docker ps # Lists only running containers
$ docker ps -a # Lists all containers
Controlling containers

# Start a new container

$ JOB=$(docker run -d ubuntu /bin/sh -c "while true; do echo Hello world; sleep 1; done")

# Stop the container

$ docker stop $JOB

# Start the container

$ docker start $JOB

# Restart the container

$ docker restart $JOB

# SIGKILL a container

$ docker kill $JOB

# Remove a container

$ docker stop $JOB # Container must be stopped to remove it
$ docker rm $JOB
Bind a service on a TCP port

# Bind port 4444 of this container, and tell netcat to listen on it

$ JOB=$(docker run -d -p 4444 ubuntu:12.10 /bin/nc -l 4444)

# Which public port is NATed to my container?

$ PORT=$(docker port $JOB 4444 | awk -F: '{ print $2 }')

# Connect to the public port

$ echo hello world | nc 127.0.0.1 $PORT

# Verify that the network connection worked

$ echo "Daemon received: $(docker logs $JOB)"
Committing (saving) a container state

Save your containers state to an image, so the state can be re-used.
When you commit your container only the differences between the image the container was created from and the current state of the container will be stored (as a diff). See which images you already have using thedocker images command.

# Commit your container to a new named image

$ docker commit &lt;container_id> &lt;some_name>

# List your images

$ docker images
You now have an image state from which you can create new instances

