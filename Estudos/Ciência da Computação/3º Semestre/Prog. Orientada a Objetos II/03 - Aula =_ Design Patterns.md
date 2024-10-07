<h2> Design Patterns </h2>

=> SINGLETON:
	
```java
public class Singleton {

    private static Singleton instance;

    private Singleton() {
    }

    public static synchronized Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
````

=> ATIVIDADE: pesquise as aplicações de cada um dos padrões de projeto criacionais estudados Singleton, Factory Method, Builder, Fluente Interface, Abstract Factory e Prototype. Crie para cada padrão 2 exemplos, contextualize os exemplos e apresente o código fonte da solução.

### 1. Singleton:

- **Aplicações:**
    1. **Configurações Globais:** O Singleton é frequentemente usado para representar configurações globais em uma aplicação, como configurações de banco de dados, configurações de log, etc.
    2. **Gerenciadores de Recursos Únicos:** Quando há a necessidade de gerenciar recursos compartilhados, como pools de conexões ou caches, o Singleton garante uma única instância para coordenar o acesso.

### 2. Factory Method:

- **Aplicações:**
    1. **Frameworks de Extensibilidade:** Em frameworks que precisam ser estendidos por aplicativos específicos, o Factory Method permite que as subclasses forneçam uma implementação específica.
    2. **Liberação de Objetos Concretos:** Quando a classe precisa delegar a responsabilidade de criação de objetos para suas subclasses.

### 3. Builder:

- **Aplicações:**
    1. **Criação de Objetos Complexos:** Útil ao construir objetos que requerem muitos parâmetros ou têm várias configurações possíveis.
    2. **Criação de Objetos Imutáveis:** Ajuda a construir objetos imutáveis, garantindo que todas as propriedades sejam definidas durante a construção.

### 4. Fluent Interface:

- **Aplicações:**
    1. **Melhor Legibilidade de Código:** Usado para criar APIs mais expressivas e legíveis, especialmente quando se encadeiam várias chamadas de método.
    2. **Configuração de Objetos de Forma Concisa:** Útil quando se deseja configurar objetos de forma fluente, em uma única expressão.

### 5. Abstract Factory:

- **Aplicações:**
    1. **Criação de Famílias de Objetos Relacionados:** Útil quando é necessário garantir que os objetos criados sejam compatíveis entre si.
    2. **Encapsulamento da Lógica de Criação:** Permite que uma família de objetos seja criada sem especificar suas classes concretas.

### 6. Prototype:

- **Aplicações:**
    1. **Criação de Objetos a Partir de Outros Objetos:** Permite a criação de novos objetos copiando um objeto existente.
    2. **Evitar o Custo de Criação:** Útil quando a criação de um objeto é mais custosa do que a clonagem.