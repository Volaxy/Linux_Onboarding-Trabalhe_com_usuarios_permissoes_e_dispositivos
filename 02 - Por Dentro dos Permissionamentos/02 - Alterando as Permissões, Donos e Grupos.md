Por padrão, ao criar um diretório, o permissionamento é `drwxr-xr-x`.

O comando `chown ubuntu:ubuntu DIRECTORY/FILE` muda o grupo ou dono de um diretório/arquivo, onde antes dos `:` será definido o dono e depois dos `:` será definido o grupo.

O comando `chmod CODECODECODE DIRECTORY/FILE` Para mudar o permissionamento de um diretório/arquivo, onde `CODE` é o código que representa um conjunto de permissões que pode ser atribuida ao grupo de 3 caracteres. Ex.: `chmod 770 /projects/`.

O comando `chmod [ugo][+-][rwxs]` modifica o acesso individualmente de um grupo de letras, onde:
* O primeiro parâmetro é qual será o tipo:
    * **u** - *Users*;
    * **g** - *Group*;
    * **o** - *Others*;
* O sinal que será usado:
    * **+** - Adicionar;
    * **-** - Remover;
* A permissão que será concedida.
    * **s** - Permissão especial de grupo, que no caso herda as permissões de grupo do pai.

O comando `ls -s FOLDER TARGET_NAME` cria um link para um arquivo ou pasta do sistema.