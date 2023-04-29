ARG PHP_VERSION
ARG CONTAINER_PACKAGE_URL

FROM ${PHP_VERSION}

LABEL maintainer="lsj_moon@163.com"

#php-extension-installer
ADD ./extensions/install-php-extensions  /usr/local/bin/

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
