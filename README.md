## What is it

Docker Compose UI is a web interface for Docker Compose.

The aim of this project is to provide a minimal HTTP API on top of Docker Compose while maintaining full interoperability with Docker Compose CLI.

## Compose file format compatibility matrix

| Compose file format  | Docker Engine |
| ------------- | ------------- |
| 3.8 | 19.03.0+ |
| 3.7 | 18.06.0+ |
| 3.6 | 18.02.0+ |
| 3.3 - 3.5 | 17.06.0+ |
| 3.0 – 3.2| 1.13.0+ |
| 2.3	| 17.06.0+ |
| 2.2	| 1.13.0+ |
| 2.1	| 1.12.0+ |
| 2.0	| 1.10.0+ |
| 1.0	| 1.9.1+ |

## Getting started

Run the following command in terminal:

`dockebuild --tag matt:1.0 .`

then 

`dockerun --name docker-compose-ui -p 5000:5000 -w /opt/docker-compose-projects/ -v /var/run/docker.sock:/var/run/docker.sock matt:1.0`

Then open your browser to `http://localhost:5000`

If you already have docker-compose installed, you can run `docker-compose up` and then open your browser to `http://localhost:8080`.


### Add your own docker-compose projects
You can download my example projects into */home/user/docker-compose-ui/demo-projects/* from https://github.com/francescou/docker-compose-ui/tree/master/demo-projects


### Note about volumes
Since you're running docker-compose inside a container you must pay attention to volumes mounted with relative paths, see [Issue #6](https://github.com/francescou/docker-compose-ui/issues/6)