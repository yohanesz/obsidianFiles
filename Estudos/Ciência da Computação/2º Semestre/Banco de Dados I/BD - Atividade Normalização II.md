1) 
<span style="color:#7317cf">Esquema relacional:</span> 
1FN(

<span style="color:#7317cf">Dependências Parciais:</span> 
(<span style="color:#7317cf">CONSULTOR_NUM</span>  => CONSULTOR_NOME, CONSULTOR_REGIÃO)
(<span style="color:#7317cf">CONTRATO_NUM</span> => CONTRATO_DATA, CONTRATO_VALOR, CLIENTE_NUM, CLIENTE_NOME, CLIENTE_REGIÃO) 
(<span style="color:#7317cf">CONSULT_NUM </span>=> CONSULT_CLASS)  
Z 
<span style="color:#7317cf">Dependências Transitiva:</span> 
(<span style="color:#7317cf">CLIENTE_NUM</span> => CLIENTE_NOME, CLIENTE_REGIÃO)


<span style="color:#7317cf">Diagrama de dependência:</span>


![[Diagrama3.svg]]

2) 
<span style="color:#7317cf">CLIENTE</span>(CLIENTE_REGIÃO, CLIENTE_NUM, CLIENTE_NOME)
<span style="color:#7317cf">CONTRATO</span>(CONTRATO_NUM, CONTRATO_DATA, CONTRATO_VALOR, CLIENTE_REGIÃO)
<span style="color:#7317cf">CONSULTOR</span>(CONSULTOR_NUM, CONSULT_CLASS, CONSULTOR_NOME, CONSULTOR_REGIÃO)
<span style="color:#7317cf">CONTRATO_CONSULTOR</span>(CONTRATO_NUM, CONSULTOR_NUM)

![[DERnormalizaçãoII.svg]]

<span style="color:#7317cf">OBS</span>: A tabela CONTRATO_CONSULTOR é uma tabela de junção, fazendo a relação de muito para muitos entre as tabelas CONTRATO e CONSULTOR.