## Run - attach and detach
* docker run image-name/app-name

* docker run -d image-name/app-name

* docker attach threadidcode


## Run tag

* docker run redis

* docker run redis:4.0  (--this is a tag)
run redis version 4.0

## run stdin
* docker run -i image-name/app-name


## run -port mapping
* docker run -p 80:5000 image/app
* docker run -p 8000:5000 image/app
* docker run -p 80001:5000 image/app

run multiple docker container and mapping to different docker host port

## docker -valume mapping 
* docker run -v /opt/datadir:/var/lib/mysql mysql


## inspect container

* docker inspect container-name

## container log

* docker logs container-name










