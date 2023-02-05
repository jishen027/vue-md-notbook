## Environment Varialbes

- color = os.environ.get('APP_COLOR')
- export APP_COLOR=buld; python app.py

- docker run -e APP_COLOR=blue app-name
- docker run -e APP_COLOR=black app-name
- docker run -e APP_COLOR=red app-name

## inspect environment varialbe

- docker inspect container-name

## Docker commnad

- docker run nigix  
  start a container

- docker ps  
  list current running containers

- docker ps -a  
  list all containers

- docker stop container_name  
  stop a container

- docker rm container_name  
  remove a container

- docker images  
  list all images

- docker rmi image_name  
  remove a image (image should not running for a container)

- docker pull image  
  only pull the image, not runing

## Docker Append a commnad

- docker run ubuntu sleep 5  
  sleep is append command

- docker exec container_name cat /etc/hosts  
  append a command into a running container

## Run - attach and detach

- docker run -d container_name/app_name  
  will run container in background

- docker attach container_id(a043d)  
  will attach back the container

## Run -tag

- docker run redis:4.0   
  :4.0 is a version tag for redis

## Run STDIN
- docker run -i container_name/app_name

- docker run -it container_name/app_name

## Run PORT mapping
- docker run -p 80:5000 container_name/webapp

## RUN Volume mapping
- docker run -v /opt/datadir:/var/lib/mysql mysql 

## Container logs
- docker logs container_name


