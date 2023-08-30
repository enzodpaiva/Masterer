![GitHub repo size](https://img.shields.io/github/repo-size/enzodpaiva/Masterer)
# Masterer 

FACOM Project - This project was submitted as a assignment for two courses, and their members are:

- Web Programming Project Team Members: Enzo Paiva, Arthur Ramires, Gabriel Cardoso, and Nicole Fernanda.

- Distributed Computing Project Team Members: Enzo Paiva, Arthur Ramires, Milena Alegre, and Vitoria Rocha.

## Made with:
- PHP 7.4 (FrameWork Laravel 8.83)
- Mysql 8
- HTML
- CSS (Bootstrap)
- JavaScript
- Docker

### Starting the Project
This project is set up in a Docker instance to facilitate its usability. To run the project locally using Docker.

### Installing Docker
You can install Docker through these links, according to your operating system:

##### windows
```
https://docs.docker.com/desktop/windows/install/
```

##### linux
```
https://docs.docker.com/engine/install/ubuntu/
```

Execute the commands below in the terminal within the project folder:

Initialize the containers (This also downloads them the first time it's executed).
```sh
docker-compose up -d
```

list containers
```sh
docker ps -a
```

Enter the application's containers.
```sh
docker exec -it {nome container} sh
```

To start the application - inside the "Masterer-app" container, run:
```sh
php artisan serve
```

### Local database configuration.

```
ServerHost: localhost
Port: 33007
Username: root
Password: root
```

##### In case of connection issues, please verify if the following drivers are enabled:

```
rewriteBatchedStatements: true
useSSL: false
```

#### Link to the containers used in this project.
##### Nginx
```
https://hub.docker.com/_/nginx
```
###### Mysql
```
https://hub.docker.com/_/mysql
```
###### Php
```
https://hub.docker.com/_/php
```

##### Redis
```
https://hub.docker.com/_/redis
```

### What are Distributed Systems:

A distributed system is a collection of computer programs that use computational resources across different central points of computing to achieve a common and shared goal. Also known as distributed computing or distributed databases, it relies on different central points to communicate and synchronize in a common network. These central points often represent different physical hardware devices but can also represent different software processes or other encapsulated recursive systems. Distributed systems aim to remove bottlenecks or single points of failure from a system.

### Distributed Computing Systems have the following characteristics:

- Resource Sharing - a distributed system can share hardware, software, or data.
- Concurrent Processing - multiple machines can process the same function simultaneously.
- Scalability - computing and processing capacity can evolve as needed when extended to additional machines.
- Error Detection - faults can be more easily detected.
- Transparency - a central point can access and communicate with other central points in the system.

### Difference between a Centralized and Distributed System:

A centralized computing system is where all computing is done by a single computer at a single location. The main difference between centralized and distributed systems is the communication pattern among the central points of the system. The state of a centralized system is contained in a central point that clients access individually. All central points in a centralized system access the central point, which can lead to network congestion and slowness. A centralized system has a single point of failure, while a distributed system does not have a single point of failure.

### Docker:

Docker is software that provides virtual containers that package your application and its dependencies into a container. From this moment, the container becomes portable, and you can use it on other machines that have Docker installed, regardless of the operating system. (fault tolerance) This way, your application always works the same way everywhere. Docker isolates the application through a virtual container as if it were a host, each container works separately, and all dependencies are allocated separately in the corresponding container, making them completely isolated processes. For example, in our project, we have separate containers for the application and the database.

### Explaining Each Technology Used:

- #### NGINX:
  - It is a web server, a program that runs and serves web requests. The software's architecture is asynchronous and event-driven, allowing it to process many requests at the same time. NGINX is also highly scalable, meaning that its service grows with increasing user traffic.

- #### MySQL:
  - MySQL is a database management system that uses the SQL language as its interface.

- #### PHP:
  - A programming language, used for developing server-side applications (backend).

- #### Redis:
  - Redis is an in-memory data structure store, commonly used as a database, cache, and message broker. Redis allows data to be stored in memory, organized into keys and values.

### Explaining Concepts Used in the Project:

- #### Client:
  - Allows users to interact with Docker and access containers via the command line or Remote API.

- #### Host:
  - Provides a complete environment for running applications, consisting of the Daemon, images, containers, network, and volumes. The Daemon is responsible for all actions related to containers and receives commands through the Client.

- #### Registry:
  - These are services that provide locations where images will be stored and downloaded from. In other words, the Registry contains the Docker repositories that host the images, such as Docker Hub.

- #### Virtualization:
  - Docker provides container-based virtualization. This virtualization model operates at the operating system level. The key difference from a VM is that a Docker container shares the Kernel with the host's operating system. This increases performance and reduces memory consumption for the container.

- #### Naming:
  - Names play an important role in all computer systems. They are used to share resources and identify entities. To resolve names, a Naming System is required. In a distributed system, the implementation of the naming system is often distributed across several machines. When you are working with containers, you take entities (application, database, etc.) and place them inside the container. To ensure that the system's communication works and is understood, we use naming systems. This naming occurs in the docker-compose file.

### Project Structure and Docker Configuration:

- The chosen code versioning tool is Github, as we are more familiar with the system.
- The project was originally developed for the Web Programming course and was reused for this course, adding functionality for Distributed Systems.
- The system is composed of containers for Php, Mysql, Redis, and Nginx.
- They all communicate through the same network and have their Dockerfiles, orchestrated by a docker-compose.yaml.
- The project's folder structure was designed to meet the requirements of the MVC pattern, which was also chosen for its practicality and ease of use.
