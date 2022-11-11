# Aquí, nostas del curso de git y github

## 01 ¿Por qué usar un sistema de control de versiones como Git?

esto inicia el repositorio
>git init

arranca el archivo, agrega los archivos modificados a algo llamado staging area (area de estado)
>git add biografia.txt  

este envia los ultimos cambios del archivo para la base de datos de control de versiones, para controlar sus cambios, mas un mensaje.  
>git commit -m 'version-1'

(digamos que se modifico algo en un achivo o archivos)

esto nos ayuda agregar todos los archivos que se hayan modificado  
>git add .

con esto guardamos los nuevos cambios
>git commit -m 'cambios sobre version-1'

cone sto vemos el estado de los archibos para ver alguno se ha modificado pero no se ha añadido  
>git status

este nos ayuda a ver el historial que se ha echo en los archivos dentro del repositorio  
>git show

para ver el historial de un solo archvo usamos el comando  
>git log bibliografia.txt

por el timo podemos llevar estos archivos a un repositorio remoto, con push y pull, pero eso se vera mas adelante

## 03 instlando git en Windows

1. ir al navegador buscar git, esta es la pagina  
    >git-scm-com

2. nos aseguramos de instalar git bash, y por lo general es darle siguiente siguiente

3. y finihs open git bash

4. listo

## 04 instalando git mac Os

1. buscamos git en safari, vamos a su sitio le damos descargar

2. nodescargar un archivo .dmg

3. le damos doble clcik

4. lego le danmos sobre la cajita amarila

5. si nos da un error, lamod lcik derecho sobre el archivo y le damos abrir

6. quiza nos pida constraseña

7. le damos install y ya quedaria por que en mac ya viene todo en uno por que esta basado en unix

## 05 instalando git en linux

1. abrimos una terminal

2. apt-get update (si o funciona)

3. sudo apt-get update, le damos y
sudo es para que nos de permisos de administrador

4. sudo apt-get upgrade

5. sudo apt-get install git

6. git --version para confirma que verision tenemos

## 06 Editores de código, archivos binarios y de texto plano

usaremos visual studio code

apesar de ser texto no son lo mismo

.txt texto plano

.rtf archivo binario

.doc archivo binario

## 07 Introducción a la terminal y línea de comandos

nos permite ver en que ruta estamos  
>pwd

para navegar a una carpeta
>cd 'nobre de la carpeta  
>dd desktop

para ir al home directamente  
>cd /

cuando esta este simbolo ~ significa que estamos en lugar de nuestros documentos o de una carpeta o usuario

cuano esta / significa que estamos en la raiz del disco

nos muestra una lista de los archivos que hay 
>ls

nos muestra todos los archivos incluyecnod los oculto
>ls -al

me muestra casi todos los archivos. pero no los ocultos
>ls -l

nos muestra el gupor de archivos pero no en un alista
>ls -a

limpa la consola  
    >ctrl + l

para regresar una carpeta anterior  
>cd ..

para crear una carptea mkdir (nombre de la carpreta)
>mkdir proyecto

para crear aun arcivo se usa la palabra touch  
>touch inicio.txt

para ver el contenido de un archivo  
>cat incio.txt

para ver el hitoria de los comandos seleccionardos  
>history

para borrar un archivo usarmos
rm inicio.txt  
pero hay que tener cuidado por que podemos borrar todo el disco

para ver como funciona un comando se le agrega --help
>rm --help

## 08 Crea un repositorio de Git y haz tu primer commit

para crear un repositorio hay que decirle donde esta la carpte principal

para iniciar el repositoio  
>git init

para iniciar visual studio desde la terminal  
>code

git status, nos muestra si hay algun cambio en un archivo y cual es estado de alchivo  
>git status

para agregar un archivo  
>git add inicio.txt  

para agregar todos los archivos  
>git add .

para quitar un arcivo despues de agregarlo pero no aver echo el commit  
>git rm --cached inicio.txt  
para quitarlo de la memmoria ram

para enviar los archvios al repositiorio  
>git commit -m 'este es el primer comid de este archivo'

es importante configurar quien es el que va a eniar el commit para ver como funciona la configurarcion
>git config

con esto podemos ver la configuracion de git que tenermos y que nos puede estar faltando
>git config --list

para ver donde estan las configuraciones guardadas  
>git config --list --show-origin

con esto vasmos a cambiar todos los usuarios globales, para mas especifico el nombre de usuario git, (para ver quien hace los cambios)  
>git config --global user.name "nombre de usuario"

siguiendo con la configuracion per esta ves vamos a cambiar el email
>git config --global user.email "user@mail.com"

una ve echo las configuraciones echas, ya podemos hacer nuestro primer commit  
>git commit -m 'esto es nuetro primer commit'

para ve el histirial de un archivo  
>git log inicio.txt

## 09 Analizar cambios en los archivos de tu proyecto con Git

si uno envia un commit son mensaje nos va a llvar a la consola de vim, para salir de ahi
>:wq
>:q
> esc :wq

para ver el historial en general de los cmabios  
>git show

para ver las diferencias entre un archivo y otro (verion mas vieja, verision reciente)
>gir diff (los el hash del archivo) (el hash del otro archivo)

para volver a un version mas vieja

## 10 ¿Qué es el staging?
git init crea el area de estado en memoria RAM llamada (staging) y el repositorio de nuestro proyecto

para añadir un archivo en staging git add . ó git add inicio.txt

despues de agregar el archivo ya se puede hacer un commit para enviarlo al repositori que se llama master

>checkout  
nos traemos los ultimos cambio o los cambios que no sotros queramos

## 11 ¿Qué es branch (rama) y cómo funciona un Merge en Git?


## 12 Volver en el tiempo en nuestro repositorio utilizando reset y checkout

para ver el historial de comits
>git log

para gresar a un version
>git reset (version del commit) --hard  
esto nos borra todo incluyendo el historial

git reset (version de commit  ) --soft  
nos regresa a la version anterios pero todo lo que tengamos en staging lo seguremos conservando en staging para el proximo commit.

esto nos permite ver los cambios que se hicieron los archvos de una menera un poco mas espcifico  
>git log --stat

para ver el archivo en su primer commit o mas bien regresar en el tiempo a la primera version  
>git chekout (el numero o hash del commit al que queremos regresar) historia.txt(nombre del archivo)

>git checkout master hisotia.txt  
estonos trae el archivo en su ultimo commit

caundo ejecutamos el checkout nos muesra el archivo al que referenciamos, si damos commit con ese checkout nos va a remplarsar por la version del checkout y esto puede ser peligroso

practicamente es como traer una version del pasado e insertarla de nuevo en la rama master

## 13 Git reset vs. Git rm

git rm  
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones.}

git rm --cached: Elimina los archivos de nuestro repositorio local y del área de staging, pero los mantiene en nuestro disco duro. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos, por lo que pasaran a un estado untracked.  

git rm --force: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

hay cun comando para hacer un agit add . y commit en el mismo comando, pero solo funciona si los archivos previamente ya les abiamos echo un add anteriormente, en archivos completamente nuevo esto no va a funcionar  
>git commmit -am "esto es un cambio nuevo"