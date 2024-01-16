# Sobrescrever/Override

O Override é usado quando queremos usar um método da classe mãe e desejamos adicionar nova funcionalidades.&#x20;



Ex: na classe mãe, criamos um método com suas propriedades, mas usaremos esse mesmo método nas classe filhas, e cada método na classe filha terá propriedades únicas adicionadas, sendo assim, devemos aplicar o override no método "filho", pois faremos tipo uma herança, estaremos sobrescrevendo. Além disso, devemos adicionar o virtual para dizer que aquele método será compartilhado.&#x20;

Na classe filha:

<div align="left">

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

Na classe mãe:

<div align="left">

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>

Após fazer essas alterações, é necessário colocar no método filho uma indicação de que estaremos executando as funcionalidades do método mãe:

<div align="left">

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

</div>
