# Lista-de-Exercicios-Shell

#### **1 Problema**
Crie um script que solicite ao usu´ario digitar o seu nome e imprime o conte´udo
no terminal.

1.1 Exemplo
Digite o seu nome: Idris Elba
Bom dia Idris Elba

    #!/bin/bash
    echo "Digite seu nome"
    read nome
    echo "bom dia $nome"
    
#### **2 Problema** #### **1 Problema**   
Crie um script que multiplique dois n´umeros que o usu´ario informar.

Primeiro Numero: 2
Segundo Numero: 3
Resultado: 6

    #!/bin/bash
    echo "Digite o primeiro numero"
    read primeiro
    echo "Digite o segundo numero"
    read segundo
    echo "a resposta é $[ $primeiro * $segundo]"
 
#### **3 Problema**

    #!/bin/bash
    echo "Digite um numero"
    read numero
    if [ $numero -ge 0 ]; then 
            echo "Positivo"
    else
            echo "Negativo"
    fi
    
#### **4 Problema**  
Crie um script resolva a tabuada do n´umero informado pelo usu´ario.

Numero: 2
2x0 = 1
2x1 = 2
...
2x10 = 20

    #!/bin/bash
    echo "Digite um numero"
    read numero
    y=1
    while [  $y -le 10  ]; do
       echo "$[$numero * $y]"
       y=$[ $y + 1 ]
    done
    
#### **5 Problema**   
Crie um script que apresente duas op¸c˜oes ao usu´ario. A primeira op¸c˜ao dever´a
mostrar o calend´ario. A segunda op¸c˜ao deve mostrar a lista de arquivos do
diret´orio.

Opcoes:
—–
1: Calend´ario
2: Listas de arquivos do diret´orio
—–
Informe sua opcao: 2
—–
Mostrar arquivos do diret´orio
—–
arquivo.txt diretorio arquivo2.txt

    #!/bin/bash
    echo "Opcoes
    ----
    1: Calendario
    ----
    2: Arquivo do diretorio"
    read opcao

    if [ $opcao = 1 ]; then
            echo | cal
    else 
            echo | ls
    fi
