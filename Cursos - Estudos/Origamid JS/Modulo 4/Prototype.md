#### prototype

 A propriedade <span style="color:green">prototype</span> é um objeto adicionado a uma função quando a mesma é criada.

~~~ JavaScript
function Pessoa(nome, idade) {
	this.nome = nome;
	this.idade = idade;
}

const andre = new Pessoa("Andre", 28);
console.log(Pessoa.prototype);
~~~

#### funcao.prototype

É possível adicionar novas propriedades e métodos ao objeto prototype.

~~~ JavaScript
Pessoa.prototype.andar = function() {
	return this.nome + 'andou';
}

Pessoa.prototype.nadar = function() {
	return this.nome = 'nadou'
}

console.log(Pessoa.prototype)
~~~

#### Acesso ao Protótipo

O objeto criado utilizando o construtor, possui acesso aos métodos e propriedades do protótipo deste construtor. Lembrando, prototype é uma propriedade e funções apenas.

~~~ JavaScript
const andre = new Pessoa('Andre', 28)

andre.nome;
andre.idade;
andre.andar();
andre.nadar()
~~~

#### _proto_

O novo objeto acessa os métodos e propriedades do protótipo através da propriedade <span style="color:green">__proto__</span> . É papel da engine fazer essa busca, não devemos falar com <span style="color:green">__proto__</span> diretamente.

~~~ JavaScript
// Acessam o mesmo método
// mas __photo__ não terá acesso ao this.nome
andre.andar()
andre.__proto__.andar()
~~~

#### Herança de Protótipo

O objeto possui acesso aos métodos e propriedades do protótipo do construtor responsável por criar este objeto. O objeto abaixo possui acesso a métodos que nunca definimos mas são herdados do protótipo de Object.

~~~ JavaScript
Object.prototype
andre.toString();
andre.isPrototypeOf();
andre.valueOf();
~~~

#### Construtores Nativos

Objetos, Funções, Números e Strings e outros tipos de dados são criados utilizando construtores. Esses construtores possuem um protótipo com propriedades e métodos, que poderão ser acessados pelo tipo de dado.

~~~ JavaScript
const pais = 'Brasil'
const cidade = new String('Rio')

pais.chartAt(0) // B
cidade.chartAr(0) // R
~~~



#### É possível acessar a função do protótipo

É comum, principalmente em códigos mais antigos, o uso direto de funções do protótipo do construtor Array.

~~~ JavaScript
const lista = document.querySelectorAll('li') 
  
//Transforma em uma array 
const listaArray = Array.prototype.slice.call(lista)
~~~

Existe o método Array.from( )

#### Método do Objeto vs Protótipo

Nos objetos nativos existem métodos linkados diretamente ao Objeto e outros linkados ao protótipo.

~~~ JavaScript
Array.prototype.slice.call(lista)
Array.from(lista)

// Retorna uma lista com os métodos / propriedades

Object.getOwnPropertyNames(Array)
Object.getOwnPropertyNames(Array.prototype)
~~~

#### Entenda  o que esta sendo retornado

Os métodos e propriedades acessoado com o  <span style="color:green">.</span> (ponto) são referentes ao tipo de dados que é retornado antes desse <span style="color:green">.</span> (ponto)


~~~ JavaScript
const Carro = {
  marca: 'Ford',
  preco: 2000,
  acelerar() {
    return true;
  }
}

Carro // Object
Carro.marca // String
Carro.preco // Number
Carro.acelerar // Function
Carro.acelerar() // Boolean
Carro.marca.charAt // Function
Carro.marca.charAt(0) // String
~~~




