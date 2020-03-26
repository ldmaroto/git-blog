# git-blog
Git Quick Reference Blog - Referencia rápida para usar GIT | Tomado del Curso de Platzi.

<h3>Referencia rápida para usar GIT</h3>

<h4><strong>Preparar un repositorio local<strong></br></h4>
<p>Permite crear una área de ensayo (staging) en memoria RAM, y una carpeta repositorio (la carpeta conocida como "/.git/":</p>

```html
git init
```

<h4><strong>Agregar cambios al área de trabajo<strong></br></h4>
<p>Para mostrar los diferentes estados de los archivos en tu directorio de trabajo y área de ensayo (staging):</p>

```html
git status
```

<p>Para ver los cambios entre tu entorno de trabajo y tu área de ensayo (staging):</p>

```html
git diff
```

<p>Para agregar cambios de tu entorno de trabajo a tu área de trabajo (staging). Si utliza ".", ase agrega todos los archivos que de tu entorno de trabajo que no estan en tu área de trabajo (staging), o bien puede tambien especificar el nombre individual de un archivo:</p>

```html
git add .
git add <nombre_de_archivo>
```

<p>Para desacer el paso anterior, utilize:</p>

```html
git rm
```

<p>Del paso anterior, si el archivo está en el caché, para remover los cambios agregados a tu área de trabajo (staging), necesitará agregar la badera --cached y el nombre del archivo:</p>

```html
git rm --cached <archivo>
```

<h4><strong>Crear una instantanea del área de trabajo en la base de datos del repositorio<strong></br></h4>
<p>Para registrar una instantánea permanente de tu área de trabajo (staging) en la base de datos del repositorio. El nombre por defecto del repositorio es "master". Si se omite la bandera -m, Git llamará un editor de texto para completar el comentario, por defecto se usa VIM, pero puede usted programar otros como Visual Studio Code.</p>

``` html
git commit -m "<Comentario>"
```

<p>Del paso anterior, lo siguiente presenta los "cambios específicos" de los archivos a partir de creado el commit. Ante muchos cambios, se usan las fechas "up/donw" para moverse en la pantalla y la tecla "q" para salir:</p>

```
git log --stat
```

<h4><strong>Traer un archivo de una instantánea del repositorio al entorno de trabajo<strong></br></h4>
<p>Traer la imagen de un archivo, de una instatánea de la base de datos hacia el entorno de trabajo. Es importante conocer la referencia de la instantanea de la base de datos del reposotorio, conocido como <commit-id>, el cual es una cadena de caracteres y números. Se puede reemplazar el <commit-id> por el nombre de la rama, ejemplo "master".</p>
  
```html
git checkout <commit-id> <archivo>
```

<h4><strong>Observar contenido del respositorio<strong></br></h4>
<p>En paso anterior, se mencionó sobre la referencia de la instantanea de la base de datos del repositorio, llamado <commit-id>. El siguiente comando, podrá ver el registro de todos los <commit-id> de la base de datos del repositorio:</p>
  
```html
git log
```

<p>Lo mismo del punto anterior, pero aplicado a un archivos específico:</p>

```html
git log <archivo>
```

<h4><strong>Eliminar cambios del repositorio<strong></br></h4>
<p><strong>Advertencia!!!:</strong> Se utiliza sobre todo para deshacer las cosas. Puede borrar todo el historial del repositorio. Uselo entendiendo lo que está haciendo</p>

```html
git reset 
```


<p>Importante, a GIT no le interesa la carpetas, solo los archivos. Las carpetas son consideradas rutas de los archivos:</p>
