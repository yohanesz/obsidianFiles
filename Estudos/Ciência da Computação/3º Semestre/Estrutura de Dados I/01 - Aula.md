
=> Maneiras de organizar de forma eficiente o fluxo do algoritmo, visando apresentar um <span style="color:#7317cf">melhor desempenho</span>.

=> As estruturas de dados lidam com três <span style="color:#7317cf">funções principais</span>:
	- Inserindo informações:
		- A entrada está em grande parte preocupada com a forma como os dados são recebidos. Que tipo de informação pode ser incluída? Os novos dados serão adicionados ao inicio fim ou algum lugar dos dados existentes?
	- Processando informações:
		- O processamento afeta a maneira como os dados são manipulados na estrutura de dados.
	- Recuperando informações
		- A recuperação é dedicada a localizar e retornar os dados armazenados na estrutura. Como podemos acessar essas informações novamente? Que passos a estrutura de dados precisa tomar para nos devolver as informações?	

=> Qual a finalidade pretendida para os dados? Alguma estrutura de dados possui uma funcionalidade idealmente adequada para essa finalidade? você deseja pesquisar, classificar ou iterar dados?

=> Quanto tempo levará para que diferentes estruturas de dados realizem várias tarefas em relação a outras estruturas de dados? Tecnicamente, duas estruturas de dados podem realizar a mesma tarefa para você, mas uma pode ser um pouco mais rápida.
 
=> <span style="color:#7317cf">Arrays</span>
=> <span style="color:#7317cf">Listas Encadeadas:</span>
	- Estrutura sequencial que consiste em uma sequência de itens em ordem linear que estão ligados uns aos outros. Portanto, você precisa acessar os dados sequencialmente e o acesso aleatório não é possível. (Trabalha com nodos).
	- Head => (key | next) => (key | next) => (key | next) => null
=> <span style="color:#7317cf">Pilhas: </span>
	- Uma estrutura LIFO (last in first out - o elemento colocado por último pode ser acessado em primeiro lugar)
	- (pilha de pratos).
=> <span style="color:#7317cf">Filas: </span>
	 - É uma estrutura FIFO (first in first out - o elemento colocado em primeiro lugar pode ser acessado em primeiro lugar).
=> <span style="color:#7317cf">Árvores:</span>
	- É uma estrutura hierárquica onde os dados são organizados hierarquicamente e estão ligados entre si. 
	- Busca binária, árvore B, árvore vermelho-preta, árvore AVL e arvore n-ária.
=>  <span style="color:#7317cf">Grafos:</span>
	- Consiste em um conjunto finito de vértices ou nós e um conjunto de arestas conectando esses vértices.
	- Pode ser usado para representar redes de mídia social. Cada usuário é um vértice e, quando os usuários se conecta, eles criam uma aresta.

<h2 style="color:#7317cf"> Conceitos Básicos </h2>

=> <span style="color:#7317cf">Tipos básicos (primitivos):</span>
	- inteiro, real, lógico e carácter

=><span style="color:#7317cf"> Tipos compostos:</span>
	- Arrays (vetores e matrizes)

=> <span style="color:#7317cf">Tipos definidos pelo usuário</span>

=> <span style="color:#7317cf">Tipos abstratos de dados (TAD):</span>
	- Dados | Operações => Classes (são utilizados atributos e métodos).
	- Visibilidade da estrutura interna do tipo fica limitada às operações.
	- Aplicações que usam o TAD são denominadas clientes do tipo de dado.
	- Cliente tem acesso somente à forma abstrata do TAD.
	- Propriedades:
		- Satisfazem as propriedades de:
		- Encapsulamento
		- Invisibilidade e reutilização
	- Código do cliente do TAD não depende de implementação.


=> <span style="color:#7317cf">Exemplo de código:</span>
```java 
public class SomaMultiplica {
	
	private int a=0, b=0;
	// construtor
	public SomaMultiplica(int n1, int n2) {
		this.a = n1;
		this.b = n2;
	}
	
	public int soma() {
		return a+b;
	}
	
	public int multiplica() {
		return a*b;
	}
}
````

```java
public class Main {

	public static void main(String[] args) {
	
		SomaMultiplica ex1 = new SomaMultiplica(3,5);
		
		System.out.println("Soma = " + ex1.soma());
		
	}
}
```
