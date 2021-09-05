# Django REST Framework & Docker



***With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.***

> What’s the downside? 

**Complexity. Docker is a complex beast under the hood. However a little knowledge can take you a long way and that’s the goal of this guide!**

## Linux Containers

**Docker is really just Linux containers which are a type of virtualization.**

**Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.**


## Containers vs Virtual Environments

***Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.***

## Install Docker

> $ docker --version
> Docker version 19.03.5, build 633a0ea


**A baking analogy we can use here is as follows:**

- A Dockerfile is the recipe for a cake

- An image is a snapshot of the recipe at a given time

- A docker-compose.yml says how to make the cake

- And the container is the actual, baked cake


## Containers

Now that we have our Python image how do we run it? Well just as a Dockerfile is a list of image instructions there is also a docker-compose.yml file that is a list of container instructions.

To demonstrate a real-world image and container example we will now “Dockerize” a basic Django web app. You might not fully understand every step but you’ll see how Docker can work to run a web application completely on its own.

Note: If you’ve never used Django before, I’ve written several books on it which have the first few chapters available online for free. Check out Django for Beginners.

Ok, so let’s create a new Django project from scratch. I’ll assume you have Pipenv already installed. If not, see here for further instructions.

On the command line, go up a directory to our code folder and create a new one called djangoapp. Then we’ll use Pipenv to install Django and enter the virtual environment shell.


## Dockerized Django


We’ll now create a Dockerfile for our image which will completely replace our local dev environment, so this will have Python 3 and Django. Then we’ll add a docker-compose.yml for the container instructions. Make each file via the command line.

> $ touch Dockerfile
> $ touch docker-compose.yml



## Conclusion


***That last example with Django probably felt a bit too fast to fully understand. And that’s ok. I wanted to show a working example without getting too bogged down in the complexity of images and containers.***

> **The important takeaways from this tutorial are this:**


- Docker is a way to run Linux containers

- Containers are a lightweight alternative to Virtual Machines

- Dockerfile is a list of instructions for creating an image

- Images are made up of one or more layers

- Containers are a running instance of an image

- docker-compose.yml controls how to run the container

- Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more complex with databases (which we didn’t cover here).

