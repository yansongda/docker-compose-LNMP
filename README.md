# docker-compose-lnmp
docker-compose with php7.0-fpm,nginx,redis,memcached,mariadb

## php7.0-fpm

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

- Adding support for handling with php file
- Adding support for hiding index.php url string
