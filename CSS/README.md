# Declarando variaveus de estilo

declarar variaveis para estilos que serão usados com frequencia facilita o trabalho e melhora o desempenho.

### como declarar

```css
:root { 
--nome-variavel: valor;
}

```

dessa maneira voce deixa os valores padonizados e faceis de utilizar.

### Como utilizar

```css
.tag {
propriedade: var(--nome-variavel);
}
```
