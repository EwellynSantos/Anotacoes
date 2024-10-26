# Shadow

Para criar sombras com CSS, você pode usar a propriedade `box-shadow` para elementos como caixas (divs, cards, botões) e `text-shadow` para aplicar sombras em textos



### Box-shadow

A sintaxe é:

```css
box-shadow: deslocamento-x deslocamento-y desfoque espalhamento cor;
```

* **deslocamento-x**: distancia da sombra no eixo horizontal (positivo para a direita, negativo para a esquerda).
* **deslocamento-y**: distancia da sombra no eixo vertical (positivo para baixo, negativo para cima).
* **desfoque** (opcional): controla o quanto a sombra será desfocada.
* **espalhamento** (opcional): aumenta ou diminui o tamanho da sombra.
* **cor**: a cor da sombra (pode ser em formato de código hexadecimal, rgb, ou nomes de cores).

exemplo:

```css
/* Sombra simples */
.elemento {
  box-shadow: 10px 10px 5px rgba(0, 0, 0, 0.3); /* sombra cinza */
}

/* Sombra mais difusa */
.elemento {
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5); /* sombra difusa e mais espalhada */
}

/* Várias sombras */
.elemento {
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5), -5px -5px 10px rgba(0, 0, 0, 0.2);
}

```





### Text-shadow

A sintaxe é:\


```css
text-shadow: deslocamento-x deslocamento-y desfoque cor;
```

* **deslocamento-x**: distancia da sombra no eixo horizontal.
* **deslocamento-y**: distancia da sombra no eixo vertical.
* **desfoque**: o quanto a sombra será desfocada.
* **cor**: a cor da sombra.

Exemplos:

```css
/* Sombra simples no texto */
.texto {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); /* sombra cinza */
}

/* Sombra colorida */
.texto {
  text-shadow: 3px 3px 6px #FF0000; /* sombra vermelha */
}

```
