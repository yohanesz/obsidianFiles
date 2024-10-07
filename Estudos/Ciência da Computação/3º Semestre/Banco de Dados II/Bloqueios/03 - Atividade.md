Com base na escolha de um SGBD, pesquise na sua documentação: 

1 - Quais as técnicas de recuperação de transação utilizadas pelo SGBD?

**1. Recuperação por Desfazer/Refazer (Undo/Redo)**

- **Desfazer:** reverte as alterações feitas por transações incompletas, restaurando o estado anterior do banco de dados.
- **Refazer:** aplica as alterações feitas por transações que foram commitadas, mas ainda não foram gravadas no disco permanentemente.

**2. Log de Transações (Transaction Log)**

- Registra todas as modificações feitas no banco de dados, permitindo que o MySQL reconstrua o estado correto após uma falha.
- O log é dividido em duas seções:
    - **Log de Ações:** registra as operações realizadas (inserções, atualizações, exclusões).
    - **Log de Desfazer:** armazena informações para reverter as operações do log de ações.

**Processo de Recuperação:**

1. **Análise do Log:** o MySQL verifica o log de transações para identificar transações incompletas.
2. **Desfazer:** as operações das transações incompletas são revertidas usando o log de desfazer.
3. **Refazer:** as operações das transações commitadas que ainda não foram gravadas no disco são aplicadas usando o log de ações.

**Tipos de Falhas e Recuperação:**

- **Falhas não-catastróficas:** afetam apenas a memória e podem ser corrigidas usando o log de transações (desfazer/refazer).
- **Falhas catastróficas:** danificam o banco de dados no disco e exigem a restauração de um backup.

**Modos de Log de Transações:**

- **Modo de Commit Completo:** garante a durabilidade das transações, mas pode ter um impacto no desempenho.
- **Modo de Commit Misto:** oferece um equilíbrio entre desempenho e durabilidade.
- **Modo de Commit Assíncrono:** prioriza o desempenho, mas pode comprometer a durabilidade em caso de falhas.

**Recursos Adicionais:**

- **Pontos de Controle:** permitem que o MySQL faça backup incremental do banco de dados, reduzindo o tempo de recuperação.
- **Binlog:** registra todas as alterações feitas no banco de dados, podendo ser usado para replicação e recuperação de falhas.