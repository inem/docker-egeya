FROM php:5.6-fpm
RUN apt-get -qqy update && apt-get -qqy install libpng12-dev libjpeg-dev
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr
RUN docker-php-ext-install gd mbstring mysql zip
COPY php-fpm.conf /etc/php5/fpm/php-fpm.conf
COPY www-pool.conf /etc/php5/fpm/pool.d/www.conf
CMD ["/usr/local/sbin/php-fpm", "-y", "/etc/php5/fpm/php-fpm.conf"]
EXPOSE 9001
