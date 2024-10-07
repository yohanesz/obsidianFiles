Declaração: pedaço de código que irá ditar as propriedades e valores a serem aplicadas a um elemento HTML.
Como escrevemos?
````css
body {
background: black;
/* color: green; essa linha será ignorada */
}
````

Cascata: quando há 2 ou mais declarações, a última será a mais relevante.
Especificidade: cada seletor tem um peso e a soma dos pesos, será levada em conta para que determinada declaração seja mais específica
````css
#id {
	/* peso 100 */
}

.class {
	/* peso 10 */
}

element {
	/* peso 1 */
}
````

Box model: todos os elementos HTML serão considerados uma caixa, assim como uma caixa de papelão, possuem determinadas propriedades como, conteúdo, largura, altura, borda, preenchimento (espaço interno), espaçamento (espaço externo).

![[box-model.png]]

Display Block {div, section, p, h1, h2, ul, li ,article}: 
Ocupa 100% da largura do elemento pai;
Ocupa sempre a sua própria linha e é posicionado abaixo do elemento anterior;
A altura é definida de acordo com o conteúdo interno;
É possível definir widht e height;
Você pode definir valores de margin-top e margin-bottom;

Display Inline {a, span, b ,i ,em}: 
Ocupa a largura total do seu conteúdo apenas;
Um elemento inline após outro elemento inline ocupam a mesma linha;
Não é possível definir widht e height;
Não é possível definir valores de margin-top e margin-bottom;
Ao aplicar o float, automaticamente eles assumem características de display block;
Se aplicado dentro de um texto, irá seguir o fluxo do conteúdo;



