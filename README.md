# vuejs-nginx-docker-boilerplate running on docker container

### development environment

Running container

```
docker-compose build

docker-compose up
```

Web - Test URL: http://localhost:8080
API - Test URL: http://localhost:8080/api/tabledata


### testing staging build

Build container for production environment
```
docker build -t vuejs-nginx-boilerplate-staging -f web/Dockerfile.staging web/.
```

Running container for testing
```
docker run -p"8080:80" vuejs-nginx-boilerplate-staging
```

Test URL: http://localhost:8080


### testing production build

Build container for production environment
```
docker build -t vuejs-nginx-boilerplate-production web/.
```

Running container for testing
```
docker run -p"8080:80" razzle-boilerplate-production
```

Test URL: http://localhost:8080


### stopping containers

```
$ docker ps

CONTAINER ID        IMAGE               COMMAND                 CREATED             STATUS              PORTS                 
c95b19cf82b9        XXXXXXXX            XXXXXXXXXXXXXXXXXXXXXXX 16 seconds ago      Up 15 seconds       0.0.0.0:8080->80/tcp   

$ docker stop c95b19cf82b9
```


### clean up

```
$ docker rmi vuejs-nginx-boilerplate-staging vuejs-nginx-boilerplate-production
```

#### Learn more about Docker
[Docker and Kubernetes: The Complete Guide](https://www.udemy.com/share/100r9ABUMeeFtTRHQ=/)

#### Learn more about Vue JS
[Vue JS Essentials with Vuex and Vue Router](https://www.udemy.com/share/1007q8BUMeeFtTRHQ=/)
