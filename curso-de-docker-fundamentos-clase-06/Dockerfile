#                               INTRUCCIONES PARA CREAR IMAGENES PERZONALIZDAs

# creando un contenedor o image con el servidor web nginx
FROM nginx:latest

# Path: /usr/share/nginx/html => ruta del contenedor nginx donde ngnix guarda los archivos q mostrara en el navegador
# Instrucciones para docker => solo para proyectos staticos q no cambiaran
COPY /sitio /usr/share/nginx/html   
# Crear un Volumen >= son para proyecto q tendra cabmios
# VOLUME [ "/sitio", "/usr/share/nginx/html"]




# Creando un contenedor => 
#  -it: En forma interactiva para ver los logs

# --rm: elimina las versiones anteriores del contenedor

# -d: el contenedor se ejecuta en un segundo plano

#  -p: mapea el puerto del contenedor con el puerto de la aplicación para exponerla

# --name: nombre del contenedor


# COMANDOS ESPECIALES DE DOCKER

# docker images --filter=reference='*:2.0'
# docker images sitioweb
# docker --no-trunc 
# docker image tag sitioweb:latest admin/sitioweb:latest
# docker rmi admin/sitioweb:latest =>desetiquetar or eliminar
# docker rmi 288e43b59d4c
# docker rmi -f 288e43b59d4c
# docker ps -a
# docker ps --size
# docker stop ad1fe1997dad => gestion de recurso
# docker stats => rendimiento del contenedor 
# docker build -t sitiowe1:latest
# docker run -it --rm -d -p 8080:80 -v ./sitio:/usr/share/nginx/html/sitio --name web nginx => gestion de volumenes entre local y contenedor
# rm img1.jpg => si se realiza desde el desktop de docker automaticamente elimaara el q se enceuntra en tu local
# docker inspect web
# docker run -it --rm -d -p 127.0.0.1:8080:80 --name web nginx ==> asignacion de una IP =>HostIp": "127.0.0.1, por default ipadress
# docker network ls => detalles del enlace sobre el entorno local -> entorno interno docker
# docker start web
# docker rm -f nombreDelContenedor


# PUENTES O REDES
# bridge -> red puente predeterminada entre contenedores
# host -> el contenedor comparte la red del host (sin aislamiento)
# none -> el contenedor no tiene red (aislado completamente)

# CREANDO UN PUENTE O RED
# docker network create platzinet

# PUBLICAR UNA IMAGEN
# docker login
# docker build -t alvaroae/linktree:latest
# docker push alvaroae/linktree:latest => publicando la image

# DEPLEGAR LA IMAGEN DE OTRO USER => ADICONAL DEBE DE HABER UNA DESCRIPCION PARA VER COMO SE EJECUTA
# docker run --name web -it -p 8080:80 alvaroae/linktree:latest 

# DESPLIEGUE SOBRE EL SISTEMA Y SUS ARCHIVOS INTERNOS DEL CONTENEDOR
# [bin  boot  dev  docker-entrypoint.d  docker-entrypoint.sh  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var]
# docker run --name web2 -it -p 8080:80 alvaroae/linktree:latest /bin/bash => abrir una shell
# docker run --name web2 -it -p 8080:80 alvaroae/linktree:latest sh => abrir una shell respecto al contenedor


# DESPLIGUE SOBRE LAS CARACTERISTICAS DE UN CONTENEDOR 
# docker inspect d18ef9c60f27


# y docker-entrypoint.sh qué?
# Bueno pues este es un script de shell que actúa como intermediario entre Docker y el comando principal, en este script se puede:
# Configurar variables de entorno
# Preparar archivos o directorios
# Ajustar permisos
# Ejecutar comandos de inicialización


# Exportación e importación de imágenes Docker con comandos CLI
# Extraer una imagen => RAZONES
# ==> LA RED DE ESA EMPRESA INABILITA LA TRAFERENCIA DE RED
# ==> EL ARCHO DE BANDA DE LA RED IMPIDA ENVIARLO O TOMAR MUCHO TIEMPO
# COMANDOS
# docker save alvaroae/linktree >| linktree.rar 
# dockder load --input linktree.rar => carga una imagen zipeado