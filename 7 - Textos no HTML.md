# Textos no HTML

Já vimos anteriormente que podemos ordenar títulos de 1 a 6:

``` html
<!DOCTYPE html>
<html>
	<head>
		
	</head>
	<body>
		<h1>Título 1</h1>
		<h2>Título 2</h2>
		<h3>Título 3</h3>
		<h4>Título 4</h4>
		<h5>Título 5</h5>
		<h6>Título 6</h6>
	</body>
</html>
```

No entanto, não é só de títulos que precisamos em uma página Web correto? É exatamente pensando nisso que o HTML possui suporte a vários outros tipos de texto. Acredito que essa será a aula mais densa em questão de conteúdo, volta o vídeo se necessário e também vou deixar os capítulos do YouTube justamente pensando nisso. 

## Textos 

Na seção abaixo vou explicar para vocês todas as tags relacionadas a textos no HTML

### Parágrafos tradicionais. 📖 

Parágrafos jornalísticos tradicionais são desenvolvidos com a tag `<p>` Assim como as tags title e h1, o conteúdo permanece 100% dentro da tag, isso significa que a forma perfeita de criar um parágrafo jornalístico seria utilizarmos a tag p um projeto extremamente útil para quem quer ser desenvolvedor seria fazermos um pequeno portfólio nos apresentando um pouco. 

``` html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Gustavo</title>
    </head>
    <body>
        <h1>Olá! Me chamo Gustavo da Silva Oliveira!</h1>
        <p>Tenho como foco desenvolver meus pequenos projetos de Startups e para desenvolver pequenos projetos para pequenas empresas.</p>
    </body>
</html>
```

### Textos em Destaque

No HTML, grande parte dos textos em destaque e das tags semânticas são criados utilizando-se de textos em negrito e em itálico. A ideia é justamente destacar esses textos, tanto para usuários comuns quanto para os mecanismos de busca. Visualmente falando, para nós a diferença semântica é mínima ou até mesmo nenhuma. No entanto, o navegador para deficientes visuais enxerga as coisas de uma forma muito diferente. O navegador lê essas informações e informa de forma diferente de acordo com a acessibilidade. 

### Negrito

Caso você queira destacar alguma parte do texto, existe a tag `<strong>` que te possibilita fazer isso. A tag `<strong>` é utilizada como uma espécie de "destaque máximo" especialmente para um texto muito importante em sua página Web.

Colocarei a partir de agora apenas pequenas partes do texto e não o texto como um todo. 

``` html
<p>Meu principal projeto sem sombra de dúvidas foi a <strong>Academy SM</strong></p>
```

### Itálico

Já para colocar seu texto em itálico, o processo é muito parecido, existe a tag `<em>` que possibilita fazer isso. Vale lembrar que o destaque da tag `<em>` é relativamente menor que o da tag `<strong>`

``` html
 <p>A <em>Academy SM</em> tende a ser útil especialmente para professores universitários e professores do ensino médio. </p>
```

Parece o Markdown não parece? Como então eu posso representar código em minha página Web? Relaxa! Existe uma tag justamente para isso!

### Código

Código pode ser representado pela tag code normalmente, um exemplo disso é uma pequena explicação que coloquei sobre C#:

``` html
<code>Console.WriteLine("Hello World!");</code>
```

O problema, é que essa tag conta com uma forte limitação, se você for notar, ao utilizar o code no markdown se você especificar a linguagem na primeira linha você consegue até mesmo formatar em alguns editores (como a VS Code) para que você exiba inclusive o tema da IDE para aquela linguagem de programação.

![Exemplo](<7.1 - Exemplo de Como o Markdown edita o código.png>)

### Textos Pequenos

Para diminuir o tamanho de um texto, existe uma tag chamada `<small>` justamente focada nisso, recurso esse que eu nem mesmo aprendi a utilizar no Markdown.

``` html
<small>Entre em contato agora!</small>
```

É claro que eu não colocaria um CTA como um texto pequeno né gente?

### Abreviações

O navegador tem um recurso extremamente útil que é exatamente de poder abreviar nomes, ao passar o mouse por cima do parâmetro, você consegue ver por extenso o texto abreviado:

``` html
<abbr title="São Paulo">SP</abbr>
```

O parâmetro title nesse contexto serve como o nome por extenso da abreviação, ao passar o mouse o usuário poderá ver o nome por extenso. 

### Endereços

O navegador também formata com qualidade os endereços dos usuários, conforme mostrado abaixo: 

``` html
<address>
    São Paulo, SP, Brasil
</address>
```

E por fim, chegamos ao fim da parte de textos.

## Listas

Existem três tipos de listas principais às quais você precisará utilizar e se adaptar como desenvolvedor, sendo elas a lista ordenada, a lista não ordenada e a lista detalhada.

### Lista Ordenada

Lista ordenada assemelha-se muito com a lista do markdown, nós podemos faze-la da seguinte forma no HTML:

``` html
<ol>
    <li>C#</li>
    <li>JavaScript</li>
    <li>TypeScript</li>
    <li>C</li>
    <li>Java</li>
</ol>
```

Essas palavras serão exibidas na página da seguinte forma:

1. C#
2. JavaScript
3. TypeScript
4. C
5. Java

### Lista Não Ordenada

Já as listas não ordenadas já não seguem à risca esse modelo implementado pelas listas ordenadas, um exemplo que pode ser utilizado podem ser os meus Frameworks Web:

``` html
<ul>
    <li>ASP.Net Core</li>
    <li>React</li>
    <li>Razor</li>
    <li>Express</li>
    <li>.NET</li>
</ul>
```

A lista ordenada será exibida da seguinte forma:

- ASP.Net Core
- React
- Razor
- Express
- .NET

### Lista Detalhada

A lista detalhada também é um recurso interessante para se usar em suas páginas Web, no contexto do seu portfólio, você pode utilizar as listas detalhadas para falar sobre os seus projetos.

``` html
<dl>
    <dt>Academy SM</dt>
    <dd>A Academy SM é um projeto educacional focado principalmente em profissionais da educação e naqueles que têm dificuldades de acesso à educação.</dd>

    <dt>Sistema de CI/CD</dt>
    <dd>Nosso sistema de CI/CD é focado para gerar builds e versões de produção das APIs que desenvolvi e mantê-las na minha máquina EC2.</dd>
</dl>
```

## Lição de Casa

Aproveite essas tags do HTML e faça um projeto se apresentando, explique sobre seus conhecimentos, habilidades técnicas e comportamentais. Eu apresentei 9 tags para vocês, é obrigatório que vocês utilizem ao menos 6 delas. 

## Fontes:

[Curso de HTML Gustavo Guanabara](<https://youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n&si=a3PhTqm5Mv-aEqKK>)

[Curso de HTML da Rafealla Ballerini](<https://youtu.be/Fhy-5CtVkiM?si=2oHVY1Rcvm0pkWYQ>)

[Curso de HTML da Free Code Camp](<https://youtu.be/kUMe1FH4CHE?si=YAxL9P07b0CA-h6x>)

Documentação da Mozilla:

[Tag p](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/p>)

[Tag strong](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/strong>)

[Tag em](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/em>)

[Tag code](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/code>)

[Tag small](<https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small>)

[Tag abbr](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/abbr>)

[Tag address](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/address>)

[Tag ol](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/ol>)

[Tag ul](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/ul>)

[Tag dl](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/dl>)