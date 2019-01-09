FROM lzw7758/alpine-php-swoole-dev
MAINTAINER lzw7758 <liuzhiwei@lzw7758.cn>

#install composer
ENV COMPOSER_ALLOW_SUPERUSER 1
RUN curl -sS https://getcomposer.org/installer | php && \
mv composer.phar /usr/local/bin/composer && \
composer self-update --clean-backups

COPY . /usr/src/myapp
WORKDIR /usr/src/myapp

#set China timezone
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
echo 'Asia/Shanghai' > /etc/timezone && \
echo "[Date]\ndate.timezone=Asia/Shanghai" > /usr/local/etc/php/conf.d/timezone.ini

EXPOSE 8080
CMD ["php", "-v"]
