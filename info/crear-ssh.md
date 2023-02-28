<!-- Windows -->
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
ssh-keygen -t rsa -b 4096 -C "villasanchezg22@gmail.com"
enter

eval $(ssh-agent -s)
eval "$(ssh-agent -s)" //mac
(Agent pid #)

ssh-add ruta donde esta la llave privada
ssh-add ~/.ssh/id_rsa

<!-- Linux -->
AddKeysToAgent yes
UseKeychain yes
IdentityFile ruta-donde-guardaste-tu-llave-privada

ssh-add -K ruta-donde-guardaste-tu-llave-privada

<!-- Repositorio -->
Agregar clave publica en GitHub

git remote -v

git remote set-url origin url-ssh-repositorio //github
git remote add url-ssh-repositorio //gitlab
git remote -v

git pull origin main
yes
git pull origin main