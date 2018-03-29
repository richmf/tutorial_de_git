# Tutorial básico para el uso de **git**

**Rich** :smile: v.2.1

En este tutorial podrás aprender rápidamente como utilizar **git** y **GitHub**. Para ello debes tener una cuenta en [GitHub](https://github.com) y tener instalado **git**. Estas herramientas son muy útiles para el control de versiones y para tener organizados los archivos que se utilizan en el desarrollo de un programa.

> **GitHub** es una empresa que se encarga de mantener repositorios en internet. Normalmente es un servicio de paga, pero si dejas que tus repositorios sean públicos, entonces el servicio es gratuito.
>
> **git** es un comando que permite llevar un control de versiones de los diferentes programas que vayamos haciendo.

El objetivo es utilizar el comando **git** en la terminal para manejar los repositorios de los programas que vayan generando.

*Se recomienda utilizar cualquier distribución de Unix o Linux, es decir, un sistema operativo decente.*

## Configuración básica de **git** en la terminal

Antes de utilizar **git** hay que realizar una configuración sencilla para indicarle al comando las credenciales que utilizaremos para generar/modificar los repositorios en internet. Para ello sólo tenemos que dar nuestro nombre de usuario y correo electrónico que utilizamos en **GitHub** para identificarnos con los siguientes comandos en la terminal: 

```
$ git config --global user.name "Nombre_de_usuario"
$ git config --global user.email "tu_email@correoelectronico.com"
```

## Para crear un repositorio

Primero hay que generar un repositorio vacío en la página de GitHub. En el caso de este tutorial utilizaremos como ejemplo la forma en la que se generó este repositorio. Para ello en la página de **GitHub** se creó el repositorio llamado *tutorial_de_git* y como resultado el sitio de internet nos generó la siguiente página para el repositorio: *https://github.com/richmf/tutorial_de_git.git* . De esta manera en los servidores de **GitHub** estará dado de alta el repositorio. Para poner archivos en nuestro repositorio basta con subir los archivos por medio del sitio de internet, pero es la manera más ineficiente que hay cuando se está desarrollando un programa y además mantenerlo actualizado. Es por ello que utilizamos el comando **git** y para ello dos maneras de proceder:

1. Podemos clonar el repositorio introduciendo el siguiente comando en la terminal:
    ```
    $ git clone https://github.com/richmf/tutorial_de_git.git
    ```
Esto creará una carpeta llamada *tutorial_de_git* en nuestra computadora y dentro de ella se encontrarán los archivos que tenemos en el repositorio.

2. La segunda opción es crear la carpeta, dar de alta a **git** dentro de la carpeta y el repositorio al que estará asociado. Esto se logra con los siguientes comandos en la terminal:
    ```
    $ mkdir tutorial_de_git
    $ cd tutorial_de_git/
    $ git init
    $ git remote add origin https://github.com/richmf/tutorial_de_git.git
    ```

Cualquiera de las dos maneras que se elijan, el resultado es el mismo. La primera opción es más utilizada cuando se quiere hacer un repositorio completamente nuevo y la segunda opción se utiliza cuando tenemos un programa que ha hemos estado desarrollando en nuestra computadora y ahora queremos utilizar **GitHub** para publicarlo o actualizarlos. De hecho, en el segundo caso basta con los últimos dos comandos para inicializar **git** en dicha carpeta, sólo hay que tomar en cuenta que el repositorio debe existir en la página de **GitHub**.

## Para agregar nuevos archivos o hacer modificaciones

Dentro de la carpeta local podemos hacer modificaciones y/o crear nuevos archivos. Para que éstos queden dentro de la estructura de actualización del repositorio, tenemos que agregarlos al índice de **git** con el siguiente comando:
```
$ git add nombre_del_archivo
```
Con esto hemos agregado el archivo a la lista de **git**. Para llevar el control de actualizaciones o modificaciones es necesario avisarle a **git** con el siguiente comando:
```
$ git commit -m "Mensaje a grabar"
```
Es importante señalar que tenemos que poner un mensaje con el que podamos identificar las modificaciones que realizamos con respecto a la versión anterior. Finalmente, ahora estamos en posición de enviar las actualizaciones al servidor de **GitHub** con el siguiente comando:
```
$ git push origin master
```

***

Una herramienta útil con la que podemos revisar el status de nuestro repositorio con el siguiente comando
```
$ git status
```
De esta manera podemos saber a que archivos tenemos hay que hacerles *add* y/o *commit*. Como se puede apreciar, la secuencia básica de los comandos es:
```
$ git add nombre_del_archivo
$ git commit -m "Mensaje a grabar"
$ git push origin master
```

De esta manera podemos tener una copia actualizada de nuestro trabajo en **GitHub**. En el otro archivo de este tutorial podemos encontrar herramientas y tips que pueden ser útiles para manejar con mayor eficiencia el comando **git**. Los temas que se abordan son en las otras partes del tutorial son:

- [Ramas y control de versiones](https://github.com/richmf/tutorial_de_git/blob/master/Ramas.md).

---

También se invita al lector que revise el [tutorial interactivo](https://try.github.io) que *Code School* ha diseñado para los usuarios novatos de **git**.

---

Regresar a las [Herramientas](http://sistemas.fciencias.unam.mx/~rich/Herramientas/index.html)

Se agradece el apoyo de los proyectos DGAPA-PAPIME:

- PE 105017 durante el año 2017. *Versión 2*

- PE 108216 durante el año 2016. *Idea original*
