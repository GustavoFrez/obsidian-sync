É um grupo de valores geralmente relacionados. Servem para guardarmos diferentes valores em uma única variável.

~~~ JavaScript
var videoGame = ['Switch','PS5', 'Xbox']

videoGame[0] // Switch
videoGame[2] // Xbox
~~~

**Métodos de array**

~~~ JavaScript
var videoGame = ['Switch','PS5', 'Xbox']

videoGame.pop() // Remove o ultimo item
videoGame.push() // insere um item ao array
~~~

**Array e Loops**

~~~ JavaScript
var videoGames = ['Switch', 'PS4', 'XBox', '3DS'];
for (var i = 0; i < videoGames.length; i++) {
  console.log(videoGames[i]);
}
~~~

**Método forEach**

O forEach é um método que executa uma função para cada iem do Array. É uma orma mais simples de utilizarmos um loop com arrays (ou array-like)

~~~ JavaScript
videoGame.forEach((item, index, array) => {
console.log(item);
});
~~~

O método tem os seguintes parâmetros: **item, index e array**.


