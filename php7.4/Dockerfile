ARG PHP_VERSION="7.4"

FROM php:${PHP_VERSION}-fpm

LABEL maintainer="lsj_moon@163.com"

# In order to be sure the COPY instruction uses the very latest version, you can run:
# docker pull mlocati/php-extension-installer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN apt-get update \
    && apt-get install -y \
        git  \
        curl \
    && chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions \
        bcmath \
        bz2 \
        calendar \
        exif \
        gd \
        intl \
        ldap \
        mysqli \
        pdo_mysql \
        opcache \
        soap \
        xsl \
        zip \
        sockets \
        mcrypt \
        redis-5.3.7 \
        amqp-1.11.0 \
        xdebug-2.9.8 \
        @composer
