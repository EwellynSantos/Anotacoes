# Lambda

É uma maneira de escrever os Gets de maneira mais concisa.

PS: por se tratar de uma forma mais eficiente de usar o get, automaticamente ele retorna um valor.



exemplos:

Antes&#x20;

<div align="left">

<figure><img src=".gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

É importante colocar o =>, pois assim especificamos que se trata de uma lambda.

Depois

<figure><img src=".gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

Segue abaixo dois exemplos:

Antes

```cpp
public int Somar(int a, int b)
{
    int resultado = a + b;
    return resultado;
}
```

Depois

```cpp
public int Somar(int a, int b) => a + b;
```















```csharp
List<int> numeros = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

List<int> numerosPares = numeros.FindAll(BuscarNumerosQueSaoPares);

bool BuscarNumerosQueSaoPares(int numero)
{
    return numero % 2 == 0;
}

foreach (int numero in numerosPares)
{
    Console.WriteLine(numero);
}
```



Depois

```cpp
List<int> numeros = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

List<int> numerosPares = numeros.FindAll(numero => numero % 2 == 0);
numerosPares.ForEach(numero => Console.WriteLine(numero));
```
