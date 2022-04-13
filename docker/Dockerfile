FROM php:7.2.6-apache

COPY /src/ /var/www/html
COPY docker/vhost.conf /etc/apache2/sites-available/000-default.conf

WORKDIR /var/www/html

RUN docker-php-ext-install pdo pdo_mysql bcmath \
    && chown -R www-data:www-data /var/www/html \
    && a2enmod rewrite && service apache2 restart