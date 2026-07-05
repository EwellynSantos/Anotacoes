# Tipos referência e tipo valor

## Tipo referência

O tipos referência são entendidos como **ponteiros**, pois eles guardam apenas a referência de onde esta o conteúdo armazenado, ou seja, **ele aponta para o conteúdo.**&#x20;

Sendo assim, a variavel é armazenada na **memória stack**, que aponta para o local onde está armazenado o conteúdo na memória heap. Para entender melhor, segue um exemplo abaixo:

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Neste exemplo, quando damos um new Product, automaticamente é criada uma caixa na Memória Stack e essa caixinha armazena a referencia/coordenada do conteúdo na Memória Heap, ou sera, ela aponta para o local da Memória Heap.&#x20;

Um detalhe importante é que quando fazemos o p2 = p1, ele passa a apontar para a mesma referência/coordenada do conteúdo armazenado na p1. &#x20;

Para conteúdos nulos, a caixinha da Memória Stack fiza vazia, sem apontar/referenciar:

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>



### **Tipos de referência**

Em C#, os principais **tipos de referência** são:

* ✅ **Classes (`class`)**
* ✅ **Strings (`string`)** _(na verdade, `string` é uma classe especial)_
* ✅ **Arrays**
* ✅ **Interfaces**
* ✅ **Delegates**
* ✅ **Records** (quando declarados com `record`, e não `record struct`)

***

## Tipos Valor

Os tipos valor são **Structs**, significa que o conteúdo é armazenado direto na caixinha da **Memória Stack**.

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Detalhe, quando fazer y = x, ele faz uma cópia do conteúdo daquela variavel, apenas.



### **Tipos de valor**

Em C#, os principais **tipos de valor** são:

* ✅ `bool`
* ✅ `byte`
* ✅ `sbyte`
* ✅ `char`
* ✅ `short`
* ✅ `ushort`
* ✅ `int`
* ✅ `uint`
* ✅ `long`
* ✅ `ulong`
* ✅ `nint`
* ✅ `nuint`
* ✅ `float`
* ✅ `double`
* ✅ `decimal`
* ✅ `struct` (qualquer estrutura criada por você ou fornecida pelo .NET, como `DateTime`, `Guid`, `TimeSpan`, `DateOnly`, `TimeOnly` etc.)
* ✅ `enum`
* ✅ `record struct`

***

## O que são Stack e Heap?

### O que são Stack e Heap?

São duas regiões de memória usadas pelo .NET para armazenar dados.

* **Stack (pilha)** → armazena dados temporários e de acesso rápido.
* **Heap (monte)** → armazena objetos que podem viver por mais tempo.



### Stack (Pilha)

A Stack funciona como uma pilha de pratos, você sempre coloca um prato no topo e sempre retira o prato que está no topo. É o conceito **LIFO (Last In, First Out)**.

**E quando o método termina:** Tudo isso é removido automaticamente.



### Heap (Monte)

A Heap é uma área muito maior da memória. É nela que ficam os objetos criados com `new`.

**E quando o método termina:** A referência(a caixinha) desaparece, mas o objeto(conteúdo) ainda está na Heap. Se nenhuma outra variável apontar para ele, ele fica "órfão". Nesse momento entra o **Garbage Collector (GC)**.



### Garbage Collector

O GC procura objetos que ninguém mais utiliza. Quando encontra objetos sem referencias, ele remove, liberando memória.

***

## Um detalhe importante (que costuma aparecer em entrevistas)

Muitas pessoas dizem:

> "Tipos de valor ficam na Stack e tipos de referência ficam na Heap."

Essa frase **é útil para começar, mas não é 100% verdadeira**.

O correto é:

* **Objetos de tipos de referência** normalmente são alocados na Heap.
* **Tipos de valor** normalmente ficam onde são declarados. Se um tipo de valor for um campo de um objeto, ele ficará **dentro desse objeto na Heap**, e não na Stack.
