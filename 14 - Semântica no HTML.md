# Semântica no HTML

Vimos a importância da semântica aplicada a diversos outros contextos dentro de nossas páginas Web, mas o local em que eu creio que ela seja mais utilizada, seja justamente na página como um todo. Mostrei na aula passada sobre como segmentar aspectos da nossa página utilizando principalmente as divs e os spans, no entanto, a partir dessa aula nós poderemos ver que a utilização deles será muito mais raro do que realmente pensamos.

Dentro do nosso currículo, podemos perceber que temos um conteúdo principal, ainda não temos navegação, mas podemos implementar, principalmente no futuro (se tudo der certo), especialmente no CSS e cada uma dessas informações, como as experiências, os idiomas e as linguagens de programação contariam como uma seção separada de nossa página Web. É exatamente pensando nisso que podemos trazer para vocês as tags semânticas, uma forma de organizar o código de uma forma mais eficiente e mais legível, principalmente para os leitores de texto próprios para alguns usuários, tais como os deficientes visuais. Essa aula tem por objetivo listar cada uma das tags semânticas e ensinar a vocês como utilizá-las corretamente e principalmente reescrever o projeto incluíndo as tags corretas.

## Sumário

1. `<main>`
2. `<section>`
3. `<article>`
4. `<nav>`
5. `<aside>`
6. `<header>`
7. `<footer>`

## 1 - O conteúdo principal da nossa página - A tag `<main>`

O conteúdo principal da nossa página pode ser encapsulado dentro da tag `<main>`, que por sinal é uma tag que assim como o div, pode encapsular diverentes tipos de conteúdo. No contexto do HTML, podemos ter apenas um por página e como o próprio nome diz, dentro do nosso currículo, creio que possamos encapsular todo o conteúdo que escrevemos até agora na nossa página. 

``` html
<main>
    <h1>Gustavo da Silva Oliveira</h1>
    <div>
        <h2>Dados Pessoais</h2>
        <ul>
            <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
            <li><a href="https://github.com/Gustavo6401">Github</a></li>
            <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
        </ul>
    </div>
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
    <div>
        <h2>Principais Projetos</h2>
        <dl>
            <dt>Canal no YouTube Escola de Programação</dt>
            <dd>Criou e publicou cursos de C#, HTML, CSS e JavaScript ajudando novos desenvolvedores.</dd>
            <dt>Academy SM - Fundador e Desenvolvedor</dt>
            <dd>Desenvolveu um Ambiente Virtual de Aprendizagem Similar ao Blackboard e ao Teams com um Marketplace voltado para educadores.</dd>
        </dl>
    </div>
</main>
```

Vale lembrar que as outras tags semânticas aqui indicadas não podem ser um elemento pai para a tag `<main>` as tags semânticas às quais eu me refiro são `header`, `footer`, `article`, `section`, `nav` e `aside`. O motivo para isso é óbvio: falei diversas vezes aqui que `<main>` foi feito justamente para encapsular o conteúdo principal da página. As outras tags possuem uma função diferente, mesmo sendo tags semânticas, por isso, não podemos utilizá-las nesse contexto. 

## 2 - A tag feita para cabeçalhos: a tag `<header>`

A melhor forma de exibirmos os cabeçalhos da página, como é um exemplo do título e de dados de navegação é justamente por meio da tag `<header>`. Além disso, você poderia utilizar até mais de um por página, especialmente em cabeçalhos de sessões e de outras partes da página, assim como a tag `<article>`. Dentro do nosso currículo, vamos reescrever o cabeçalho da página, contendo o nosso nome, nosso portfólio e nosso LinkedIn:

``` html
<header>
    <h2>Dados Pessoais</h2>
    <ul>
        <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
        <li><a href="https://github.com/Gustavo6401">Github</a></li>
        <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
    </ul>
</header>
```

Como podemos incluir mais de um header por página, uma ideia boa seria faermos modificações diretamente em cada um dos títulos da nossa página, deixando o `<main>`, dessa forma:

``` html
<main>
    <h1>Gustavo da Silva Oliveira</h1>
    <header>
        <h2>Dados Pessoais</h2>
        <ul>
            <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
            <li><a href="https://github.com/Gustavo6401">Github</a></li>
            <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
        </ul>
    </header>
    <div>
        <header>
            <h2>Currículo</h2>
        </header>
        <div>
            <header>
                <h3>Desenvolvedor Freelance</h3>
            </header>
            <p>Desenvolve e mantêm uma plataforma SaaS para criadores de conteúdo educacionais melhorando a acessibilidade para estudantes e Educadores</p>
            <p>Construiu sites de e-commerces e checkouts para autores, viabilizando a automação nas vendas digitais</p>
            <p>Proporcionou soluções de gerenciamento de e-mail para pequenas empresas, otimizando a comunicação.</p>
        </div>
        <div>
            <header>
                <h3>Empresa 1</h3>
            </header>
            <p>Desenvolvimento e Manutenção do Sistema de Controle de Estoque.</p>
            <p>Criação de Documentação do Sistema de Controle de Estoque.</p>
            <p>Suporte aos analistas nas demandas de Call Center.</p>
        </div>
        <div>
            <header>
                <h3>Empresa 2</h3>
            </header>
            <p>Desenvolveu Melhorias em Sistemas Industriais.</p>
            <p>Atendimento ao cliente em sistemas industriais.</p>
            <p>Sustentação de sistema de armazém existente.</p>
            <p>Acesso a servidores em um Ambiente de Produção (Windows Server 2005).</p>
        </div>
    </div>
    <div>
        <header>
            <h2>Habilidades</h2>
        </header>
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
    <div>
        <header>
            <h2>Idiomas</h2>
        </header>
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
    <div>
        <header>
            <h2>Principais Projetos</h2>
        </header>
        <dl>
            <dt>Canal no YouTube Escola de Programação</dt>
            <dd>Criou e publicou cursos de C#, HTML, CSS e JavaScript ajudando novos desenvolvedores.</dd>
            <dt>Academy SM - Fundador e Desenvolvedor</dt>
            <dd>Desenvolveu um Ambiente Virtual de Aprendizagem Similar ao Blackboard e ao Teams com um Marketplace voltado para educadores.</dd>
        </dl>
    </div>
</main>
```

É muita coisa? Sim! Mas aos poucos, vamos deixando tudo da forma mais correta possível. 

Vale lembrar que cada um desses `<div>` possuem divisões semânticas extremamente importantes, é exatamente por isso que também temos uma tag chamada `<section>`.

## 3 - Segmentando Dados Corretamente - A tag `<section>`

A tag `<section>` é considerada a forma certa de criarmos diferentes seções dentro de uma página Web, perceba que visívelmente, utilizar `<header>` dentro de uma `<div>` não é algo que faça tanto sentido semântico assim, no entanto, quando estamos falando de utilizar `<section>`, as coisas tornam-se extremamente semânticas e o `<header>` começa a fazer muito mais sentido. No caso das `<div>` que antigamente eram elementos pai de `<h2>` e `<h3>`, faremos modificações afim de incluirmos `<section>` em cada um deles. A página agora vai ficar assim:

``` html
<main>
    <h1>Gustavo da Silva Oliveira</h1>
    <header>
        <h2>Dados Pessoais</h2>
        <ul>
            <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
            <li><a href="https://github.com/Gustavo6401">Github</a></li>
            <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
        </ul>
    </header>
    <section>
        <header>
            <h2>Currículo</h2>
        </header>
        <section>
            <header>
                <h3>Desenvolvedor Freelance</h3>
            </header>
            <p>Desenvolve e mantêm uma plataforma SaaS para criadores de conteúdo educacionais melhorando a acessibilidade para estudantes e Educadores</p>
            <p>Construiu sites de e-commerces e checkouts para autores, viabilizando a automação nas vendas digitais</p>
            <p>Proporcionou soluções de gerenciamento de e-mail para pequenas empresas, otimizando a comunicação.</p>
        </section>
        <section>
            <header>
                <h3>Empresa 1</h3>
            </header>
            <p>Desenvolvimento e Manutenção do Sistema de Controle de Estoque.</p>
            <p>Criação de Documentação do Sistema de Controle de Estoque.</p>
            <p>Suporte aos analistas nas demandas de Call Center.</p>
        </section>
        <section>
            <header>
                <h3>Empresa 2</h3>
            </header>
            <p>Desenvolveu Melhorias em Sistemas Industriais.</p>
            <p>Atendimento ao cliente em sistemas industriais.</p>
            <p>Sustentação de sistema de armazém existente.</p>
            <p>Acesso a servidores em um Ambiente de Produção (Windows Server 2005).</p>
        </section>
    </section>
    <section>
        <header>
            <h2>Habilidades</h2>
        </header>
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
    </section>
    <section>
        <header>
            <h2>Idiomas</h2>
        </header>
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
    </section>
    <section>
        <header>
            <h2>Principais Projetos</h2>
        </header>
        <dl>
            <dt>Canal no YouTube Escola de Programação</dt>
            <dd>Criou e publicou cursos de C#, HTML, CSS e JavaScript ajudando novos desenvolvedores.</dd>
            <dt>Academy SM - Fundador e Desenvolvedor</dt>
            <dd>Desenvolveu um Ambiente Virtual de Aprendizagem Similar ao Blackboard e ao Teams com um Marketplace voltado para educadores.</dd>
        </dl>
    </section>
</main>
```

O melhor de tudo: a tag `<section>` é uma tag extremamente poderosa justamente porque nós podemos aninhar sections, o grande exemplo disso é justamente a parte das experiências. Perceba como a utilização de diferentes headers faz muito mais sentido agora, justamente por isso. Vale lembrar também que essa parte das experiências na minha opinião faz bastante sentido começarmos a explicar sobre a próxima tag semântica: a tag `<article>`, que por sinal, será a próxima tag a ser explicada. Tenham em mente que a tag `<section>` deve ser utilizada quando queremos organizar tudo de forma semântica e principalmente quando não podemos utilizar outras tags semânticas como `<article>`, `<header>` ou `<footer>`. Perceba como eu inseri um `<header>` no topo da página, justamente pensando nisso.

## 4 - Preparando Conteúdo Autocontido - Tag `<article>`

A tag `<article>` possui uma qualidade que destaca ela das outras tags: ela é voltada justamente para conteúdo que faça sentido em outras páginas ou outros blocos de páginas. Um exemplo são comentários de redes sociais, posts de um blog, notícias ou uma série de outras coisas. Digamos que eu coloque uma notícia que fala a respeito da Academy SM, do Escola de Programação ou de qualquer outro projeto que eu exerça, eu poderia incluir diretamente no meu currículo utilizando a tag `<article>`. Algumas pessoas podem argumentar inclusive que a sessão de Experiências Profissionais do próprio currículo serviria para a utilização da tag `<article>`, porém, eu tenho que discordar disso por um motivo importante: 

#### 1 - A sessão de Experiências não faz sentido em qualquer contexto.

A seção de experiências dessa página foi pensada 100% em atender os requisitos da minha página. "Experiâncias Profissionais" não pode e hipótese alguma operar como bloco independente, diferentemente se eu colocasse algum outro bloco, como uma notícia sobre algum projeto ou até mesmo um post de rede social. Se eu colocasse algum dos posts do Canal Escola de Programação, faria bastante sentido que eu criasse uma sessão de experiências também. Atualmente então, podemos concluir que não faz muito sentido utilizarmos a tag `<article>` aqui. 

Mudando um pouco de assunto, podemos perceber que a navegação da nossa página ficou longa e maçante, eu não gostaria que o meu usuário tivesse que fazer várias e várias rolagens para que ele chegue ao seu objetivo principal. Justamente penando nisso, temos a próxima tag: a tag `<nav>`.

## 5 - Preparando a Navegação da Página - Tag `<nav>`

A tag `<nav>` é importante pois o objetivo dela é justamente incluirmos os elementos de navegação dentro da nossa página. Uma coisa muito importante é que podemos incluir mais de um elemento do tipo `<nav>` dentro da nossa página. Vou ensinar algumas coisas que eu não havia ensinado previamente: links e navegação no HTML, mas claro, estamos falando de links internos da página. 

A criação de Links depende especialmente da tag `<a>`, manteremos um link para cada seção da nossa página. Precisamos primeiro criar Ids em cada uma das sessões dentro do nosso `<main>` e um também dentro do `<header>` principal. 

``` html
<header id="dados">
<section id="experiencias">
<section id="habilidades">
<section id="idiomas">
<section id="projetos">
```

A sua VSCode te ajuda a navegar de forma intuitiva dentre as muitas seções da sua página web. Isso pode tornar o processo de criação dos Ids como um processo bem mais fácil. Uma forma de minimizar e facilitar a navegação é justamente clicar nessa seta para baixo inserida no section que você quer modificar.

![Seta VS Code](<imgs/Aula 14/14.1 - Ícones ao Lado - VS Code.png>)

Uma forma de que você acesse outra seção de uma forma mais rápida é clicar diretamente nesse `<section>`, ele é bastante útil justamente para que você vá até a outra section em que você precisa digitar os Ids:

![Seções](<imgs/Aula 14/14.2 - sections no HTML.png>)

Uma forma de otimizar esse trabalho é justamente minimizar cada um deles e criar um Id separado para cada.

![Ids nas Sections](<imgs/Aula 14/14.3 - Colocando Ids nas sections.png>)

E quanto à parte de navegação? Bom, eu admito não ter ensinado vocês nem mesmo a utilizarem links e eu vou pular direto para navegação né? 😅 Mais para frente, vamos falar um pouco mais profundamente sobre o funcionamento da tag a, no caso, por ora, o que faremos é justamente criar uma lista não ordenada. Essa lista não ordenada será responsável por manter os links da nossa página, até porque eu vou colocar um link dentro de cada elemento `<li>`. Isso é meio que uma estrutura "padrão" para as minhas barras de navegação, futuramente, se tudo der certo, ensinarei a estilizar elas de forma correta. No meio das fontes pretendo manter uma referência para o site da W3Schools que na minha opinião, além da documentação da Mozilla é o melhor site para aprender um pouco mais sobre HTML, CSS e JavaScript, inclusive, enquanto o Canal Escola de Programação (e se) o Canal não tiver conteúdo sobre HTML, CSS e JavaScript, na minha opinião é o site que eu mais indico. 

Depois dessas alterações o nosso header ficará desse jeito:

``` html
<header id="dados">
    <section>
        <h2>Dados Pessoais</h2>
        <ul>
            <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
            <li><a href="https://github.com/Gustavo6401">Github</a></li>
            <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
        </ul>
    </section>
    <nav>
        <ul>
            <li>
                <a href="#dados">Dados Pessoais</a>
            </li>
            <li>
                <a href="#experiencias">Experiências Profissionais</a>
            </li>
            <li>
                <a href="#habilidades">Habilidades</a>
            </li>
            <li>
                <a href="#idiomas">Idiomas</a>
            </li>
            <li>
                <a href="#projetos">Projetos</a>
            </li>
        </ul>
    </nav>
</header>
```

O nosso código HTML ficou da seguinte forma e creio que essa seja a última alteração que faremos nessa aula. Futuramente, vamos incluir um footer já não sei se vamos incluir um aside ou alguma outra tag semântica.

``` html
<main>
    <h1>Gustavo da Silva Oliveira</h1>
    <header id="dados">
        <section>
            <h2>Dados Pessoais</h2>
            <ul>
                <li><a href="https://www.linkedin.com/in/gustavo-oliveira-918900182/">LinkedIn</a></li>
                <li><a href="https://github.com/Gustavo6401">Github</a></li>
                <li><a href="https://gustavo6401.github.io/">Portfólio</a></li>
            </ul>
        </section>
        <nav>
            <ul>
                <li>
                    <a href="#dados">Dados Pessoais</a>
                </li>
                <li>
                    <a href="#experiencias">Experiências Profissionais</a>
                </li>
                <li>
                    <a href="#habilidades">Habilidades</a>
                </li>
                <li>
                    <a href="#idiomas">Idiomas</a>
                </li>
                <li>
                    <a href="#projetos">Projetos</a>
                </li>
            </ul>
        </nav>
    </header>
    <section id="experiencias">
        <header>
            <h2>Experiências Profissionais</h2>
        </header>
        <section>
            <header>
                <h3>Desenvolvedor Freelance</h3>
            </header>
            <p>Desenvolve e mantêm uma plataforma SaaS para criadores de conteúdo educacionais melhorando a acessibilidade para estudantes e Educadores</p>
            <p>Construiu sites de e-commerces e checkouts para autores, viabilizando a automação nas vendas digitais</p>
            <p>Proporcionou soluções de gerenciamento de e-mail para pequenas empresas, otimizando a comunicação.</p>
        </section>
        <section>
            <header>
                <h3>Empresa 1</h3>
            </header>
            <p>Desenvolvimento e Manutenção do Sistema de Controle de Estoque.</p>
            <p>Criação de Documentação do Sistema de Controle de Estoque.</p>
            <p>Suporte aos analistas nas demandas de Call Center.</p>
        </section>
        <section>
            <header>
                <h3>Empresa 2</h3>
            </header>
            <p>Desenvolveu Melhorias em Sistemas Industriais.</p>
            <p>Atendimento ao cliente em sistemas industriais.</p>
            <p>Sustentação de sistema de armazém existente.</p>
            <p>Acesso a servidores em um Ambiente de Produção (Windows Server 2005).</p>
        </section>
    </section>
    <section id="habilidades">
        <header>
            <h2>Habilidades</h2>
        </header>
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
    </section>
    <section id="idiomas">
        <header>
            <h2>Idiomas</h2>
        </header>
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
    </section>
    <section id="projetos">
        <header>
            <h2>Principais Projetos</h2>
        </header>
        <dl>
            <dt>Canal no YouTube Escola de Programação</dt>
            <dd>Criou e publicou cursos de C#, HTML, CSS e JavaScript ajudando novos desenvolvedores.</dd>
            <dt>Academy SM - Fundador e Desenvolvedor</dt>
            <dd>Desenvolveu um Ambiente Virtual de Aprendizagem Similar ao Blackboard e ao Teams com um Marketplace voltado para educadores.</dd>
        </dl>
    </section>
</main>
```

## 6 - Colocando Conteúdo Relacionado: Tag aside

O propósito da tag aside é simples: mostrar conteúdo relacionado, tais como uma outra barra de navegação, anúncios ou até mesmo links complementares, semelhante ao que é desenvolvido em alguns projetos que desenvolvi. A ideia é exataente colocar um conteúdo que não depende muito do conteúdo principal. Com isso, a ideia é que ela seja colocada fora do `<main>` e dentro do `<body>`. Existe uma página Web na qual futuramente eu pretendo inserir no Aside. 

![Exemplo](<imgs/Aula 14/14.4 - Grupos - Enviar Tarefas.png>)

Mostrei a foto dessa página como um exemplo, não quer dizer que a página estéticamente bela, pois ela não está. O objetivo foi justamente mostrar um exemplo de barra de navegação lateral. Essa barra inclusive é utilizada por vários componentes, mediante a isso, me lembrei justamente da tag aside. Sinto justamente isso nas tags `<article>`, `<aside>` e `<footer>`, a capacidade de reaproveitar o conteúdo, o que é bastante aproveitável por Frameworks e Libs como o React JS e o Blazor. Se tudo der certo, teremos futuros cursos dessas tecnologias. 

## 7 - Criando rodapés para a nossa página

Não criaremos um rodapé ainda, mas dentro do rodapé assim como nos livros colocamos o número das páginas, nos rodapés, nós podemos colocar outras informações importantes, tais como Links de Redes Sociais, informações de direitos autorais assim como o fizemos em nosso `tfoot` na aula sobre tabelas. Um exemplo claro de página que utiliza um rodapé é a página do Gengo, podemos perceber que eles utilizaram muito bem o rodapé para colocarem links instituicionais e principalmente as informações de direitos autorais. O link para o site é esse [daqui](https://gengo.com/). Na construção de páginas institucionais, principalmente com CSS poderemos utilizar com uma certa frequência a tag `footer`. 

## Mas e Quando Utilizar Divs?

Como eu havia dito anteriormente, divs e spans são recursos feitos para serem utilizados. Um exemplo ao qual eu gosto muito de utilizar divs é exatamente nos formulários. Basicamente, existem dois casos aos quais eu gosto de utilizar bastante:

### 1 - Quando a Div não possui nenhum Peso semântico

Isso é: campos de formulários, partes ocultas que podem ser mostradas posteriormente com JavaScript, tais como mensagens de erro são exemplos aos quais eu defendo a utilização de divs. Mensagens de erro são um exemplo que por vezes não carrega tanto peso semântico assim. O Bootstrap por exemplo utiliza muitos spans para informar que um determinado campo não foi inserido corretamente. 

### 2 - Quando Queremos modificar as exibições CSS. 

Uma prática comum em páginas HTML é justamente modificar o comportamento padrão do CSS, como eu havia citado anteriormente, por padrão, label e input são elementos que são alinhados, ou seja, não se pula a linha de um elemento para o outro. Com isso, eu crio com frequência uma div para pular uma linha de um para o outro. Um exemplo de código que eu poderia citar para a utilização de um div está na nossa aula sobre formulários no HTML:

``` html
<fieldset>
    <legend>Dados Pessoais</legend>
    <div>
        <label for="nome">Nome</label>
        <input type="text" maxlength="20" required placeholder="Nome" id="nome" />
    </div>
    <div>
        <label>E-Mail</label>
        <input type="email" placeholder="E-Mail" />
    </div>
    <div>
        <label>Senha</label>
        <input type="password" />
    </div>
    <div>
        <label>Telefone</label>
        <input type="tel" pattern="" />
    </div>
</fieldset>
```

Esse é um exemplo clássico de utilização de divs. Perceba que não existe relação semântica entre os divs e os inputs. Esse é um caso em que não caberia a utilização de outras tags, tais como `<section>` ou `<article>`, mais importante ainda que essas divs são filhas do `<fieldset>` outra tag igualmente importante semanticamente. Nesses casos, podemos utilizar Divs da melhor forma possível.

## Conclusão

O objetivo dessa aula foi ajudar para que as páginas de vocês mantenham o máximo de semântica possível. Isso não apenas mantém sua página mais acessível, como também, os mecanismos de buscas premiam quem faz tudo de forma semântica. O objetivo foi ensiná-los a utilizar as tags corretamente, inclusive a tag `<div>`.

## Fontes:

[Diferença Entre section e article](https://pt.stackoverflow.com/questions/326021/qual-a-diferen%c3%a7a-sem%c3%a2ntica-entre-section-e-article)

[Sections no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/section)

[Articles no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/article)

[Navs no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/nav)

[Headers no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/header)

[Footer no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/footer)

[Main no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/main)

[Aside no HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/aside)

[Curso de HTML da FreeCodeCamp](https://youtu.be/kUMe1FH4CHE?si=MPvCjViUXrT8Dsc3)

[Curso de HTML e CSS do Gustavo Guanabara](https://www.youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n)

[Curso de HTML da Raffaella Ballerini](https://youtu.be/Fhy-5CtVkiM?si=wtn-SWdjussSDxLQ)

[Curso de CSS da FreeCodeCamp](https://youtu.be/OXGznpKZ_sA?si=U84DmXFYVbQ1cihZ)