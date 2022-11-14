#### Objetos

Criar um objeto é bem simples, basta definirmos uma variável e iniciar a definição do seu valor com chaves { }. Mas e se precisarmos criar um novo objeto, com as mesmas caracteristicas do anterior ?


#### Constructor Functions

Para isso existem as Constructor Functions, ou seja, Funções Construtoras que são responsáveis por construir novo objetos sempre chamamos a mesma.

~~~ JavaScript
function Carro() {
	this.marca = "Marca";
	this.preco = 50000;
}
const honda = new Carro();

const fiat = new Carro();

fiat.marca = "Fiat";
~~~

Sempre que criarmos uma função construtora a regra é usar PASCAL CASE onde a primeira letra é maiuscula e o resto minuscula.

#### new Keyword

A palavra chave <span style="color:green">new</span> é responsável por criar um novo objeto baseado na função que passarmos a frente dela.

~~~ JavaScript
const honda = new Carro()

// 1 Cria um novo objeto
honda = {}

// 2 Define o protótipo
honda.prototype = Carro.prototype

// 3 Aponta a variável this para o objeto
this = honda

// 4 Executa a função. subtituindo this pelo objeto
honda.marca = "Marca";

// 5 Retorna o novo objeto
return honda = {
	marca: 'Marca',
	preco: 0,
}
~~~

#### this Keyword

O <span style="color:green">this</span>  faz referência ao próprio objeto construído com a Coonstructor Function.

~~~ JavaScript
function Carro (marca, precoInicial) {
	const taxa = 1.2;
	const precoFinal = precoInicial * taxa
	this.marca = marca
	this.preco = precoFinal
	console.log(this)
}

const honda = new Carro('Honda', 2000)
~~~

* Variáveis dentro da Constructor estão 'protegidas'

Exemplo real :

Quando mudamos a propriedade seletor, o objeto Dom irá passar pa selecionar o novo seletor em seus métodos. 

~~~ JavaScript
function Dom() {
  this.seletor = 'li';
  const element = document.querySelector(this.seletor);
  this.ativo = function() {
    element.classList.add('ativo');
  };
}

const lista = new Dom();
lista.seletor = 'ul';
lista.ativo();

const lastLi = new Dom();
lastLi.seletor = 'li:last-child';
lastLi.ativo();
~~~
