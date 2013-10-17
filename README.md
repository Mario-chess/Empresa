Empresa
=======

Es una WebApp destinada a los empresarios que deseen registrar sus empresas en la MobileApp Ubiatech.

Pasos para manejar GitHub
=========================

Hasta el momento se espera que la máquina de desarrollo este sincronizada con GutHub a trávés
de una clave SSH.

* git init
* git add . (Con el punto solo se cargaran los cambios realizados)
* git commit -m 'Comentario'
* git remote add origin git@github.com:Mario-chess/Empresa.git

Hasta acá es lo básico. Ahora dos comandos que siempre deben ser manejados, no obligatoriamente, pero si por buena practica.

* git pull origin master

Esto permite actualizar nuestro Working Copy, es decir trabajar con lo último.
Con esto evitamos tener que estar clonando a cada momento el proyecto.

* git push origin master

Se usa cuando estamos seguros que los cambios realizados funcionan corretamente, con esto
se actualizará el "MainLine", es importante estar seguros de que funciona, ya que en un futuro
los demás miembros del Equipo trabajaran sobre dicha versión.

Diferencia entre Branches y Forks
=================================

* Branches:

* Forks:

Manejo de Branches
==================

Debe estar claro, que un Brach, representa una nueva Funcionalidad (Ej. Modulo de Ventas, Modulo de Compras, etc.).

Esto significa que si modificamos un branch en particular, borramos o añadimos archivos, ésta incluirá dichos cambios pero no así las demás ramas.

Crear un nuevo Branch:

* git branch Nuevo_Branch

Cambiar de un Branch a otro. Por defecto nos encontramos en el Brach Master.

* git checkout Otro_Brach

Para comprobar en que Branch (Rama) nos encontramos:

* git branch

En caso de haber creado un branch por equivocación se puede usar este comando, ya que desde la interfaz no se puede eliminar un Branch.

* git push origin :branch_to_delete

En caso de que hayamos creado un Brach Local con:

* git branch Name_Local_Branch

Podemos Borrarlo usando:

* it branch -d Name_Local_Branch