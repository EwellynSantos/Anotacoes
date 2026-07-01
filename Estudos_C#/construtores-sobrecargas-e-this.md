# Construtores, Sobrecargas e This

### Construtores

é uma operação especial da classe, que executa no momento da instanciação do **objeto**

Usos comuns :&#x20;

* Definir valores iniciais para propriedades e campos;
* Garantir que o objeto comece em um estado válido;
* Receber informações obrigatórias para a criação do objeto;
* Executar alguma configuração necessária antes do objeto ser utilizado.

***

### Sobrecargas

Sobrecarga é quando você cria **várias versões do mesmo método (ou construtor)**, mas com **parâmetros diferentes**.

A ideia é permitir que a mesma ação seja executada de formas diferentes, dependendo das informações disponíveis.

O compilador escolhe automaticamente qual método chamar com base na **quantidade** e nos **tipos dos parâmetros**.

***

### This

`this` é uma **referência ao objeto atual**, ou seja, à instância da classe que está executando o código.

Ele é usado para:&#x20;

* acessar explicitamente os membros do próprio objeto.

Ex:

```csharp
public class Pessoa
{    public string Nome; //<- esta referenciando essa propriedade ali em baixo
        public void Apresentar()    
        {        
                Console.WriteLine(this.Nome); // <- aqui
        }
}
```



* Diferenciar parametros de atributos quando esses possuem o mesmo nome

Ex:

Para nao ter ambiguidade, pois há 2 "Nome", é utilizado o this pra referenciar o parametro

```csharp
public class Pessoa
{
    public string Nome; //<- esse não X
    
    public void Apresentar(string Nome) //<- ele esta referenciando esse 
                                        //parametro ali em baixo
    {
        Console.WriteLine(this.Nome); //<- aqui
    }
}
```



* chamar outro construtor da mesma classe



```csharp
public class Pessoa
{
    public string Nome;
    public int Idade;
    
    public Pessoa(string nome)
    : this(nome, 0) //<- Aqui o construtor de aixo [e reaprovitado
    {
    }

    public Pessoa(string nome, int idade)
    {
        Nome = nome;
        Idade = idade;
    }
}
```

Neste exemplo, o intuito é nao ter repetição de código, centralizando a lógica em um unico construtor.
