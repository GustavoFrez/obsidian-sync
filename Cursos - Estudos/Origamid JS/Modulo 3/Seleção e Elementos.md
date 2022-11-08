#### ID

<span style="color:green">getElementById</span>  seleciona e retorna elementos do DOM.

~~~ JavaScript
// Seleciona pelo ID
const animaisSection = document.getElementById('animais')
const contatoSection = document.getElementById('contato')

// Retorna null caso não exista
const naoExiste = document.querySelectorById('teste')
~~~

#### Classe e Tag

<span style="color:green">getElementByClassName e getElementByTagName</span>  selecionam e retornam uma lista de elementos do DOM. A lista retornada está ao vivo, isto significa que se elementos forem adicionados, ela será automaticamente atualiazada.

~~~ JavaScript
// Seleciona pelo ID
const gridSection = document.getElementByClassName('grid-tal')

// Seleciona todas as UL's retorna uma HTMLCollection
const ul = document.getElementByTagName('ul')

// Retorna o primeiro elemento
console.log(grid-tal[0])
~~~


<span style="color:green">querySelector</span>  retorna o primeiro elemento que combinar com o seu seletor CSS.

~~~ JavaScript

const gridSection = document.querySelector('.animais') // classe CSS
const ul = document.querySelector('#animais') // id CSS

const navItem = primeiroUl.querySelector('li') // Busca dentro do UL apenas

// pega todas as classes 
const animaisImg = document.querySelectorAll('.animaisImg') 

//Pega a terceira posição do array da NODELIST 
console.log(animaisImg[2])

~~~


#### HTMLCollection vs NodeList

A diferença está nos métodos e propriedades de ambas. Além disso a NodeList retornada com o querySelectorAll é estática.
No caso de add uma classe como  mesmo nome o HTMLCollection atualiza os valores se existiam 3 com o add ficam 4 e já no NodeList permanecem 3.


#### Array-Like

HTMLCollection e Nodelist são array-like, parecem uma array mas não são. O método de **Array** <span style="color:green">forEach()</span> por exemplo, existe apenas em NodeList.

~~~ JavaScript

const gridSection = document.querySelector('.animais')

gridSelection.forEach((gridItem, index, array) => {
	gridItem.classList.add('azul');
	console.log(index) // index do item do array
	console.log(array) // a array completa
})
~~~

É possivel transformar array-like em uma Array real usando o método <span style="color:green">Array.from(gridSelecion)</span>


