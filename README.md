## What is it

Docker eCommerce platforms is a web interface that comes pre-packaged with localhost docker compose projects.

The aim of this project is to provide developers minimal effort to set up eCommerce platforms to test extensions or to get a feel of the platform.

## Getting started (development)

Run the following command in terminal:

`dockebuild --tag docker-ecps:1.0 .`

then

`docker run -d --name docker-ecps -p 5000:5000 -w /opt/docker-compose-projects/ -v /var/run/docker.sock:/var/run/docker.sock docker-ecps:1.0`

You can then connect to the UI at `http://localhost:5000`

## Getting started (normal)
WIP


### Add your own docker-compose projects
You add projects into demo-projects/* and rebuild the image for them to take affect.


### Note about volumes
Since you're running docker-compose inside a container you must pay attention to volumes mounted with relative paths, see [Issue #6](https://github.com/francescou/docker-compose-ui/issues/6)