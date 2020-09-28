# Django REST Framework

Docker is really just Linux containers which are a type of virtualization.
in recent years Linux containers, also known as “containerization,” has become increasingly popular. For most applications, a virtual machine provides far more resources than are needed and a container is more than sufficient.

This, fundamentally, is what Docker is. A way to implement Linux containers!

Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

Install Docker (Links to an external site.)

$ docker-compose --version
docker-compose version 1.24.1, build 4667896b

To confirm Docker installed correctly we can run our first command docker run hello-world. This will download an official image and then run the container.

A good command to inspect Docker is docker info which we can run now. It will contain a lot of output but focus on the top lines which show we now have 1 container which is stopped and 1 image.

$ docker info
Containers: 1
 Running: 0
 Paused: 0
 Stopped: 1
Images: 1
Images and Containers Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.

When we ran hello-world we used an official Docker image. We did not have to create the image ourself. But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.

A baking analogy we can use here is as follows:

A Dockerfile is the recipe for a cake An image is a snapshot of the recipe at a given time A docker-compose.yml says how to make the cake And the container is the actual, baked cake There are a large number of official images available on Docker Hub for common software like different flavors of Linux, programming languages, and so on. For example, the Hello World image is there.

## **_references:_**

**_read_**

1. [Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

1. [basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

1. [hash table wiki](https://en.wikipedia.org/wiki/Hash_table)

**_vedio_**

1. [-what is a hash table? ](https://www.youtube.com/watch?v=MfhjkfocRR0)

## Done

[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)