# O que são `<div>` e `<span>` no HTML?

A tag div e a tag span são tags genéricas e que não possuem valor por si próprias, podendo representar vários tipos distintos de elementos, até mesmo inputs se aplicarmos o atributo que mantém ela editável ou até mesmo textos normais. Em resumo, são componentes 100% genéricos. Eles são importantes pois são utilizados para destacar e agrupar conteúdo em páginas HTML. 

As páginas mostradas até aqui no nosso curso de HTML e de CSS na minha opinião foram extremamente simples, a partir de agora, começaremos a partir para páginas mais pesadas e com cada vez mais conteúdo. É exatamente por isso que eu decidi preparar essa aula sobre segmentação no HTML e no CSS, para que isso possa fixar cada vez mais em sua mente. A primeira coisa que temos que aprender para aprendermos a desenvolver páginas com divs e spans corretamente são justamente as diferenças cruciais entre div e span.

## Então, Gustavo, qual a diferença entre div e span? 🤔

`<div>` e `<span>` são tags que carregam diferenças fundamentais em sua renderização: `<div>` é uma tag que funciona a nível de bloco, enquanto `<span>` funciona a nível de linha. Isso quer dizer que por padrão, uma `<div>` ocupa toda a largura que foi ocupada préviamente pelo seu elemento pai. As divs são utilizadas com frequência por elementos dentro do `<body>` da nossa página, isso significa que por padrão, as divs vão ocupar toda a largura da nossa página. A única forma de evitar isso é justamente colocar a `div` dentro de um elemento com uma largura menor, mas isso é assunto para uma aula de CSS. Por consequência, os elementos que forem colocados abaixo de uma div automaticamente serão pulados para a próxima linha, observe e digite em seu navegador o seguinte código:

``` html
<body>
    <div>Oi</div>
    <div>Tudo Bem?</div>
    <div>Meu Nome é Gustavo</div>
    <div>Qual o Seu Nome?</div>
    <div>É um prazer te conhecer!</div>
</body>
```

Perceba que o comportamento é muito similar à tag `<p>`, especialmente no sentido de que não importa o que aconteça, todos os dados estão sendo renderizados um abaixo do outro. 

Isso é algo que dá para modificar no CSS, mas é exatamente por isso que utilizamos tantas divs no desenvolvimento das nossas aplicações, elas não só possuem esse comportamento padrão (diga-se de passagem) deveras interessante, como também podemos segmentar a nossa página de forma muito mais eficiente. Perceba que se utilizarmos `<span>`, os dados continuarão a ser renderizados na mesma linha, digitem o seguinte código aqui, abaixo do `<div>É um prazer te conhecer!</div>`: 

``` html
<div>
    <span>Oi</span>
    <span>Tudo Bem?</span>
    <span>Meu nome é Gustavo</span>
    <span>Qual o Seu Nome?</span>
    <span>É um prazer te conhecer!</span>
</div>
```

## Inserindo elementos dentro do div

Como eu havia mostrado em aulas anteriores, praticamente qualquer elemento dentro do `<body>` pode ser inserido dentro de uma `<div>`, inclusive, uma própria `<div>`! Vamos então criar nesse exemplo, uma tabela com vários campeonatos de futebol, como a Serie A, a Liga Brasileira, a Premier League e a Bundesliga

``` html
<div>
    <h1>Campeonato Brasileiro</h1>
    <ol>
        <li>Santos</li>
        <li>São Paulo</li>
        <li>Palmeiras</li>
        <li>Corinthians</li>
        <li>Flamengo</li>
    </ol>
</div>
<div>
    <h1>Premier League</h1>
    <ol>
        <li>Manchester City</li>
        <li>Chelsea</li>
        <li>Arsenal</li>
        <li>Liverpool</li>
        <li>Manchester United</li>
    </ol>
</div>
<div>
    <h1>Serie A</h1>
    <ol>
        <li>Milan</li>
        <li>Internazionale</li>
        <li>Juventus</li>
        <li>Roma</li>
        <li>Atalanta</li>
    </ol>
</div>
<div>
    <h1>La Liga</h1>
    <ol>
        <li>Real Madrid</li>
        <li>Barcelona</li>
        <li>Atlético de Madrid</li>
        <li>Valência</li>
        <li>Sevilla</li>
    </ol>
</div>
<div>
    <h1>Bundesliga</h1>
    <ol>
        <li>Bayern München</li>
        <li>Borussia Dortmund</li>
        <li>Hamburg</li>
        <li>Bayer Leverkusen</li>
        <li>RB Leipzig</li>
    </ol>
</div>
```

## Melhorando nosso exemplo utilizando Langs

Podemos fazer com que o nosso exemplo melhore exponencialmente aplicando o atributo lang nele. Como podemos ver, estamos mostrando campeonatos de outros países (que não o Brasil), mediante a isso, creio que seja ideal estruturarmos tudo utilizando o atributo lang.

``` html
<div lang="pt-BR">
    <h1>Campeonato Brasileiro</h1>
    <ol>
        <li>Santos</li>
        <li>São Paulo</li>
        <li>Palmeiras</li>
        <li>Corinthians</li>
        <li>Flamengo</li>
    </ol>
</div>
<div lang="en">
    <h1>Premier League</h1>
    <ol>
        <li>Manchester City</li>
        <li>Chelsea</li>
        <li>Arsenal</li>
        <li>Liverpool</li>
        <li>Manchester United</li>
    </ol>
</div>
<div lang="it">
    <h1>Serie A</h1>
    <ol>
        <li>Milan</li>
        <li>Internazionale</li>
        <li>Juventus</li>
        <li>Roma</li>
        <li>Atalanta</li>
    </ol>
</div>
<div lang="es">
    <h1>La Liga</h1>
    <ol>
        <li>Real Madrid</li>
        <li>Barcelona</li>
        <li>Atlético de Madrid</li>
        <li>Valência</li>
        <li>Sevilla</li>
    </ol>
</div>
<div lang="de">
    <h1>Bundesliga</h1>
    <ol>
        <li>Bayern München</li>
        <li>Borussia Dortmund</li>
        <li>Hamburg</li>
        <li>Bayer Leverkusen</li>
        <li>RB Leipzig</li>
    </ol>
</div>
```

Pronto! Adaptamos cada uma das divs para diferentes idiomas! 

# Projeto da Aula - Currículo

Agora que aprendemos um pouco mais a respeito de divs, tenho a responsabilidade de montar junto com você um projeto do zero para que possamos ilustrar o conceito das divs de uma forma um pouco mais estruturada. O projeto dessa aula será um currículo completamente em HTML em que vou inserir informações como os meus dados pessoais, meus principais projetos, minhas experiências de trabalho, idiomas e linguagens de prograação e marcação.

## Iniciando o Projeto.

Dentro da pasta da aula 13 - Divisões no HTML, temos uma pasta chamada "projeto" contendo o nosso arquivo `index.html`, dentro desse projeto, vamos criar do zero o nosso currículo. Uma forma de lidar com ele é bem simples, simplesmente clicamos no arquivo `index.html` e abrimos ele corretamente, afim de começarmos a escrever em cima dele. 

Após aberto, podemos começar a informar os nossos dados pessoais, com informações como nome, Linkedin, Portfólio e prinipalmente a cidade em que moro. Para isso, vamos primeiro utilizar dentro do arquivo `index.html` o comando HTML 5, no título da página, colocareos a descrição: "Currículo", sua página deve estar dessa forma:

``` html
<!DOCTYPE html>
<html lang="pt-Br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículo</title>
</head>
<body>
    
</body>
</html>
```

O título principal deve claramente ser o seu nome completo, mediante a isso, seria de grande ajuda acima de tudo criarmos uma seção na nossa página por meio de uma div. Por conta disso, cada div contará com um h2 encabeçando cada parte da nossa página. É importante citar que não ensinei vocês a utilizarem a tag a, no entanto, já aviso que vamos utilizar a tag a para colocarmos links na nossa página. No entanto, não ensinarei de forma um pouco mais aprofundada sobre isso agora. 

A sessão de dados pessoais deve ficar da seguinte forma:

``` html
<body>
    <h1>Gustavo da Silva Oliveira</h1>
    <div>
        <h2>Dados Pessoais</h2>
        <ul>
            <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
            <li><a href="https://github.com/Gustavo6401">Github</a></li>
            <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
        </ul>
    </div>
</body>
```

## Experiências.

Para as Experiências, eu pretendo utilizar uma Lista Detalhada, no caso, eu não sei se dá processo se eu informar o nome das empresas em que trabalhei, no entanto, não quero arriscar, é exatamente por isso que eu vou colocar tudo de uma forma um pouco mais cautelosa. Vale informar que quando estamos falando de experiências profissionais, estamos falando justamente de colocar uma div dentro de uma outra div, o que exigirá apenas um pouco mais de trabalho. 

``` html
<div>
    <h2>Currículo</h2>
    <div>
        <h3>Desenvolvedor Freelance</h3>
        <p>Desenvolve e mantêm uma plataforma SaaS para criadores de conteúdo educacionais melhorando a acessibilidade para estudantes e Educadores</p>
        <p>Construiu sites de e-commerces e checkouts para autores, viabilizando a automação nas vendas digitais</p>
        <p>Proporcionou soluções de gerenciamento de e-mail para pequenas empresas, otimizando a comunicação.</p>
    </div>
    <div>
        <h3>Empresa 1</h3>
        <p>Desenvolvimento e Manutenção do Sistema de Controle de Estoque.</p>
        <p>Criação de Documentação do Sistema de Controle de Estoque.</p>
        <p>Suporte aos analistas nas demandas de Call Center.</p>
    </div>
    <div>
        <h3>Empresa 2</h3>
        <p>Desenvolveu Melhorias em Sistemas Industriais.</p>
        <p>Atendimento ao cliente em sistemas industriais.</p>
        <p>Sustentação de sistema de armazém existente.</p>
        <p>Acesso a servidores em um Ambiente de Produção (Windows Server 2005).</p>
    </div>
</div>
```

O método que eu utilizei para falar sobre as minhas experiências profissionais foi exatamente esse: separar tudo entre tópicos e aos poucos ir fazendo pequenas alterações. Vocês podem escrever um pequeno texto também. 

## Habilidades

Para as nossas habilidades relacionadas à programação e habilidades comportamentais, eu vou criar uma pequena tabela, bastante semelhante ao que eu já havia feito em aulas anteriores, eu gostaria que você tabém fizesse algo semelhante. 

``` html
<div>
    <h2>Habilidades</h2>
    <table>
        <thead>
            <th>Descrição</th>
            <th>Habilidade</th>
        </thead>
        <tbody>
            <tr>
                <th scope="rowgroup" rowspan="5" id="liguagens-programacao">Linguagens de Programação</th>
                <td headers="liguagens-programacao">C#</td>
            </tr>
            <tr>
                <td headers="liguagens-programacao">JavaScript</td>
            </tr>
            <tr>
                <td headers="liguagens-programacao">TypeScript</td>
            </tr>
            <tr>
                <td headers="liguagens-programacao">Java</td>
            </tr>
            <tr>
                <td headers="liguagens-programacao">Kotlin</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="2" id="linguagens-marcacao">Linguagens de Marcação</th>
                <td headers="linguagens-marcacao">HTML</td>
            </tr>
            <tr>
                <td headers="linguagens-marcacao">CSS</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="6" id="frameworks">Frameworks</th>
                <td headers="frameworks">.Net</td>
            </tr>
            <tr>
                <td headers="frameworks">Spring Boot</td>
            </tr>
            <tr>
                <td headers="frameworks">Asp.Net</td>
            </tr>
            <tr>
                <td headers="frameworks">React JS</td>
            </tr>
            <tr>
                <td headers="frameworks">Node JS</td>
            </tr>
            <tr>
                <td headers="frameworks">Astro</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="3" id="databases">Bancos de Dados</th>
                <td headers="databases">Microsoft SQL Server</td>
            </tr>
            <tr>
                <td headers="databases">MongoDB</td>
            </tr>
            <tr>
                <td headers="databases">Cassandra</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="4" id="developmentPractices">Práticas de Desenvolvimento</th>
                <td headers="developmentPractices">Git</td>
            </tr>
            <tr>
                <td headers="developmentPractices">Domain Driven Design (DDD)</td>
            </tr>
            <tr>
                <td headers="developmentPractices">Design Patterns</td>
            </tr>
            <tr>
                <td headers="developmentPractices">Testes Unitários</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="3" id="otherTools">Outras Ferramentas</th>
                <td headers="otherTools">Docker</td>
            </tr>
            <tr>
                <td headers="otherTools">RabbitMQ</td>
            </tr>
            <tr>
                <td headers="otherTools">AWS</td>
            </tr>
            <tr>
                <th scope="rowgroup" rowspan="8" id="awsServices">Serviços da AWS</th>
                <td headers="awsServices">S3</td>
            </tr>
            <tr>
                <td headers="awsServices">EC2</td>
            </tr>
            <tr>
                <td headers="awsServices">RDS</td>
            </tr>
            <tr>
                <td headers="awsServices">Dynamo DB</td>
            </tr>
            <tr>
                <td headers="awsServices">CloudFront</td>
            </tr>
            <tr>
                <td headers="awsServices">Route 53</td>
            </tr>
            <tr>
                <td headers="awsServices">Rekognition</td>
            </tr>
            <tr>
                <td headers="awsServices">VPC</td>
            </tr>
        </tbody>
    </table>
</div>
```

Vale lembrar que precisamos criar uma tag style com um pouco de CSS para que a nossa tabela fique minimamente decente:

``` html
<style>
    table, th, tr, td, caption {
        border: 1px solid #000;
        font-family: 'Courier New', Courier, monospace;
        border-collapse: collapse;
        padding: 0.5rem;
    }
</style>
```

## Idiomas

Não sei vocês, mas eu particularmente atualmente tenho mais de um idioma, justamente por isso, eu pensei em uma seção chamada "Idiomas" pensando nisso e se você vem de ramos como Hotelaria é bem provável que você também possua mais de um idioma no currículo.

``` html
<div>
    <h2>Idiomas</h2>
    <table>
        <thead>
            <th scope="col">Idioma</th>
            <th scope="col">Nível</th>
        </thead>
        <tbody>
            <tr>
                <td>Inglês</td>
                <td>C1</td>
            </tr>
            <tr>
                <td>Francês</td>
                <td>A2</td>
            </tr>
            <tr>
                <td>Alemão</td>
                <td>A1</td>
            </tr>
        </tbody>
    </table>
</div>
```

## Projetos Pessoais

Por fim, podemos criar uma lista detalhada especialmente pensando em meu canal no YouTube. 

``` html
<div>
    <h2>Principais Projetos</h2>
    <dl>
        <dt>Canal no YouTube Escola de Programação</dt>
        <dd>Criou e publicou cursos de C#, HTML, CSS e JavaScript ajudando novos desenvolvedores.</dd>

        <dt>Academy SM - Fundador e Desenvolvedor</dt>
        <dd>Desenvolveu um Ambiente Virtual de Aprendizagem Similar ao Blackboard e ao Teams com um Marketplace voltado para educadores.</dd>
    </dl>
</div>
```

Honestamente, após verificar o projeto no navegador, eu vi que tudo está muito feio, essa lista detalhada beira o ilegível. Exatamente por isso eu fiz modificações no CSS para deixar tudo com uma fonte bem melhor, mesmo que a ideia seja usar o mínimo de CSS possível. Mas é que os meus olhos agradecem, sabe? As modificações foram feitas diretamente na tag style, na linha 7.  

``` css
* {
    font-family: 'Courier New', Courier, monospace;
}

table, th, tr, td, caption {
    border: 1px solid #000;
    border-collapse: collapse;
    padding: 0.5rem;
}
```

Honestamente, eu não gosto da Times New Roman não, de verdade. Essa fonte monoespaçada é bem melhor. 

## Finalizando

Bom, agora eu creio que podemos finalizar o nosso projeto, nosso currículo não está tão belo, mas honestamente, está bem melhor. 

# Fontes:

[Curso de HTML da FreeCodeCamp](https://youtu.be/kUMe1FH4CHE?si=MPvCjViUXrT8Dsc3)
[Curso de HTML e CSS do Gustavo Guanabara](https://www.youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n)
[Curso de HTML da Raffaella Ballerini](https://youtu.be/Fhy-5CtVkiM?si=wtn-SWdjussSDxLQ)
[Curso de CSS da FreeCodeCamp](https://youtu.be/OXGznpKZ_sA?si=U84DmXFYVbQ1cihZ)
[Documentação da Mozilla - div](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/div)
[Documentação da Mozilla em Inglês - div](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/div)
[DevMedia - Entendo a tag div](https://www.devmedia.com.br/trabalhando-com-div-em-html/37209)
[div Tag - W3Schools](https://www.w3schools.com/Tags/tag_div.asp)
[Documentação da Mozilla - span](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/span)
[Documentação da Mozilla em Inglês - span](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/span)