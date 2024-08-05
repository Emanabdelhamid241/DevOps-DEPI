# Jenkins Docker Client

This repository provides a Docker image with Jenkins and Docker CLI installed. It allows you to run Jenkins jobs that require Docker commands.

## Docker Hub Image

The Docker image is available on Docker Hub at: [emanabdelhamed241/jenkins-docker-client](https://hub.docker.com/r/emanabdelhamed241/jenkins-docker-client)

## How to Use

### Pull the Image

To pull the Docker image from Docker Hub, use the following command:

```sh
docker pull emanabdelhamed241/jenkins-docker-client
```

##Run the Container
####map to port 9090
```sh
docker run -it -p 9090:8080 -v /var/run/docker.sock:/var/run/docker.sock emanabdelhamed241/jenkins-docker-client
```

##Access Jenkins
```sh 
http://localhost:9090
```
