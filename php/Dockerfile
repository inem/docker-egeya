FROM php:5.6-fpm
RUN apt-get -qqy update && apt-get -qqy install git libpng12-dev
RUN docker-php-ext-install mbstring mysql gd
COPY php-fpm.conf /etc/php5/fpm/php-fpm.conf
COPY www-pool.conf /etc/php5/fpm/pool.d/www.conf
CMD ["/usr/local/sbin/php-fpm", "-y", "/etc/php5/fpm/php-fpm.conf"]
EXPOSE 9001
