
Strings, números, boolean, objetos e mais possuem propriedades e métodos. Por isso são Objetos:

~~~ JavaScript
var nome = 'André'

nome.length; // 5
nome.charAt(1) // 'n'
nome.replace('ré', 'rei') // 'Andrei'
nome; // 'André'
~~~

Uma string herda propriedades e métodos do construtor **String()**
No exemplo acima nehuma dos métodos altera a variável nome.

#### Números também são Objetos.

Por um breve momento o número é envolvido em um Objeto (coerção), tendo acesso assim as suas propriedades e métodos.

~~~ JavaScript
var altura = 1.8

altura.toString() // '1.8'
altura.toFixed() // 2
~~~


#### Elementos do DOM também são Objetos.

~~~ JavaScript
var btn = document.querySelector(".btn");

btn.classList.add('azul') // adiciona a classe azul
btn.innerText // 'Clique'

btn.addEventListener("click", function () {
	console.log("Clicou");
});
~~~

Praticamente todos os efeitos com JS são feitos utilizando propriedades e métodos de Objetos do DOM.


