## Iniciar Git
git int


## Configuración de Git
git config

git config --list

git config --list --show origin

git config --list --show-origin

git config --global

git config --global user.name "SC"

git config --global user.email "jesuscastellanospaez@hotmail.com"


## Agragar a la zona de preparación
git add Archivo.txt

git add .


## Ver estado
git status


## Quitar de la zona de preparación
git rm --cached archivo.txt (Quitar de la zona de preparación).


## Realizar commint
git commit -m "Este es el pimer commit de este archivo"

git commit -am "Este es el pimer commit de este archivo"


## Ver el historial de cambios del archivo
git log

git log Archivo.txt


## Muestra todos los cambios sobre un archivo
git show Archivo.txt


## Comparar versiones
git diff commint commint


## Volver a una versión anterior
git reset commit --hard (borramos todos los cambios y lo que tengamos en staging)

git reset commit --soft (soft conservamos cambios y lo que tengamos en staging)

git checkout (commit) Archivo.txt

git checkout (rama) Archivo.txt


## Ver Cambio en bytes
git log --stat(Cambio en bytes)


## Crear una rama
git branch (branchName)


## Cambiar de rama
git checkout (branchName)


## Merge entre branchs
git merge (branchName)


## Traer un repositorio externo
git remote add origin (url)

git remote (muestra el origen)

git remote -v(es verval)

git pull origin master --allow-unrelated-histories (Fuerza la union de las diferentes historias)

git pull origin master (Descarga cambios)

git push (origin) (master) (Sube Cambios)


## Seguridad
ssh-keygen -t rsa -b 4096 -C "jesuscastellanospaez@gmail.com" (crea la llave publica y privada)

eval $(ssh-agent -s) (saber si el agente ssh esta ejecuntando)

ssh-add ~/.ssh/id_rsa (agregar la llave privada)

git remote set-url origin git@github.com:gsuscastellanosSC/hyperblog.git (cambiar url para que sea con ssh)


## TAGS
git log --all(Muesta toda la historia)

git log --all --graph (Muestra toda la historia con la ineracción de las ramas)

git log --all --graph --decorate --oneline

alias arbolito="git log --all --graph --decorate --oneline"(forma de alias en linux)

git tag -a v0.1 -m "apendiendo tags en git" (hash del commit) (crear un tag)

git show-ref --tags

git push origin --tags (enviar los tags al repositorio remoto)

git tag -d v0.1   && $ git push origin :refs/tags/v0.1 (Borrar tags)


## ramas
git show-branch --all (¿Cuales branch existen y sus historias)

gitk (igual que la anterior per con gui)

git push origin :[nombre_branch] (Elimina rama remota)


## Crear fuente nueva
git remote add upstream (url-github)

git pull upstream master (trae todos los cabios de master del origen upstream)