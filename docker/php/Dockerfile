FROM tonacastelan/docker-php:latest

ARG USER_ID
ARG GROUP_ID

RUN useradd -u 1000 -ms /bin/bash -g www-data www

COPY docker/php/php.ini /usr/local/etc/php/conf.d/overrides.ini
COPY . .

USER www

WORKDIR /application

CMD ["php-fpm"]