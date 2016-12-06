# Docker-elk

This is a custom image for UI I'm using for my docker-elk project. 
We are not actually installing Kibana but we are installing Nginx on top of debian:wheezy image and exposing appropriate ports and setting config. We have included code for our scatterplot in custompages folder to be deployed to the root of the nginx web server.

Even though this image is built to ideally run in conjunction with other two images but you may edit and use it by updating config and creating a separate image.

## Getting Started

There are two ways to use this image.
1. Simply build the image using given Dockerfile and config file using docker build command as follows:
Clone the repository to your machine and cd into it.

```
docker build -t <name of your choice> .
```
2. For this to work, download docker-elasticsearch, docker-logstash and docker-elk-ui images to your machine inside a folder let's say docker-elk. Now cd to that folder and this image (and other) will be built from scratch automatically when you fire coomand as below :

```
docker-compose up --build
```

### Prerequisites

What things you need to install the software and how to install them

You need to install docker and docker-compose (optional if you plan to run only UI).
Please use latest versions for both as some of the commands may not work in older versions.


## Running the tests

To test this, you need to have ES running at localhost:9200 running either in docker or on host.
In any case verify that ES url specified in config is reachable from this host as it will be called from js ajax call.

If you have spun up all (E,L,K) containers, you can open below URL and check if you see any graphs: 

http://127.0.0.1/responseplot.html    or  http://127.0.0.1/urlplot.html 



## Deployment

You can deploy this on any cloud env that supports docker containers like Amazon EC2 etc.




## Authors

* **Akshay Mishra** 
