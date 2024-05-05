---
description: Math.random gera número aleatórios.
---

# N° aleatório (Math.random)

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Lembrando que se eu multiplicar por algum número(ex: 10), será definido que os números aleatórios serão até o penúltimo(9), pois nao inclui o número multiplicado (10), e para inclui-lo pracisa somar 1. exemplo:&#x20;

parseInt (Math.random() \* 10 ) +1;

conforme o exemplo abaixo, ele gera números extensos:

<div align="left">

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

</div>

agora, para que tenhamos um numero inteiro antes do ponto, precisamos multiplicar esse valor, conforme abaixo:

<div align="left">

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

mas em muito casos, nao vamos querer todos esses números decimais a direita, queremos apenas o número antes do ponto, e para isso vamos utilizar o **parseInt.**

O parseInt é uma função utilizada para pegar apenas o inteiro de algo.&#x20;

<div align="left">

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>
