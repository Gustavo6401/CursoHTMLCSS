# Tabelas no HTML

As tabelas são uma das ferramentas mais essenciais para a organização dos dados, principalmente em contextos como arquivos de texto ou arquivos PDF. Utilizo essa ferramenta com muita frequência para melhor organização dos meus estudos. E quem disso que dentro de uma página Web isso deve ser diferente? 

Pense nas páginas HTML como um grande documento escrito feito para fazermos uma análise de dados. Existem diversos contextos aos quais nós poderiamos utilizar as tabelas, um exemplo? Preços, notas escolares e vários outros tipos de páginas que exigem a exibição de dados estruturados. 

## A Tag `<table>`

A tag `<table>` é responsável pela criação de tabelas no HTML. Dentro da nossa tabela, podemos elaborar uma forma de estruturar melhor os nossos dados. Dentro dela, podemos incluir diversas tags, como `<tr>` (table row) e `<td>`, de forma a estruturar e organizar melhor os nossos dados. Utilizaremos no nosso exemplo, uma tabela para mostrarmos ao nosso usuário, as linguagens de programação e marcação que já entendemos:

``` html
<table>
    <tr>
        <td>Linguagem</td>
        <td>Meu Nível</td>
    </tr>
    <tr>
        <td>C#</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>HTML</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>CSS</td>
        <td>Básico</td>
    </tr>
</table>
```

Para que os dados fiquem um pouco mais visíveis, vamos criar uma tag chamada `<style>`, OK? Isso daqui já está entrando nas tarefas de CSS, pois o elemento `table` por padrão não possui uma borda, por isso, vamos criá-la com CSS, OK?

``` html
<style>
    table, th, tr, td, caption {
        border: 1px solid #eee;
        font-family: 'Courier New', Courier, monospace;
        border-collapse: collapse;
        padding: 0.5rem;
    }
</style>
```

Mais para frente, iremos entender melhor o que foi feito acima, especialmente sobre regras CSS! 

## Títulos de Tabelas

Um título para uma tabela pode ser criado por meio da tag `<caption>`, no caso dessa tabela, o título pode ser "Minhas Linguagens de Programação". A forma de montar isso? Muito simples! O elemento `<caption>` não se importa com a quantidade de colunas na sua tabela, ele serve apenas como uma coluna unificada na sua tabela para a exibição dos seus dados. 

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <tr>
        <td>Linguagem</td>
        <td>Meu Nível</td>
    </tr>
    <tr>
        <td>C#</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>HTML</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>CSS</td>
        <td>Básico</td>
    </tr>
</table>
```

Está bem interessante né? Bom, eu diria que essa tabela não está ainda tão interessante para deficientes visuais ou alguns outros usuários que necessitam de alguma assistência, por conta disso, existe a semântica de tabelas. 

## Semântica de Tabelas

A partir daqui, vamos aprender sobre outros elementos do HTML, tais como `<thead>`, `<tbody>` e `<tfoot>` e `<th>`. O objetivo é fazer com que o navegador entenda um pouco mais sobre o que nós escrevemos, o que é a descrição e o que são os dados a serem exibidos para o nosso usuário final. O objetivo das tags semânticas é de exatamente informar ao navegador cada uma dessas informações, afim de tornar a exibição mais voltada para certos usuários. 

### Implementando cabeçalhos nas tabelas: `<thead>` e `<th>`

A tag `<thead>` é uma tag voltada para o cabeçalho da tabela. Sabemos que os dados da nossa tabela são o nome das linguagens de programação, correto? Exatamente! No caso, C#, HTML e CSS. Sabendo disso, concluímos que a palavra "Linguagem" e o "Nível" não são necessariamente o nome dos nossos dados. Um exemplo disso, seria se criarmos uma tabela no Microsoft Word ou até mesmo uma planilha de Excel. 

![Print Excel](<imgs/12.1 - Print Excel.png>)

Como você pode ver, a parte preta da nossa tabela também possui sua própria cor, é o que chamamos então de cabeçalho da tabela. O objetivo é ser a parte de cima da tabela, como eu havia falado, que mostra informações como a categoria de cada um dos dados. 

O objetivo da tag `<th>` é semelhante ao da nossa tag `<thead>`, ela possui o objetivo de conseguirmos colocar as descrições dos dados da nossa tabela. Vamos agora, reescrever a nossa tabela para que ela inclua um cabeçalho melhor: 

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <thead>
        <tr>
            <th>Linguagem</th>
            <th>Meu Nível</th>
        </tr>
    </thead>
    <tr>
        <td>C#</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>HTML</td>
        <td>Básico</td>
    </tr>
    <tr>
        <td>CSS</td>
        <td>Básico</td>
    </tr>
</table>
```

Perceba em seu navegador que o elemento `<th>` possui até mesmo uma distinção entre os demais elementos chamados `<td>`. Esse é o objetivo dele mesmo: colocar o nome da sua coluna de forma que seja visualmente divergente de outros termos em sua página Web. 

### Melhorando nossos Dados com `<tbody>`

Como `<thead>` é uma tag voltada muito mais para títulos e descrições, temos também a tag `<tbody>`, voltada especialmente para o corpo da nossa página Web, dentro dela, podemos inclusive incorporar todos os dados da nossa página. 

Para reescrevermos a tabela, nós poderemos simplesmente adicionar uma tag `<tbody>` dentro da nossa aplicação.

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <thead>
        <tr>
            <th>Linguagem</th>
            <th>Meu Nível</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>C#</td>
            <td>Básico</td>
        </tr>
        <tr>
            <td>HTML</td>
            <td>Básico</td>
        </tr>
        <tr>
            <td>CSS</td>
            <td>Básico</td>
        </tr>
    </tbody>
</table>
```

Essa prática possui diversos benefícios e vou listá-los um por um:

#### 1 - Na Utilização de JavaScript.

Lembra-se da primeira abordagem e da primeira table que criamos? Pois é! Só tinham table rows e table data. Isso é péssimo pois as tabelas também incluem um nome de cada uma das categorias. No nosso caso, se formos gerar dinamicamente conteúdo utilizando JavaScript futuramente teríamos diversos problemas, pois poderiamos gerar HTML por cima do nome da categoria. Hoje em dia, podemos simplesmente colocar tudo no `<tbody>`, como deve ser feito. Enqunto o `<thead>` é voltado para descrições, o `<tbody>` é voltado especialmente para os seus dados. Com isso, a coexistência dos dois seria considerada bastante pacifica. 

#### 2 - Experiência de Usuário

A experiência de usuário, principalmente para deficientes visuais agrade usuários com deficiência visual, sendo uma prática muito bem vista por leitores de tela.

### Por último, `<tfoot>`

`<tfoot>` é uma tag com um funcionamento bastante semelhante à `<thead>` e `<tbody>`, mas ao invés dos títulos das colunas ou dos dados, poderemos incluir alguma espécie de Rodapé de página, claramente, quero assinar aqui o meu nome nessa tabela. 

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <thead>
        <tr>
            <th>Linguagem</th>
            <th>Meu Nível</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>C#</td>
            <td>Básico</td>
        </tr>
        <tr>
            <td>HTML</td>
            <td>Básico</td>
        </tr>
        <tr>
            <td>CSS</td>
            <td>Básico</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Gustavo da Silva Oliveira</td>
        </tr>
    </tfoot>
</table>
```

Isso daqui é um exemplo de utilização para as nossas tabelas.

## Tornando nossos Dados Mais Complexos `colspan` e `rowspan`

Imagine que você está criando um sistema de uma hamburgueria que oferece combos de lanches e de soremesas? O sistema incluiria alguns combos com lanches, acompanhamentos, no caso de uma batata frita ou de Nuggets de frango e alguns seriam acompanhados de sobremesesas? Sabemos então que:

1. Todos os combos possuem um lanche
2. Todos os combos possuem uma bebida
3. Nem todos os lanches possuem acompanhamentos
4. Nem todos os lanches possuem sobremesas.

Sabendo dessas questões e de que algumas colunas podem não ser preenchidas, faço-lhes a seguinte pergunta: **Vale a pena usar tables para montar esse cardápio? 🤔**

Se você respondeu que sim, está terminantemente correto! 

Uma técnica para que possamos "pular linhas" ou "pular colunas" dentro de uma tabela e deixá-la muito melhor é utilizarmos colspan e rowspan. O objetivo é informar ao navegador a quantidade de linhas ou colunas que serão puladas. 

Nós temos essa tabela aqui:

| Hamburguer            | Acompanhamento          | Bebida    | Sobremesa        | Preço    |
| --------------------- | ----------------------- | --------- | ---------------- | -------- |
| X-Burguer Bacon       | Batatas Cheddar e Bacon | Coca-Cola | Sundae Chocolate | R$ 60,00 |
| X-Burguer Tradicional | Batatas Cheddar e Bacon | Coca-Cola | Não Têm          | R$ 50,00 |
| X-Burguer Tradicional | Não Têm                 | Coca-Cola | Sundae Chocolate | R$ 50,00 |

Poderemos então, pular o acompanhamento, assim como a sobremesa dos itens 2 e 3. A forma que vamos fazer isso é relativamente simples. 

``` html
<table>
    <caption>Combos</caption>
    <thead>
        <tr>
            <th>Hamburguer</th>
            <th>Acompanhamento</th>
            <th>Bebida</th>
            <th>Sobremesa</th>
            <th>Preço</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batatas Cheddar e Bacon</td>
            <td colspan="2">Coca-Cola</td>
            <td>R$ 50,00</td>
        </tr>
        <tr>
            <td colspan="2">X-Burguer Tradicional</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 50,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="5">A melhor Hamburgueria do Bairro!</td>
        </tr>
    </tfoot>
</table>
```

Eu particularmente achei que uma melhor ideia era incluirmos o colspan nas linhas em que não temos valores, no entanto, vale lembrar que em casos como o do `<tfoot>`, o uso de `colspan` torna-se essencial. Verifique agora no seu navegador como está. 

### `rowspan`

O `rowspan` possui uma funcionalidade muito parecida. Mas ao invés de pularmos colunas, pulamos linhas. Podemos voltar com o exemplo do nosso currículo para ilustrarmos melhor isso. 

``` html
<table>
    <caption>Minhas Tecnologias</caption>
    <thead>
        <th>Descrição</th>
        <th>Tecnologia</th>
    </thead>
    <tbody>
        <tr>
            <td>Linguagens de Programação</td>
            <td>C#</td>
        </tr>
        <tr>
            <td rowspan="2">Linguagens de Marcação</td>
            <td>HTML</td>
        </tr>
        <tr>
            <td>CSS</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Gustavo da Silva Oliveira</td>
        </tr>
    </tfoot>
</table>
```

Digite esse código e verifique o resultado no navegador.

## Aplicando Diferentes Estilos em Colunas

De fato, eu falei para vocês que não iamos ter CSS agora correto? De certa forma eu estava errado, pois o estudo de CSS é essencial dentro desse contexto. No caso, temos as tags `<colgroup>` e `<col>`, essas tags são focadas em aplicar estilos ou propriedades em diferentes grupos de colunas, um exemplo disso é que podemos fazer exatamente isso com cada uma de nossas linhas do nosso combo. No meu caso, agora vamos ilustrar uma hamburgueria com delivery próprio e agora, cada um dos combos contará com ao menos uma sobremesa, um sanduíche, um acompanhamento e uma bebida:

| Hamburguer            | Acompanhamento          | Bebida    | Sobremesa        | Preço    |
| --------------------- | ----------------------- | --------- | ---------------- | -------- |
| X-Burguer Bacon       | Batatas Cheddar e Bacon | Coca-Cola | Sundae Chocolate | R$ 60,00 |
| X-Burguer Tradicional | Batatas Cheddar e Bacon | Coca-Cola | Torta de Morango | R$ 60,00 |
| X-Burguer Tradicional | Batata Clássica         | Coca-Cola | Sundae Chocolate | R$ 60,00 |
| X-Burguer Bacon       | Batata Clássica         | Coca-Cola | Torta de Morango | R$ 60,00 |

No topo da tabela, poderemos utilizar a tag `<colgroup>` justamente para isso.

Uma forma de representar isso é bastante simples:

``` html
<table>
    <caption>Combos</caption>
    <colgroup>
        <col span="1" style="background-color: white;">
        <col span="1" style="background-color: aqua;">
        <col span="1" style="background-color: deeppink;">
        <col span="1" style="background-color: yellow;" >
        <col span="1" style="background-color: lime;">
    </colgroup>
    <thead>
        <tr>
            <th>Hamburguer</th>
            <th>Acompanhamento</th>
            <th>Bebida</th>
            <th>Sobremesa</th>
            <th>Preço</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="5">A Melhor Hamburgueria do Bairro!</td>
        </tr>
    </tfoot>
</table>
```

Como podes ver, nós conseguimos aplicar algumas cores a cada uma das suas colunas, isso ajuda a diferenciar cada um dos elementos da sua tabela e cada uma das suas categorias. Agora você sabe como agrupar colunas e aplicar propriedades a cada uma delas. 

O atributo `span` serve para indicarmos o número de colunas às quais nós estamos aplicando uma determinada regra. No caso de cada uma das nossas cols, colocamos o número 1, isso significa que as nossas regras escritas em cima daquele componente só vão se aplicar a uma coluna. 

## Agrupando Colunas e Linhas de Forma Semântica

Bom, os navegadores ao montar a tabela entendem muito bem que o nosso elemento `<th>` refere-se sempre à nossa coluna, correto? Não necessariamente, uma coisa que esqueci de citar no nosso exemplo do `rowspan` foi justamente esse, muitas vezes um `<th>` refere-se a um grupo de colunas, colunas, linhas ou até mesmo um grupo de linhas. Quer um exemplo?

``` html
<table>
    <caption>Combos</caption>
    <colgroup>
        <col span="1" style="background-color: white;">
        <col span="1" style="background-color: aqua;">
        <col span="1" style="background-color: deeppink;">
        <col span="1" style="background-color: yellow;" >
        <col span="1" style="background-color: lime;">
    </colgroup>
    <thead>
        <tr>
            <th>Hamburguer</th>
            <th>Acompanhamento</th>
            <th>Bebida</th>
            <th>Sobremesa</th>
            <th>Preço</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="5">A Melhor Hamburgueria do Bairro!</td>
        </tr>
    </tfoot>
</table>
```

Esse é um exemplo clássico em que o nosso `<th>` está diretamente relacionado com cada um dos nossos elementos de coluna. No entanto, existem casos em que o `th` possui um escopo de linha, como é o caso desse daqui:

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <tbody>
        <tr>
            <th>C#</th>
            <td>Básico</td>
        </tr>
        <tr>
            <th>HTML</th>
            <td>Básico</td>
        </tr>
        <tr>
            <th>CSS</th>
            <td>Básico</td>
        </tr>
    </tbody>
</table>
```

Como podes ver, para cada linha da nossa tabela, em coloquei um `<th>` separado. 

### Bom, mas você me Mostrou uma tabela um pouco diferente né Gustavo? 🤔

Exatamente! É exatamente por isso que podemos informar o Escopo do nosso `<th>`. No caso da primeira tabela, é claro que o escopo de cada um deles seria `column`:

#### Scope = column

``` html
<table>
    <caption>Combos</caption>
    <colgroup>
        <col span="1" style="background-color: white;">
        <col span="1" style="background-color: aqua;">
        <col span="1" style="background-color: deeppink;">
        <col span="1" style="background-color: yellow;" >
        <col span="1" style="background-color: lime;">
    </colgroup>
    <thead>
        <tr>
            <th scope="col">Hamburguer</th>
            <th scope="col">Acompanhamento</th>
            <th scope="col">Bebida</th>
            <th scope="col">Sobremesa</th>
            <th scope="col">Preço</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batatas Cheddar e Bacon</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Tradicional</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Sundae Chocolate</td>
            <td>R$ 60,00</td>
        </tr>
        <tr>
            <td>X-Burguer Bacon</td>
            <td>Batata Clássica</td>
            <td>Coca-Cola</td>
            <td>Torta de Morango</td>
            <td>R$ 60,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="5">A Melhor Hamburgueria do Bairro!</td>
        </tr>
    </tfoot>
</table>
```

#### Scope = row:

``` html
<table>
    <caption>Minhas Linguagens</caption>
    <tbody>
        <tr>
            <th scope="row">C#</th>
            <td>Básico</td>
        </tr>
        <tr>
            <th scope="row">HTML</th>
            <td>Básico</td>
        </tr>
        <tr>
            <th scope="row">CSS</th>
            <td>Básico</td>
        </tr>
    </tbody>
</table>
```

#### Scope = rowgroup

``` html
<table>
    <caption>Minhas Tecnologias</caption>
    <thead>
        <th scope="col">Descrição</th>
        <th scope="col">Tecnologia</th>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Linguagens de Programação</th>
            <td>C#</td>
        </tr>
        <tr>
            <th scope="rowgroup" rowspan="2">Linguagens de Marcação</th>
            <td>HTML</td>
        </tr>
        <tr>
            <td>CSS</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Gustavo da Silva Oliveira</td>
        </tr>
    </tfoot>
</table>
```

## Mas e Gustavo, como Lidar com colspans e rowspans?

Bom, foi exatamente por isso que criaram o Headers, exatamente para que possamos lidar diretamente com esse tipo de tabelas.

``` html
<table>
    <caption>Combos</caption>
    <colgroup>
        <col span="1" style="background-color: white;">
        <col span="1" style="background-color: aqua;">
        <col span="1" style="background-color: deeppink;">
        <col span="1" style="background-color: yellow;" >
        <col span="1" style="background-color: lime;">
    </colgroup>
    <thead>
        <tr>
            <th id="hamburguer">Hamburguer</th>
            <th id="acompanhamento">Acompanhamento</th>
            <th id="bebida">Bebida</th>
            <th id="sobremesa">Sobremesa</th>
            <th id="preco">Preço</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td headers="hamburguer">X-Burguer Bacon</td>
            <td headers="acompanhamento">Batatas Cheddar e Bacon</td>
            <td headers="bebida">Coca-Cola</td>
            <td headers="sobremesa">Sundae Chocolate</td>
            <td headers="preco">R$ 60,00</td>
        </tr>
        <tr>
            <td headers="hamburguer">X-Burguer Tradicional</td>
            <td headers="acompanhamento">Batatas Cheddar e Bacon</td>
            <td headers="bebida" colspan="2">Coca-Cola</td>
            <td headers="preco">R$ 50,00</td>
        </tr>
        <tr>
            <td headers="hamburguer" colspan="2">X-Burguer Tradicional</td>
            <td headers="bebida">Coca-Cola</td>
            <td headers="sobremesa">Sundae Chocolate</td>
            <td headers="preco">R$ 50,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="5">A melhor Hamburgueria do Bairro!</td>
        </tr>
    </tfoot>
</table>
```

O atributo `headers` serve para referenciar cada um dos Ids que precisamos referenciar em nossa tabela. Fique tranquilo, pois futuramente você irá lidar com JavaScript, por isso, o retrabalho exigido para que nós possamos construir um table será gradativamente diminuído. 

## Conclusão. 😊

Pudemos ver muito sobre tabelas. Minha meta posteriormente assim como em formulários é receber dados vindos de uma API Rest e utilizarmos JavaScript para exibi-los em nosso navegador. 

# Fontes:

[Curso de HTML da FreeCodeCamp](https://youtu.be/kUMe1FH4CHE?si=MPvCjViUXrT8Dsc3)
[Curso de HTML e CSS do Gustavo Guanabara](https://www.youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n)
[Curso de HTML da Raffaella Ballerini](https://youtu.be/Fhy-5CtVkiM?si=wtn-SWdjussSDxLQ)
[Curso de CSS da FreeCodeCamp](https://youtu.be/OXGznpKZ_sA?si=U84DmXFYVbQ1cihZ)
[Tag table](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/table)
[Tag tr](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/tr)
[Tag td](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/td)
[Tag thead](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/thead)
[Tag tbody](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/tbody)
[Tag tfoot](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/tfoot)
[Tag th - Português](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/th)
[Tag th - Inglês](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/th)
[Tag caption - Português](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/caption)
[Tag caption - Inglês](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/caption)
[Tag colgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/colgroup)
[Tag col](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/col)