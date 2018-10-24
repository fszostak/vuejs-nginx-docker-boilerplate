# vuejs-nginx-docker-boilerplate running on docker container

### development environment

Running container

```
docker-compose build

docker-compose up
```

Web - Test URL: http://localhost:3080
API - Test URL: http://localhost:3080/api/tabledata

API Mockup URL: http://localhost:3000


### testing production build

Build container for production environment
```
docker build -t vue-nud web/.
```

Running container for testing
```
docker run -p"80:80" vue-nud
```

Test URL: http://localhost


