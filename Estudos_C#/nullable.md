# Nullable

### Nullable

**Structs(tipo valor)** não aceitam valores valores nulos por padrão, mas podemos utilizar o nullable para torna-las nulas/opcionais.&#x20;

<mark style="color:$warning;">Exemplo:</mark>

```csharp
public class Cadastro 
{
    public string Email {get; set;}
    public int? Idade {get; set;} //<- adicionei a "?" para torna-la 
                                 //    nula/opcional
}
```

Como no exemplo acima, o **int** é um tipo valor, sendo assim não pode ser nulo como a String que é um tipo referencia. Então para deixar esse campo opcional, adicionamos a interrogação. &#x20;

***

### Coalescência nula

#### ??

A coalescência nula (??) é um operador utilizado para fornecer um valor padrão quando uma variavel é nula.&#x20;

<mark style="color:$warning;">Exemplo:</mark>

```csharp
string? nome = null;

string resultado = nome ?? "Visitante"; //<- aqui
```

No exemplo acima, veja que se a vaiavel `nome` tiver um valor, entao é atribuida a variavel `resultado`, se não, atribui o valor "Visitante".



#### ??=

A coalescencia nula (??=) é utilizada para atribuir um valor apenas se a variavel for nula.

<mark style="color:$warning;">Exemplo:</mark>

```csharp
string? nome = null;

nome ??= "Visitante"; //<- aqui
```

Neste exemplo, essa expressão equivale a: se `nome` é nula, recebe "Visitante". bem parecido com o `if`

