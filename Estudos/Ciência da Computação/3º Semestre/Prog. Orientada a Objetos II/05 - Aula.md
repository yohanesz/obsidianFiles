
### Generics e Wildcards

Trabalhar com elementos onde a estrutura não é conhecida;
Tipo genérico: parâmetro para um tipo

=> Os wildcards em Java são usados para representar um tipo desconhecido em operações genéricas. Eles permitem que você crie código mais flexível e reutilizável, especialmente em coleções e métodos genéricos. Existem três tipos principais de wildcards: Upper Bounded Wildcards (extends), Lower Bounded Wildcards (super) e Unbounded Wildcards (tipo desconhecido sem relação). Vamos explorar cada um deles.
### 1. Upper Bounded Wildcards (Extends)

O wildcard `? extends T` é usado quando você quer garantir que o tipo genérico seja um subtipo de `T` ou `T` mesmo. Isso é útil quando você quer consumir elementos de uma coleção genérica, mas não precisa saber o tipo exato.

Por exemplo, se você tem uma lista de `Number` e quer iterar sobre ela, pode usar `? extends Number`:

````java
List<? extends Number> numbers = new ArrayList<Integer>(); for (Number number : numbers) { System.out.println(number); }
````

Neste caso, `? extends Number` permite que você use qualquer tipo que seja um `Number` ou uma subclasse de `Number`.

### 2. Lower Bounded Wildcards (Super)

O wildcard `? super T` é usado quando você quer garantir que o tipo genérico seja um supertipo de `T` ou `T` mesmo. Isso é útil quando você quer adicionar elementos a uma coleção genérica, mas não precisa saber o tipo exato.

Por exemplo, se você tem uma lista de `Object` e quer adicionar um `String` a ela, pode usar `? super String`:
````java
List<? super String> objects = new ArrayList<Object>(); objects.add("Hello");
````


Neste caso, `? super String` permite que você use qualquer tipo que seja um `String` ou uma superclasse de `String`.

### 3. Unbounded Wildcards (Tipo desconhecido sem relação)

Um wildcard sem restrições (`?`) é usado quando você não tem informações sobre o tipo genérico. Isso é útil quando você quer aceitar qualquer tipo em uma coleção genérica.

Por exemplo, se você tem uma lista de `Object` e quer adicionar qualquer tipo de objeto a ela, pode usar `?`:

````java
List<?> objects = new ArrayList<Object>(); objects.add("Hello"); objects.add(123);
````

Neste caso, `?` permite que você use qualquer tipo.

### Conclusão

Os wildcards em Java são uma ferramenta poderosa para escrever código genérico mais flexível e reutilizável. Eles permitem que você trabalhe com tipos desconhecidos de maneira segura, garantindo que o código seja compatível com uma ampla gama de tipos sem perder a segurança de tipo.