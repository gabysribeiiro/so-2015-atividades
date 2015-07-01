======================
Glossário de comandos
======================

:Disciplina: Fundamentos de Sistemas Operacionais
:Professor: Jurandy Soares
:Nome: Gabriella da Silva Ribeiro 
:Matrícula: 20141144010812
:Data: 01/07/2015

cat 
O "cat" exibe o que há dentro de determinado arquivo. Ele é útil quando deseja ler ou exibir um arquivo de texto. 
Exemplo: cat TEXTO.txt – Exibe o conteúdo do arquivo TEXTO.txt 
cd 
O comando “cd” serve para acessar e mudar de diretório corrente. Ele é utilizado para a navegação entre as pastas do computador. 
Exemplo: cd /home/baixaki/Desktop – Acessa a pasta correspondente à área de trabalho do usuário baixaki.

cowsay 
Desenvolvido por Tony Monroe, a proposta do Cowsay é promover uma certa interação com o usuário GNU/Linux, sendo que o programa gera a figura de uma vaquinha contando frases variadas toda vez que o terminal é aberto.  
 
1. Para instalar a vaquinha e o seu pacote das frases, digite no terminal (em distribuições baseadas no Debian):  
 
$ sudo apt-get install cowsay fortunes-br  
 
2. Quase pronto! Agora iremos configurar sua inicialização no terminal, para tanto, editaremos o arquivo ".bashrc" com o GEdit ou outro editor de texto similar:  
 
$ gedit .bashrc  
 
3. Desça até a última linha, adicione o seguinte comando no final do arquivo e depois salve:  
 
 
fortune | cowsay 

echo 
echo [opções] [argumentos] 
Os argumentos são repetidos na saída padrão. 
Descrição 
Este comando mostra os argumentos na saída padrão seguido por uma nova linha. 
Algumas opções do comando 
-n : não adiciona uma nova linha após mostrar os argumentos. 
-e : habilita interpretação dos códigos de escape após barra invetida. 
-E : suprime explicitamente a interpretação de códigos de escape após barra invertida. 
São exemplos de códigos de escape: 
\a : alerta (Sino). 
\b : retroceder. 
\c : suprime próxima saída. 
\e : caractere de escape. 
\f : alimentação de página (FF). 
\n : nova linha (NL). 
\r : retorno de carro (CR). 
\t : tabulação horizontal. 
\v : tabulação vertical. 
Exemplos 
O comando 
echo teste 
apenas mostra a palavra "teste" na saída padrão, enquanto o comando 
echo 
mostra uma linha em branco. 
Este comando pode ser usado para exibir todos os nomes de arquivos de um diretório em ordem alfabética. Por exemplo, 
echo /* 
lista o conteúdo do diretório raiz. 
O comando 
echo -e /etc/* "\n" /* 
mostra o conteúdo do diretório /etc, define uma nova linha com o código de escape "\n" e, em seguida, mostra o conteúdo diretório raiz. 
Este comando pode também ser utilizado na programação shell para escrever mensagens na saída padrão. Por exemplo, 
echo 'erro de execução' 
mostra a mensagem definida entre aspas simples no terminal do usuário. 
Para verificar o conteúdo da variável de ambiente PATH, basta digitar na linha de comando 
echo "$PATH" 
 
env 
Executa um programa/comando em um ambiente modificado.
env [opções] [comando]
São algumas das opções deste comando
-u variável : remove a variável de ambiente especificada durante a execução do comando.
-i : ignora todas as variáveis de ambiente.
Comentários sobre as opções do comando
Suponha a existência da seguinte definição no sistema
alias ls=’ls –color=tty’
O uso do comando alias, neste exemplo, significa que, sempre que o usuário digitar
ls
e o sistema executará
ls –color=tty
Portanto, a listagem dos arquivos de um diretório sempre aparecerá colorida. Para fazer com que o sistema ignore as modificações feita pelo comando alias e qualquer variável de ambiente, basta digitar
env -i ls
Observações
O comando env, sem qualquer argumento, lista as variáveis de ambiente.

exit 
Terminar a sessão, ou seja, a shell (mais ajuda digitando man sh ou man csh) 

help 
mostra o HELP (arquivo de ajuda) do comando que você digitou;

HISTTIMEFORMAT="%d/%m/%y" 
Para adicionar a data e hora no comando history.

hostname 
Este comando mostra ou muda o nome do computador na rede.

Algumas opções do comando
-a : mostra o alias da máquina (se for usado).
-i : mostra o(s) endereço(s) IP(s) da máquina.
-s : mostra o nome curto da máquina (até o primeiro '.').
--help : lista as opções do aplicativo.
--version : mostra informações sobre o aplicativo.
Observações
Se o comando hostname for usado sem parâmetros, o nome da máquina é exibido.
Se o comando hostname for seguido por um nome, é alterado o nome da máquina.
O nome da máquina fica armazenado em /etc/hostname.
As informações sobre as máquinas da rede são armazenadas em /etc/hosts.

ifconfig 
Visualizar os ips da nossa máquina, entre outras funções relacionadas com ips

last 
Indica o último login de utilizadores

lastb 
Descrição do comando 

ls 
Exibe os arquivos que estão dentro da pasta na qual o usuário está no momento. 
Para usá-lo basta digitar ls. Existem variações, tais como ls -l, com a qual é possível obter informações mais detalhadas sobre os arquivos, como permissões e tamanho. 

mkdir 
Enquanto o rmdir remove, este comando cria diretórios. 
Exemplo: mkdir DIRETORIO – A pasta DIRETORIO foi criada no local onde o usuário se encontrava.

nome="fulano"
Descrição do comando 

passswd 
Mudar a password do nosso utilizador 

pwd 
Exibe a pasta atual na qual o usuário se encontra. 
Exemplo: Se o usuário baixaki digitar cd ~/ e em seguida digitar pwd, o retorno será /home/baixaki . 

set 
Define variáveis da sessão, ou seja, da shell, na C shell, na bash ou na ksh

tree 
Um programa que pode ser muito útil para apresentar a estrutura de diretórios e subdiretórios no Linux é o comando tree. Sua visualização facilita a análise da estrutura de subdiretórios e arquivos de um dado diretório alvo.

Sua função básica é apresentar no console do Linux a estrutura de diretórios no formato de árvore. Abaixo, um exemplo da saída visual deste comando

tree

Para utilizar este comando, basta:

?
1
tree
Caso o comando não exista, no Debian, para instalá-lo basta:

?
1
aptitude install tree
Além desta utilidade de visualizar graficamente a estrutura de subdiretórios e arquivos, outra utilidade do comando tree é obter a lista txt de todos os subdiretórios existentes dentro de um diretório. Para isto, basta:

?
1
tree -d > lista.txt
Abaixo um exemplo do formato de saída do comando acima apresentado:
./subdiretorio1
./subdiretorio1/diretorio1
./subdiretorio1/diretorio2
./subdiretorio2
./subdiretorio3
./subdiretorio3/diretorio1
./subdiretorio4
./subdiretorio4/diretorio1
./subdiretorio4/diretorio2
./subdiretorio4/diretorio2/diretorio

Outra opção é utilizar o comando ‘find’ para fazer a mesma função. Abaixo um exemplo do comando:

?
1
find . -type d

tty 
O TTY é um comando no Linux usado em uma prompt ou shell de comando que dá informações sobre o terminal que um usuário está no momento. Digitar "tty" em um prompt de comando do Linux ou Unix produzirá uma saída específica exclusiva para aquele terminal.

vim 
Editor de texto full-screen melhorado (vi improved) 

wait 
Descrição do comando 

wall 
Descrição do comando

which 
 Busca de arquivos no sistema de forma muito rápida. Busca por executáveis nos PATHs exportados.
    Ex.: 
      which httpd
      resultado: /usr/sbin/httpd 

    Ex.:
    which X 
    resultado: /usr/bin/X11/X 

while 
Executa um bloco de código enquanto sua condição for verdadeira.
    Ex.: 
        while <condição>;do
            bloco de código/ comando...
        done
    
    Ex.: 
         while true;do
           echo "O velho e bom, Hello World!!!"
         done
    
    Ex.: 
        name="Nação Livre"

        while [ "$name" = "Nação Livre" ];do
          echo "Mundo open source !!!"
          echo "Eu adoro programar !!!"
        done

who 
Mostra-nos quem está logado no sistema 

whoami 
Exibir o nome do usuário. Ex: whoami 

write
Escrever uma mensagem para um usuário. 
Ex: write colega "Mensagem" 
Echo "Mensagem" | write colega 
Cowsay -f koala "Mensagem" | write colega 
 

