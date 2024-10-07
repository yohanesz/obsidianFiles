
### <span style="color:#7317cf">CLASSE</span> 

* Modelo de implementação;
* Ao construir uma casa, a classe seria a planta da casa;
* Principais componentes:
	Nome da Classe;
	Atributos (variáveis);
	Métodos (funções);

### <span style="color:#7317cf">OBJETO</span>


* Aplicação dos modelos definidos na classe;
* <span style="color:#66e0ff">Classe</span> é apenas um arquivo, ao ser lançada na memória RAM, vira um objeto para ser manipulável;
	* Exemplo : Uma oficina mecânica
	* Objetos: carro, mecânico, ferramentas, peças.
	* Mesmo se eu tiver 10 mecânicos, virá apenas de uma classe.

### <span style="color:#7317cf">ATIVIDADE </span>

* <span style="color:#66e0ff">Bola:</span>
	Classe: Bola (nome do objeto deve ser generalizado para abranger os diversos tipos de bola);
	Atributos: tipo, peso, tamanho, material;
	Métodos: jogar, mover, encher;

*  <span style="color:#66e0ff">Carro:</span>
	Classe: veículo 
	Atributos: modelo, tamanho, cor, marca, número de rodas, lugares;
	Métodos: frear, acelerar, ré;

### <span style="color:#7317cf">CÓDIGO BOLA</span>

````java
package Poo;

	public class Bola { // objeto bola;
		private float tamanho = 100; // atributo tamanho e tipo;
		private String tipo = "Futebol"; // private para não ser alterado
	
	public float getTamanho() {
	return tamanho;
	}
	
	public void setTamanho(float tamanho) {
	this.tamanho = tamanho;
	}
	
	public String getTipo() {
	return tipo;
	}
	
	public void setTipo(String tipo) {
	this.tipo = tipo;
	}	
}
````


````java
package Poo;

	public class BolaMain {
		public static void main(String[] args) {
		
		Bola b = new Bola();
		
		b.tamanho = 23.5f;
		b.tipo = "futebol";
		
		System.out.println(b.tamanho);
		System.out.println(b.tipo);
		}
	}
````

<span style="color:#66e0ff">Atributos</span> foram colocados como <span style="color:#66e0ff">privados</span> para eventualmente ser criado procedimentos para validação dos mesmos, por exemplo, evitar colocar no atributo peso um valor negativo. 
Pode se <span style="color:#66e0ff">atribuir valores</span> aos <span style="color:#66e0ff">atributos iniciais privados</span>, para que se o valor setado pelo usuário no procedimento não passe pela verificação, o valor atribuído inicialmente continue sendo o valor do atributo.