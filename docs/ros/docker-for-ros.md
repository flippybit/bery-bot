# Docker for ROS

## cheat sheet of docker commands

### Docker Container Management Commands

### This section features the essential commands related to the lifecycle of Docker containers. Learn how to create, manage, and remove containers from your Docker system using the below commands.

See the containers currently running on the system:
docker ps

See all the containers, both running and non-running:
docker ps -a

Create a container (without starting it):
docker create [image]

Create an interactive container with pseudo-TTY:
docker create -it [image]

Rename an existing container:
docker rename [container] [new-name]

Delete a container (if it is not running)
docker rm [container]

Forcefully remove a container, even if it is running:
docker rm -f [container]

View logs for a running container:
docker logs [container]

Retrieve logs created before a specific point in time
docker logs -f --until=[interval] [container]



View real-time events for a container:
docker events [container]

Update the configuration of one or more containers:
docker update [container]

View port mapping for a container:
docker port [container]

Show running processes in a container:
docker top [container]

View live resource usage statistics for a container
docker stats [container]

Show changes to files or directories on the filesystem:
docker diff [container]

Copy a local file to a directory in a container:
docker cp [file-path] CONTAINER:[path]