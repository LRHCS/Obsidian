# Docker overview

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

**Responsive deployment and scaling**

Docker’s container-based platform allows for highly portable workloads. Docker containers can run on a developer’s local laptop, on physical or virtual machines in a data center, on cloud providers, or in a mixture of environments.

Docker’s portability and lightweight nature also make it easy to dynamically manage workloads, scaling up or tearing down applications and services as business needs dictate, in near real time.

**Running more workloads on the same hardware**

Docker is lightweight and fast. It provides a viable, cost-effective alternative to hypervisor-based virtual machines, so you can use more of your compute capacity to achieve your business goals. Docker is perfect for high density environments and for small and medium deployments where you need to do more with fewer resources.

# Container
-   is a runnable instance of an image. You can create, start, stop, move, or delete a container using the DockerAPI or CLI.
-   can be run on local machines, virtual machines or deployed to the cloud.
-   is portable (can be run on any OS)
-   Containers are isolated from each other and run their own software, binaries, and configurations.
- 
## [What is a container image?](https://docs.docker.com/get-started/#what-is-a-container-image)

When running a container, it uses an isolated filesystem. This custom filesystem is provided by a **container image**. Since the image contains the container’s filesystem, it must contain everything needed to run an application - all dependencies, configuration, scripts, binaries, etc. The image also contains other configuration for the container, such as environment variables, a default command to run, and other metadata.

We’ll dive deeper into images later on, covering topics such as layering, best practices, and more.

# Share the Container with the others
## Create a repo[](https://docs.docker.com/get-started/04_sharing_app/#create-a-repo)

To push an image, we first need to create a repository on Docker Hub.

1.  [Sign up](https://www.docker.com/pricing?utm_source=docker&utm_medium=webreferral&utm_campaign=docs_driven_upgrade) or Sign in to [Docker Hub](https://hub.docker.com/).
    
2.  Click the **Create Repository** button.
    
3.  For the repo name, use `getting-started`. Make sure the Visibility is `Public`.
## Push the image[](https://docs.docker.com/get-started/04_sharing_app/#push-the-image)

1.  In the command line, try running the push command you see on Docker Hub. Note that your command will be using your namespace, not “docker”.
    
    ```
     $ docker push docker/getting-started
     The push refers to repository [docker.io/docker/getting-started]
     An image does not exist locally with the tag: docker/getting-started
    ```
    
    Why did it fail? The push command was looking for an image named docker/getting-started, but didn’t find one. If you run `docker image ls`, you won’t see one either.
    
    To fix this, we need to “tag” our existing image we’ve built to give it another name.
    
2.  Login to the Docker Hub using the command `docker login -u YOUR-USER-NAME`.
    
3.  Use the `docker tag` command to give the `getting-started` image a new name. Be sure to swap out `YOUR-USER-NAME` with your Docker ID.
    
    ```
     $ docker tag getting-started YOUR-USER-NAME/getting-started
    ```
    
4.  Now try your push command again. If you’re copying the value from Docker Hub, you can drop the `tagname` portion, as we didn’t add a tag to the image name. If you don’t specify a tag, Docker will use a tag called `latest`.

--- 
We use Dockerfile to create an image. Image is like a template, with a image we can create multiple container
# Dockerfile
``FROM python:3.8-slim-buster``
python is a image, after the : is the name of the patch

``WORKDIR /app ``
working directory

``COPY . .``
the first . means the files of the current directory, the second . means the path in the docker image

``RUN pip3 install -r requirments.txt``
here you can use all of the shell command

``CMD ["python3", "app.py"]``


``docker build -t my-finance .``
-t is the name . tells docker it should find the DOCKERFILE in the current directory

``docker run -p 80:5000 -d my-finance``
we connect the port 80 in the image with the port 5000 in our local machine

-d means detache, it runs the image at the background

# docker-compose.yml

```docker
version : "3"

services :
	web:
		build: .
		ports: 80:5000
	db:
		image : "mysql"
		envirement:
			// name of the database
			MYSQL-DATABASE: finance-db
			// password
			MYSQL-ROOTPASSWORD: SECRET
		volumes:
			- my-finance-data:/var/lib/mysql
volumes :
	my-finance-data:
```

docker compose up -d