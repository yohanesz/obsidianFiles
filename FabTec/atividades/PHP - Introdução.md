## 1. Sintaxe

As páginas contendo algum script PHP devem ser salvas com a extensão `.php`;
Páginas .php podem ter código `HTML e código PHP`;
Para finalizar uma linha de código PHP é usado o `ponto e vírgula`;
Para iniciar um bloco de script em PHP é necessário usar o padrão abaixo:
````php
<?php
// comandos
?>
````

#### Variáveis: 
Para declarar uma variável usa-se o símbolo `$`;
PHP 
PHP é case sensitive;
Tipos: `inteiro, ponto flutuante, string, array e objeto`

Exemplos:
````php
<?php

$muitoLouco = 1; //Inteiro
$muitoLouco = "String" //String
$muitoLouco = 1.24 //Float

?>
````

Strings podem ser atribuídas de duas maneiras: 

1 - `aspas simples (')`:
Desta maneira, o valor da variável
será exatamente o texto contido entre as
aspas (com exceção de \\ e \'.

2 - `aspas duplas (")`:
Desta maneira, qualquer variável ou
carácter de escape será expandido antes de ser atribuído.
(troca $exemplo pela variável; aceita /n).

Comando para mostrar valores:
````php
<?php

$texto = “Rodrigo Curvêllo”;
echo $texto;

//

$nome = “Rodrigo”;
$sobrenome = “ Curvêllo”;
echo “Seu nome completo é”.$nome.” “.$sobrenome;

?>
````

PESQUISAR SOBRE NGINX