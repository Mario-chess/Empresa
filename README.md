Trabajando con GitHub
=========================

Para comenzar se espera que la máquina de desarrollo este sincronizada con GitHub a trávés de una clave SSH.

Ahora los pasos básicos que se deben realizar para interactuar con el Repositorio son:

* git init
* git add . (Con el punto solo se cargaran los cambios realizados)
* git commit -m 'Comentario'
* git remote add origin git@github.com:Mario-chess/Empresa.git


Hasta el momento vimos lo básico. Ahora aprenderemos dos comandos que siempre deben ser manejados, practicamente son el alma de todo.

* git pull origin master

Esto permite actualizar nuestro __Working Copy__, es decir trabajar con lo último.
Con esto evitamos tener que clonar a cada momento el proyecto.

* git push origin master

Se usa cuando estamos seguros que los cambios realizados funcionan corretamente, haciendo esto
se actualiza el __Branch__ sobre el cual se está trabajando (más adelante profundizaremos en lo que son los Branches), Hay que tener en cuenta que cuando se realizan cambios en el MainLine es necesario estar seguros de que nuestros cambios funcionan, ya que en un futuro
los demás miembros del Equipo trabajaran sobre dicha versión.

## Diferencia entre Branches y Forks [Ver]
(http://stackoverflow.com/questions/3329943/git-branch-fork-fetch-merge-rebase-and-clone-what-are-the-differences)

* Branches: 

* Forks:

### ¿Qué son los Pull Request? 

## Manejo de Branches


Debe estar claro, que un Brach, representa una nueva Funcionalidad (Ej. Modulo de Ventas, Modulo de Compras, etc.).

Esto significa que si modificamos un branch en particular, borramos o añadimos archivos, ésta incluirá dichos cambios pero no así las demás ramas.

__Crear un nuevo Branch:__

* git branch Nuevo_Branch

__Cambiar de un Branch a otro. Por defecto nos encontramos en el Brach Master.__

* git checkout Otro_Brach

__Para comprobar en que Branch (Rama) nos encontramos:__

* git branch

En caso de haber creado un branch por equivocación se puede usar este comando, ya que desde la interfaz no se puede eliminar un Branch.

* git push origin :branch_to_delete

En caso de que hayamos creado un Brach Local con:

* git branch Name_Local_Branch

Podemos Borrarlo usando:

* git branch -d Name_Local_Branch

## ¿Cómo mantener un MainLine?


Tener varios Branches significa que tenemos muchas funcionalidades ramificadas, pero hay que tener en cuenta que tener demasidas ramas dificultará la tarea de mantener un MainLine Completo.

Supongamos que tengo un Branch "Modulo de ventas", trabajo sobre el y lo subo al repositorio, este Branch no esta aún en el MainLine, pero se sabe que este modulo esta completo y funciona correctamente y por tanto se lo debe agregar al MainLine. Para lograr esto lo que se debe hacer es:

__Situarnos en el Branch Master, que representa nuestro MainLine:__

* git checkout master

__Y ahora mezclaremos nuestro master con el Brach (Funcionalidad) Modulo_ventas:__

* git merge Modulo_ventas
* git push origin master

Una vez que la nueva funcionalidad fue aceptada y adherida al Mainline, ya no tiene sentido mantenerla y podemos borrarla:

* git branch -d Modulo_ventas

## ¿Cómo volvemos a un estado anterior?

__Deshacer un Merge__ para volver a un estado antes de mezclar las ramas:

* git reset --hard HEAD

__Ojo:__ Con esto volvemos al estado anterior del merge en nuestra __máquina de desarrollo.__, es necesario hacer un push nuevamente.

__Deshacer un commit__ en caso de que nos demos cuenta que no funciona como debería.

* git revert HEAD

Y posteriormente debemos hacer un nuevo push.

__Ojo:__ Solo se puede deshacer el último commit con este comando.

__Si se quiere deshacer un commit anterior__, se puede usar:

* git revert (parametros)

Aunque su uso requiere de mucho cuidado.

http://blog.solucionex.com/git/borrar-ultimo-commit-con-reset-y-revert-en-git

# Trabajando sobre el repositorio de otra persona

https://help.github.com/articles/fetching-a-remote


## NOTA


_Por costumbre yo suelo poner el nombre del Branch al final de cada pull y push, pero no es necesario, ya que basta con poner "git push origin"  y "git pull origin", ya que desde que hacemos el checkout .... se sabe cual Branch tiene el control de las operaciones._