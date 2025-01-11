# NotesPT.md

**Disclaimer:** This document contains notes I have taken throughout my Fullstack development course. There is also a separate file available in English in the repository. You can access it here: [NotesEN.md](https://github.com/Nixwzy/learningFS/blob/main/notesEN.md).

Este arquivo contém anotações que fiz ao longo do meu curso de desenvolvimento Fullstack. Nele, estão documentados conceitos e exemplos práticos relacionados a tecnologias como PHP, Laravel, NodeJS e React. É um repositório pessoal de aprendizado, onde registro informações importantes que adquiri durante as aulas.

# Objetivo com o NotesPT.md
Tenho como principal objetivo, ao concluir certos módulos do curso e adquirir conhecimento suficiente, tornar o Notes um grande site com anotações e tópicos relacionados ao Desenvolvimento FullStack.<br>
A ideia é construir um repositório digital completo que aborde diversos aspectos do desenvolvimento web, como Frontend, Backend, Banco de Dados, DevOps, e Boas Práticas de Programação.<br>
A visão para o futuro é que o site seja uma referência pessoal, mas também útil para outras pessoas que estão em processo de aprendizagem.


# Curso de HTML5 e CSS
Como introdução, este curso explora os fundamentos do desenvolvimento web, abordando desde a estruturação de documentos HTML até o uso de CSS para estilização e layout. Ao longo das aulas, são cobertos tópicos essenciais como seletores, propriedades de estilo, design responsivo e boas práticas de acessibilidade, proporcionando uma base sólida para a criação de sites modernos e funcionais.

**Aviso**: O NotesPT serve como um bloco de anotações pessoal, onde registro conceitos e práticas que considero mais relevantes, podendo não conter informações exaustivas sobre todos os temas abordados no curso.

## Seletor CSS

```css
nomeElemento {
    /* seleciona todas as ocorrências do elemento */
}

#idElemento {
    /* seleciona a id específica do elemento */
}

.classElemento {
    /* seleciona a classe específica do elemento */
}

elemento, outroElemento, outroElemento2 {
    /* seleciona vários elementos ao mesmo tempo */
}

elemento outroElemento {
    /* seleciona um elemento dentro de outro */
}
```

## Bordas em CSS

```css
elemento {
    border: espessura tipo cor;
}
```

### Tipos de borda
- `solid` -> Mais usada
- `dotted`
- `dashed`
- `double`
- `groove`

### Posições de borda

```css
elemento {
    border-bottom: espessura tipo cor;
}

elemento {
    border-top: espessura tipo cor;
}

elemento {
    border-left: espessura tipo cor;
    border-right: espessura tipo cor;
}

elemento {
    border-radius: espessura;
}
```

## Criar uma div redonda utilizando border (e também manipular formatos)

```css
.div {
    background-color: #00FF00; /* fazendo a div ser visível */
    width: 200px;
    height: 200px;
    border-radius: 100px; 
    border: 3px solid darkgreen;
    
    /* para certificar da div ser redonda, o border-radius deve ser a metade
    do tamanho do quadrado */
}
```

## Margin e paddings

Todo elemento HTML tem 4 propriedades distintas:
- Conteúdo (text);
- border;
- padding;
- margin.

### Manipular padding

```css
/* Manipulando todos os lados do padding com valores diferentes */
.exemplo {
    padding: cima, baixo, esquerda, direita;
}
.exemplo {
    padding: 1px, 2px, 3px, 4px;
}

/* Manipulando cima/baixo e esquerda/direita com o mesmo valor */
.exemplo {
    padding: 10px, 20px;
}

/* Aplicando apenas um valor para todos os lados */
.exemplo {
    padding: 10px;
}
```

## Width e Height

width -> largura  
height -> altura  

Existem formas de determinar o tamanho de width/height, alguns deles são:

```css
.example {
    width: 100px;
    /* 100 pixels */
}

.example {
    width: 100%;
    /* utiliza 100% da largura disponível do elemento pai */
}

.example {
    width: auto;
    /* mesma coisa de não definir nada */
}

.example {
    width: inherit;
    /* herda o tamanho do item anterior */
}

.example {
    min-width: 50px;
    max-width: 500px;
    width: 550px;
    /* A largura não será menor de 50px nem maior de 500px */
}
```

## Box-Sizing

```css
* {
    box-sizing: content-box;
    /* ou */
    box-sizing: border-box;
}

/* O uso do asterisco no CSS é um seletor universal. */
/* content-box: padding e border não são incluídos nas dimensões, sendo somados ao objeto. */
/* border-box: o valor total da dimensão inclui padding e borda. */
```

## Atributos na tag anchor (link)

### Target
Utilizar o target="_blank" dentro da tag anchor faz a página ser aberta em uma nova guia.

```html
<a href="pagina.html" target="_blank">Nova Página</a>
```

### Title
Utilizar title faz com que, ao passar o mouse, uma mensagem apareça.

```html
<a href="pagina.html" title="Mensagem">Nova Página</a>
```

## Formatação em HTML

```html
<b>bold</b> -> Negrito, sem semântica de relevância.
<strong>strong</strong> -> Negrito, com semântica de relevância.

<i>italic</i> -> Itálico, sem semântica de relevância.
<em>emphasize</em> -> Itálico, com semântica de relevância.

<small>small</small> -> A fonte se torna menor, em relação ao tamanho previamente especificado.

<del>del</del> -> Risca o texto.

<mark>mark</mark> -> Destaca o texto. (Aplica um background com cor padrão amarela)

<sup>sup</sup> -> Exibe o texto sobrescrito.

<sub>sub</sub> -> Exibe o texto subscrito.

<u>underline</u> -> Sublinha o texto, sem semântica de relevância.

<abbr>abbr</abbr> -> Define uma abreviação em forma de hover.

<code>code</code> -> Define um trecho de código dentro do texto.

<pre>pre</pre> -> Define um texto pré-formatado.
```

## Criar tabelas CSS

```html
<table></table> -> Criar tabela;
<tr></tr> -> Cria linhas (horizontais);
<td></td> -> Cria colunas (verticais);
```

Uma tabela é basicamente:

```html
   <table class="table" width="400" border="1">
      <thead>
        <tr>
          <th>Header 1</th>
          <th>Header 2</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Conteúdo</td>
          <td>Conteúdo</td>
        </tr>
        <tr>
          <td>Conteúdo</td>
          <td>Conteúdo</td>
        </tr>
        <tr>
          <td>Conteúdo</td>
          <td>Conteúdo</td>
        </tr>
      </tbody>
    </table>

```
## Formulário

Para criar um formulário:
```html
<form>
</form>
```

Tendo dois atributos:

### Atributo Action
```html
<form action="proximaPagina.html">

</form>
```
Define para onde os dados do formulário serão enviados.

### Atributo Method
Especifica como os dados serão enviados:

GET: envia os dados via URL (usado para requisições simples).
POST: envia os dados no corpo da requisição (mais seguro para dados sensíveis).
```html
<form method="GET">

</form>

<form method ="POST">

</form>
```
### Input

```html
<form action="proximaPagina.html" method="GET">
    <input type="type" name="name"/>
    <input type="submit">
</form>
```
No caso acima, o que for colocado no input, será enviado como dado armazenado em forma de "name" para a próxima página.

### Alguns tipos de Input

- text
    - email
    - password
- radio 
- checkbox
- submit

E vários outros, podendo ser checados aqui: [Input Types](https://www.w3schools.com/html/html_form_input_types.asp).

### Select

```html
<form action="proximaPagina.html" method="GET">
    <select name="name">
        <option value="value">Opção 1</option>
        <option value="value">Opção 2</option>

        <input type="submit">
    </select>
</form>
```
O submit fará com que o valor (value) selecionado através das opções do select seja enviado para a próxima página.

- Atributo Selected:
```html
<form action="proximaPagina.html" method="GET">
    <select name="name">
        <option value="value">Opção 1</option>
        <option value="value" selected>Opção 2</option>

        <input type="submit">
    </select>
</form>
```
A opção que aparecerá como padrão, sempre será a primeira, caso não seja colocado o atributo selected, que torna a opção como padrão.

## Input Type File

Ao implementar um input type file, deve-se colocar, nos atributos de formulário, o atributo **enctype="multipart/form-data"** para o servidor conseguir receber o arquivo.
```html
<form method="POST" action= "example.php" enctype="multipart/form-data">
    <input type="file" name="photo" accept="image/*" /> /* Exemplo */
</form>
```

## Herança
No CSS, a herança permite que alguns estilos sejam passados de um elemento pai para seus filhos. Por exemplo, se você definir a cor do texto no elemento <body>, todos os textos filhos herdarão essa cor, a menos que outra regra mais específica seja aplicada.

## Especificidade

A especificidade define a prioridade das regras aplicadas ao mesmo elemento. Regras mais específicas prevalecem sobre as menos específicas. A ordem de especificidade, em ordem crescente, geralmente é: seletores de tipo (elementos como div, p), classes (.classe), e, mais alto, IDs (#id). Se dois seletores têm a mesma especificidade, o último no código será aplicado. **Um exemplo disso:**

**HTML**
```html
<html>
    <body>
    <div class="container">
        Este é um texto qualquer.   <!-- Texto que será alterado -->
    </div>
  </body>
</html>
```

**CSS**

```css
.container {
    color: #FF0000; /* cor vermelha */
}

/* div {
    color: #0000FF; cor azul
}
    Esta seleção, se for competir com .container (classe dentro da div), a classe ganha, por causa da especificidade mais alta da classe .container em comparação ao seletor de elemento div. Ou seja, a cor vermelha permanece. 


body .container {
    color: #00FF00; cor verde
}
    Esta seleção, se for competir com .container, body .container vence por ter maior especificidade, pois envolve tanto o seletor body quanto .container. Ou seja, a cor verde prevalece.
 */
```

**Lembrando:** O CSS é processado de cima para baixo, ou seja, o navegador lê e aplica o CSS na ordem em que está no arquivo. 
Assim, se houver duas regras com a mesma especificidade para o mesmo elemento, a última regra no código prevalece. 
Isso é especialmente útil para substituir estilos com regras mais recentes ou específicas.

## Unidades de Medida em HTML e CSS
**em** -> relativa (multiplicativo) ao tamanho da fonte do elemento pai. </br>
**rem** -> relativa ao root element (elemento raiz).</br>
**%** -> porcentagem (em relação ao elemento pai).</br>
**vw e vh** -> viewport width e viewport height, medem a largura e altura com base no tamanho da janela de visualização.</br>
**vmin e vmax** -> baseiam-se na menor e maior dimensão da viewport, respectivamente.</br>
**px** -> pixels </br>
**pt** -> points (1/72 in)</br>
**cm** -> centímetros</br>
**mm** -> milímetros</br>
**ch** -> largura do caractere</br>

## Object-fit
A propriedade **object-fit** do CSS é usada para especificar como o conteúdo (geralmente imagens) de um elemento deve se ajustar ao seu container.

### Valores de object-fit:

1. **fill**:
   - Este é o valor padrão.
   - O conteúdo é esticado para preencher completamente o container, ignorando a proporção original. Isso pode fazer com que o conteúdo fique distorcido.
     ```css
     img {
       object-fit: fill;
     }
     ```

2. **contain**:
   - O conteúdo é ajustado para caber completamente dentro do container, preservando sua proporção original. Se o conteúdo não preencher todo o espaço do container, ele será centralizado, e o espaço restante será deixado em branco.
     ```css
     img {
       object-fit: contain;
     }
     ```

3. **cover**:
   - O conteúdo é redimensionado para cobrir todo o container, preservando sua proporção. Isso pode resultar em parte do conteúdo sendo cortada, mas garante que não haja espaços em branco no container.
     ```css
     img {
       object-fit: cover;
     }
     ```

4. **none**:
   - O conteúdo mantém seu tamanho original, sem redimensionamento. Se o conteúdo for maior que o container, ele transbordará, e se for menor, haverá espaço vazio.
     ```css
     img {
       object-fit: none;
     }
     ```

5. **scale-down**:
   - Este valor combina os comportamentos de none e contain. O conteúdo será redimensionado apenas se for maior que o container, mas manterá sua proporção.
     ```css
     img {
       object-fit: scale-down;
     }
     ```

## Picture source media
Em termos de responsividade, a tag picture, junta da tag source media, ajuda ao site se adequar em relação ao tamanho da tela.

```html
<picture>
  <source media="(min-width: 650px)" srcset="imagem1.jpg">
  <source media="(min-width: 450px)" srcset="imagem2.jpg">
  <img src="imagem3.jpg" alt="Imagem responsiva">
</picture>
```

No caso acima, caso a largura da tela (sendo utilizando o min-width, poderia ser um height ou algum outro) for 650px ou mais, a imagem 1 será exibida; </br>
Caso a largura da tela seja entre 450px e 649px, a imagem 2 será exibida;</br>
Caso não cumpra nenhum desses requisitos e seja menor que 450px, a imagem 3 será exibida. (lembra muito o if-else statement lol)</br>

## CSS: @media
O @media é um recurso do CSS que permite adaptar o layout e o design de uma página conforme o tamanho da tela é alterado.
Um exemplo disso:
```css
body {
  background-color: green; /* cor padrão do background será verde caso nenhuma das requisições @media forem satisfeitas */
}

@media (min-width: 1000px) {
  body {
    background-color: blue; /* quando a tela tiver no mínimo 1000px, a cor do background será azul */
  }
}
@media (min-width: 700px) and (max-width:999px) { /* quando a tela tiver entre 700 e 999 px, a cor será vermelha */
  body {
    background-color: red;
  }
}
@media (min-width: 300px) and (max-width: 699px) { /* quando a tela estiver entre 300 e 699 px, a cor será amarela */
  body {
    background-color: yellow;
  }
}
```
Não precisando se ater apenas à cor do background, outras características podem ser adicionadas ao CSS, para adaptar o estilo da página html em relação ao tamanho disponível na tela.

### @media only print
```css
@media only print {
    body {
        display: none;
    }
}
```
O **only print** basicamente faz com que o estilo dentro desse media query seja modificado apenas quando a página for impressa.

### @media orientation

O **@media** pode ser usado para alterar o layout com base na orientação da tela, seja **landscape** (paisagem) ou **portrait** (retrato).

- Criando quatro divs (quadrados) com a classe box:
```html
  <body>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </body>
  ```
  Nesse caso, eu quero que quando a tela do celular estiver em portrait, as caixas sejam exibidas em pé, e quando estiver em landscape, deitadas.</br>
  Para isso, basta inserir o código em CSS:
  ```css
  body {
  display: flex;
  background-color: #CCC; /* definindo o fundo da página */
}

.box { /* definindo as caracteristicas das boxes */
  width: 100px;
  height: 100px;
  border: 3px solid black;
  background-color: #CDC;
  margin: 2pt;
}

@media (orientation: landscape) { /* definindo o @media para quando estiver em modo paisagem */
  body {
    flex-direction: row;
  }
}

@media (orientation: portrait) { /* definindo o @media para quando estiver em modo retrato */
  body {
    flex-direction: column;
  }
}
```
Nesse caso, a página fica assim:
- Modo Paisagem:
<p></p>
<img src="assetsForNotes\landscapeExample.png">
<p></p>
- Modo Retrato:
<p></p>
<img src="assetsForNotes\portraitExample.png">
<p></p>

### @media aspect-ratio
O @media (aspect-ratio) é uma consulta de mídia usada para aplicar estilos baseados na proporção de largura e altura da tela. </br>
A proporção é expressa como a relação entre a largura e a altura de um dispositivo, como 16/9, 4/3, entre outros.

```css
@media (aspect-ratio: 16/9) {
  body {
    background-color: blue; /* quando a tela tiver uma proporção de 16:9, o background será azul */
  }
}
@media (aspect-ratio: 4/3) {
  body {
    background-color: green; /* quando a tela tiver uma proporção de 4:3, o background será verde */
  }
}
```
### Função var em CSS
Confusões à parte, a função var existe no CSS e serve para adicionar variáveis de estilos, para quando precisar deles, só colocar no código.</br>
Para setar uma variável, basta realizar o comando `:root` e colocar as variáveis embaixo. Exemplo:
```css
:root {
  --bg-vermelho: red; /* atenha-se à sintaxe, o : antes de root e o -- antes da variável são obrigatórios) */
  --fonte-dezesseis: 16pt;
}
```
Agora, toda vez que quiser que o background tenha a cor vermelha e a fonte seja tamanho 16pt, basta:
```css
.divQualquer {
  background-color: --bg-vermelho;
  font-size: --fonte-dezesseis;
}
```

## Tornar um vídeo em sua página responsivo
Tornar um vídeo (tag iframe) responsivo é uma tarefa difícil, mas existe uma forma utilizando uma técnica de aspect ratio para tornar um frame de vídeo responsivo.
### Entendendo a matemática por trás do código
O aspect ratio é a razão entre a largura e altura de um vídeo ou imagem. O aspect ratio mais comum é o 16:9.</br>
Exemplo:</br>
Uma tela com resolução de 1920x1080 tem um aspecto de 16:9 pois a largura é 16 vezes maior que a altura.<br/>
`(1920/1080 = 16/9)`

- Criando uma div para o container do vídeo (class video) e área do vídeo (class videoArea)
```html
<body>
  <div class="video">
    <div class="videoArea">
      <iframe width="560" height="315" src="assets/videoQualquer.mp4" />
    </div>
  </div>
</body>
```
```css
.video {
  width: 100%;
  max-width: 800px;
  margin: auto;
}

.videoArea {
  position: relative;
  height: 0px;
  background-color: green;
  padding: 0px 0px 56.25%; /* aspect ratio de 16:9 */
}

.videoArea iframe {
  position: absolute;
  top: 0px;
  bottom: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  border: 0px;
}
```

O segredo para manter a responsividade está em como utilizamos o padding no contêiner do vídeo. No caso do código acima, o `padding-top` de 56,25% é o que garante que o vídeo mantenha a proporção 16:9, independentemente do tamanho da tela.

Para chegarmos nesse valor `(56,25%)`, foi necessário entender como transformar esse aspect ratio em porcentagem. Entenda dessa forma:
$$
\frac{9}{16} \times 100 = 56.25\%
$$

## Função calc( )

Útil para layouts responsivos e cálculos dinâmicos de tamanhos.

```css
.elemento {
  width: calc(100%- 20px); /* subtrai 50px da largura total */
  margin: calc(10px - 2%); /* adiciona uma valor fixo com uma porcentagem */
}
```

## Tags de Semântica
- Header
- Footer
- Nav
- Section
- Article 
- Aside
- Time

## @keyframes em CSS
A regra @keyframes em CSS permite criar animações definindo as etapas (ou "frames") que o elemento passará ao longo do tempo. Cada etapa define o estado da animação em diferentes porcentagens de progresso, de 0% (início) a 100% (final). Exemplo:

```css
@keyframes exemplo {
  0% {
    background-color: red;
    top: 0px;
    left: 0px;
  }
  25% {
    background-color: yellow;
    top: 0px;
    left: 200px;
  }
  50% {
    background-color: blue;
    top: 200px;
    left: 200px;
  }
  75% {
    background-color: green;
    top: 200px;
    left: 0px;
  }
  100% {
    background-color: red;
    top: 0px;
    left: 0px;
  }
}
```
Aqui, o elemento mudará de cor e posição ao longo da animação. Para aplicar esta animação ao elemento, usamos propriedades de animação como **animation-name**, **animation-duration**, **animation-delay**, e **animation-iteration-count**:

```css
.exemplo {
  width: 150px;
  height: 150px;
  background-color: red;
  position: absolute;
  animation-name: exemplo;
  animation-duration: 4s;
  animation-delay: 1s;
  animation-iteration-count: infinite;
}
```
Neste exemplo, a animação ocorre a cada 4 segundos, com uma pausa de 1 segundo antes de começar, e se repete infinitamente.

## Transition em CSS

A propriedade **transition** em CSS é usada para criar efeitos de transição suave ao alterar uma ou mais propriedades de um elemento. Ela define a duração, o estilo de transição e a propriedade que será animada.

```css
.button {
  width: 100px;
  height: 40px;
  background-color: blue;
  transition: background-color 0.5s ease;
}

.button:hover {
  background-color: green;
}
```
Neste caso, ao passar o mouse sobre .button, a cor de fundo mudará suavemente de azul para verde em 0,5 segundos. A função ease cria uma transição com uma velocidade suave.

## Listas de descrição `<dl>`, `<dt>`,`<dd>`
Cada termo (definido em `<dt>`) tem uma descrição correspondente (definida em `<dd>`).

- `<dl>`: container de lista de descrição
- `<dt>`: título
- `<dd>`: descrição

```html
<dl>
  <dt>HTML</dt>
  <dd>Linguagem de marcação usada para criar páginas web.</dd>

  <dt>CSS</dt>
  <dd>Estiliza o layout das páginas web.</dd>

  <dt>JavaScript</dt>
  <dd>Linguagem de programação para adicionar interatividade.</dd>
</dl>
      <!-- usei chat gpt pra dar esses exemplos rsrsrs -->
```
## Flexbox
```css
.container {
  display: flex;
}
```
Os elementos são distribuídos em linha ou coluna, de acordo com o espaço disponível, ajustando-se automaticamente ao tamanho do container.

### Redistribuição flex:[valor]

- **Distribuição igual entre os itens:**

```css
.container {
  display: flex;
}
.item {
  flex: 1; /* tamanhos iguais para todos itens preenchendo tamanho disponível dentro do container */
}
```
- **Distribuição distinta entre os itens (flex-grow):**

```css
.container {
  display: flex;
}
.item1 {
  flex: 2; /* este item crescerá duas vezes mais do que os outros */
}
.item2 {
  flex: 1; /* este item crescerá uma vez, ou seja, menos que o item1 */
}
.item3 {
  flex: 1; /* este item terá o mesmo crescimento que o item2 */
}

```

### Order
Reordena o item (sim.)
```css
.item3 { /* supondo que existam 4 itens */
  order: 2 /* coloca o item 3 no lugar do item 2, reordenando a... ordem. */
} /* o que era [1][2][3][4], tornou-se [1][3][2][4]
```

```css
.container {
  display: flex;
}

.item1 {
  order: 0; /* Ordem inicial */
}

.item2 {
  order: -1; /* Vai aparecer primeiro */
}

.item3 {
  order: 1; /* Vai aparecer depois do item 1 */
}

.item4 {
  order: 2; /* Vai aparecer depois do item 3 */
}
```

### Propriedades do Flexbox (algumas)

- `flex-direction`: define a direção dos itens
  - `row` **(padrão)**: alinha horizontalmente
  - `column`: alinha verticalmente
- `justify-content`: alinha os itens ao longo do eixo principal
  - `flex-start` : início do container
  - `center`: centro do container
  - `space-between`: distribui os itens com espaço igual entre eles.
  - `space-around`: distribui os itens com espaço igual ao redor deles. </br></br>
 
<div style="border: 1px solid white; border-radius: 10px; width: fit-content; padding: 10px; text-align: center; margin-left: auto; margin-right: auto;">
  <p><b style="font-size: 20px">Para entender o próximo item:</b></p>
  <p><b>Eixo principal:</b> Direção do flex-direction.</p>
  <p><b>Eixo transversal:</b> Sentido perpendicular ao eixo principal.</p>
  <p>Sendo assim, se o <b>flex-direction</b> for <b>row</b> (horizontal/linha), <b>o align-items</b> valerá para o sentido vertical.<br/>
  <i>E vice-versa.</i>
</div>
</br></br>


- `align-items`:
  - `stretch` **(padrão)**: os itens ocupam todo o espaço disponível no eixo transversal.
  - `center`: centraliza os itens no eixo transversal.
  - `flex-start` e `flex-end`: alinha os itens no início ou no final do container.
- `flex-wrap`: wrap text, decide se os itens quebram a linha ou não se não couberem no container.
  - `nowrap` **(padrão)**: os itens ficam em uma única linha.
  - `wrap`: os itens quebram para a linha seguinte se o espaço não for suficiente.
- `align-self`: mesma coisa do align-items, mas para apenas um item. pode receber os mesmos valores do align-items.

# Curso de JavaScript

Iniciado o curso de JavaScript, estarei colocando minhas anotações neste repositório até que hajam estudos práticos para serem feitos.


## Diferença entre var, let e const

### `var`
- Escopo: Global ou da função onde foi declarada.
- Permite redeclaração e reatribuição.
- Comportamento peculiar: Pode ser utilizada antes de ser declarada devido ao "hoisting".
- Exemplo:
  ```javascript
  console.log(a); // undefined (hoisting)
  var a = 10;
  console.log(a); // 10
  ```

### `let`
- Escopo: Bloco ({...}), função ou global.
- Permite reatribuição, mas não redeclaração no mesmo escopo.
- Exemplo:
  ```javascript
  let b = 20;
  b = 30; // OK
  let b = 40; // Erro (não pode redeclarar no mesmo escopo)
  ```

### `const`
- Escopo: Bloco ({...}), função ou global.
- Não permite redeclaração nem reatribuição.
- Ideal para valores que não devem mudar.
- Exemplo:
  ```javascript
  const c = 50;
  c = 60; // Erro (não pode reatribuir)
  ```

---

## Quando usar e quando não usar

### `var`
- **Quando usar**: Evitar o uso de `var` no código moderno devido ao escopo global e comportamento imprevisível.
- **Quando não usar**: Sempre que possível, prefira `let` ou `const`.

### `let`
- **Quando usar**: Quando o valor precisa mudar ao longo do código.
- **Quando não usar**: Evite usar se o valor for constante e não precisa ser reatribuído.

### `const`
- **Quando usar**: Sempre que o valor não deva mudar, como configurações, constantes matemáticas ou identificadores.
- **Quando não usar**: Quando você sabe que o valor precisará ser atualizado.

---

### Resumo
- Use `const` por padrão para garantir imutabilidade.
- Use `let` apenas quando for necessário reatribuir valores.
- Evite `var` em código moderno.


## (Alguns) Tipos de Variáveis

### String:
- **Definição**: Utilizada para representar textos. Sempre envolvida por aspas simples (`'`), aspas duplas (`"`) ou crases (\`\`).

```javascript
let name = "Guilherme"; // String com aspas duplas
let city = 'Rio de Janeiro'; // String com aspas simples
let message = `Olá, ${name}! Bem-vindo ao ${city}.`; // Template string com crases
```
### Number:
- **Definição**: Representa números inteiros (int em python) e decimais (float em python).

```javascript
let age = 25; // Número inteiro
let price = 19.99; // Número Decimal
```

### Boolean
- **Definição**: Representa valores lógicos, podendo ser `true` ou `false`.
```javascript
let isLoggedIn = true; // Usuário logado
let hasPermission = false; // Usuário não tem permissão
```
### Object
- **Definição**: Utilizado para armazenar coleções de dados ou entidades mais complexas.
```javascript
let person = {
  name: "Guilherme",
  age: 21,
  isStudent: true
};
```

### Array
- **Definição**: É uma lista ordenada de valores.
```javascript
let colors = ["red", "blue", "green"];
```

## Estrutura Condicional If / Else

**Exemplo** de uma estrutura simples if/else:

```javascript

let idade = 21; // Variável para ser consultada;

if (idade > 17) { // Condição determinada
  console.log('Maior de idade.'); // Evento condicional
} else {
  console.log('Menor de idade.'); // Evento caso a condição não seja satisfeita
}
```

## Condicional dupla If / Else

```javascript
let idade = 21;
if (idade < 12) {
  console.log('Criança');
} else if (idade > 12 && idade <= 17) {
  console.log('Adolescente');
} else if (idade >= 18) {
  console.log('Maior de Idade');
}
```

## Diferença entre == e ===

### `==` (Igualdade abstrata)
- Compara dois valores, realizando **conversão de tipo** quando necessário.
- Exemplo:
  ```javascript
  console.log(5 == '5'); // true (os valores são iguais, apesar de tipos diferentes)
  ```

### `===` (Igualdade estrita)
- Compara dois valores **sem conversão de tipo**, exigindo que sejam do mesmo tipo e valor.
- Exemplo:
  ```javascript
  console.log(5 === '5'); // false (número não é igual a string)
  ```

### Resumo
Use `===` sempre que possível para evitar resultados inesperados devido à conversão automática de tipos.

---

## Multicondicionais: `&&` e `||`

### `&&` (E lógico)
- Retorna `true` apenas se **todas as condições forem verdadeiras**.
- Exemplo:
  ```javascript
  let idade = 25;
  let temCarteira = true;

  if (idade >= 18 && temCarteira) {
    console.log('Pode dirigir.'); // Será executado porque ambas as condições são verdadeiras
  }
  ```

### `||` (OU lógico)
- Retorna `true` se **ao menos uma condição for verdadeira**.
- Exemplo:
  ```javascript
  let temCNH = false;
  let temPermissaoEspecial = true;

  if (temCNH || temPermissaoEspecial) {
    console.log('Pode dirigir.'); // Será executado porque uma das condições é verdadeira
  }
  ```

### Resumo
- Use `&&` para exigir que **todas as condições** sejam verdadeiras.
- Use `||` para permitir que **qualquer uma das condições** seja verdadeira.


## Switch Case
- **Descrição**: Utilizado para executar diferentes blocos de código com base no valor de uma variável.
- Exemplo:
  ```javascript
  let cor = 'vermelho';

  switch (cor) {
    case 'azul':
      console.log('A cor é azul.');
      break;
    case 'vermelho':
      console.log('A cor é vermelha.');
      break;
    default:
      console.log('Cor desconhecida.');
  }
  ```

## Funções
- **Descrição**: Blocos de código reutilizáveis que podem ser chamados para realizar tarefas.
- Exemplo:
  ```javascript
  function soma(a, b) {
    return a + b;
  }
  console.log(soma(5, 10)); // 15
  ```

## Arrow Function
- **Descrição**: Uma forma mais concisa de escrever funções.
- Exemplo:
  ```javascript
  const soma = (a, b) => a + b;
  console.log(soma(5, 10)); // 15
  ```
- **Nota**: Arrow functions não possuem seu próprio `this`.


## Loop For
- **Descrição**: Usado para iterar sobre uma sequência com um número conhecido de repetições.
- Exemplo:
  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i); // 0, 1, 2, 3, 4
  }
  ```

## Loop While
- **Descrição**: Usado para iterar enquanto uma condição for verdadeira.
- Exemplo:
  ```javascript
  let i = 0;
  while (i < 5) {
    console.log(i); // 0, 1, 2, 3, 4
    i++;
  }
  ```

## Funções em Array

### `push()`
- **Descrição**: Adiciona um ou mais elementos ao final do array.
- Exemplo:
  ```javascript
  let frutas = ['maçã', 'banana'];
  frutas.push('laranja');
  console.log(frutas); // ['maçã', 'banana', 'laranja']
  ```

### `pop()`
- **Descrição**: Remove o último elemento do array e o retorna.
- Exemplo:
  ```javascript
  let frutas = ['maçã', 'banana', 'laranja'];
  let ultimaFruta = frutas.pop();
  console.log(ultimaFruta); // 'laranja'
  console.log(frutas); // ['maçã', 'banana']
  ```

### `shift()`
- **Descrição**: Remove o primeiro elemento do array e o retorna.
- Exemplo:
  ```javascript
  let frutas = ['maçã', 'banana'];
  let primeiraFruta = frutas.shift();
  console.log(primeiraFruta); // 'maçã'
  console.log(frutas); // ['banana']
  ```

### `unshift()`
- **Descrição**: Adiciona um ou mais elementos ao início do array.
- Exemplo:
  ```javascript
  let frutas = ['banana'];
  frutas.unshift('maçã');
  console.log(frutas); // ['maçã', 'banana']
  ```

### `map()`
- **Descrição**: Cria um novo array com os resultados da aplicação de uma função em cada elemento.
- Exemplo:
  ```javascript
  let numeros = [1, 2, 3];
  let dobrados = numeros.map(x => x * 2);
  console.log(dobrados); // [2, 4, 6]
  ```

### `filter()`
- **Descrição**: Cria um novo array com todos os elementos que passam no teste de uma função.
- Exemplo:
  ```javascript
  let numeros = [1, 2, 3, 4];
  let pares = numeros.filter(x => x % 2 === 0);
  console.log(pares); // [2, 4]
  ```

### `reduce()`
- **Descrição**: Reduz o array a um único valor, aplicando uma função acumuladora.
- Exemplo:
  ```javascript
  let numeros = [1, 2, 3, 4];
  let soma = numeros.reduce((acumulador, valorAtual) => acumulador + valorAtual, 0);
  console.log(soma); // 10
  ```

### `forEach()`
- **Descrição**: Executa uma função para cada elemento do array (não retorna um novo array).
- Exemplo:
  ```javascript
  let numeros = [1, 2, 3];
  numeros.forEach(x => console.log(x)); // 1, 2, 3
  ```

### `find()`
- **Descrição**: Retorna o primeiro elemento que satisfaz a condição de uma função.
- Exemplo:
  ```javascript
  let numeros = [1, 2, 3, 4];
  let encontrado = numeros.find(x => x > 2);
  console.log(encontrado); // 3
  ```

### `join()`
- **Descrição**: Concatena todos os elementos de um array em uma única string, separados por um delimitador especificado (por padrão, uma vírgula).
- Exemplo:
  ```javascript
  let frutas = ['maçã', 'banana', 'laranja'];
  let listaFrutas = frutas.join(', ');
  console.log(listaFrutas); // 'maçã, banana, laranja'
  ```
  
### `sort()`
- **Descrição**: Ordena os elementos de um array in place (ou seja, modifica o array original). Por padrão, ordena os elementos como strings em ordem alfabética.
- Exemplo com **strings**:
  ```javascript
  let frutas = ['laranja', 'banana', 'maçã'];
  frutas.sort();
  console.log(frutas); // ['banana', 'laranja', 'maçã']
  ```
- Exemplo com **números** (não funciona):
  ```javascript
  let numeros = [10, 5, 20, 2];
  numeros.sort(); 
  console.log(numeros); // [10, 2, 20, 5] (ordem alfabética de strings, não numérica)
  ```
- Exemplo de ordenação funcional com **números**:

  ```javascript
  numeros.sort((a, b) => a - b); // Ordem crescente
  console.log(numeros); // [2, 5, 10, 20]
  ```
   ```javascript
  numeros.sort((a, b) => b - a); // Ordem descrescente
  console.log(numeros); // [20, 10, 5, 2]
  ```
- Exemplo de `sort()` com listas/objetos:
  ```javascript
  let cars = [
    { brand: "Fiat", year: 2022 },
    { brand: "BMW", year: 2018 },
    { brand: "Ferrari", year: 2020 }
  ];

  // Crescente
  cars.sort((a, b) => a.year - b.year);
  console.log()

   // Decrescente
  cars.sort((a, b) => b.year - a.year);
  console.log()

## POO em JavaScript

A Programação Orientada a Objetos (POO) em JavaScript permite estruturar e organizar o código de forma mais modular e reutilizável. 
Com o uso de classes, herança e métodos, é possível representar entidades do mundo real em objetos no código.

### Classes e seus métodos
- **Constructor e This**: O método `constructor` é usado para inicializar um objeto com propriedades específicas. 
  O `this` refere-se ao contexto atual da instância da classe. <br><br>**Importante:** Em JavaScript (e em muitas outras linguagens orientadas a objetos), é uma convenção nomear classes começando com letra maiúscula (PascalCase). Essa prática ajuda a diferenciar classes de outras estruturas, como funções e variáveis


```javascript
  // Definindo a classe Person
  class Person {
    // O método constructor é chamado automaticamente ao criar uma nova instância da classe
    constructor(name, age) {
      // 'this.name' e 'this.age' criam propriedades na instância do objeto
      // 'name' e 'age' são parâmetros recebidos ao criar a instância
      this.name = name; // Define o nome da pessoa
      this.age = age;   // Define a idade da pessoa
    }
  }
  
  // Criando instâncias da classe Person
  // A criação de um objeto a partir de uma classe é chamada de instância. Isso é feito utilizando a palavra-chave: 'new'.
  let p1 = new Person("Guilherme", 21);
  let p2 = new Person("Hellen", 20);   
  let p3 = new Person("Genivaldo", 50);

  console.log(`P1 = ${p1.name} tem ${p1.age} anos`); // script.js:17 P1 = Guilherme tem 21 anos
  console.log(`P2 = ${p2.name} tem ${p2.age} anos`); // script.js:18 P2 = Hellen tem 20 anos
  console.log(`P3 = ${p3.name} tem ${p3.age} anos`); // script.js:19 P3 = Genivaldo tem 50 anos
  ```
  
- **Ação (Métodos)**: Métodos são funções definidas dentro de uma classe para realizar ações específicas nos objetos.

```javascript
  class Person {
  age = 0;  // Inicializando a propriedade 'age' com valor padrão 0
  steps = 0; // Inicializando a propriedade 'steps' com valor padrão 0

  constructor(name) {
    this.name = name;
  }

  stepForward() { // Função para adicionar passos à instância
    this.steps++;
  }

  setAge(newAge) { // Função para adicionar idade à instância
    if (typeof newAge == "number") {
      this.age = newAge;
    } else {
      console.log("Idade não é um número.");
    }
  }
}

let p1 = new Person("Guilherme", 21);
let p2 = new Person("Hellen", 20);
let p3 = new Person("Genivaldo", 50);

p1.setAge(20); // Configurando a idade da instância 'p1' usando o método 'setAge'
p1.stepForward(); // Incrementando os passos da instância 'p1' usando o método 'stepForward'
console.log(`${p1.name} tem ${p1.age} anos e deu ${p1.steps} passo(s).`); // Saída: "Guilherme tem 20 anos e deu 1 passo(s)."
```
  
- **Getter e Setter**: Getters permitem acessar propriedades privadas ou protegidas, enquanto setters permitem alterá-las de forma controlada.
```javascript
var _v = 0;  // Variável privada para armazenar o valor de 'v'

// Definindo o objeto 'obj' com um getter e setter para a propriedade 'v'
var obj = {
  // Getter: método para acessar o valor de 'v' de forma personalizada
  get v() {
    // Retorna o valor de '_v' formatado como uma string
    return "Value: " + _v;  
  },

  // Setter: método para definir o valor de 'v' de forma personalizada
  set v(value) {
    // Modifica o valor de '_v', multiplicando o valor atribuído por 2
    _v = value * 2;
  },
};

// Acessando a propriedade 'v' usando o getter (não é necessário parênteses)
console.log(obj.v);  // Saída: "Value: 0" - O getter é chamado, retornando "Value: " concatenado com o valor de '_v' (0)

// Atribuindo um valor à propriedade 'v', o setter é chamado
obj.v = 5;  // O setter é chamado, o valor de 5 é multiplicado por 2 e atribuído a '_v' (resultando em 10)

// Acessando novamente a propriedade 'v' com o getter após a modificação
console.log(obj.v);  // Saída: "Value: 10" - O getter retorna "Value: " concatenado com o novo valor de '_v' (10)

```
- **Herança**: Classes podem herdar propriedades e métodos de outras classes usando a palavra-chave `extends`. Isso promove reuso de código.
```javascript
  class Person {
  age = 0; // Propriedade 'age' inicializada com o valor padrão 0

  constructor(name) {
    this.name = name; // Define o nome da pessoa ao criar a instância
  }

  greet() {
    console.log(`${this.name} diz Olá!`); // Método para exibir uma saudação personalizada
  }
}

class Student extends Person {
  constructor(name, id) {
    // O método 'super' é usado para chamar o construtor da classe pai (Person)
    // Isso permite inicializar a propriedade 'name' definida na classe pai
    super(name);
    this.id = id; // Adiciona a propriedade 'id', exclusiva da classe Student
  }
}

// Criando uma instância da classe Student, que herda de Person
let p1 = new Student("Guilherme", 1); // A instância inclui 'name' da classe pai e 'id' da classe atual
p1.age = 21; // A propriedade 'age' é acessível porque foi herdada da classe pai (Person)

// Chamando o método 'greet', herdado da classe pai
p1.greet(); // Saída: "Guilherme diz Olá!"

// Exibindo as informações da instância 'p1', incluindo propriedades herdadas e definidas na classe Student
console.log(`${p1.name} tem ${p1.age} anos e matrícula #${p1.id}`);
// Saída: "Guilherme tem 21 anos e matrícula #1"
```
- **Variável/Método Estático**: Métodos ou variáveis estáticas pertencem à classe em si, e não às instâncias, sendo acessíveis diretamente pela classe.
```javascript
class Person {
  static hands = 2; // Propriedade estática: pertence à classe Person, não às instâncias.
  age = 0; // Propriedade de instância: pertence a cada objeto criado.

  constructor(name) {
    this.name = name; // Define o nome da pessoa ao criar a instância.
  }

  say() {
    // Acessa a propriedade estática 'hands' diretamente pela classe Person.
    console.log(`Oi, eu sou ${this.name} e tenho ${Person.hands} mãos.`);
  }
}

let p1 = new Person("Guilherme"); // Cria uma instância de Person com o nome "Guilherme".
p1.hands = 1000; // Esta linha **não altera** a propriedade estática 'hands'.
// Em vez disso, cria uma nova propriedade 'hands' **na instância 'p1'**, mas ela não afeta a propriedade estática da classe.

p1.say(); // Saída: "Oi, eu sou Guilherme e tenho 2 mãos."
```
- **Factory**: Um padrão de projeto que utiliza funções para criar e retornar objetos sem a necessidade de instanciar explicitamente uma classe.
```javascript
class Person {
  age = 0; // Inicializa a propriedade 'age' com o valor padrão 0.

  constructor(name) {
    this.name = name; // Define o nome da pessoa no momento da criação da instância.
  }
}

function createPerson(name, age) {
  // Função fábrica que cria uma instância da classe Person.
  let p = new Person(name); // Cria uma nova instância de Person com o nome fornecido.
  p.age = age; // Define a idade da pessoa criada.
  return p; // Retorna a instância criada.
}

let p1 = createPerson("Guilherme", 21); // Cria uma nova pessoa chamada 'Guilherme' com 21 anos.

console.log(`${p1.name} tem ${p1.age} anos.`); // Saída: "Guilherme tem 21 anos."
```
## Introdução a Requisições

### Requisições
Requisições são solicitações enviadas de um cliente para um servidor, geralmente com o objetivo de obter ou enviar dados. No contexto do desenvolvimento web, isso pode envolver a comunicação entre navegadores, servidores e APIs.

### Síncrono e Assíncrono
- **Síncrono**: A execução do código espera que a operação atual termine antes de passar para a próxima. Isso pode levar a travamentos em processos longos.
- **Assíncrono**: O código pode continuar sendo executado enquanto espera pela conclusão de uma operação, melhorando o desempenho e a experiência do usuário.

### O que é uma API?
API (Application Programming Interface) é uma interface que permite a comunicação entre diferentes sistemas. No desenvolvimento web, APIs são usadas para acessar funcionalidades ou dados externos.

## Callbacks
Callbacks são funções passadas como argumento para outras funções, permitindo a execução de código após a conclusão de uma operação. Isso é comum em operações assíncronas, como requisições a servidores.

```javascript
// Exemplo de Callback
function fetchData(callback) {
  setTimeout(() => {
    console.log("Dados recebidos");
    callback();
  }, 1000);
}

fetchData(() => {
  console.log("Processando os dados recebidos");
});
```

## Requisições HTTP através da função `fetch`
A função fetch é uma API nativa do JavaScript usada para realizar requisições HTTP de forma assíncrona. Ela permite que você envie e receba dados de servidores de maneira eficiente e simplificada.

```javascript
function fetchExample() {
  fetch('https://jsonplaceholder.typicode.com/posts') // Envia uma requisição e retorna uma promise
    
  .then((data) => { // Espera a promise e executa
      console.log(data) // Saída: Response
  })
}
```

### `.catch` e `.finally`
- `.catch`: Identifica erros.
- `.finally`: Indica o final da requisição (ou realiza alguma outra tarefa final).
```javascript
function clicou() {
  fetch('https://jsonplaceholder.typicode.com/err0r') // Url errada
    .then((response) => {
      return response.json();
    })
    .then((json) => {
      console.log(json[0].title);
    })
    .catch((error) => {
      console.log('Erro:', error); // Identifica o erro
    })
    .finally(() => {
      console.log('Final da requisição') // Executa no final da requisição
    })
}

document.querySelector('#botao').addEventListener('click', clicou);
```


## Nota Importante sobre Variáveis com elementos HTML
É importante ressaltar que quando uma variável interage com algum elemento HTML dentro do projeto, deve-se utilizar um cifrão `$` para chamar essa variável. Exemplo:
```javascript
// Neste caso, quero selecionar um elemento de botão dentro do meu arquivo HTML.

const $botao = document.querySelector('.botao');
```

## Métodos de requisição HTTP: GET, POST, PUT e DELETE

Os métodos HTTP são utilizados para comunicação entre o cliente (navegador ou aplicação) e o servidor. Aqui estão os quatro métodos mais comuns:

- **GET**: Usado para recuperar informações do servidor. Este método solicita dados e não realiza alterações no lado do servidor.
  - Exemplo: Buscar lista de usuários de um banco de dados.

- **POST**: Usado para enviar dados ao servidor, geralmente para criar novos recursos. Este método frequentemente inclui informações no corpo da requisição.
  - Exemplo: Registrar um novo usuário.

- **PUT**: Usado para atualizar ou substituir um recurso existente no servidor. Requer a identificação do recurso a ser modificado.
  - Exemplo: Atualizar o e-mail de um usuário.

- **DELETE**: Usado para remover um recurso específico do servidor.
  - Exemplo: Deletar um usuário de uma lista.

Esses métodos, quando utilizados em conjunto com APIs REST, formam a base para a construção de sistemas web modernos.

"""
## Métodos de Strings

### Manipulação e Análise de Strings
- **charAt(index)**: Retorna o caractere no índice especificado.
- **concat(str1, str2, ...)**: Junta duas ou mais strings.
- **includes(substring)**: Verifica se a string contém a substring especificada.
- **indexOf(substring)**: Retorna o índice da primeira ocorrência da substring.
- **lastIndexOf(substring)**: Retorna o índice da última ocorrência da substring.
- **slice(start, end)**: Extrai parte de uma string entre os índices especificados.
- **substring(start, end)**: Similar ao slice, mas não aceita índices negativos.
- **toLowerCase()**: Converte a string para letras minúsculas.
- **toUpperCase()**: Converte a string para letras maiúsculas.
- **trim()**: Remove espaços em branco do início e fim da string.
- **replace(searchValue, newValue)**: Substitui parte da string por outra.
- **split(separator)**: Divide a string em um array com base no separador.

## Métodos de Arrays

### Manipulação e Iteração
- **push(element)**: Adiciona um ou mais elementos ao final do array.
- **pop()**: Remove o último elemento do array.
- **shift()**: Remove o primeiro elemento do array.
- **unshift(element)**: Adiciona um ou mais elementos ao início do array.
- **splice(start, deleteCount, items)**: Adiciona ou remove elementos em qualquer posição.
- **slice(start, end)**: Retorna uma cópia superficial de uma parte do array.
- **indexOf(element)**: Retorna o índice da primeira ocorrência do elemento.
- **lastIndexOf(element)**: Retorna o índice da última ocorrência do elemento.
- **includes(element)**: Verifica se o array contém o elemento especificado.

### Iteração e Transformação
- **forEach(callback)**: Executa uma função para cada elemento.
- **map(callback)**: Cria um novo array com os resultados de aplicar uma função a cada elemento.
- **filter(callback)**: Retorna um novo array contendo apenas os elementos que passam em uma condição.
- **reduce(callback, initialValue)**: Reduz o array a um único valor.
- **find(callback)**: Retorna o primeiro elemento que satisfaz a condição.
- **findIndex(callback)**: Retorna o índice do primeiro elemento que satisfaz a condição.

### Outras Operações
- **join(separator)**: Junta todos os elementos do array em uma string.
- **reverse()**: Inverte a ordem dos elementos do array.
- **sort(compareFunction)**: Ordena os elementos do array.
- **every(callback)**: Verifica se todos os elementos passam na condição.
- **some(callback)**: Verifica se ao menos um elemento passa na condição.

## Datas

JavaScript utiliza o objeto **`Date`** para manipulação de datas e horas. Abaixo estão os métodos mais importantes para trabalhar com datas, acompanhados de exemplos.

### Criando um Objeto Date
```javascript
// Data atual
const now = new Date();
console.log(now);

// Data específica (Ano, Mês [0-11], Dia, Hora, Minuto, Segundo, Milissegundo)
const specificDate = new Date(2025, 0, 9, 15, 30, 0); // 9 de Janeiro de 2025, 15:30
console.log(specificDate);

// Criando uma data a partir de uma string (padrão ISO 8601 ou outros formatos)
const fromString = new Date("2025-01-09T15:30:00");
console.log(fromString);

```

### Métodos para Obter Informações de uma Data
```javascript
const date = new Date();

// Obtendo partes da data
console.log(date.getFullYear()); // Ano (ex: 2025)
console.log(date.getMonth()); // Mês (0-11, onde 0 é Janeiro)
console.log(date.getDate()); // Dia do mês (1-31)
console.log(date.getDay()); // Dia da semana (0-6, onde 0 é Domingo)
console.log(date.getHours()); // Hora (0-23)
console.log(date.getMinutes()); // Minutos (0-59)
console.log(date.getSeconds()); // Segundos (0-59)
console.log(date.getMilliseconds()); // Milissegundos (0-999)
console.log(date.getTime()); // Timestamp (milissegundos desde 1 Jan 1970)

```

### Métodos para Definir Informações de uma Data
```javascript
const date = new Date();

// Alterando partes da data
date.setFullYear(2026);
date.setMonth(11); // Dezembro
date.setDate(25); // Dia 25
date.setHours(10, 30, 0); // Hora, Minuto, Segundo

console.log(date); // 25 de Dezembro de 2026, 10:30:00
```

### Formatando Datas
```javascript
const date = new Date();

// Convertendo para string legível
console.log(date.toString()); // Formato completo
console.log(date.toDateString()); // Apenas data
console.log(date.toTimeString()); // Apenas hora
console.log(date.toISOString()); // Formato ISO 8601
console.log(date.toLocaleDateString("pt-BR")); // Data no formato local
console.log(date.toLocaleTimeString("pt-BR")); // Hora no formato local
```

### Operações com Datas
```javascript
const start = new Date("2025-01-01");
const end = new Date("2025-01-09");

// Diferença em milissegundos
const diffMs = end - start;
console.log(diffMs);

// Convertendo para dias
const diffDays = diffMs / (1000 * 60 * 60 * 24);
console.log(diffDays);
```

## Objeto Math em JavaScript

O objeto Math em JavaScript oferece uma variedade de métodos e propriedades úteis para cálculos matemáticos. Ele é amplamente utilizado para operações como arredondamento, geração de números aleatórios, trigonometria e muito mais.

## Métodos mais utilizados

### Arredondamento
```javascript
console.log(Math.round(4.7)); // Arredonda para o inteiro mais próximo (5)
console.log(Math.ceil(4.3)); // Arredonda para cima (5)
console.log(Math.floor(4.7)); // Arredonda para baixo (4)
console.log(Math.trunc(4.7)); // Remove a parte decimal (4)
```

### Números Aleatórios
```javascript
console.log(Math.random()); // Retorna um número entre 0 (inclusivo) e 1 (exclusivo)
console.log(Math.random() * 10); // Número entre 0 e 10
console.log(Math.floor(Math.random() * 100)); // Inteiro entre 0 e 99
```

### Máximo e Mínimo
```javascript
console.log(Math.max(10, 20, 30)); // Retorna o maior número (30)
console.log(Math.min(10, 20, 30)); // Retorna o menor número (10)

```

### Potência e Raiz
```javascript
console.log(Math.pow(2, 3)); // Potência (2³ = 8)
console.log(Math.sqrt(16)); // Raiz quadrada (4)
console.log(Math.cbrt(27)); // Raiz cúbica (3)
```

### Valores Absolutos
```javascript
console.log(Math.abs(-10)); // Retorna o valor absoluto (10)
```

### Funções Trigonométricas
```javascript
console.log(Math.sin(Math.PI / 2)); // Seno de 90 graus (1)
console.log(Math.cos(Math.PI)); // Cosseno de 180 graus (-1)
console.log(Math.tan(Math.PI / 4)); // Tangente de 45 graus (1)
```


### Logaritmos
```javascript
console.log(Math.log(1)); // Logaritmo natural de 1 (0)
console.log(Math.log10(100)); // Logaritmo de base 10 de 100 (2)
console.log(Math.log2(8)); // Logaritmo de base 2 de 8 (3)
```


## Constantes Importantes
```javascript
console.log(Math.PI); // Valor de PI (3.141592653589793)
console.log(Math.E); // Base do logaritmo natural (2.718281828459045)
console.log(Math.LN2); // Logaritmo natural de 2 (0.693)
console.log(Math.SQRT2); // Raiz quadrada de 2 (1.414)
```

# Curso de TypeScript

## Types Primitivos em TypeScript

### 1. number
Representa números, incluindo inteiros e decimais. Não distingue entre inteiros e números de ponto flutuante.
```typescript
let idade: number = 25;
let temperatura: number = -10.5;
```

### 2. string
Representa texto. Strings podem ser delimitadas por aspas simples ('), aspas duplas (") ou crases (`) para templates.

```typescript
let nome: string = "Alice";
let mensagem: string = `Olá, ${nome}!`;
```

### 3. boolean
Representa valores lógicos: true ou false.

```typescript
let ativo: boolean = true;
let finalizado: boolean = false;
```

### 4. null
Representa um valor nulo.

```typescript
let valor: null = null;
```

### 5. undefined
Representa uma variável que ainda não foi atribuída.

```typescript
let indefinido: undefined = undefined;
```

### 6. bigint
Representa números inteiros muito grandes. É indicado pelo sufixo n.

```typescript
let grandeNumero: bigint = 123456789123456789123456789n;
```

### 7. symbol
Representa um identificador único.

```typescript
let simbolo: symbol = Symbol("id");
```

### Diferença entre null e undefined:
- null é um valor explicitamente vazio.
- undefined indica que algo ainda não foi definido.


### Uso em Tipagem Opcional
TypeScript permite combinar tipos primitivos usando **union types:**
```typescript
let resultado: string | number;
resultado = "Sucesso"; // válido
resultado = 200; // válido
```

Esses tipos ajudam a evitar erros comuns e fornecem maior segurança durante o desenvolvimento.

### Type em Arrays
No TypeScript, arrays podem armazenar múltiplos valores do mesmo tipo. Você pode especificar o tipo dos elementos dentro de um array de várias formas. Aqui estão alguns dos métodos mais comuns de definir tipos para arrays:

```typescript
let numeros: number[] = [1, 2, 3, 4, 5];
```
**Tipo genérico:**
```typescript
let numeros: Array<number> = [1, 2, 3, 4, 5];
```

### Types em parâmetros de função
```typescript
function saudacao(nome: string) {
    return `Olá, ${nome}!`;
}

let mensagem = saudacao("Hellen");

```
### Types no retorno de função
```typescript
function saudacao(nome: string): string {
    return `Olá, ${nome}!`;
}

let mensagem = saudacao("Hellen"); 
```
### Propriedades Opcionais em TypeScript
```typescript
interface Usuario {
    nome: string;
    idade?: number; // Propriedade opcional '?'
}

const usuario1: Usuario = { nome: "Hellen" };
const usuario2: Usuario = { nome: "Guilherme", idade: 21 };

console.log(usuario1); // { nome: "Hellen" }
console.log(usuario2); // { nome: "Guilherme", idade: 21 }
```
## Definir Types e Interfaces

Em TypeScript, tanto `types` quanto `interfaces` são usados para definir a estrutura de *dados*, como **objetos**, **funções** ou **tipos** de variáveis. Ambos ajudam a garantir que os dados sejam estruturados corretamente e que seu uso seja seguro em tempo de compilação. Embora ambos desempenhem funções semelhantes, existem diferenças importantes entre eles.

- `type`
O type é uma maneira de criar um alias para um tipo ou uma combinação de tipos. Você pode usar **type** para definir tipos simples ou tipos compostos, como uniões, interseções e tipos literais.

Exemplo de uso básico de type:

```typescript
type Usuario = {
    nome: string;
    idade: number;
}

const usuario: Usuario = { nome: "Maria", idade: 25 };

```

`interface`
A interface é usada principalmente para definir a estrutura de objetos e pode ser extendida ou implementada por outras interfaces ou classes. Ela é mais adequada para descrever objetos e suas propriedades.

Exemplo de uso básico de interface:
```typescript
interface Usuario {
    nome: string;
    idade: number;
}

const usuario: Usuario = { nome: "João", idade: 28 };

```
### Diferenças entre type e interface

1. **Extensão:**
   - `Interface` pode ser **extendida**, ou seja, você pode criar novas interfaces baseadas em outras existentes usando `extends`.
   - `Type` não pode ser estendido diretamente, mas **pode ser combinado usando interseção de tipos (&).**

2. **Declaração Múltipla:**
   - `Interface` permite **múltiplas declarações** com o mesmo nome. Elas são mescladas automaticamente, permitindo a modificação ou adição de propriedades.
   - `Type` não permite declarações múltiplas com o mesmo nome. Se você tentar, obterá um erro.

3. **Usabilidade:**
   - `Interface` é mais usada para **definir objetos e pode ser implementada por classes.**
   - `Type` é mais flexível e pode ser usado para **tipos primitivos, literais, funções,** e até mesmo **uniões e interseções**.

**Quando Usar:**

- Use 'interface' quando estiver lidando com objetos que precisam ser extensíveis ou quando quiser garantir uma estrutura que pode ser implementada por classes.
- Use 'type' quando precisar de tipos mais complexos, como uniões, interseções ou tipos literais.

### Declarando Types em Funções

```typescript
type MathFunction = (n1: number, n2: number) => number;

const somar: MathFunction = (n1, n2) => {
  return n1 + n2;
}

// Deve ser declarado ao lado do nome da função

```


