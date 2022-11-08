
### Funções

Ao criar um função, você pode definir **parâmetros**  (peso e altura)

~~~javascript
function calculaImc(peso, altura) {
const imc = peso / altura ** 2;
return imc;
}
~~~

Ao executar a função você pode passar argumentos

~~~javascript
calculaImc(80, 1.80)
calculaImc(55, 1.50)
~~~

**Argumentos podem ser funções** 

~~~javascript
addEventListener("click", function () {
console.log("Clicou");
});
~~~

A função possui dois argumentos.
 - Primeiro é a string 'click'
 - Segundo é uma função anônima

Funções anônimas 

~~~javascript
function()

// Arrow Function
() => {}
~~~


**Funções podem ou não retornar um valor**

Quando não definimos o return, a função irá retornar undefined. O código interno da função é executado normalmente, independente de existir valor de return ou não.

~~~javascript
function imc2(peso, altura) {
const imc = peso / altura ** 2;
console.log(imc);
}

imc2(80, 100) // retorna o imc
console.log(imc2(75,1,60)) // retorna o imc e undefined
~~~

**Escopo Léxico**

Funções conseguem sempre acessar variáveis que foram criadas no contexto **pai**

~~~javascript
const profissao = "Front";

function dados() {
	const nome = "André";
	var idade = 25;
		function outrosDados() {
			const endereco = "Rua qualquer da vida";
			var idade = 29;
			return `${nome}, ${idade}, ${endereco}, ${profissao}`;
		}
	return outrosDados();
}
console.log(dados()); // Retorna nome idade endereco e profissão
console.log(outrosDados()) // Dá error
~~~

Neste exemplo a função dados consegue pegaro valor de profissão pois se encontra fora do escopo da função.

No segundo console  de outrosDados() não conseguimos acessar os dados pois a mesma função não da acesso ao espoco da acessar os dados dentro da função dados().



