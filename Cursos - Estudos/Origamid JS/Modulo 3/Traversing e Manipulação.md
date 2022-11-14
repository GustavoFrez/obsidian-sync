#### outerHTML - innerHTML - innerText

Propriedades que retornam uma string contendo o html ou texto. É possível atribuir um novo valor para as mesmas.

<span style="color:green">element.innerText = 'Novo Texto'</span>  

~~~ JavaScript
const menu = document.querySelector('.menu')

menu.outerHTML // todo o html do elemento
menu.innerHTML // html interno
menu.innerTxt // texto, sem tags

menu.innerText = '<p>Texto</p>' // a tag vai como texto
menu.innerHTML = '<p>Texto</p>' // a tag é renderizada 
~~~

#### Transversing

Como navergar pelo DOM, utilizando suas prioridades e métodos.

~~~ JavaScript
const lista = document.querySelector('.animais-lista')

lista.parentElement // pai
lista.parentElement.parentElement // pai do pai
lista.previousElementSibling // elemento acima
lista.nextElementSibling // elemento abaixo

lista.children // HTMLCollection com os filhos
lista.children[0] // primeiro filho
lista.children[--lista.children.length]; // ultimo filho

lista.querySelectorAll('li') // todas as LI's
lista.queySelector('li:last-child') // último filho
~~~

#### Element vs Node

Element's representam um elemento HTML ou seja uma TAG. Node representa um nó e poder ser  elemento (Element), texto, comentário quebra de linha e mais.

~~~ JavaScript
const lista = document.querySelector('.animais-lista')

lista.previousElementSibling // elemento acima
lista.ElementSibling // node acima
~~~

Geralmente estamos atras de um Element.


#### Manipulando Elementos

~~~ JavaScript
const lista = document.querySelector('.animais-lista');
const contato = document.querySelector('.contato');
const titulo = contato.querySelector('.titulo');

contato.appendChild(lista); // move lista para o final de contato
contato.insertBefore(lista, titulo); // insere a lista antes de titulo
contato.removeChild(titulo); // remove titulo de contato
contato.replaceChild(lista, titulo); // substitui titulo por lista
~~~

#### Novos elementos

Podemos criar novos elementos com o método <span style="color:green">createElement()</span>

~~~ JavaScript
const animais = document.querySelector('.animais');

const novoH1 = document.createElement('h1')
novoH1.innerText = 'Novo título'
novoH1.classList.add('titulo')

animais.appendChild(novoH1)
~~~


#### Clonar Elementos

Todo elemento selecioanado é único. Para criarmos um novo elemento baseado no anterior, é necessário utilizar o método <span style="color:green">cloneNode()</span>

~~~ JavaScript
const titulo = document.querySelector('.h1');

const clonarTitulo = titulo.cloneNode(true)
const contato = document.querySelector('.contato')

contato.appendChild(cloneTitulo)
~~~

