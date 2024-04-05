FROM nginx:latest

# Copia el archivo de configuración de NGINX desde el mismo directorio que el Dockerfile
COPY ./default.conf /etc/nginx/conf.d/

# Exponer el puerto 80
EXPOSE 80

# CMD por defecto para iniciar NGINX
CMD ["nginx", "-g", "daemon off;"]
