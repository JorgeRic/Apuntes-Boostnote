# GIT Y GITHUB
Sistema de control de versión distribuido(DVCS):

Es un sistema que registra los cambios en un archivo o conjunto de archivos a lo largo del tiempo para que pueda recuperar versiones especificas más adelante.
Estos sistemas te permiten tener diferentes versiones de cada archivo que componen tu proyecto para que puedas recuperar una versión antigua en caso de que se rompa algo de tu codigo.
El DVCS usualmente trabaja con una plataforma de alojamiento de codigo(code hosting), donde se almacena el codigo de su equipo para compartirlo con otros miembros de su equipo.

## GIT
Es un tipo de DVCS
Permite utilizar el sistema de versiones en tu equipo

Configuración de nuestro Git en nuestro equipo:
$ git config --global user.name "Jorge Rico"
$ git config --global user.email jorrillop@hotmail.com

$ git init es el comando que indica a Git que la carpeta en la que te encuentras ahora será un repositorio de Git. Git rastrea todos los cambios en las carpetas y archivos de la carpeta en la que actualmente te encuentras
Con $ rm -rf .git eliminas la carpeta del Git
Debemos crear un repositorio Git en una carpeta de proyecto especifica. No en una carpeta de alto nivel. 
Solo queremos que rastree los cambios de una carpeta, y no de todas las carpetas y archivos de tu equipo local

$ git status nos dice que archivos y carpetas estan siendo rastreadas

Para añadir un archivo al area de preparación usamos:
$ git add nombre del archivo
$ git status

Para incluir todos los archivos de mi proyecto utilizamos:
$ git add -A
$ git status

Para eliminar un archivo del area de preparación utilizamos:
$ git reset (nombre del archivo)
$ git status

commit es una instantanea del estado de los archivos y de las carpetas
Con $ git commit guardamos los cambios
Debemos añadir un mensaje para saber posteriormente el motivo de la actualización
Esto se hace así:
$ git commit -m”comentario”
$ git status

Con $ git log podemos ver todos los cambios que hemos hecho en nuestro proyecto (incluyendo quien los hizo y cuando)
Podemos volver a un commit anterior si queremos recuperarlo
Cuando se han hecho muchos commit en un proyecto pueden aparecer muchas hojas de dialogo. Pulsando “q” salimos de la pantalla en nuestro terminal

Pasos a seguir para añadir archivos de Git:
git init

git status

git . (añadimos todos los archivos de la carpeta actual a Git)
git add nombre de archivo (añadimos el archivo deseado a Git)

git commit -m “comentario” actualizamos el archivo

git log (podemos ver quien y cuando se hicieron los cambios)

git push añadimos el archivo actualizado a GitHub

Con git clone copiamos el proyecto de otro colaborador
                                                                                       

## GITHUB
Es una plataforma de alojamiento de codigo para el control de revisiones y colaboración. Permite trabajar a varios miembros en un mismo proyecto desde diferentes sitios

Añadir un repositorio remoto: git remote
Hay dos tipos de repositorio: local y remoto
Cuando hacemos cambios locales debemos de añadir a nuestro repositorio remoto, pero cuando hagamos cambios en nuestro repositorio remoto debemos añadirlos a nuestro repositorio local.
El primer paso es conectar los dos repos. Esto se puede hacer usando el comando git remote add <alias>(origin) <github-url>(dirección exacta de donde esta en la nube)
git push / comando para añadir codigo desde un repositorio local a un remoto
git push <alias> <remote-branch-name> 
github-repo / nombre del repositorio remoto al que queremos enviar el fichero.
Podemos tener multiples repositorios remotos, por lo que le damos un nombre
master / rama a la que estamos añadiendo a gibhub
$ git push github-repo master
Extracción desde un repositorio remoto: git pull
Con git pull traemos el codigo desde el GitHub a nuestro repositorio local
git pull <alias> <remote-branch-name>

Git te permite controlar tu codigo, Github te permite colaborar con tus compañeros de equipo


Añadir colaboradores:

Pinchamos el nombre del proyecto
Setting
Option colabotators
buscamos el nombre del colaborador
Mandamos invitación al mail del colaborador deaseado