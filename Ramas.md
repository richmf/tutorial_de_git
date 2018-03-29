# Ramas

Las *Ramas* son utilizadas para llevar un control de las versiones sin afectar la versión original o principal (*master*). Esto resulta de mucha utilidad ya que si tenemos un programa que sabemos que funciona bien, podemos empezar a generar una nueva versión manteniendo la anterior intacta hasta el momento en que tengamos la necesidad de fusionarlas.

Para crear una rama y ubicarse en ella hay que utilizar el siguiente comando:
```
$ git checkout -b mi_rama
```
Para regresar al la rama principal o *master* es con el siguiente comando:
```
$ git checkout master
```
Si queremos borrar la rama es con el siguiente comando:
```
$ git branch -d mi_rama
```
Al igual que con la rama principal, es necesario hacer ```add``` y  ```commit``` a los archivos modificados. En este caso para que las actualizaciones lleguen al repositorio en **GitHub** es con el siguiente comando:
```
$ git push origin mi_rama
```
De esta manera podemos tener en el mismo repositorio diferentes versiones, típicamente una o varias que estamos modificando para mejorar la principal o *master*.

### Ejemplo

supongamos que queremos hacer una rama y en ésta hacemos una modificación a un archivo del repositorio. Para ello ejecutamos la siguiente secuencia de comandos:
```
$ git checkout -b rama
# Hacer modificaciones en algún archivo
$ git add archivo_modificado 
$ git commit -m "Actualización en una rama"
$ git push origin rama
```
Cabe notar que la forma de hacerlo es muy similar a como se hace con la rama principal, pero las actualizaciones van a dar a la nueva rama.

## Actualizar y combinar ramas

Antes de actualizar o combinar nuestro repositorio es necesario revisar las diferencias entre las ramas que con las que estamos trabajando. Es por ello que el comando **git** tiene una herramienta que nos permite saber cuales son las diferencias entre los archivos. Para ello hay que ejecutar el siguiente comando:
```
$ git diff rama_1 rama_2
```
De esta manera, **git** nos desplegará las diferencias que hay entre las ramas que estamos solicitando. El comando **git** tiene un algoritmo para actualizar las ramas, pero aún así es responsabilidad del usuario revisar que las actualizaciones de su repositorio trabajen de manera adecuada. Para combinar ramas hay que ubicarse con ```checkout``` en la rama que queremos actualizar y posteriormente ejecutamos el siguiente comando:
```
$ git merge rama_de_origen_para_fusionar
```

Frecuentemente trabajamos diferentes etapas o actualizaciones de un mismo repositorio en varios computadoras. Para ello existe un comando que actualiza tu repositorio local con el último ```commit``` del repositorio en internet. Esto muy útil cuando trabajas en la escuela y después en tu casa o en la computadora de alguien más. Este comando es:
```
$ git pull
```
En ocasiones no nos gustan los cambios que hemos realizado en un archivo de nuestro directorio local. Para ello podemos volver a la versión anterior que se encuentra en línea con el siguiente comando:
```
$ git checkout -- archivo_de_la_version_en_linea
```
Si de plano no te gustan los cambios que has realizado a todo el directorio puedes ejecutar la siguiente secuencia:
```
$ git fetch origin
$ git reset --hard origin/master
```

En todos los casos que hagas actualizaciones recuerda revisar el status de tu **git** local y de hacer ```add``` a los archivos modificados.

Regresar a la página principal del [tutorial de git](https://github.com/richmf/tutorial_de_git)

Regresar a las [Herramientas](http://sistemas.fciencias.unam.mx/~rich/Herramientas/index.html)