### <span style="color:#7317cf">COESÃO</span>

Uma classe deve ter apenas uma responsabilidade e deve realizar essa tarefa de maneira satisfatória, ou seja, uma classe não deve assumir responsabilidades que não são suas.
(alta coesão)
### ACOPLAMENTO

Aplicação do SOLID
UML = Unified Modeling Language (Diagrama de classes) 
Comportamentais(Caso de uso, sequencia);
(baixo acoplamento)

### Diagrama de classe

(-) = private (não é acessível fora da classe);
(+) = public (acessível dentro da classe);
(#) = protected (consegue acessar se estiver dentro do mesmo package);

Relacionamento entre classes

associação:
generalização (herança) = relacionamento entre o geral ou genérico e o especifico. Permite substituir uma classe filha pela classe progenitor (pai). 
um filho pode ter vários pais.


dependência
associação ()  


ATIVIDADE:
Em um sistema de atendimento médico é necessário definir uma lista de atendimento, essa lista de atendimento é definida pela prioridade do paciente. É necessário ter o controle dos médicos e suas respectivas especialidades. Em relação as pessoas atendidas e os médicos, é importante ter seu nome e sua data de nascimento. A prioridade na ordem do atendimento de um paciente é definida por 5 perguntas. Para cada atendimento é importante saber a data e hora de inicio e fim. Um atendimento pode ter a opção de emissão de atestado


