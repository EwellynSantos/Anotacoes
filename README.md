# Menu

Menu hamburgue

Utilizar os seguintes elementos:

da forma abaixo, permite criar um menu que quando clicamos, as informações apareçam

````css
```css

.cabecalho {
    ...
    position: relative; /*menu-hamburger*/
}



.lista-menu { /*menu-hamburger*/
    display: none;
    position: absolute;
    top: 100%;
}


/* o ~ é como uma condicional(if) no css.
se o botão estiver checked, o lista menu ira aparecer, usando o elemento display block*/
.container__botao:checked ~ .lista-menu { /*menu-hamburger*/
    display: block;
}
```

```html
<header class="cabecalho">
        <div class="container">
            <input type="checkbox" id="menu" class="container__botao">
            <label for="menu">
                <span class="cabecalho__menu container__imagem"></span>
            </label>
            <ul class="lista-menu">
                <li class="lista-menu__titulo">Categorias</li>
                <li class="lista-menu__item">
                    <a href="#" class="lista-menu__link">Programação</a>
                </li>
            </ul>
```
````
