A convensão quando se cria um disco, é criar na pasta */media*, onde vai ser armazenado todos os discos montados.

O comando `mount DISK DIR` monta um disco no diretório especificado, Ex.: `mount /dev/sdb1 /media/disk2`, disponibilizando o ponto de montagem para os usuários do sistema..

> Essa formatação não foi feita de forma automática, então caso a máquina seja reiniciada, o disco formatado não vai estar disponível para os usuários

O arquivo */etc/fstab* armazena os ponteiros que montam os discos no sistema quando a máquina é iniciada.

> Caso seja editado de forma incorreta, o sistema pode dar problemas na inicialização

O comando `blkid` mostra os **UUID's** dos dispositivos.

> Para motivos de backup, o arquivo */etc/fstab* pode ser copiado como um backup na mesma pasta da seguinte forma (estando dentro da pasta */etc/*): `sudo cp fstab fstab.bk`, assim, caso dê problemas na inicialização, vai existir um arquivo de backup.

Para montagem automática do disco quando o sistema iniciar, é precisa editar o arquivo */etc/fstab*, pode ser feito da seguinte forma (estando na pasta */etc/*):
1. Abrir o editor de textos: `vi fstab`;
1. Colocar o registro do novo disco escrevendo o seguinte: `UUID="7d42ce14-f46c-432a-97fe-74b64200f532" /media/disk2 ext4 defaults 0 2`, onde:
    * O 1º parâmetro informa o *UUID* do disco;
    * O 2º parâmetro informa o diretório do disco;
    * O 3º parâmetro informa o sistema de arquivos;
    * O 4º parâmetro informa as *flags*;
    * O 5º parâmetro informa é a ordem em que vão ser checadas as inconsistências no disco na hora da inicialização;
> A linha também poderia ser escrita da seguinte forma: `/dev/sdb1 /media/disk2 ext4 defaults 0 2`