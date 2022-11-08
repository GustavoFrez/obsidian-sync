
#### forEach()

Constatemente vamos selecionar uma lista de itens do DOM. A melhor forma para interagirmos com os mesmo é utilizando este método.

~~~ JavaScript
// Seleciona pelo ID
const imgs = document.querySelectorAll('img')

imgs.forEach(function(item) {
console.log(item)
})
~~~


#### ForEach e Array

<span style="color:green">forEach</span> é um método de Array, alguns objetos array-like possuem este método. Caso não possua, o ideal é transformá-los em uma array.

~~~ JavaScript
const titulo = document.getElementByClassName('titulo')
const titulosArray = Array.from()

titulosArray.forEach(function(item) {
console.log(item)
})
~~~
 
#### Arrow Function

Sintaxe curta em relação a function expression. Basta remover a palavra chave function e adicionar a fat => após os argumentos.

~~~ JavaScript
const titulo = document.getElementByClassName('titulo')
const titulosArray = Array.from()

titulosArray.forEach((item) => {
	console.log(item)
})
~~~




