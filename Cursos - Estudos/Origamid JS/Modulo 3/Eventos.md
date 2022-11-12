#### addEventListener

  Adiciona uma função ao elemento, esta chamada de <span style="color:green">callback</span> que será ativada assim que certo <span style="color:green">evento</span> ocorrer neste elemento.

~~~ JavaScript
const img = document.querySelector('img')

//elemento.addEventListener(event, callback, options)
img.addEventListener('click', function() {
	console.log('Clicou')
})

// O terceiro parâmetro é opcional.
~~~

#### Propriedades do Event


~~~ JavaScript
const animais = document.querySelector('.animais-lista')

function executarCallback(event) {
	const currentTarget = event.currenrTarget // this
	const target = event.target // onde o clique ocorreu
	const type = event.type // tipo de evento
	const path = event.path 
	console.log(currentTarget, target, type, path)
}

animaisLista.addEventListener('click', executarCallback)
~~~

#### event.preventDefault()

Previne o comportamento padrão do evento no browser. No caso de um link externo, por exemplo, irá previnir que o link seja ativado.

~~~ JavaScript
const linkExterno = document.querySelector('a[href^="http"]')

function clickNoLink(event) {
	event.preventDefault()
	console.log(event.currentTarget.href)
}

linkExterno.addEventListener('click', clickNoLink)
~~~

#### This

A palavra chave  <span style="color:green">this</span> é uma palavra especial de JavaScript, que pode fazer referência a diferentes objetos dependendo do contexto. No caso eventos, ela fará referência ao elemento em que addEventListener foi adicionado.

~~~ JavaScript
const img = document.querySelector('img')

function callback(event) {
	console.log(this) // retorna a img
	console.log(this.getAttribute('src')) // 
}

img.addEventListener('click', callback)
~~~

#### Diferentes Eventos

Existem diversos eventos como   <span style="color:green">click</span>,   <span style="color:green">scrool</span>,   <span style="color:green">resize</span>,   <span style="color:green">keydown</span>,   <span style="color:green">keyup</span>,   <span style="color:green">mouseenter</span> e mais. Eventos poser acionados a diferentes elementos, como o   <span style="color:green">window</span> e   <span style="color:green">document</span> também.

~~~ JavaScript
const h1 = document.querySelector('h1')

function callback(event) {
	console.log(event.type, event) // retorna a img
}

h1.addEventListener('click', callback)
window.addEventListener('scroll', callback)
~~~

####  Keyboard

Você pode adicionar atalhos para facilitar a navegação no seu site, através de eventos do <span style="color:green">keyboard</span>.

~~~ JavaScript
function handleKeyboard(event) {
	if(event.key === 'a')
		document.body.classList.toggle('azul');
	else if (event.key === 'v')
		document.body.classList.toggle('vermelho')
}

window.addEventListener('keydown', callback)
~~~

