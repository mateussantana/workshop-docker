# Introdução ao docker

![docker-logo](https://www.docker.com/sites/default/files/social/docker_facebook_share.png)


## Installation
[https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/link)


## Hello World
```bash
docker run hello-world
```

## Python example
```bash
docker run python:3 python --version

docker run -it -v $PWD/python:/myapp -w /myapp python:3 python python.py
```

## Nginx web server
```bash
docker run -p 80:80 nginx
# /usr/share/nginx/html

docker exec -it <container> bash

docker run -p 80:80 -v $PWD/nginx:/usr/share/nginx/html nginx

docker exec -it <container> bash
```

## Laravel application example
```bash
# createing a laravel project from composer
docker run --rm -v $PWD/laravel:/app composer create-project laravel/laravel .

docker run --rm -v $PWD/laravel:/app -w /app php:8.0 php artisan -V

# running laravel: will fail
docker run --rm -it -p 80:8000 -v $PWD/laravel:/app -w /app php:8.0 php artisan serve

# running laravel: successfuly
docker run --rm -it -p 80:8000 -v $PWD/laravel:/app -w /app php:8.0 php artisan serve --host=0.0.0.0

# sudo chown mateus laravel -R
```

## Angular example
```bash

```

## Alias
```bash

```
