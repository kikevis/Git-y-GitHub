ssh-keygen -t rsa -b 4096 -C "tu@email.com"

eval $(ssh-agent -s)
eval "$(ssh-agent -s)"
(Agent pid #)

ssh-add ruta donde esta la llave privada
ssh-add ~/.ssh/id_rsa

Linux
AddKeysToAgent yes
UseKeychain yes
IdentityFile ruta-donde-guardaste-tu-llave-privada

ssh-add -K ruta-donde-guardaste-tu-llave-privada