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


