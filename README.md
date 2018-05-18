## Proyecto de Control de Versiones

Esta es la página de github.io que hostea la documentación del proyecto


### Conceptos básicos

**Workspace:** Es el estado real de nuestros ficheros. Tal y como los vemos en nuestro editor.

**Stage:** Aquí se encuentran los cambios sobre nuestros ficheros que se incluirán en el próximo commit. Cuando hacemos un git add, un git rm o un git mv, estamos introduciendo cambios en el stage, indicándole a Git que en el próximo commit esos cambios irán incluidos.

**Commits (locales)**: Cada commit es un grupo de cambios sobre uno o varios ficheros, con una descripción, una fecha, un autor, etc. La gran diferencia con SVN es que los commits en Git son locales hasta que no se efectúa la subida al servidor. Estos commits locales (importante que sean locales) pueden ser modificados sin peligro (con modificados quiero decir que se les pueden añadir más cambios, actualizar su mensaje o incluso eliminarlos).

**Commits (remotos)**: Cuando se suben cambios al servidor (o como se le llama en Git: el remoto), se considera que estos entran a formar parte del histórico compartido entre los desarrolladores del proyecto y, por lo tanto, no es buena práctica modificarlos del mismo modo en que se hace cuando los commits son locales (además hacerlo puede provocar importantes quebraderos de cabeza).

**1- Cambios en mi workspace**

**2- Se agregan los cambios al stage (add)**

**3- Commit**

**4- Se suben los cambios al remoto (push)**




### Primeros pasos

$ git init

$ git config --global user.name [name]

$ git config --global user.email [email]

$ git config --global core.autocrlf input



$ git remote add origin **[URL]**

Esto creará un remote con la URL indicada y el nombre "origin"

Para ver los remotes que ya están asignados se utiliza **git remote -v**




### Git status

git status -sb

Muestra: 

**Changes to be commited:** Esta sección muestra los cambios añadidos al stage y que formarán parte del próximo commit.

**Changes not staged for commit:** En esta sección se muestran los cambios que se han hecho sobre nuestros ficheros, pero que no han sido añadidos al stage y por tanto no formarán parte del próximo commit.

**Untracked files:** Aquí se ven los ficheros que están en nuestro workspace de los que Git no tiene conocimiento aún. Es decir, no forman parte del control de versiones y por tanto, lógicamente, no formarán parte del próximo commit.





### Añadir cambios al stage

$ git add
$ git add 1.txt 2.txt 3.txt

Para mover o renombrar ficheros:

$ git mv oldname.txt newname.txt
$ git mv 1.txt carpeta/carpeta


Para eliminar ficheros:

$ git rm 1.txt



Para ahorrarnos los dos pasos de add y rm, se utiliza un solo comando:

$ git add --all




### Quitar cambios al stage

Si queremos hacer unstage (quitar del stage) de los cambios sobre 2.txt, ejecutamos el comando **$ git reset HEAD 1.txt 2.txt 3.txt**

Para quitar todos los cambios usamos el comando **$ git reset HEAD .**







### Listar ramas
Para listar las ramas existentes en nuestro repositorio, usaremos:

git branch -va

```
$ git branch -va
* master                  bed4c52 Commit de ejemplo
  dev                     bd81885 Another commit
  remotes/origin/master   bed4c52 Commit de ejemplo
  remotes/origin/dev      bed4c52 Commit de ejemplo
```




### Crear ramas
Para crear una nueva rama en nuestro repositorio y  movernos a ella, usamos el comando:


$ git checkout -b mi-rama

La nueva rama que estamos creando estará **basada**(incluído el último commit) en la rama en la que nos encontremos en ese momento.



También podemos crear una rama nueva basada en una remota en lugar de local.

$ git checkout -b mi-rama origin/master



### Movernos entre ramas

Utilizaremos el comando

$ git checkout mi-rama

Si la rama a la que vamos afecta **(entra en conflicto)** a los cambios que tengamos en nuestro workspace o stage, no se realizará el cambio de rama.

Para poder hacerlo tendremos que **limpiar el workspace y el stage** antes de movernos de rama.
Para ello podemos utilizar dos métodos:


**Hacer un commit de todos los cambios:** No es lo recomendado, ya que estaremos haciendo un commit incluyendo aquello que supuestamente está aun por terminar.

**Guardar el estado en el stash:** Guardamos los cambios en el stash para sacarlos posteriormente.




### Eliminar ramas

$ git branch -D mi-rama




### Mostrar historial de commits

Utilizaremos el comando

$ git status

El resultado se muestra en orden cronológico descendente



