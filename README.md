# Revisao-POO-Mobile
# Exercício — Animal

## Atividade proposta

1. Crie uma classe `Animal` com um atributo `nome` e um método `emitirSom()`.

2. Crie duas classes filhas (`Cachorro` e `Gato`) que sobrescrevem `emitirSom()`.

3. Instancie os dois objetos e chame `emitirSom()` em cada um.

4. Faça a mesma atividade também em Kotlin.

---

## Java

```java
class Animal {
    String nome;

    Animal(String nome) {
        this.nome = nome;
    }

    void emitirSom() {
        System.out.println("O animal emite um som.");
    }
}

class Cachorro extends Animal {

    Cachorro(String nome) {
        super(nome);
    }

    @Override
    void emitirSom() {
        System.out.println(nome + " faz: Au Au!");
    }
}

class Gato extends Animal {

    Gato(String nome) {
        super(nome);
    }

    @Override
    void emitirSom() {
        System.out.println(nome + " faz: Miau!");
    }
}

public class Main {
    public static void main(String[] args) {

        Cachorro cachorro = new Cachorro("Rex");
        Gato gato = new Gato("Mimi");

        cachorro.emitirSom();
        gato.emitirSom();
    }
}
```

### Saída

```text
Rex faz: Au Au!
Mimi faz: Miau!
```

---

## Kotlin

```kotlin
open class Animal(val nome: String) {

    open fun emitirSom() {
        println("O animal emite um som.")
    }
}

class Cachorro(nome: String) : Animal(nome) {

    override fun emitirSom() {
        println("$nome faz: Au Au!")
    }
}

class Gato(nome: String) : Animal(nome) {

    override fun emitirSom() {
        println("$nome faz: Miau!")
    }
}

fun main() {

    val cachorro = Cachorro("Rex")
    val gato = Gato("Mimi")

    cachorro.emitirSom()
    gato.emitirSom()
}
```

### Saída

```text
Rex faz: Au Au!
Mimi faz: Miau!
```
