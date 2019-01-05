FROM php:7.2-cli
RUN pecl install redis-4.0.1 \
&& pecl install xdebug-2.6.0 \
&& pecl install swoole \
&& docker-php-ext-enable redis xdebug swoole \
&& docker-php-ext-configure gd --with-png-dir --with-jpeg-dir --with-freetype-dir\
&& docker-php-ext-install gd

RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql

COPY . /usr/src/myapp
WORKDIR /usr/src/myapp

EXPOSE 9501