# git-blog
Git Quick Reference Blog - Referencia rápida para usar GIT | Tomado del Curso de Platzi.

<h3>Referencia rápida para usar GIT.</h3>

<h4><strong>1. Preparar un repositorio local.<strong></br></h4>
<p>Permite crear una área de ensayo (staging) en memoria RAM, y una carpeta para la base de datos del repositorio (la carpeta conocida como "/.git/", donde se guardan los cambios atómicos de nuestro código):</p>

```html
$ git init
```

<h4><strong>2. Agregar cambios al área de trabajo<strong></br></h4>
<p>Para mostrar los diferentes estados de los archivos (si estan: "Tracked" o "Untracked") en tu entorno de trabajo, utilice el próximo comando. Si un archivo está "Tracked", este formará parte del área de trabajo (staging):</p>

```html
$ git status
```

<p>Para observar los cambios entre tu entorno de trabajo y tu área de ensayo (staging):</p>

```html
$ git diff
```

<p>Para agregar cambios de tu entorno de trabajo a tu área de trabajo (staging). Si utliza ".", se agrega todos los archivos con estado "Untracked" de tu entorno de trabajo a tu área de trabajo (staging). Tambien puedes especificar el nombre individual de un archivo:</p>

```html
$ git add .
$ git add <nombre_de_archivo>
```

<p>Para desacer el paso anterior, es decir sacar un archivo del áre de trabajo (cambiar el estado "Tracked" a "Untracked"), utilize:</p>

```html
$ git rm
```

<p>Del paso anterior, si el archivo está en el caché, para remover los cambios agregados de tu área de trabajo (staging), necesitará agregar la badera --cached y el nombre del archivo:</p>

```html
$ git rm --cached <archivo>
```

<h4><strong>3. Crear una instantanea del área de trabajo en la base de datos del repositorio<strong></br></h4>
<p>Para registrar una instantánea permanente de tu área de trabajo (staging) en la base de datos del repositorio. El nombre por defecto del repositorio es "master". Si se omite la bandera -m, Git llamará un editor de texto para completar el comentario, por defecto se usa VIM, pero puede usted programar otros como Visual Studio Code.</p>

``` html
$ git commit -m "<Comentario>"
```

<p>Recordar que para hacer un "commit", Git necesita saber quienes somos nosotros, para ello necesitas corres estos comandos, en el entorno global de Git:</p>

``` html
$ git config --global user.email "<correo_electronico>"
$ git config --global user.name "<nombre_de_usuario>"
```

<p>Si necesita ver la configuración por defecto de tu "Git", use este comando:</p>

``` html
$ git config --list
```

<p>Si necesita ver donde está guardado la configuración de tu "Git", use este comando:</p>

``` html
$ git config --list --show-origin
```

<p>Una vez realizado el "commit", lo siguiente presenta los cambios en el repositorio:</p>

```html
$ git log
$ git log <archivo>
```

<p>Lo siguiente presenta los "cambios específicos" de los archivos a partir de creado el "commit". Ante muchos cambios, se usan las fechas "up/donw" para moverse en la pantalla y la tecla "q" para salir:</p>

```html
$ git log --stat
$ git log --stat <archivo>
```

<p>Si necesita ver con detalle los cambios de un determinado archivo en el repositorio (presentará todos los commit que afectaron al archivo), utilice:</p>

```html
$ git show <archivo>
```

<h4><strong>4. Traer un archivo de una instantánea del repositorio al entorno de trabajo<strong></br></h4>
<p>Traer la imagen de un archivo, de una instatánea de la base de datos hacia el entorno de trabajo. Es importante conocer la referencia de la instantanea de la base de datos del reposotorio, conocido como <commit-id>, el cual es una cadena de caracteres y números. Se puede reemplazar el <commit-id> por el nombre de la rama, ejemplo "master".</p>
  
```html
$ git checkout <commit-id> <archivo>
```

<h4><strong>5. Observar contenido del respositorio<strong></br></h4>
<p>En paso anterior, se mencionó sobre la referencia de la instantanea de la base de datos del repositorio, llamado <commit-id>. El siguiente comando, podrá ver el registro de todos los <commit-id> de la base de datos del repositorio:</p>
  
```html
git log
```

<p>Lo mismo del punto anterior, pero aplicado a un archivos específico:</p>

```html
git log <archivo>
```

<h4><strong>6. Eliminar cambios del repositorio<strong></br></h4>
<p><strong>Advertencia!!!:</strong> Se utiliza sobre todo para deshacer las cosas. Puede borrar todo el historial del repositorio. Uselo entendiendo lo que está haciendo</p>

```html
git reset 
```

<h4><strong>7. Crear una rama<strong></br></h4>
<p>Basicamente es copiar una rama existente, por lo general "master". </p>

```html
$ git branch <nombre_de_rama> 
```


<p>Importante, a GIT no le interesa la carpetas, solo los archivos. Las carpetas son consideradas rutas de los archivos:</p>
<p>Nombre comunes de Ramas: master, development, hotfix.</p>
