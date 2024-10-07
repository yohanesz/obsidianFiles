
1) 
<span style="color:#7317cf">Esquema relacional:</span> 1FN(<span style="color:#7317cf">FAT_NUM, PROD_NUM</span>, PROD_NOME, PROD_PRECO, FORN_CODIGO, FORN_NOME, VENDA_DATA, QUANT_VENDIDA).
<span style="color:#7317cf">Dependências parciais:</span> (FAT_NUM => VENDA_DATA) (PROD_NUM => PROD_NAME, PROD_PRECO, FORN_CODIGO, FORN_NOME)
<span style="color:#7317cf">Dependência transitiva:</span> (FORN_CODIGO => FORN_NOME)

<span style="color:#7317cf">Diagrama de dependência:</span> ![[Untitled Diagram 1.svg|850]]
2) 
Segunda Forma Normal:

<span style="color:#7317cf">Fatura</span>(FAT_NUM, VENDA_DATA)
<span style="color:#7317cf">Produto</span>(PROD_NUM, PROD_PRECO, FORN_CODIGO, FORN_NOME)
<span style="color:#7317cf">Venda</span>(FAT_NUM, PROD_NUM, QUANT_VENDA)

![[DERnormalizaçãoII.svg]]                                                                                                


3) 
Terceira Forma Normal: 

<span style="color:#7317cf">Fatura</span>(FAT_NUM, VENDA_DATA)
<span style="color:#7317cf">Produto</span>(PROD_NUM, PROD_NAME, PROD_PRECO, FORN_CODIGO)
<span style="color:#7317cf">Fornecedor</span>(FORN_CODIGO, FORN_NOME, FORN_CODIGO)
<span style="color:#7317cf">Venda</span>(FAT_NUM, PROD_NUM, QUANT_VENDIDA)

![[Untitled Diagram 2.svg|300]]