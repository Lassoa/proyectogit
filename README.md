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

git init

git config --global user.name [name]

git config --global user.email [email]

git config --global core.autocrlf input



git remote add origin **[URL]**

Esto creará un remote con la URL indicada y el nombre "origin"

Para ver los remotes que ya están asignados se utiliza **git remote -v**




### Git status

Muestra: 

**Changes to be commited:** Esta sección muestra los cambios añadidos al stage y que formarán parte del próximo commit.

**Changes not staged for commit:** En esta sección se muestran los cambios que se han hecho sobre nuestros ficheros, pero que no han sido añadidos al stage y por tanto no formarán parte del próximo commit.

**Untracked files:** Aquí se ven los ficheros que están en nuestro workspace de los que Git no tiene conocimiento aún. Es decir, no forman parte del control de versiones y por tanto, lógicamente, no formarán parte del próximo commit.


