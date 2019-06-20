# Data Science 101 - Lab 02

## Data Science Project - Plantilla

[![1*sBqK_JA3Sh6ebWkYBEKgUw.png](https://cdn-images-1.medium.com/max/800/1*sBqK_JA3Sh6ebWkYBEKgUw.png)]

## Git

¿Qué es un control de versiones, y por qué debería importarte? Un control de versiones es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo, de modo que puedas recuperar versiones específicas más adelante.

La principal diferencia entre Git y cualquier otro VCS (incluyendo Subversion y sus amigos) es la forma en la que manejan sus datos. Conceptualmente, la mayoría de los otros sistemas almacenan la información como una lista de cambios en los archivos. Estos sistemas (CVS, Subversion, Perforce, Bazaar, etc.) manejan la información que almacenan como un conjunto de archivos y las modificaciones hechas a cada uno de ellos a través del tiempo.
Git no maneja ni almacena sus datos de esta forma. Git maneja sus datos como un conjunto de copias instantáneas de un sistema de archivos miniatura. Cada vez que confirmas un cambio, o guardas el estado de tu proyecto en Git, él básicamente toma una foto del aspecto de todos tus archivos en ese momento, y guarda una referencia a esa copia instantánea. Para ser eficiente, si los archivos no se han modificado Git no almacena el archivo de nuevo, sino un enlace al archivo anterior idéntico que ya tiene almacenado. Git maneja sus datos como una secuencia de copias instantáneas.

#### 1. La Línea de Comandos
Existen muchas formas de usar Git. Por un lado tenemos las herramientas originales de línea de comandos, y por otro lado tenemos una gran variedad de interfaces de usuario con distintas capacidades.

#### 2. Instalación

Para la instalación en Windows, descargar la versión mas reciente [aqui](http://git-scm.com/download/win)

#### 3. Configuración
Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo electrónico. Esto es importante porque los "commits" de Git usan esta información, y es introducida de manera inmutable en los commits que envías:

`$ git config --global user.name "Pedro Perez"`
`$ git config --global user.email pedroperez@example.com`

#### 4. Como obtener Ayuda de Git

Si alguna vez necesitas ayuda usando Git, existen tres formas de ver la página del manual (manpage) para cualquier comando de Git:

`$ git help <verb>`
`$ git <verb> --help`
`$ man git-<verb>`

#### 5. Inicializando un repositorio en un directorio existente
Si estás empezando a seguir un proyecto existente en Git, debes ir al directorio del proyecto y usar el siguiente comando:

`$ git init`
 
#### 6. Clonando un repositorio existente
Si deseas obtener una copia de un repositorio Git existente — por ejemplo, un proyecto en el que te gustaría contribuir — el comando que necesitas es git clone.

Puedes clonar un repositorio con `git clone [url]`. Por ejemplo, si quieres clonar la librería de Git llamada libgit2 puedes hacer algo así:

`$ git clone https://github.com/libgit2/libgit2`


#### 7. Ciclo add, commit, push

La herramienta principal para determinar qué archivos están en qué estado es el comando `git status`. 

Para comenzar a rastrear un archivo debes usar el comando `git add`.

Para confirmar los cambios usamos el comando `git commit`.


## Project Jupyter

#### 1. Instalación

Para instalar tenemos 2 opciones, usar el administrador de paquetes de python **pip**, o instalar la versión mas reciente de Anaconda. Para mas detalles clic [aqui](https://jupyter.org/install.html).



### Asignación

1. Investigar 2 librerías de python.
2. Elaborar un notebook de jupyter que contenga: la instalacion de cada una de las librerias dentro del ambiente jupyter, la importación de cada una de ellas y por ultimo una breve documentación de una función de cada libreria.
3. Enviar al correo el archivo .ipynb con el nombre segun el formato nombredelestudiante.ipynb.







