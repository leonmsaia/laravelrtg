# Usa la imagen oficial de MySQL como base
FROM mysql:8

# Copia el archivo de configuración personalizado
# COPY ./my.cnf /etc/mysql/my.cnf

# Establece las variables de entorno
ENV MYSQL_DATABASE=laravel \
    MYSQL_USER=laravel \
    MYSQL_PASSWORD=secret \
    MYSQL_ROOT_PASSWORD=secret

# Expone el puerto 3306
EXPOSE 3306
