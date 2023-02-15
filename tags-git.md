<!-- Tags -->
git log --all --graph --decorate --oneline //historia del proyecto

git tag -a v0.1 -m "Primer tag" # //agregar tag al commmit

git show-ref --tags //etiquetas creadas

git push origin --tags //enviar etiquetas al repositorio

git tag -d nombre-tag //borrar tag local

git push origin :refs/tags/nombre-tag //borrar tag de github

<!-- alias en git -->
alias arbolito = "git log --all --graph --decorate --oneline"