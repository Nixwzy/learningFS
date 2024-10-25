# NotesPT.md

**Disclaimer:** This document contains notes I have taken throughout my Fullstack development course. There is also a separate file available in English in the repository. You can access it here: [NotesUS.md](https://github.com/Nixwzy/learningFS/blob/main/notesEN.md).

Este arquivo contém anotações que fiz ao longo do meu curso de desenvolvimento Fullstack. Nele, estão documentados conceitos e exemplos práticos relacionados a tecnologias como PHP, Laravel, NodeJS e React. É um repositório pessoal de aprendizado, onde registro informações importantes que adquiri durante as aulas.



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
## Atributos de Formulário

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