---
description: usado para dividir a tela de maneira mais organizada
---

# Display Grid

Normalmente temos o conteiner pai, que definirá o layout todo do projeto, lá podemos definir a quantidade de colunas e linhas que a tela terá de um modo geral. Os itens dentro desse container herda alguns estilos, podendo também ter suas proprias divisões e interações.&#x20;

### Columns (<mark style="color:yellow;">grid-tamplete-columns</mark>)

podemos definir as colunas com a propriedade <mark style="color:yellow;">grid-tamplete-columns</mark>, onde definimos a quantidade de colunas e o tamanho.

Usando o <mark style="color:yellow;">**auto**</mark>, podemos definir colunas que preencham todo os espaço disponivel de acordo com a quantidade de colunas, ou seja, ela será responsiva. Mas também podemos mesclar, podendo criar colunas com tamanho auto ou com tamanho definido(<mark style="color:yellow;">**pixels, rem, em**</mark>):

Abaixo definimos 3 colunas com tamanho auto

<div data-full-width="true">

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

O que resultou em:

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

usando medidas, podemos mesclar:

<figure><img src=".gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Resultado

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>



### Rows(<mark style="color:yellow;">grid-tamplate-rows</mark>)

o <mark style="color:yellow;">grid-tamplate-rows</mark> definirá os tamanhos das linhas, nao a quantidade. Podendo realizar variações de tamanho, veja:

<figure><img src=".gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

Resultado:

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>



### Propriedade <mark style="color:yellow;">FR</mark>(fração)

Essa propriedade pode der usada tanto no <mark style="color:yellow;">grid-tamplete-rows</mark> quanto no <mark style="color:yellow;">grid-tamplete-columns</mark>. Basicamente ela referencia uma fração da tela, entao podemos definir de maneira organizada como a tela será dividida. O legal é que ela é responsiva, então ela preenche todo o espaçi disponivel e se adequa as telas, entao nao precisa se preocupar, além disso, ela é melhor que o <mark style="color:orange;">auto</mark> por que podemos definir a fração de qualquer maneira. Veja:

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Resultado:

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>





### Propriedade Repeat

Uma maniera de otimizar a criação de colunas ou tamanho de linhas é usar a propriedade repeat, pois nela podemos definir a quantida e o tamanho. Sintaxe:

```css
repeat(quantidade, tamanho)
```

Veja:

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Definimos 4 colunas com 200px cada:\


<figure><img src=".gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



### Propriedade minmax()

permite que voce defina valores máximos e m´nimos que um item pode ter em tela.Além disso, pode pode usar todas as propriedade de medidas, como pixel, rem, em e fr. Sintaxe:

```css
minmax(mínimo de tamanho, maximo de tamanho)
```





### Propriedade Gap, Row-Gap e Column-Gap

o row-gap e o coluns gap são utilizados par dar espaçamento entre os itens de forma separada, já o gap é a junção dos dois.





### Propriedade Justify-itens e align-itens

O justtify é utilizado para alinhar horizontalmente o item-filho dentro do content-pai, já o aling é para alinhar verticalmente o item-filho dentro do content-pai.



### Propriedade Justify-content e align-content

O justtify é utilizado para alinhar horizontalmente o content, já o aling é para alinhar verticalmente o content.



### Propriedade Place-itens

é uma junção do justify-itens e aling-itens, onde podemos em conjunto  alinhas as propriedades. Sintaxe:

```css
place-itens: propriedade propriedade.
```





### Grid-template-areas

Ele define como será a separação do seu layout num todo, onde voce pode definir variaveis e quanto espaço essas variaveis vao ocupar no seu layout.

por exemplo, abaixo vamo criar as areas no html, sendo elas: header, aside, article, section e footer:

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

agora vamos definir nosso grid-tamplate-areas, que é onde vamos criar variaveis e definir quais espaços serão ocupados:\


<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Ou seja, o header ocupou 2 espaços, o aside e o article ocupando 1 espaço da mesma row, o section ocupa 2 espaços e o footer também.



Agora iremos atribuir essas variaveis aos itens desse layout, para que eles sejam identificados e respondam ao layout determinado:

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

E esse é o resultado:

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
