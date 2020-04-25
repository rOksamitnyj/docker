FROM php:5.6-apache

RUN docker-php-ext-install mysqli \
    && docker-php-ext-enable mysqli

# Install xdebug
RUN pecl config-set php_ini /etc/php5/apache2/php.ini \
    && pecl channel-update pecl.php.net \
    && pecl install xdebug-2.5.5
#&& docker-php-ext-enable xdebug

# Enable XDebug
ADD xdebug.ini 	/usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini


WORKDIR /var/www/html

EXPOSE 80
CMD ["apache2-foreground"]
