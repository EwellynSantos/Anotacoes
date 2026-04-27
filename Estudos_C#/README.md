# Tipos basicos de dados

### Tipos Básicos do c\#

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:$success;">Notes:</mark>&#x20;

* 1 byte possui 8 bits, e fazendo um calculo de cobina;'oes, podemos fazer 256 combinações.&#x20;
* O tipo string é imutavel, ou seja, se atribuir um novo valor a string, na verdade voce está criando um novo valor.&#x20;



<mark style="background-color:blue;">Dúvidas:</mark>

**A escolha de um tipo basico influencia na compilação ou rendimento do programa?**

\
👉 R: a escolha do tipo **não muda o tempo de compilação de forma relevante**, mas muda _como o código é gerado e validado_.

👉 R: Em performance a escolha do tipo pode impactar bastante.&#x20;

#### Performance: Tipos de valor vs referência

* `int`, `double`, `bool` → **value types (structs)**
* `string`, `object` → **reference types**

Impactos:

* Value types geralmente são **mais rápidos** (armazenados na stack)
* Reference types usam **heap + garbage collector**



### 🧠 Heap e Garbage Collector (explicação simples e direta)

#### 📦 Heap

O **heap** é uma área de memória onde ficam objetos mais complexos.

**📚 Stack vs Heap**

| Stack                         | Heap                        |
| ----------------------------- | --------------------------- |
| Rápido                        | Mais lento                  |
| Automático                    | Gerenciado                  |
| Tipos simples (`int`, `bool`) | Objetos (`string`, classes) |

**🧹 Garbage Collector (GC)**

O Garbage Collector é o cara que limpa a memória automaticamente.

O que ele faz:

* Encontra objetos que **não estão mais sendo usados**
* Libera memória do heap

Quando o método termina:

* `nome` não é mais acessível
* O GC eventualmente remove `"João"` da memória

***

#### ⚠️ Impacto na performance

O GC é ótimo, mas:

* Ele pode pausar o programa momentaneamente
* Muitas alocações no heap → mais trabalho pro GC

### 🎯 Resumo final

**Heap e GC**

* Heap → onde ficam objetos
* GC → limpa automaticamente
* Mais objetos → mais trabalho → possível impacto
