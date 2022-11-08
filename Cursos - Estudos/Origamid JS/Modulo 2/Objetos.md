
### Objeto

Conjunto de variáveis e funções, que são chamadas de propriedade e métodos.

~~~javascript
var pessoa = {
	nome: "Rafael",
	idade: 18,
	sexo: "Masculino",
};
~~~

**Métodos**

É uma propriedade que possuí uma função no local do seu valor.

~~~javascript
var quadrado = {
	lados: 4,
	area: function(lado) {
		return lado * lado
	},	
	perimetro: function(lado) {
		return this.lados * lado
	},
};

quadrado.lados // 4
quadrado.area(5) // 25
quadrado.perimetro(5) // 20
~~~

Podemos também usar a propriedade do objeto sem a palavra **function** pasasndo valor diretamente para o parametro.

~~~javascript
var SemPalavraFunction = {
	lados: 4,
	area(lado) {
		return lado * lado;
	},
	perimetro(lado) {
		return this.lados * lado;
	},
};
~~~

Objetos servem para organizar o seu código em pequenas partes reutilizáveis.


**Os objetos são DOT NOTION GET**

Acesse as propriedades de um objeto utilizando  ponto final, neste caso estamos pegando os valores e atribuindo a uma nova variável. 

~~~javascript
var menu = {
	width: 900,
};

const tamanho = menu.width; // tamanho vai receber o valor de 900
~~~

**Os objetos são DOT NOTION SET**

Quando atribuímos valores também a nosso objeto através de DOT

~~~javascript
var menu = {
	width: 900,
};

menu.color = '#FFF'
~~~

Neste exemplo objeto menu recebe a propriedade color com o valor atribuído.

~~~javascript
{
	width: 900,
	color: '#FFF'
};
~~~

**A palavra chave THIS ira fazer uma referência ao próprio objeto**

~~~ JavaScript
var height = 120;
var menu = {
  width: 800,
  height: 50,
  metadeHeight() {
    return this.height / 2;
  }
}

menu.metadeHeight(); // 25
// sem o this, seria 60
~~~

### Tudo é Objeto

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


