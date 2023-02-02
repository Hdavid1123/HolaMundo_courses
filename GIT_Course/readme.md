# GIT / GITHUB Y CONFIGURACIONES:

## Usos de GIT :

- Historial : volver sobre cambios en versiones de código.

- Almacenar código.

- Trabajar en equipo.

- Detectar cuando se introdujo un error.

## Algunos comando importantes:

- git config --global user.name "Name"
- git congif --global user.emal "hola@mundo.com"

El "--global" hace que git trabaje todos lo proyectos con esta configuración; para un proyecto en específico que necesitemos otros datos se ejecuta sin esta parte del código.

- git config --global core.editor "vscode"

- git config --list

- git config <key> : para mirar una clave específica como por ejemplo "user.name", etc.

- git config --global -e : mostrar el archivo de configuración en el editor de código.

## Configuración de saltos de línea entre Linux o Windows:

Los sistemas operativos de Windows tratan los saltos de línea usando los caracteres "CR + LF", mientras que en Linux o Mac solo tenemos "LF", por lo tanto para configurar la eliminación o descarga del "CR" usamos:

- git config --global core.autocrlf "input - Linux / true - Windows".
_________________________________________

- git add : 

Seleccionar todos los archivos que presentan cambios (estapa de Stage), estos elementos pueden sacarse de esta etapa.

Existen muchas formas de añadir los archivos la más usada es cuando estamos seguros de que todos los cambios queremos incluirlos y es con "." (Mala práctica porque podemos agregar binarios muy grandes)

Para agregar una carpeta completa usarmos "git add Carpeta/"

Para agregar extensiones de archivos hacemos "*.txt" correspondiente a una expresión regular.

Para agregar varios archivos dejamos un espacio entre ellos.
____________________________________________

- git commit : 

Luego del commit siempre el archivo se lleva a un servidor, como por ejemplo Git Hub. Para realizar este generalmente agregamos "-m" para enviar un mensaje explicativo sobre el commit realizado.

- rm "archivo.txt" : eliminar + git commit.
- git rm "archivo.txt" : junta los dos comandos anteriores.

- git restore --staged <file> : retrocede los cambios de la etapa de Stage.

- git mv "archivo1.txt" "archivo.txt"

## Archivos que se ignoran siempre:

Por ejemplo, las variables de configuración como usuarios, contraseñas, etc.

Para esto generamos un archivo donde colocamos en cada línea el archivo o carpeta que queremos ignorar

## Otra forma de mostrar un git status con menos info

- git status -s : 

Este entrega los archivos que han presentado modificaciones con la siguiente notación:

Colores : Rojo -> No seguido, Verde -> En Stage
M: modificado 
?? : archivo no agregado
A : archivo que está siendo agregado (en Stage)

- git diff : Representa los cambios que estamos agregando. Suele mostrar los saltos de línea como el hecho de borrar y volver a escribir una línea pues esta no contaba inicialmente con "CR". Al agregar "--stage" muestra solo los cambios que han sido subidos al stage.

- git log : Muestra el historial de cambio pero con mucha información incluyendo incluso los correos electrónicos de quien hizo el cambio. Para facilitar la visión de este archivo usamos "--oneline".

Este último le da un ID de modificación y también el mensaje que pusimos en el commit.

