
### atividade - serialização

1 - O que é um plano serial? 

R: Quando as transações são executadas uma após a outra, em série, sem sobreposição ou paralelismo. 

2 - O que é um plano serializável? 

R: Quando podemos alterar a ordem e o resultado final da execução das transações seja equivalente a algum plano serial.

3 - Por que um plano serial é considerado correto? 

R: Um plano serial é considerado correto porque garante a consistência dos dados. 

4 - Por que um plano serializável é considerado correto?

R: Um plano serializável é considerado correto porque mantém a consistência dos dados, assim como um plano serial, enquanto permite uma execução mais eficiente, permitindo que as transações sejam executadas em paralelo ou de forma intercalada. Isso é importante em sistemas de banco de dados com alto volume de transações, onde a execução serial de transações pode causar um gargalo de desempenho. No entanto, ao garantir que o resultado final seja equivalente a algum plano serial, mesmo que as transações sejam executadas concorrentemente, a integridade dos dados é preservada.

5 - Discuta como a seriabilidade é usada para garantir o controle de concorrência em um sistema de banco de dados.

R: Através de uma técnica de controle de concorrência, e não pelo teste de seriabilidade

Dentro de 2 transações a seriabilidade garante o controle de concorrência pois as operações que são executadas devem seguir o mesmo resultado de um plano serial propriamente dito, porém usando operações concorrentes executadas intercaladamente. 

6 - 

| T1               |        T2         |
| :--------------- | :---------------: |
| ler_item(x);     |   ler_item(x);    |
| x: = x - n;      |    x: = x + m;    |
| escrever_item(x) | escrever_item(x); |
| ler_item(y);     |                   |
| y: = y + n;      |                   |
| escrever_item(y) |                   |

6.1 - Liste todos os planos possíveis para as transações da figura acima e determine quais são conflito serializáveis (correto) e quais não são.



7 - Quais dos seguintes planos é serializável (conflito)?
Para cada plano seriálizavel, determine os planos seriais e equivalentes

a) r1(x); r3(x); w1(x); r2(x); w3(x);
b) r1(x); r3(x); w3(x); w1(x); r2(x);
c) r3(x); r2(x); w3(x); r1(x); w1(x);
d) r3(x); r2(x); r1(x); w3(x); w1(x);

r = read
w = write

Exemplo para a construção da resposta para a questão 4

| T1                | T2                |
| ----------------- | ----------------- |
| ler_item(x);      |                   |
| x: = x - n;       |                   |
|                   | ler_item(x);      |
|                   | x: = x + m;       |
| escrever_item(x); |                   |
| ler_item(y);      |                   |
|                   | escrever_item(x); |
| y: = y + n;       |                   |
| escrever_item(y); |                   |



| T1          | T2  | T3  |
| ----------- | --- | --- |
| ler_item(x) |     |     |
