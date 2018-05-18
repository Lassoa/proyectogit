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

### 

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Lassoa/proyectogit/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
