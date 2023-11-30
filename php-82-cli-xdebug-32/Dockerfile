FROM php:8.2
COPY --from=composer /usr/bin/composer /usr/bin/composer
RUN apt-get update && apt-get -y install libzip-dev libicu-dev default-mysql-client librdkafka-dev
RUN docker-php-ext-install pdo_mysql zip intl
RUN pecl install xdebug-3.2.0
RUN docker-php-ext-enable xdebug
RUN pecl install rdkafka
RUN docker-php-ext-enable rdkafka
