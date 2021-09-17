FROM php:8.0-fpm

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

COPY ./php.ini /usr/local/etc/php/
COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN usermod -u 1000 www-data

WORKDIR /var/www
EXPOSE 9000