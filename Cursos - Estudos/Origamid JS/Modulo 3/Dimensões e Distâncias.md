#### Height e Width

Essas são propriedades e métodos dos objetos <span style="color:green">Elemet</span> e <span style="color:green">HTMLElement</span>, a maioria delas são Read Only.

~~~ JavaScript
// Seleciona pelo ID
const section = document.querySelector('.animais')

section.clientHeight // height + padding
section.offsetHeight // height + padding + border
section.scrollHeight // height total, mesmo dentro de scrool

section.scrollWidth // width total, mesmo dentro de scrool
~~~


#### offsetTop e offsetLeft

~~~ JavaScript
// Seleciona pelo ID
const section = document.querySelector('.animais')

// Distancia entre o topo do elemento e o topo da página 
section.offsetTop

//Distância entre o canto esquerdo do elemento e o canto esquerdo da página
sectiom.offsetLeft

~~~

#### Window

~~~ JavaScript
window.innerWidth // widht da janela
window.outerWidht // soma dev tools também
window.innerHeight // height da janela 
window.outerWidth // soma a barra de endereço

window.pageYOffset // distância total do scroll horizontal
window.pageXOffset // distância total do scroll vertical

if(window.innerWidth < 600) {
	console.log('Tela menor que 600px')
}
~~~
