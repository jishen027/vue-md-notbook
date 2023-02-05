## Docker registry

```cmd
docker run nginx
```

image: docker.io/nginx/nginx

      Registry /User /Image

- Deploy private Registry

```cmd
docker run -d -p 5000:5000 --name  registry registry:2

docker image tag my-image localhost:5000/my-image

docker push localhost:5000/my-image

docker pull localhost:5000/my-image

docker pull 192.168.56.100:5000/my-image
```

