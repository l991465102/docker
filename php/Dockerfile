FROM lzw7758/alpine-php-swoole-dev
MAINTAINER lzw7758 <liuzhiwei@lzw7758.cn>

#install composer
ENV COMPOSER_ALLOW_SUPERUSER 1
RUN curl -sS https://getcomposer.org/installer | php && \
mv composer.phar /usr/local/bin/composer && \
composer self-update --clean-backups


WORKDIR /myapp

EXPOSE 9501
CMD ["php", "/myapp/start.php"]
