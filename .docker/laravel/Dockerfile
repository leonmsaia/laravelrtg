# Usa la imagen oficial de PHP como base
FROM php:8.2-fpm

# Instala dependencias necesarias
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    libzip-dev \
    libpq-dev \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev

# Instala extensiones de PHP necesarias
RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd pdo pdo_mysql zip

# Instala Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Configura la carpeta de trabajo
WORKDIR /var/www/html

# Copia los archivos de Laravel a la carpeta de trabajo
COPY ../app /var/www/html

# Expone el puerto 9000
EXPOSE 9000

# Comando por defecto para ejecutar el servidor PHP-FPM
CMD ["php-fpm"]
