O comando `umount PATH` desmonta um disco (pode ser passado tanto o dispositivo quanto o diretório como parâmetro).

O comando `mount -a` é o comando que é executado quando o sistema inicializa para montagem dos discos.

> Assim, caso seja necessário verificar se as modificações feitas no arquivo */etc/fstab* estão feitas de forma correta, esse comando pode ser usado para teste de montagem, e caso ocorra algum erro, o terminal vai informar o erro na tela.