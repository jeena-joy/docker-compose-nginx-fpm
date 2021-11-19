### docker-compose-nginx-fpm
Hosting a website in nginx-phpfpm container

```sh
# tree .
.
├── docker-compose.yml
├── nginx.conf
└── website
    └── index.php

1 directory, 3 files
```




```sh
# docker-compose up -d
Creating network "compose_nginx" with the default driver
Creating nginx   ... done
Creating php-fpm ... done
```



```sh
# docker ps -a
CONTAINER ID   IMAGE                  COMMAND                  CREATED              STATUS              PORTS                                   NAMES
8ed5ccaf8e60   php:7.4.0-fpm-alpine   "docker-php-entrypoi…"   About a minute ago   Up About a minute   9000/tcp                                php-fpm
bf88ca168f86   nginx:1.20-alpine      "/docker-entrypoint.…"   2 minutes ago        Up 2 minutes        0.0.0.0:8080->80/tcp, :::8080->80/tcp   nginx
```
