FROM php

RUN apt-get update -y \
  && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
  && php composer-setup.php \
  && php -r "unlink('composer-setup.php');" \
  && mv composer.phar /usr/local/bin/composer \
  && apt-get install -y libzip-dev zlib1g-dev libpq-dev\
  && docker-php-ext-install zip pdo pdo_pgsql pdo_mysql\
  && apt-get install git -y
