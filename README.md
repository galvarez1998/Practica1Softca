		Practica 1 Git

1. Crear un repositorio en vuestro GitHub llamado Practica1Softca
2. Clonar vuestro repositorio en local.

	$ git clone  http://github.com/galvarez1998/Practica1Softca.git

README
3. Crear (si no lo habéis creado ya) en vuestro repositorio
local  un documento README.md

	$ touch README.dm 

Commit inicial
4. Añadir al README.md los comandos utilizados hasta ahora
y hacer un commit inicial con el mensaje commit inicial.

	$ git add README.md
	$ git commit –m “commit inicial”

Push inicial
5. Subir los cambios al repositorio remoto.

	$ git push origin 

Ignorar archivos
6. Crear en el repositorio local un fichero llamado privado.txt.

	$ touch privado.txt

7. Crear en el repositorio local una carpeta llamada privada.

	$ mkdir private

8. Realizar los cambios oportunos para que tanto el archivo
como la carpeta sea ignorada por git.

	$ touch .gitignore
	$ vim .gitignore 
		# ignore el archivo privado.txt
		privado.txt
		# ignore el archivo privado
		privada/
	$ git add .
 
Añadir fichero 1.txt
9. Añadir fichero 1.txt al repositorio local.

	$ touch 1.txt
	$ git add 1.txt

Crear el tag v0.1
10. Crear un tag v0.1.

	$ git tag -a v0.1

Subir el tag v0.1
11. Subir los cambios al repositorio remoto.
 
	$ git tag v0.1 -m "message"

Crear una rama v0.2
12. Crear una rama v0.2.

	$ git branch v0.2

13. Posiciona tu carpeta de trabajo en esta rama.

	$ git checkout v0.2

Añadir fichero 2.txt
14. Añadir un fichero 2.txt en la rama v0.2.

	$ touch 2.txt

Crear rama remota v0.2
15. Subir los cambios al repositorio remoto.

	$ git add 2.txt
	$ git commit –m “message”
	$ git push origin

16. Posicionarse en la rama master.

	$ git checkout master

Merge directo
17.Hacer un merge de la rama v0.2 en la rama master.

	$ git merge v0.2

Merge con conflicto
18. En la rama master poner Hola en el fichero
1.txt y hacer commit.

	$ vim 1.txt
        	Hola
	$ git add 1.txt
	$ git commit –m “message”

19. Posicionarse en la rama v0.2 y poner Adios
en el fichero "1.txt" y hacer commit.

	$ git checkout v0.2
	$ vim 1.txt
        	Adios
	$ git add 1.txt
	$ git commit –m “message”

20. Posicionarse de nuevo en la rama master y hacer
un merge con la rama v0.2

	$ git checkout master
	$ git merge v0.2

Listado de ramas
21. Listar las ramas con merge y las ramas sin merge.
	
	$ git branch --merged	 
	$ git branch --no-merged

Arreglar conflicto
22. Arreglar el conflicto anterior y hacer un commit.
    
    $ git add .
	$ git commit -m "message"

Borrar rama
23. Crear un tag v0.2

	$ git tag v0.2 -m "message"

24. Borrar la rama v0.2

	$ git branch –D v0.2

Listado de cambios
25. Listar los distintos commits con sus ramas y sus tags.
 
	$ git log --oneline