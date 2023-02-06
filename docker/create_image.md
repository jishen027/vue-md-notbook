### How to create my own image

1. create a docker file

``` docker 
FROM Ubuntu 

RUN apt-get updates
RUN apt-get install python

RUN pip install flask
RUN pip install flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run
```


2. build image 
```
docker build Dockerfile -t container/app
```

3. make it avaliable
```
docker push container/app
```


### CMD

``` javascript
docker run ubuntu [COMMNAD]

docker run ubuntu sleep 5

docker ps
```

## write command in the docker file 

- docker file : ubuntu-sleeper
```
FROM Ubuntu

CMD sleep 5
```

```javascript
docker build ubuntu-sleeper .

docker run ubuntu-sleeper
```

## entry point and cmd 
```
FROM uBUNTU

ENTRYPOINT ["sleep"]

CMD ["5"]
```

```javascript
// overwrite the cmd in docker file
docker run ubuntu-sleeper 5
```

In this case, if only run `docker run ubuntu-sleeper`, it will sleep 5 second.




