# Renderizaçao de Listas

<figure><img src=".gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

inicialmente criamos um componente, onde usamos o metodo map para "mapear" o array, adicionamos tambem o index, que seria o id (o ideal é que o id seja criado no backend e atrelado ao frontend)

<figure><img src=".gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

Em App.jsx nós importamos e criamos o array com a lista, assim ela será implementada na tela.                             ![](<.gitbook/assets/image (3) (1) (1).png>)



Agora faremos a Condiçao da lista

<div align="left">

<figure><img src=".gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

A condiçao é: se a lista tiver um tamanho maior que zero <mark style="color:purple;">**itens.length > 0**</mark>, entao <mark style="color:purple;">**?**</mark> mapeie os itens e os index da lista <mark style="color:purple;">**itens.map((item, index) =>**</mark>** ,** e imprima a lista em um paragrafo <mark style="color:purple;">**(\<p key={index}> {item} \</p> )**</mark>  se nao <mark style="color:purple;">**:**</mark> imprima p seguinte paragrafo <mark style="color:purple;">**\<p> Não há itens na lista \</p>**</mark>
