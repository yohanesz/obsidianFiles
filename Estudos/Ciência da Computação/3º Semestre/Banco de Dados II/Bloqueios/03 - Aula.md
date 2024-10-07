=> Atualizações perdidas:
- Duas transações que irão mexer no mesmo atributo, uma seguido da outra (T1,T2). 
- T1 - Irá comprar 100 itens (já havia 35 itens)
- T2 - Irá vender 30 itens (restando 105)
=> Atualização pode ser perdida 


|                          T1                          |                          T2                          |
| :--------------------------------------------------: | :--------------------------------------------------: |
|                     ler_item(x);                     |                                                      |
|                     x: = x - n;                      |                                                      |
|                                                      |                     ler_item(x);                     |
|                                                      |                      x: = x+m;                       |
| <span style="color:#66e0ff">escrever_item(x);</span> |                                                      |
|   <span style="color:#66e0ff">ler_item(y);</span>    |                                                      |
|                                                      | <span style="color:#7317cf">escrever_item(x);</span> |
|                      y: = y + n                      |                                                      |
|                  escrever_item(y);                   |                                                      |
=> "<span style="color:#7317cf">escrever_item(x)</span>" = escreve o x incorreto
=> "<span style="color:#66e0ff">escrever_item(x) / ler_item(y)</span>" = atualização perdida

|        T1        |        T2        |
| :--------------: | :--------------: |
|   ler_item(x)    |                  |
|     x: x - n     |                  |
| escrever_item(x) |                  |
|                  |   ler_item(x);   |
|                  |    x: = x + m    |
|                  | escrever_item(x) |
|   ler_item(y);   |                  |
=> T1 falha

|        T1         |       T2        |
| :---------------: | :-------------: |
|                   |    sum: = 0;    |
|                   |  ler_item(a);   |
|                   | sum: = sum + a; |
|   ler_item(x);    |                 |
|    x: = x - n;    |                 |
| escrever_item(x); |                 |
|                   |  ler_item(x);   |
|                   | sum: = sum + x; |
|                   |  ler_item(y);   |
|                   | sum: = sum + y; |

