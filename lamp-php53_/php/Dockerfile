FROM orsolin/docker-php-5.3-apache

# Install xdebug
RUN pecl config-set php_ini /etc/php5/apache2/php.ini && pecl channel-update pecl.php.net && pecl install xdebug-2.2.7
#&& docker-php-ext-enable xdebug

# Enable XDebug
ADD xdebug.ini /etc/php5/apache2/conf.d/docker-php-ext-xdebug.ini

WORKDIR /htdocs


