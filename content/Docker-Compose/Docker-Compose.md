## What is Docker-compose and why do you need it?

When using Docker extensively, the management of several different containers quickly becomes cumbersome.

Docker Compose is a tool that helps us overcome this problem and easily handle multiple containers at once.

Docker Compose works by applying many rules declared within a single **docker-compose.yml** configuration file. 

These YAML rules, both human-readable and machine-optimized, provide us an effective way to snapshot the whole project from ten-thousand feet in a few lines.

Almost every rule replaces a specific Docker command so that in the end we just need to run: *docker-compose up*

We can get dozens of configurations applied by Compose under the hood.

The Docker-compose file should have at least one service, and optionally volumes and networks.

* Services
   
  Services refer to the configuration of the application. They specify different components that are part of the application namely: frontend, backend, DB

* Volumes and Networks

  Volumes, on the other hand, are physical areas of disk space shared between the host and a container, or even between containers. In other words, a volume is a shared directory in the host, visible from some or all containers.

    Similarly, networks define the communication rules between containers, and between a container and the host. Common network zones will make containers' services discoverable by each other, while private zones will segregate them in virtual sandboxes.


Here are few links which can be referred for examples and further details:

* [Source 1](https://www.baeldung.com/docker-compose)

* [Source 2](https://takacsmark.com/docker-compose-tutorial-beginners-by-example-basics/)

