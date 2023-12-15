# Dicionário

**Criando um dicionário:**

<div data-full-width="true">

<figure><img src=".gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>



**Adicionando no dicionário:**&#x20;

voce vai procurar pela chave (nomeBanda) e adicionar os valores nessa chave.&#x20;

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Outro exemplo:

```php
var notasAlunos = new Dictionary<string, Dictionary<string, List<int>>> {
    { "Ana", new Dictionary<string, List<int>> {
        { "C#", new List<int> { 8, 7, 6 } },
        { "Java", new List<int> { 7, 6, 5 } },
        { "Python", new List<int> { 9, 8, 8 } }
    }},
    { "Maria", new Dictionary<string, List<int>> {
        { "C#", new List<int> { 6, 5, 4 } },
        { "Java", new List<int> { 8, 7, 6 } },
        { "Python", new List<int> { 6, 10, 5 } }
    }},
```
