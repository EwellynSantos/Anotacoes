# Encapsulamento, Properties e Auto Properties

## Encapsulamento

É o principio que consiste em proteger os dados de um objeto e controlar como eles podem ser acessados ou modificados.

Com o encapsulamento, aplicamos modificados de acesso, como por exempo o private nos atributos, dessa forma impossibilita a alteração ou visualização do atributo de forma indevida. E além de adicionar os modificadores, é necessário criar métodos que permitam a visualização e modificação de maneira correta.&#x20;

***

## Properties

As propriedades são a forma padrão do C# de controlar o acesso aos atributos de uma classe.&#x20;

Quando adicionamos o { get; set; } a um atributo, o compilador cria um atributo oculto, como se fosse assim:

```csharp
private string _nome;

public string Nome
{
    get
    {
        return _nome;
    }

    set
    {
        _nome = value;
    }
}
```

Esse `_nome` é chamado de **backing field** e, nas propriedades automáticas (`{ get; set; }`), ele é gerado automaticamente pelo compilador.

A grande vantagem das properties é controlar o que entra, dessa maneira voce pode adicionar condições para a propriedade set, como por exemplo:

```csharp
private int _idade;

public int Idade
{
    get
    {
        return _idade;
    }

    set
    {
        if (value >= 0) //<--- aqui temos a condição
            _idade = value;
    }
}
```

***

## Auto Properties

As **Auto-Properties (Propriedades Automáticas)** são uma forma simplificada de declarar uma propriedade quando você **não precisa escrever a lógica do `get` e do `set`**.

As formas mais comuns são:

```csharp
// Leitura e escrita
public string Nome { get; set; }

// Apenas leitura
public string Nome { get; }

// Leitura pública e escrita apenas pela classe
public decimal Saldo { get; private set; }
```
