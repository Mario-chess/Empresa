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

Conforme vayamos aprendiendo, vamos actualizando este Doc.


En caso de haber creado un branch por equivocación se puede usar este comando, ya que desde la interfaz no se puede eliminar un Branch.

* git push origin :branch_to_delete