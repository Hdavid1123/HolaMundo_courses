# Docker Commands

1. docker images : lista todas las imagenes descargadas hasta el momento

## Etiquetas:

- REPOSITORY : nombre de la imagen.
- TAG : etiquetas "latest".
- IMAGE ID : identificador.
- CREATED : tiempo de creación en Docker Hub.
- SIZE : espacio en disco duro.

Se puede descargar exactamente la misma imagen pero con etiquetas distintas, el mejor diferenciador de estas es el ID.

El formato para descargar con una versión a elección está dada por la notación:

    tec : version

## Crear contenedores

Para crear un contenedor es necesario tener una imagen de base, en este caso, el uso de mongo puede facilitar crear un contenedor debido a que no necesita tantas variables de configuración.

Comando:

- docker create mongo / docker container create mongo
- docker start + ID del contenedor creado.

- docker ps : muestra una tabla con el estado de los contenedores además de las siguientes características.

- CONTAINER ID : un ID reducido en tamaño que puede ser usado para manejar el contenedor de la misma manera.

- IMAGE : imagen de base.

- COMMAND : comando interno usado para la creación del contendor.

- CRATED : fecha de creación del contenedor.

- STATUS : estado.

- PORTS : puerto que está utilizando.

- NAMES : nombre que se colocó el contenedor.

_________

- docker stop

Cuando detenemos un contenedor creado, el comando "docker ps" no lo mostrará, para ver todos los contenedores agregamos "-a".

- docker rm "name".

Para nombra nuestros contenedores hacemos:

- docker create --name monguito mongo.

## Port Mapping.


