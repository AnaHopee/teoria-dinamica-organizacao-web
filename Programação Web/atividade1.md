# Atividade 1: Descrevendo Efeitos Visuais com JavaScript

## Como o JavaScript é utilizado para criar efeitos visuais

JavaScript é amplamente utilizado para adicionar efeitos visuais em páginas web, pois permite manipular dinamicamente os elementos da interface do usuário. Ele atua diretamente no DOM (Document Object Model), possibilitando alterações em estilos, posições, tamanhos e classes CSS de elementos em tempo real.

## Interação entre JavaScript e CSS

Com JavaScript, é possível acessar e modificar os estilos de um elemento diretamente:

```javascript
document.getElementById("elemento").style.color = "red";
document.getElementById("elemento").style.fontSize = "24px";
```
Também é comum alterar classes CSS com classList, o que permite aplicar estilos predefinidos:

```javascript
document.getElementById("elemento").classList.add("ativo");
document.getElementById("elemento").classList.remove("inativo");
```

## Animações Simples com JavaScript Puro

Animações básicas podem ser criadas usando funções como `setInterval()` ou `requestAnimationFrame()`:

````javascript
let box = document.getElementById("box");
let pos = 0;
let animar = setInterval(() => {
    if (pos >= 300) clearInterval(animar);
    else {
        pos++;
        box.style.left = pos + "px";
    }
}, 10);
````
Move um elemento 300px para a direita de forma gradual.

## Uso de Bibliotecas para Efeitos Mais Complexos

Bibliotecas JavaScript tornam mais fácil e eficiente aplicar animações complexas e responsivas:

*jQuery*

```javascript
$("#elemento").fadeOut(1000);
```
*GSAP (GreenSock Animation Platform)*

```javascript
gsap.to("#elemento", { duration: 1, x: 100, opacity: 0 });
```
Essas bibliotecas oferecem controle refinado sobre as animações e melhor compatibilidade entre navegadores.

*Exemplos de Funcionalidades Comuns*
Fade in/out

Sliders

Animação de rolagem

Parallax

Transições suaves

FONTES:

https://www.w3schools.com/js/js_htmldom_css.asp

https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style

https://greensock.com/docs/

