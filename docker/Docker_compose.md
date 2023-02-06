## Docker composer
```javascript
docker run container_name/app_name

docker run mongodb

docker run redis:alpine

docker run ansible

```

user docker composer run complex applications

docker-compose.yml
```yml
services:
  web:
    image: "contaimer_name/app"
  database: 
    image: "mongodb"
  messaging:
    image: "redis:alpine"
  orchestration:
    image: "ansible"
```

```bash
docker-compose up
```


- docker run multiple applications
```cmd
docker run -d --name=redis redis

docker run -d --name=db postgres:9.4 result-app

docker run -d --name=vote -p 5000:80 voting-app

docker run -d --name=result -p 5001:80

docker run -d --name=worker worker
```

- docker run --links
link applications


```cmd
docker run -d --name=redis redis

docker run -d --name=db postgres:9.4 --link db:db result-app

docker run -d --name=vote -p 5000:80 --link redis:redis voting-app

docker run -d --name=result -p 5001:80

docker run -d --name=worker --link db:db --link redis:redis worker
```

- docker compose
```yml
redis: 
  image: redis
db: 
  image: postgres: 9.4
vote:
  image: voting-app
  ports:
    - 5000:80
  links:
    - redis

result: 
  image: result-app
  ports: 
    - 5001:80
  links:
    - db

worker: 
  image: worker
  links:
    - redis
    - db
```

- run compose file
```cmd
docker-conpose up
```

### Docker compose - build
```yml
redis: 
  image: redis
db: 
  image: postgres: 9.4
vote:
  build: ./vote
  ports:
    - 5000:80
  links:
    - redis

result: 
  build: ./result
  ports: 
    - 5001:80
  links:
    - db

worker: 
  image: worker
  links:
    - redis
    - db
```


### Docker compose -version
- version 1
```yml
redis: 
  image: redis
db: 
  image: postgres: 9.4
vote:
  build: ./vote
  ports:
    - 5000:80
  links:
    - redis
```

- version 2  
```yml
version: 2
services: 
  redis: 
    image: redis

    networks:
      - back-end
  db: 
    image: postgres: 9.4
    network: 
      - backend-end
  vote:
    build: ./vote
    network: 
      - front-end
      - back-end

  result: 
    image: result
    network: 
      - front-end 
      - back-end

networks: 
  front-end: 
  back-end: 
```

- version 3
```yml
version: 3
services: 
  redis: 
    image: redis
  db: 
    image: postgres: 9.4
  vote:
    build: ./vote
    ports:
      - 5000:80
```




