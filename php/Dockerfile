FROM php:7.3.5-fpm

RUN apt-get update && apt-get install -y zlib1g-dev libicu-dev g++ libxml2-dev autoconf pkg-config libssl1.0-dev librabbitmq-dev libssh-dev libyaml-dev

RUN docker-php-ext-install pdo_mysql bcmath iconv pcntl mbstring intl calendar sockets

RUN pecl install -o -f redis \
&& rm -rf /tmp/pear \
&& docker-php-ext-enable redis \
&& pecl install -o -f yaml \
&& rm -rf /tmp/pear \
&& docker-php-ext-enable yaml \
&& pecl install amqp \
&& rm -rf /tmp/pear \
&& docker-php-ext-enable amqp

COPY ./conf.d/redis.ini $PHP_INI_DIR/conf.d/redis.ini

RUN usermod -u 1000 www-data
