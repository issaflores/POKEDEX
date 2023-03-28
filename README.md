# O que é HTML?
HTML, ou H yper T ext Markup Language , é uma linguagem de marcação usada para definir a estrutura e os elementos em uma página da web. Tudo como botões, menus, imagens, etc. são definidos usando HTML.

A estrutura básica do HTML é a seguinte:

<article>
  <img />
</article>
As tags HTML são colocadas entre colchetes angulares. Se uma tag HTML permitir que outras tags HTML estejam dentro dela, como uma imagem ou parágrafo dentro de um artigo, as tags internas são seus filhos. Em nosso exemplo acima, a imgtag é filha da articletag.

Depois de especificar todos os filhos para a tag, você deve fechar a tag HTML com uma tag final. As tags HTML são fechadas com uma barra ( /) após o primeiro colchete angular.

Tags de fechamento automático
A exceção a isso é mostrada no meu exemplo com a imgtag. Em HTML, existem algumas tags que fecham automaticamente. Com tags de fechamento automático, a barra é colocada antes do colchete angular final e não há necessidade de uma tag de fechamento. Isso ocorre porque essas tags não podem ter filhos. Por exemplo, a imgtag mostrada acima é a tag HTML para exibir uma imagem. Logicamente não faz sentido permitir que outra tag seja exibida dentro dela, porque é uma imagem.

Atributos de tags HTML
No meu exemplo acima, temos uma tag de imagem. No entanto, há um problema. Embora tenhamos uma tag, como o navegador sabe qual imagem exibir? Podemos fornecê-lo com um atributo que forneça à tag uma URL ou o local da imagem que gostaríamos que ela exibisse.

<img src="http://bit.ly/charizardgif" />
Neste exemplo, temos uma tag de imagem. O srcatributo é o nome do argumento, neste caso é a fonte ou localização da imagem que queremos mostrar. Em seguida, informamos entre aspas a localização de nossa imagem, http://bit.ly/charizardgif.

##O que é CSS?
CSS ou C ascading S tyle Sheets é uma linguagem de folha de estilo que permite adicionar estilo ao seu HTML.

Coisas como adicionar um plano de fundo, alterar sua fonte e definir os tamanhos dos elementos HTML são coisas que podem ser feitas em CSS.

Vamos aprender como o CSS funciona por exemplo:

.game {
  background-color: #000;
}
A sintaxe CSS é diferente do HTML. Em vez de colchetes angulares, usamos chaves e ponto e vírgula. Vamos decompor o exemplo acima.

Seletores e Classes CSS
.game {
Aqui temos nosso seletor de CSS. Um seletor CSS informa ao nosso navegador quais elementos HTML ele gostaria de estilizar. Neste exemplo, você pode notar que nosso seletor é .game. O ponto informa ao nosso navegador que estamos procurando uma classe e o nome dessa classe é game.

Na próxima linha temos o seguinte:

background-color: #000;
Neste caso, background-coloré uma propriedade que queremos alterar e #000é o valor para o qual queremos alterar a cor de fundo. #000é uma representação hexadecimal de uma cor. Na programação, frequentemente usamos cores hexadecimais para obter cores específicas. Essas cores estão em RGB. Portanto, #000traduza para 0 quantidade de vermelho, 0 quantidade de verde e 0 quantidade de azul. Assim, #000é preto.

CSS também nos permite usar alguns nomes de cores como preto ou vermelho, mas usar hex nos permite ter mais flexibilidade e personalização.

O que é uma aula?
Uma classe é uma forma de identificar elementos HTML que são semelhantes, devem compartilhar um estilo comum e/ou sua finalidade.

Para definir a classe de um elemento HTML, especifique-os no classatributo da seguinte forma:

<div class="orange dog">
</div>
Neste exemplo, damos ao nosso divelemento duas classes. Os elementos HTML podem ter várias classes e devem ser separados por um espaço. A primeira classe que fornecemos é orange. Se definimos orangeem css assim:

.orange {
  background-orange: orange;
}
Isso definiria o plano de fundo não apenas desse elemento como laranja, mas de todos os elementos que também possuem a classe laranja.

A segunda classe que fornecemos é dog. Para este exemplo, poderíamos assumir que nosso divelemento deve representar ou exibir um cachorro porque damos a ele a dogclasse. Assim poderíamos definir um estilo universal que todo cachorro deve seguir assim:

.dog {
  width: 100px;
}
Basicamente, estamos dizendo que todos os cães, ou todos os elementos HTML com a dogclasse, devem ter uma largura de 100 pixels. Simples o suficiente, certo?

Mas e se quisermos que os cachorros laranja tenham apenas 50 pixels de largura? Talvez os cachorros laranja sejam sempre menores. Podemos abordá-lo assim:

.orange.dog {
  width: 50px;
}
Aqui estamos fornecendo a classe orangee a classe dogcombinada. Observe que não há espaço entre .orangee .dog. É assim que diríamos se um elemento HTML tem a classe orange e dog usa esse estilo.

Esse seletor também é mais específico do que apenas orangeou dog. Significa que nosso navegador exibirá suas propriedades sobre os outros se definirmos todos os 3 exemplos.

Selecionar elemento por ID
#attack {
  color: orange;
  font-family: "Times New Roman";
}
Neste exemplo, falaremos sobre como selecionar um elemento específico para estilizar. Digamos que temos uma imagem, é um botão especial para atacar. Queremos apenas que esse botão específico tenha esse estilo. Em vez de usar uma classe, usaremos um ID. Um ID é um identificador exclusivo para um elemento HTML que nos permite destacar esse elemento específico. Podemos definir esse atributo semelhante a uma classe:

<button id="attack"></button>
A única diferença é que só podemos atribuir um ID a um elemento. Portanto, com base em nossos exemplos, nosso botão tem o id attack. Em nosso CSS, informaremos ao nosso navegador que queremos selecionar um ID. Então usamos o símbolo hash ( #) seguido do nosso ID. Isso dirá ao navegador para estilizar nosso botão para ter texto laranja e usar a fonte Times New Roman.

Geralmente é uma boa ideia usar classes em vez de IDs para aplicar estilos. Facilita a leitura e compreensão do código.

Seletores de elementos
button {
  border-color: blue;
  border-style: solid;
  border-width: 1px;
}
Agora, veremos o caso de quando queremos estilizar todo um tipo específico de tag ou elemento. Nesse caso, queremos estilizar cada botão em nossa página. Para fazer isso, não especificamos um ponto ou um hash. Em vez disso, especificamos o nome da tag. Neste exemplo, estamos dizendo aos nossos navegadores para estilizar cada botão com uma borda azul, que é uma linha sólida e tem 1 pixel de largura ao redor do botão.

Estilizando crianças
.opponent .pokemon {
  width: 100px;
  height: 100px;
}
E se estivermos no cenário em que queremos estilizar um filho de um elemento? Neste exemplo, queremos estilizar o pokemonque pertence ou é filho de nosso opponent. Apenas nosso oponente, não o nosso pokemon. Especificaremos a classe pai .opponente, com um espaço, especificaremos a classe filha .pokemon. Assim, nosso opponent's pokemonterá largura e altura de 100 pixels;

Essa classe filha pode ser substituída por um ID, um tipo de elemento ou qualquer outro seletor também. Existem outras maneiras de selecionar elementos filhos para ser mais específico, mas neste tutorial usaremos apenas este método para manter as coisas simples.

Estruturando nosso jogo usando HTML
Começaremos criando o seccionamento de nosso jogo em duas partes. O jogo e o menu onde podemos ver as mensagens e as ações que podemos escolher para o nosso Pokémon.

Para fazer isso, precisamos criar dois divelementos HTML com suas respectivas classes.

Em HTML, um divelemento é uma seção do documento. divsignifica divisão, ou seja, por padrão, quando você usa um divelemento, os elementos depois dele irão quebrar em uma nova linha em vez de permanecer na mesma linha. divs são as tags HTML mais comuns que você verá e usará.

<div class="game">
</div>
<div class="menu">
</div>
O que precisamos
Vamos pensar um pouco sobre os elementos HTML de que precisamos. Precisamos de quatro botões para nossos ataques e um local para uma mensagem em nosso menu. Para o jogo, precisamos

duas imagens para o nosso Pokemon
um lugar para exibir nosso HP (Saúde)
o nome e o nível do nosso Pokémon
quantos pokémons temos
e uma caixa para manter todas essas informações organizadas
Também precisaremos de uma maneira de diferenciar as coisas do nosso oponente das nossas, então seria bom se tivéssemos dois pais diferentes: playere opponentassim pudéssemos saber qual filho pertence a quem.

Primeiro vamos adicionar nossos pais para cada jogador:

<div class="game">
  <div class="opponent">
  </div>
  <div class="player>
  </div>
</div>
Adicionando nosso Pokémon
Em seguida, adicionaremos nosso Pokémon. Usaremos uma imgtag para exibir nossas imagens na tela e dar a aula a elas pokemon.

<div class="game">
  <div class="opponent">
    <img class="pokemon" src="http://bit.ly/charizardgif" />
  </div>
  <div class="player>
    <img class="pokemon" src="http://bit.ly/blastoisegif" />
  </div>
</div>
Forneci a cada imgtag os URLs de nossa imagem apropriada em seu srcatributo. Eu fiz essas URLs de antemão, mas você pode usar qualquer imagem que quiser, desde que seja carregada na Internet com uma URL que você possa usar.

Formatando nossa view usando CSS
Definindo nossas dimensões básicas
Como você pode notar, as coisas não se parecem muito com um jogo, ou mesmo com caixas. Vamos definir alguns tamanhos usando CSS para que possamos começar a visualizar melhor nosso jogo.

Vamos definir a altura de nosso .gameto 480pxe 800px. Isso dará ao nosso jogo um tamanho fixo, facilitando o design por enquanto.

.game {
  height: 480px;
  width: 800px;
}
Aplicaremos a mesma largura, mas uma altura menor para o menu:

.menu {
  height: 120px;
  width: 800px;
}
Adicionando planos de fundo
Agora, vamos adicionar um pouco de cor à nossa paisagem branca chata.

Usaremos uma imagem de um plano de fundo da sequência de batalha de Pokémon para o plano de fundo do nosso jogo.

.game {
  background-image: url('http://bit.ly/pokemonbg');
  background-size: 100% 100%;
  background-repeat: no-repeat;
  ...
}
Aqui estamos definindo a background-imagepropriedade para o url de nossa imagem de plano de fundo, informando ao nosso navegador que o tamanho de nosso plano de fundo deve ser 100%a altura e a largura de nosso .game, e que não queremos que nosso plano de fundo se repita.

Também queremos um plano de fundo para o nosso menu. Uma bela cor cinza deve servir. Frequentemente gosto de usar #333 como minha cor cinza para planos de fundo:

.menu {
  background-color: #333;
  ...
}
Posicionando nosso Pokémon
Agora que temos nossos antecedentes, podemos posicionar nossos Pokémon em suas posições de batalha.

Definindo limites
