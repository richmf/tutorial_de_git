# Tutorial básico para el uso de **git**

**Rich** :smile:
v.1.0

En este tutorial podrás aprender rápidamente como utilizar **git** y **GitHub**. Para ello debes tener una cuenta en [GitHub](https://github.com) y tener instalado **git**. Estas herramientas son muy útiles para el control de versiones y para tener organizados los archivos que se utilizan en el desarrollo de un programa.

> **GitHub** es una empresa que se encarga de mantener repositorios en internet. Normalmente es un servicio de paga, pero si dejas que tus repositorios sean públicos, entonces el servicio es gratuito.
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

Primero hay que generar un repositorio vacío en la página de GitHub. En el caso de este tutorial utilizaremos como ejemplo la forma en la que se generó este repositorio. Para ello en la página de GitHub se creó el repositorio llamado *tutorial_de_git* y como resultado el sitio de internet nos generó la siguiente página para el repositorio: *https://github.com/richmf/tutorial_de_git.git* . De esta manera en los servidores de **GitHub** estará dado de alta el repositorio. Para poner archivos en nuestro repositorio basta con subir los archivos por medio del sitio de internet, pero es la manera más ineficiente que hay cuando se está desarrollando un programa y además mantenerlo actualizado. Es por ello que utilizamos en comando **git**. En este caso hay dos maneras de proceder:

    1. Podemos clonar el repositorio itroduciendo el siguiente comando en la terminal:
    ```
    git clone https://github.com/richmf/tutorial_de_git.git
    ```
    Esto creará una carpeta llamada *tutorial_de_git* en nuestra computadora y dentro de ella se encontrarán los archivos que tenemos en el repositorio.

    2. La segunda opción es 



Regresar a las [Herramientas](http://sistemas.fciencias.unam.mx/~rich/herramientas/index.html)