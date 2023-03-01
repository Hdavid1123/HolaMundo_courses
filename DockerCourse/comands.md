# Docker Commands

1. docker images : lista todas las imagenes descargadas hasta el momento

## Etiquetas:

- REPOSITORY : nombre de la imagen.
- TAG : etiquetas "latest".
- IMAGE ID : identificador.
- CREATED : tiempo de creación en Docker Hub.
- SIZE : espacio en disco duro.

2. docker pull "tec":"version"

Se puede descargar exactamente la misma imagen pero con etiquetas distintas, el mejor diferenciador de estas es el ID.

3. docker image rm "tec":"version"

## Crear contenedores

Para crear un contenedor es necesario tener una imagen de base, en este caso, el uso de mongo puede facilitar crear un contenedor debido a que no necesita tantas variables de configuración.

Comando:

4. docker create mongo / docker container create mongo
5. docker start + ID del contenedor creado.

6. docker ps : muestra una tabla con el estado de los contenedores además de las siguientes características.

- CONTAINER ID : un ID reducido en tamaño que puede ser usado para manejar el contenedor de la misma manera.

- IMAGE : imagen de base.

- COMMAND : comando interno usado para la creación del contendor.

- CRATED : fecha de creación del contenedor.

- STATUS : estado.

- PORTS : puerto que está utilizando.

- NAMES : nombre que se colocó el contenedor.

_________

7. docker stop + ID : pausa la ejecución del contenedor pero este sigue creado, con docker ps -a se puede mostrar todos los contenedores que están creados aunque no se estén ejecutando.

Cuando detenemos un contenedor creado, el comando "docker ps" no lo mostrará, para ver todos los contenedores agregamos "-a".

- docker rm "name".

Para nombra nuestros contenedores hacemos:

- docker create --name monguito mongo.

## Port Mapping.

8. docker create -p27017:27017 --name monguito mongo

En este caso la notación es "creación" "-p_puertofisico:puertocontenedor" "nombre 'name'" "imagen_base"

9. docker logs (--follow) +ID/NAME : muestra los registros del contenedor por lotes, usando --follow, podemos seguir escuchando los logs emitidos por el contenedor.

10. docker run : busca la imagen que le decimos, sino la encuentra la descarga. Crea un contenedor asociado a esta imagen. Inicia el contenedor. Muestra los logs asociados a esta imagen, y si salimos de la muestra de los logs entonces detiene el contenedor.

Para usar este comando en modo "dettached" luego de run escribimos "-d". Además cualquiera de las configuraciones asociadas a los puertos, nombres y configuraciones de los comandos: create, start y ps funcionan.

Ej: docker create -p27017:27017 --name monguito mongo

Cada que ejecutamos el comando de docker run siempre creará un nuevo contenedor, i.e tendremos tantos contenedores como ejecuciones de docker run.




