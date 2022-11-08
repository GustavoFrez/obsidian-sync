
#### Escopo de função:

Variavéis declaradas dentro de funções não são acessadas fora da mesmas.

~~~ JavaScript
function mostraCarro() {
	var carro = "Fusca";
	console.log(carro);
}

mostraCarro(); // Fusca no console
console.log(carro); // Erro, carro is not defined
~~~

Porque existe o escopo ? 
	O escopo evita o conflito entre nomes.

#### Const

Const mantém o escopo do bloco, impede a redeclaração e impede a modificação do valor da variável, evitando bugs no código.

~~~ JavaScript
const mes ='Dezembro'
mes = 'Janeiro' // erro, tentou modificar o valor

const semana; // erro declarou sem valor

const data = {
	dia: 28,
	mes: 'Dezembro',
	ano: 2018
}  

data.dia = 29 //Funciona
data = 'Janeiro' // erro
~~~

#### Let

Mantém o escopo do bloco, impede a redeclaração, mas permite a modificação do valor da variável.

~~~ JavaScript
let ano;
ano = 2018
ano++
console.log(ano) // 2019

let ano = 2020 // erro, redeclarou a variável
~~~

