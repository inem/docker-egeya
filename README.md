# docker-egeya
Dockerized [Egeya blogging engine ](http://blogengine.ru)

```docker-compose up ```
and you up and running with PHP-FPM + NGINX + Egeya in separate data container


Continue setup with following credentials:
```
MySQL host: db
MySQL user: egeya
MySQL password: nexus
```
Point your browser to Nginx container ip:port, set your password on first install page and go!

Egeya app volume is located in /egeya folder of data container

It's also adopted for use with nginx-proxy container. Use option in
docker-compose.yml with [nginx-proxy container](https://github.com/jwilder/nginx-proxy).
Read [this post](http://jasonwilder.com/blog/2014/03/25/automated-nginx-reverse-proxy-for-docker/).
```
...
  environment:
    - VURTUAL_HOST=myhost.com
...
```

```
nginx:
  image: jwilder/nginx-proxy
  ports:
    - "80:80"
  volumes:
    - /var/run/docker.sock:/tmp/docker.sock:ro
  restart: always
```
