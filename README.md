# Spark GraphFrames Hackathon
Spark graph processing training and hackathon 

## Build Docker images
This builds all images needed for the setup.
```
cd docker
./build.sh
```        

## Prepare environment
This script creates required directories, which are used by the setup.
```
./init_env.sh
```

## Start application
```
# this will start Docker compose application
# run from the project root

SHARED_DIR=`pwd`/shared-vol docker-compose -f docker/docker-compose.yml up
```

## Application URLs

- [JupyterLab](http://localhost:8888)
- [Spark master](http://localhost:8080/home)
- [Spark worker I](http://localhost:8081) 
- [Spark worker II](http://localhost:8082) 
- [Spark Application UI](http://localhost:4040)

## Cleanup Docker env
Removes all stopped containers and deletes images with intermediate layers.
```
cd docker
./cleanup.sh
```
