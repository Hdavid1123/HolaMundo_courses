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

- git add : 

Seleccionar todos los archivos que presentan cambios (estapa de Stage), estos elementos pueden sacarse de esta etapa.

Existen muchas formas de añadir los archivos la más usada es cuando estamos seguros de que todos los cambios queremos incluirlos y es con "." (Mala práctica porque podemos agregar binarios muy grandes)

Para agregar una carpeta completa usarmos "git add Carpeta/"

Para agregar extensiones de archivos hacemos "*.txt" correspondiente a una expresión regular.



- git commit : 

Luego del commit siempre el archivo se lleva a un servidor, como por ejemplo Git Hub.

