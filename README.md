# Lista-de-Exercicios-Shell

#### **1 Problema**
Crie um script que solicite ao usuário digitar o seu nome e imprime o conteúdo
no terminal.

1.1 Exemplo
Digite o seu nome: Idris Elba
Bom dia Idris Elba

    #!/bin/bash
    echo "Digite seu nome"
    read nome
    echo "bom dia $nome"
    
#### **2 Problema** #### **1 Problema**   
Crie um script que multiplique dois números que o usuário informar.

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
Crie um script que identifique se o usuário informou um número positivo, negativo ou zero.
Numero: 2
Positivo

    #!/bin/bash
    echo "Digite um numero"
    read numero
    if [ $numero -ge 0 ]; then 
            echo "Positivo"
    else
            echo "Negativo"
    fi
    
#### **4 Problema**  
Crie um script resolva a tabuada do número informado pelo usuário.

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
Crie um script que apresente duas opções ao usuário. A primeira opção deverá
mostrar o calendário. A segunda opção deve mostrar a lista de arquivos do
diretório

Opcoes:
—–
1: Calendário
2: Listas de arquivos do diretório
—–
Informe sua opcao: 2
—–
Mostrar arquivos do diretório
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
