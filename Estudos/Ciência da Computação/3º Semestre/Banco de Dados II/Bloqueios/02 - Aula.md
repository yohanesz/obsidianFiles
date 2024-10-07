=> Transação Protelada:
	- A atualização do banco de dados físico só é realizada após a transação atingir o ponto de consolidação (COMMIT). 
	- Antes que a consolidação seja alcançada, as transações atualizam seus dados no buffer. 
	-  Durante a consolidação, as atualizações são registradas no log e, então, gravadas no banco de dados. 
	- Se a transação for abortada antes do ponto de consolidação não terá alterado o banco de dados – o comando desfazer (UNDO) não será necessário. 
	- Se o sistema falhar depois que uma transação é consolidada no log, mas antes de serem salvas no banco de dados 
	- o SGBD utiliza o log para refazer (REDO) a transação e atualizar o banco de dados.
	- Considerando um sistema em que o controle de concorrência usa bloqueio em duas fases: 
		 os bloqueios permanecem em efeito até que a transação alcance seu ponto de consolidação. 
	- PROCEDIMENTO RDU_M - para entradas de ponto verificação (checkpoint) feitas no log. 
		- as transações T consolidadas (lista de efetiviação) desde o último checkpoint 
		-  as transações T’ ativas (lista de ativas). 
		-  refazer (REDO) todas as operações write das transações efetivadas no log, na sequencia em que elas se encontram no log. 
		-  transações ativas e não efetivadas serão canceladas e resubmetidas

=> Transação Imediata:

=> As técnicas de recuperação baseiam-se na propriedade de atomicidade
=> O SGBD (Sistema Gerenciador de Banco de Dados) utiliza o log de transações para rastrear todas as transações que atualizam o banco de dados.
=> Essas informações armazenadas no log são utilizadas pelo SGDB  em uma solicitação de recuperação acionada pelo comando ROLLBACK.
=> Alguns SGDBRs utilizam o log de transações para recuperar um estado consistente de BD, refazendo operações perdidas.
=> Falha de sistema no momento da transação:
	 O SGDB examinará todas as transações não consolidadas nesse log, utilizando o ROLLBACK para recuperar o BD para o seu estado anterior.
=> Conclusão do processo de recuperação:
	 O SGDB gravará no log todas as transações consolidadas que não foram gravadas fisicamente no BD antes da falha.
=> A emissão do ROLLBACK antes do encerramento de uma transação, o SGBD irá restaurar o BD apenas para essa transação específica, não para todas. – mantém a durabilidade das transações consolidadas.
=> Buffers:
	- São áreas de armazenamento temporário na memória principal utilizadas para acelerar as operações de disco.
	- O SGBD lê os dados do disco físico e armazena uma cópia deles em um “buffer” na memória principal.
	- Uma transação, atualiza a cópia dos dados no buffer – melhora o tempo de processamento.
	- Os buffers que possuem dados atualizados são gravados em um disco físico em uma única operação.
=> Pontos de verificação:
	- São operações em que o SGBD grava todos os buffers atualizados no disco.
	- A operação de ponto de verificação também é registrada no log de transações.
	- O banco de dados físico e o log de transações ficam em sincronia.
	- São escalonados automaticamente pelo SGBD várias vezes por hora.