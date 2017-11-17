# docker-compose-LNMP
Docker-compose with latest php-fpm,nginx,redis,memcached,mariadb

This repo is associated with [docker-php7-fpm](https://github.com/yansongda/docker-php7-fpm) and [docker-nginx](https://github.com/yansongda/docker-nginx)

If you are looking for LNMongoP, please go to [docker-compose-LNMongoP](https://github.com/yansongda/docker-compose-LNMongoP)

## php-fpm

### Added ext
- bcmath
- bz2 
- gd 
- iconv 
- mcrypt 
- mysqli
- pdo
- pdo_mysql
- zip
- mongodb
- redis
- memcached
- swoole

### Modified php.ini
- memory_limit = 256M
- post_max_size = 20M
- upload_max_filesize = 20M


## nginx

### Modified nginx.conf
- client_max_body_size 22m;    
- server_tokens off;
- gzip  on;

### Modified default.conf
- html root path: /www/public
- Adding support for handling with php file
- Adding support for hiding index.php url string
