É uma interface que representa documentos HTML e XML através de objetos. Com ela é possível manipular a estrutura, estilo e conteúdo destes documentos.

~~~ JavaScript
console.log(window)
// window é o objeto global do browser
//possuí diferentes métodos e propriedades

window.innerHeight // retorna a altura do browser
~~~

Ao inspecionar o elemento com o Chrome, você está vendo a representação oficial do DOM.

O DOM nos possibilita acessar suas propriedades através da palavra chave <span style="color:green">window</span>

~~~ JavaScript
const href = window.location.href;
console.log(href);

if (href === "http://127.0.0.1:5500/oque-e-o-dom/index.html") {
	console.log("Foi para a pagina");
}
~~~

Representação do DOM:

![[Pasted image 20221106195607.png]]


#### Window e Document

São os objetos principais do DOM, boa parte da manipulação é feita através dos seus métodos e propriedades.

~~~ JavaScript
window.alert('Isso é um alerta')
alert('Isso é um alerta') // Funciona

document.querySelector('h1') // Seleciona o primeiro H1
document.body // retorna o body

~~~

window é um objeto global, por isso não precisamos chamar ele na frente dos seus métodos e propriedades.


#### Node
Toda tag html é representada pelo objeto Element e por isso herda os seus métodos e propriedades. Element é um tipo de objeto Node.

~~~ JavaScript
const titulo = document.querySelector('h1')

titulo.innerText // retorna o texto
titulo.classList // retona as classes
titulo.id // retorna o id
titulo.offsetHeight // retona a altura do elemento

titulo.addEventListener('click', callback)
// ativa a função callback do click no título.
~~~

