# NotesPT.md

**Disclaimer:** This document contains notes I have taken throughout my Fullstack development course. There is also a separate file available in English in the repository. You can access it here: [NotesUS.md](https://github.com/Nixwzy/learningFS/blob/main/notesUS.md).

Este arquivo contém anotações que fiz ao longo do meu curso de desenvolvimento Fullstack. Nele, estão documentados conceitos e exemplos práticos relacionados a tecnologias como PHP, Laravel, NodeJS e React. É um repositório pessoal de aprendizado, onde registro informações importantes que adquiri durante as aulas.


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
O only print basicamente faz com que o estilo dentro desse media query seja modificado apenas quando a página for impressa.

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

# @media aspect-ratio
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

