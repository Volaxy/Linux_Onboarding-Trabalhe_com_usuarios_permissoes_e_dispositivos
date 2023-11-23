O comando `su - USER` muda do usuário atual para outro, onde o *USER* é o nome do usuário que foi criado.

O comando `sudo group GROUP_NAME` cria um grupo.

O comando `sudo usermod -aG GROUP_NAME USER_NAME` adiciona um usuário a um grupo, onde:
* `-a`: Adiciona o usuário ao grupo;
* `-G`: Adicione o usuário aos grupos suplementares;
* `-g`: Troca o grupo primário do usuário;

No arquivo */etc/group* é possível adicionar um usuário à um grupo colocando o nome do usuário após os `:`, Ex.: `projects:x:1000:test,test1`.

O comando `sudo userdel USER_NAME` apaga um usuário, e o `sudo groupdel apaga um grupo`.