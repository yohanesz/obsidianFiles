1 -  Em banco de dados, a transação é um conjunto de operações que são tratadas em bloco e possuem quatro propriedades, formando a sigla ACID: atomicidade, consistência, isolamento e durabilidade. Sobre as propriedades de uma transação, é correto afirmar: 

a) a durabilidade exclui, após uma transação com sucesso, os dados alterados.
b) a atomicidade determina que, havendo falha em uma ação do bloco, deverá ser desfeita apenas a operação anterior do bloco. 
c) a consistência garante que os valores de chaves primárias não sejam alterados. 
<span style="color:#7317cf">d) o isolamento impede que outras transações interfiram na transação corrente.</span>

2 -  Marque a alternativa correta. 
a) A otimização de consultas é uma técnica para garantir as propriedades ACID de transações de sistemas de bancos de dados. 
<span style="color:#7317cf">b) A técnica de modificação adiada consiste em uma abordagem para recuperação baseada em log, na qual as transações são reajustadas para garantir menor custo de processamento de consultas. </span>
c) Ao adotar o bloqueio de duas fases em todas as transações de um escalonamento, a serializabilidade é garantida, bem como o aumento da concorrência no SGBD. 
d) O uso de Timestamp é uma das técnicas aplicadas em transações de bancos de dados para prevenir a ocorrência de deadlock. 

3 - Sobre transações e seus comandos na linguagem SQL, avalie as seguintes afirmativas.

I. Os comandos COMMIT, ROLLBACK e DROP fazem parte do controle de transações do SQL; 
II. O comando ROLLBACK fecha o bloco da transação e é a indicação que a transação deve ser terminada, mas tudo que tentou ser feito deve ser descartado porque alguma coisa errada aconteceu e ela não pode terminar normalmente. Nada realizado dentro dela será́ perdurado no banco de dados; 
III. Commit em duas fases refere-se a uma transação que pode utilizar dois ou mais bancos de dados (multi- database), que podem estar localizados em servidores diferentes. Durante uma transação em bancos com essa característica garante-se que o Commit seja realizado em todos os bancos participantes ou em nenhum, ou seja, ou grava tudo ou não grava nada; 
IV. Com relação a uma transação atômica deve-se executar com sucesso todas as suas operações ou, em caso de falha, desfazer apenas as operações já́ executadas que causaram a falha. 

Marque a opção que corresponde somente às afirmativas verdadeiras. 

a) Apenas I e II. 
<span style="color:#7317cf">b) Apenas II e III. </span>
c) Apenas II e IV. 
d) Apenas III e IV.
e) Apenas I e IV. 

4 - Para garantir as propriedades ACID de um Sistema Gerenciador de Banco de Dados (SGBD) da Assembleia Legislativa do Piauí́, um Analista de TI verificou que: 
I. A execução de uma transação deve levar o banco de dados de um estado íntegro a um outro estado íntegro; 
II. Os efeitos de uma transação em caso de sucesso (commit) devem persistir no banco de dados mesmo em casos de quedas de energia, travamentos ou erros. Garante que os dados estarão disponíveis em definitivo. 

Assinale a opção que corresponde CORRETAMENTE aos protocolos I e II, respectivamente, as propriedades ACID. 
<span style="color:#7317cf">a) Consistência e Durabilidade. </span>
b) Consistência e Atomicidade. 
c) Durabilidade e Atomicidade.
d) Durabilidade e Isolamento. 
e) Isolamento e Atomicidade. 

5 -  A recuperação de falhas de transação significa que o banco de dados é restaurado ao estado consistente mais recente antes da falha. A recuperação é dependente de técnicas de atualização da base de dados ao longo das transações: adiada (quando não atualizam fisicamente o banco de dados até o ponto de confirmação – commit) ou imediata (que pode atualizar a base de dados antes do ponto de confirmação). 

Considere as afirmações abaixo sobre técnicas de recuperação de falhas de transação não catastróficas. 

I. Baseiam-se em informações sobre as mudanças que foram aplicadas aos itens de dados pelas diversas transações, tipicamente mantidas em um log de sistema. 
II. Em caso de falhas em atualização adiada, como nenhuma alteração foi efetivamente feita na base de dados, este tipo de recuperação é chamado de No-Undo/No-Redo. 
III. A técnica denominada Undo/No-Redo é usada para recuperação de falhas em atualização imediata e requer o uso da estratégia force para decidir quando os buffers atualizados da memória principal são gravados de volta no disco. 
IV. A técnica denominada Undo/Redo é outra alternativa para recuperação de falhas em atualização imediata. É necessária quando o ponto de confirmação foi atingido, mas não há garantias de que todas as mudanças tenham sido gravadas em disco. Isto é resultado da adoção da estratégia steal/no-force. 

Quais estão corretas? 
a) Apenas I e III. 
<span style="color:#7317cf">b) Apenas I, II e III. </span>
c) Apenas I, III e IV. 
d) Apenas II, III e IV. 
e) I,II,III e IV. 

6 - Sobre recuperação de banco de dados, é correto afirmar que: 

a) as técnicas de atualização imediata postergam qualquer atualização real no banco de dados em disco até que uma transação atinja o seu ponto de confirmação (commit). 
<span style="color:#7317cf">b) o log do sistema mantém informações sobre as mudanças nos itens de dados das transações, com o objetivo de restaurar o sistema em caso de falha. </span>
c) a recuperação de falhas catastróficas costuma ser feita com a técnica UNDO/NO-REDO, porque não exige um log nos sistemas monousuários. 
d) as técnicas de atualização adiada podem aplicar mudanças ao banco de dados no disco antes que a transação alcance uma conclusão bem-sucedida.
e) sombreamento é a técnica de gravação do cache dos blocos de discos no mesmo local do diretório original com o objetivo de recuperar os blocos em caso de falha. 

7 - Para garantir algumas das propriedades ACID de um Sistema Gerenciador de Banco de Dados (SGBD), um Analista de Sistemas, verificou que: 
I. os protocolos de Controle de Concorrência garantem a consistência dos dados por meio de acessos concorrentes; e 
II. os protocolos de Recuperação de Falhas garantem a consistência dos dados após falhas do sistema. 

Correspondem corretamente aos protocolos I e II, respectivamente, as propriedades ACID: 
a) Isolação e coerência 
b) Durabilidade e atomicidade 
<span style="color:#7317cf">c) Isolação e atomicidade </span>
d) Durabilidade e capacidade 
e) Capacidade e agilidade

___________________________________________
1 - Considere o gráfico a seguir. Quais transações devem ser refeitas (redo) e quais transações devem ser desfeitas (undo) ou canceladas/resubmetidas? Considere cada uma das técnicas estudadas.

![[Pasted image 20240303155058.png]]
<span style="color:#7317cf">Protelada (redo no-undo) (com checkpoint/commit)</span>
- T1,T3 e T4 efetivadas no banco
- T2, T5, T7 resubmetida (redo)
- T6 cancela e resubmete
<span style="color:#7317cf">Imediata (redo undo) (log e banco em sincronia)</span>
- T1,T2,T3,T4,T5,T7 efetivadas no banco
- T6 desfeita (undo)
--------------------------------------------------------------------
<span style="color:#7317cf">1 - O que são as entradas de log do tipo UNDO e REDO? </span>
	- **UNDO:** Essas entradas de log são usadas para reverter as alterações realizadas por uma transação. Se uma transação falhar ou for abortada, as entradas UNDO do log são aplicadas para desfazer as modificações feitas pela transação no banco de dados, deixando-o em um estado consistente.
	- **REDO:** Por outro lado, as entradas REDO são utilizadas para refazer ou reaplicar as alterações de uma transação que foram comprometidas com sucesso. Se ocorrer uma falha no sistema após a confirmação de uma transação, as entradas REDO ajudam a recuperar o estado consistente do banco de dados, repetindo as operações da transação.

<span style="color:#7317cf">2 -  O que se entende por reversão (rollback) de transação? </span>
	Reversão de transação, ou rollback, é o processo de desfazer as alterações feitas por uma transação que foi abortada, falhou ou foi explicitamente revertida. O objetivo é garantir que o banco de dados retorne a um estado consistente e estável, sem as modificações incompletas ou incorretas.

<span style="color:#7317cf">3 - Quais dentre as técnicas de recuperação não existem nenhuma reversão?</span>
	As técnicas de recuperação que não envolvem reversão são normalmente associadas a sistemas que utilizam logs de pontos de verificação (checkpoint) para permitir uma recuperação mais eficiente sem a necessidade de desfazer transações individuais. Essas técnicas visam restaurar o banco de dados a partir de um estado consistente anterior sem aplicar operações de UNDO.

<span style="color:#7317cf">4 -Discuta as operações UNDO e REDO e as técnicas de recuperação que cada uma usa. </span>
	- **UNDO:** É associado a técnicas de recuperação que desfazem transações não confirmadas ou falhas. A recuperação pode envolver a aplicação das entradas UNDO a partir do log para reverter as modificações.
	- **REDO:** Está relacionado a técnicas que reaplicam transações confirmadas para recuperar o banco de dados após uma falha. As entradas REDO são usadas para refazer as operações comprometidas.

<span style="color:#7317cf">5 - Para que é usado o log do sistema? Quais são as entradas típicas de um log de sistema? </span>
	O log do sistema é usado para registrar atividades significativas no sistema de gerenciamento de banco de dados. As entradas típicas incluem início e término de transações, alterações de dados, operações de UNDO e REDO, checkpoints, mensagens de erro, entre outros. O log do sistema é crucial para a recuperação e integridade do banco de dados em caso de falhas ou interrupções.

<span style="color:#7317cf">6 - O que são checkpoints e por que são importantes?</span>
	Checkpoints são pontos no tempo em que o sistema faz uma gravação coordenada de todos os dados modificados no banco de dados em um arquivo de log persistente. Isso ajuda a criar um ponto de recuperação consistente. Checkpoints são importantes porque reduzem o tempo de recuperação após uma falha, minimizando a quantidade de UNDO e REDO necessárias. Eles ajudam a garantir a consistência e a integridade do banco de dados, permitindo uma recuperação mais eficiente.
