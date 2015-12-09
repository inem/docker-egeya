FROM php:5.6-apache

RUN a2enmod rewrite
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev \
&& rm -rf /var/lib/apt/lists/* \
&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
&& docker-php-ext-install gd mbstring mysqli

RUN mkdir /egeya
WORKDIR /egeya

RUN chown -R www-data:www-data /egeya
