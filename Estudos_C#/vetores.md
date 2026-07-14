# Vetores

Vetor é um arranjo unidimensional, é uma estrutura de dados:

* Homogenea (dados do mesmo tipo)
* Ordenada (elementos acessados por meio de posiçoes)
* Alocada de uma vez só, em um bloco contíguo de memória

Vantagens:

* Acesso imediato aos elementos pela sua posição

Desvantagens:

* Tamanho fixo
* Dificuldade para se realizar inserções e deleções



Como declarar um vetor?

```csharp
var n = 3;

double[] vect = new double[n]; //<- aqui estou criando um vetor

for(i = 0; i >= n; i++) //<- neste for estou adicionando os valores no vetor
{
    double price = Console.ReadLine();
    vect[i] = price;
}
```

Detalhe importante, uma vez que voce deleta o conteudo em um indice do vetor, a "caixinha" permanece lá, vazia.&#x20;
