FROM php:fpm
MAINTAINER yansongda <me@yansongda.cn>

COPY sources.list /etc/apt/sources.list
COPY php.ini /usr/local/etc/php/conf.d/

WORKDIR /www

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libbz2-dev libmcrypt-dev libmemcached-dev libssh-dev \
  && pecl install -o -f mongodb swoole redis memcached \
  && docker-php-ext-install bcmath bz2 gd iconv mcrypt mysqli pdo pdo_mysql zip \
  && docker-php-ext-enable redis memcached mongodb swoole \
  && rm -rf /var/lib/apt/lists/* \
  && rm -rf /tmp/pear

ENTRYPOINT ["docker-php-entrypoint"]

EXPOSE 9000

CMD ["php-fpm"]