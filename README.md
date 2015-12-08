# docker-egeya
Dockerized Egeya blogging engine

```docker-compose up ```
and you up and running with PHP-FPM + NGINX + Egeya in separate data container


Continue setup with following credentials:

MySQL host: db
MySQL user: egeya
MySQL password: nexus

Point your browser to Nginx container ip:port, set your password on first install page and go!

Egeya app volume is located in /egeya folder of data container
