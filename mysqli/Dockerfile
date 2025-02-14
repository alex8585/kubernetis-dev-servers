FROM php:8.4-fpm

# Обновление и установка зависимостей
RUN apt-get update -y && apt-get install -y \
    default-libmysqlclient-dev \
    && docker-php-ext-configure mysqli --with-mysqli \
    && docker-php-ext-install mysqli \
    && docker-php-ext-enable mysqli

# Убедимся, что php-fpm работает
CMD ["php-fpm"]

