# Garbage Collector

O **Garbage Collector (GC)** é o componente do .NET responsável por **gerenciar automaticamente a memória**. Seu trabalho é identificar objetos que não estão mais sendo utilizados pelo programa e liberar a memória ocupada por eles.

#### Como ele funciona?

1. O programa cria objetos na **Heap**.
2. Enquanto existir alguma referência apontando para um objeto, ele permanece na memória.
3. Quando um objeto deixa de ser referenciado (fica inacessível), ele se torna elegível para coleta.
4. Em algum momento, o GC executa, identifica esses objetos e libera a memória.

#### Quando o GC é executado?

Ele **não roda em intervalos fixos** (como a cada minuto ou hora).

O .NET decide automaticamente quando executá-lo, principalmente com base em fatores como:

* quantidade de memória disponível;
* pressão de memória (muitos objetos sendo criados);
* necessidade de liberar espaço para novas alocações.

#### Gerações

Para melhorar a performance, o GC divide os objetos em três gerações:

* **Geração 0:** objetos recém-criados (a maioria é descartada rapidamente).
* **Geração 1:** objetos que sobreviveram a uma coleta da Geração 0.
* **Geração 2:** objetos que permanecem vivos por bastante tempo.

O GC coleta com mais frequência a **Geração 0**, pois é onde está a maior parte dos objetos temporários.

#### Resumindo

* O GC **gerencia automaticamente a memória** da Heap.
* Ele **remove apenas objetos que não possuem mais referências**.
* **Não possui um horário fixo para executar**; o runtime decide o melhor momento.
* Utiliza um sistema de **gerações (0, 1 e 2)** para tornar a coleta mais eficiente.
* Na grande maioria dos casos, **você não precisa (nem deve) chamar o GC manualmente** com `GC.Collect()`. O runtime faz isso de forma mais eficiente do que uma chamada manual.
