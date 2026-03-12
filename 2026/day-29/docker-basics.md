# Introduction to docker...

What is Docker?<br>
What is a container and why do we need them? <br>
A container is a lightweight package that includes an application and all its dependencies (libraries, runtime, system tools).
Containers allow applications to run consistently across different environments such as a developer's laptop, testing server, or production cloud.
Before containers, developers often faced the problem:
"It works on my machine but not on the server."
Containers solve this problem by packaging the application with everything it needs to run.

Containers vs Virtual Machines — what's the real difference?
| Feature        | Containers    | Virtual Machines       |
| -------------- | ------------- | ---------------------- |
| OS             | Share host OS | Each VM has its own OS |
| Size           | Lightweight   | Heavy                  |
| Startup        | Seconds       | Minutes                |
| Resource usage | Low           | High                   |
| Performance    | Faster        | Slower                 |

Note : Virtual Machines virtualize hardware, while containers virtualize the operating system.

What is the Docker architecture? (daemon, client, images, containers, registry) <br>
Demon :-The Docker daemon (dockerd) is responsible for:
Managing containers
Managing images
Handling networks and volumes
Running containers<br>
client :- The Docker client is the command-line interface used by users.(eg. docker run, docker pull, docker build) this cmds communicate with docker.<br>
image :- A Docker image is a read-only template used to create containers.
(eg.nginx,ubuntu,mysql,redis)
Images are stored in Docker registries.<br>
containers :- A container is a running instance of an image.
eg.
Image → nginx
Container → running nginx web server.<br>
registry :- A Docker registry stores images.
The most common registry is Docker Hub, where users can download and share images.
<br>
Draw or describe the Docker architecture in your own words.
Developer
   │
   ▼
Docker Client (CLI)
   │
   ▼
Docker Daemon
   │
   ├── Containers
   ├── Images
   └── Networks/Volumes
   │
   ▼
Docker Registry (Docker Hub)<br>

## install docker
Output explanation:
Docker checks if the hello-world image exists locally.
If not, Docker pulls the image from Docker Hub.
Docker creates a container from the image.
The container runs a program that prints a confirmation message.
