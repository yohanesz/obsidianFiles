### <span style="color:#7317cf"> OBJETOS E CLASSES</span>

Coisa material ou abstrata que pode ser percebida pelos sentidos e descrita por meio das suas características comportamentos e estado atual.
<span style="color:#66e0ff">Exemplo: </span>

Há várias canetas de diferentes cores e tamanhos, mas há características em comum que fazem uma caneta, ser uma caneta. Podemos nos referir a essas características como moldes, para produzir outras canetas, esse molde será nossa <span style="color:#66e0ff">classe</span>, e as demais canetas produzidas a partir desse molde serão chamadas de <span style="color:#66e0ff">objeto</span>,

<span style="color:#66e0ff">ATRIBUTOS</span> (características) = Coisas que uma caneta tem: modelo, cor, ponta, carga, tampada;
<span style="color:#66e0ff">MÉTODOS</span> (comportamentos) = Coisas que uma caneta faz: escreve, rabisca, pinta, tampa, destampa;
<span style="color:#66e0ff">ESTADO</span> (características atuais) = Como a caneta está: 50% de carga, ponta fina, azul, destampada, escrevendo; 


### <span style="color:#7317cf">CLASSE</span>
````Java
public class Caneta {

	String modelo; // referência a atributos
	String cor;
	float ponta;
	int carga;
	boolean tampada;
	
	void status() {
	System.out.print("Uma caneta " + this.cor);
	System.out.println(" está tampada? " + this.tampada);
	}
	
	
	void rabiscar() { // referência a métodos
		if (this.tampada == true) {
			System.out.println("Erro, não posso rabiscar!");
		} else {
			System.out.println("Estou rabiscando");
	}
	
	void tampar() {
	}
	
	void destampar() {	
	}
}
````

Transformar de classe para objeto chamamos de instanciar 

### <span style="color:#7317cf">OBJETO</span>
````Java
package exemplo;

public class Exp {

	public static void main(String[] args) {
	
	Caneta c1 = new Caneta(); // criando(instanciando) objeto c1
	c1.cor = "Azul";
	c1.ponta = 0.5f;
	c1.tampada = false;
	
	c1.status();
	c1.rabiscar();
	
	}
}
````


