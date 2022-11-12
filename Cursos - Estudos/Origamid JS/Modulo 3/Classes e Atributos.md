#### classList

Retorna uma lista com classes do elemento. Permite adicionar, remover e verificar se contém.

~~~ JavaScript
const menu = document.querySelector('menu')

menu.className // string
menu.classList // lista de classes
menu.classList.add('ativo') // add classe 
menu.classList.add('ativo, mobile') // duas classes
menu.classList.remove('ativo')
menu.classList.toggle('ativo') // adiciona/ remove a classe
menu.classList.contains('ativo') // true ou false
menu.classList.replace('ativo', 'inativo')
~~~

#### getAttribute e setAttribute

Métodos que retornam ou definem de acordo com o atributo selecionado.

~~~ JavaScript
const img = document.querySelector('img')

img.getAttribute('src') // valor de src
img.setAttribute('alt', 'Texto Alternativo') // muda o alt
img.hasAttribute('id') // true or false
img.removeAttribute('alt') // remove o alt

img.setAttributes() // true or false
~~~

#### Read Only vs Writable

Existem propriedades que não permitem a mudança de seus valores, essas são consideradas <span style="color:green">READ ONLY</span> ou seja somente leitura.

~~~ JavaScript
const animais = document.querySelector('.animais')

animais.className // string com o nome da classe
animais.className = 'azul' // substitui completamente a string
animais.className +=  'vermelho'// adiciona vermelho a string

animais.attributes = 'class="ativo"' // não funciona, read-only


