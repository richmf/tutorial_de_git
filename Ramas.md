# Ramas

Las *Ramas* son utilizadas para llevar un control de las versiones sin afectar la versión original o principal (*master*). Ésto resulta de mucha utilidad ya que si tenemos un programa que sabemos que funciona bien, podemos empezar a generar una nueva versión manteniendo la anterior intacta hasta el momento en que tengamos la necesidad de fusionarlas.

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
Al igual que con la rama principal, es necesario hacer hacer *add* y  *commit* a los archivos modificados. En este caso para que las actualizaciones lleguen al repositorio en **GitHub** es con el siguiente comando:
```
$ git push origin mi_rama
```
De esta manera podemos tener en el mismo repositorio diferentes versiones, típicamente una o varias que estamos modificando para mejorar la principal o *master*.

## Actualizar y combinar ramas

Antes de actualizar o combinar nuestro repositorio

Regresar a la página principal del [tutorial](https://github.com/richmf/tutorial_de_git)

Regresar a las [Herramientas](http://sistemas.fciencias.unam.mx/~rich/herramientas/index.html)