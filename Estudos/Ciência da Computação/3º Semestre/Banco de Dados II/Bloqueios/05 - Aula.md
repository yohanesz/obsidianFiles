### Métodos de Bloqueio

=> O bloqueio garante a utilização exclusiva de um item de dados por uma transação atual.
=> O bloqueio é liberado quando a transação é concluída.
=> As informações bloqueadas são controladas por um gerenciador de bloqueio.
=> Cada bloqueio pode ser um registro na tabela de bloqueio com três campos: nome do item de dado, LOCK, transação de bloqueio e uma fila para as transações que estão esperando para acessar o item.

=> **Bloqueio no nível de banco de dados**, o banco inteiro é bloqueado (não é mais viável)

=> **Bloqueio no nível de página**, uma tabela pode usar várias páginas e uma página pode conter várias linhas de uma ou mais tabelas.

=> **Bloqueio no nível de linha**, a linha inteira é bloqueada.
=> as transações de T1 e T2 podem acessar linhas diferentes da mesma tabela

=> Bloqueio no nível de linha, o atributo é bloqueado.
=> as transações T1 e T2 podem acessar a mesma linha, desde que solicitem atributos diferentes nessa linha

### Tipos de Bloqueio

**Binário**: 
=> Possui apenas dois estados, bloqueado e desbloqueado.
=> 
.... (Falta o resto)


=> Garantindo serialização pelo bloqueio em duas fases:

a) 

|      T1       |     |      T2       |
| :-----------: | --- | :-----------: |
| read_lock(y)  |     | read_lock(x)  |
| read_item(y)  |     | read_item(x)  |
|   unlock(y)   |     |   unlock(x)   |
| write_lock(x) |     | write_lock(y) |
| read_item(x)  |     | read_item(y)  |
|  x: = x + y   |     |  y : = x + y  |
| write_item(x) |     | write_item(y) |
|   unlock(x)   |     |    unlock     |

b) Valores iniciais: x = 20, y = 30. Resultado do plano de execução serial T1 seguido por 
T2 : x = 50, y = 80 
Resultado do plano serial T2 seguido por 
T1 : x = 70, y = 50

c) 

|      T1       |      T2       |
| :-----------: | :-----------: |
| read_lock(y)  |               |
| read_item(y)  |               |
|   unlock(y)   |               |
|               | read_lock(x)  |
|               | read_item(x)  |
|               |   unlock(x)   |
|               | write_lock(y) |
|               | read_item(y)  |
|               |  x: = x + y   |
|               | write_item(y) |
|               |   unlock(y)   |
| write_lock(x) |               |
| read_item(x)  |               |
| write_item(x) |               |
|   unlock(x)   |               |

1 - As transações T1 e T2 seguem o protocolo em duas fases?

2 - Qual é a regra para seguir o protocolo de duas fases?