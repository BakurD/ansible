FROM php:8.2.5-fpm

# Установка библиотеки sockets
RUN apt-get update && apt-get install -y \
    libsocket-perl

RUN docker-php-ext-install pdo mysqli pdo_mysql sockets
# Копирование конфигурационного файла php.ini
COPY php.ini /usr/local/etc/php/

# Установка рабочей директории
WORKDIR /var/www/html

# Открытие порта 9000 для FPM
EXPOSE 9000

# Запуск FPM
CMD ["php-fpm"]
