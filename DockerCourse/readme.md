# Docker

Es un sistema de contendores que permiten la utilización de la misma versión de un programa específico junto con todas sus dependencias, mediante el uso o la generación de una imagen.

## Estructura:

- Linux Alpine (más ligero)
- Imagen 1
- Imagen 2  *Dependencias*
- Imagen 3
- Capa de Aplicación.

La idea es que los contenedores pesan poco con respecto a una máquina virtual. Las máquinas virtuales pesan gigas mientras que los contenedores cientos de megas.

## Comparando con máquinas virtuales:

Las máquinas virtuales usan el Hardware mientras continenen el kernel y las aplicaciones.

Docker en cambio solo tiene un kernel de referencia sin embargo, usa el del sistema operativo para trabajar conteniendo solo las aplicaciones.

## Adicional: Tipos de Virtualizaciones:

1. Paravirtualización: Conceptos: Host (Anfitrión) y  Gest (Cliente). Intenta entregar la mayor cantidad de accesio del Hardware a los clientes.

2. Virtualización parcial: Algunos componentes del Hardware se virtualiza.

3. Virtualización completa: El hardware deja de existir como tal puesto que la aplicación usa uno completamente virtualizado.

Para cualquiera de estos tres Docker es superior tanto en tamaño como en rendimiento puesto que parte desde arriba del Kernel.

## Docker Desktop:

Máquina virtual que corre Linux y ejecuta conteiner, para Windows esta puede correr de manera nativa mediante WSL2 (Windows Subsystem for Linux).

Contiene: Docker Compose, CLI (commend line interface) y otras herramientas que permiten el acceso tanto al sistema de archivos como a la red.