Ao digitar o comando `ls -l`, uma série de informações é exibida, onde na 1ª coluna:
* A primeira letra (`d`) indica se aquele item é um diretório.

Cada item só pode pertencer à um único grupo e ter somente um único dono.

Depois da primeira letra, as 9 letras seguintes são separadas em 3 grupos de 3 letras:
* **user**;
* **group**;
* **other**;

A letra `x` em relação a um diretório, indica que o usuário tem permissão para entrar dentro da pasta, mas caso seja um arquivo, significa que tem direito de execução.

A representação númeral é a seguinte:
* **7** = *rwx*;
* **6** = *rw-*;
* **5** = *r-x*;
* **4** = *r--*;
* **3** = *-wx*;
* **2** = *-w-*;
* **1** = *--x*;
* **0** = *---*;