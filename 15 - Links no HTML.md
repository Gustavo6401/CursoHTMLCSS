# Links no HTML

Links são a alma da Internet, é exatamente por isso que os selecionamos como o penúltimo assunto dentro do contexto do HTML e do CSS. Em aulas passadas, links internos, externos e de blocos já foram mostrados aqui no nosso canal, mas não com a profundidade que esses temas mereciam ser abordados, a aula de hoje será baseada unica e exclusivamente na tag a e no funcionamento dela. 

## A alma da Internet - a Tag `<a>` e o atributo `href`

Lembra que eu falei que a Internet foi construída em cima de muitos e muitos hiperlinks? Se você for para pensar, grandes exemplos de páginas que possuem diversos são o Google, o YouTube, os sites de conteúdo adulto, o Bing e as redes sociais, sejam esses links externos ou internos, justamente por isso esses sites utilizam com frequência a tag `a`, mesmo que seja para acessar uma pequena parte do conteúdo da página Interna, como mostrado na outra aula. 

Nesse ponto, entra o atributo `href`. Esse atributo é responsável por indicar qual link nós iremos acessar, se você assistiu as nossas aulas sobre `divs`, sabe que montamos um portfólio que redireciona para outros links, tais como o LinkedIn ou até mesmo o Github. Mediante a isso, podemos perceber que quando se fala do resto da Internet isso não é diferente, podemos informar normalmente o Link ao qual queremos acessar no atributo `href`. Um claro exemplo disso é justamente um Link para a minha plataforma, que por sinal, ainda não está funcionando corretamente, mas que estou montando tudo aos poucos, especialmente a Academy SM.

``` html
<a href="https://academysm.com">Academy SM</a>
```

### Mas Gustavo, e se eu criar um link sem um Href? 🤔

Então, no caso não acontecerá nada, mas isso não é uma boa prática. O máximo que você pode fazer é justamente criar um texto simples com uma formatação de Link, vamos inclusive criar esse exemplo aqui em baixo: 

``` html
<a>Link Falso</a>
```

Perceba como esse Link não possui absolutamente nada, isso é um grande exemplo do que acontece com Links sem o atributo `href`. Há quem diga inclusive que isso pode confundir navegadores e leitores de tela voltados para deficientes visuais, mediante a isso, não é considerada uma boa prática criarmos textos dessa forma. Recomendo muito mais a utilização de tags `p` ou `span` para que você possa fazer isso.

## Links Internos

Links Internos são links que apontam para diferentes seções dentro de nossa página, um grande exemplo disso é o nosso portfólio, dentro dele, criamos diferentes seções, cada uma com o seu Id diferente, e exatamente por isso nós criamos uma barra de navegação para que possamos acessar com muito mais facilidade o conteúdo de dentro da página. No caso, o que faremos é até mesmo uma modificação bastante radical: vamos criar 50 `br` e embaixo disso criaremos uma seção, no caso, iremos modificar radicalmente aqui o nosso HTML, pois nós seremos responsáveis por colocar o Link dentro de uma barra de navegação. Por mais que essa seja uma aula de Links, nós nunca podemos perder o pensamento semântico. Separar os pedaços do HTML é essencial para uma boa visibilidade em diferentes leitores de tela. 

Para que possamos criar os 50 elementos `br` automaticamente, temos que utilizar o comando `50*br` dentro da nossa VS Code, vamos lá? 

![Brs](<imgs/Aula 15/15.1 - br X 50.png>)

Após criarmos isso, temos que criar uma pequena seção em que podemos incluir outras informações, como um pequeno formulário, eu simplesmente colocarei a mensagem: obrigado por vir até aqui! 😁 O nome da minha seção será agradecimento e eu criarei um link Interno para o acesso à essa seção. Seu código HTML deve ficar dessa forma:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Links no HTML</title>
</head>
<body>
    <header>
        <a href="https://academysm.com">Academy SM</a>
        <a href="#agradecimento">Agradecimento</a>
    </header>
    <main>
        <section>
            <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
        </section>
        <section id="agradecimento">
            <p>&#9813; Obrigado! 😁 &#9819;</p>
        </section>
    </main>
</body>
</html>
```

De quebra, ainda coloquei alguns símbolos, tais como duas rainhas do xadrez e uma cara feliz. 

## Links Externos

Já foram mostrados como podemos criar links externos, no entanto, vale lembrar que a Internet foi construída com isso. 

Já para referenciarmos Links externos, podemos simplesmente referenciar no atributo `href` a URL externa à qual nós queremos referenciar. 

``` html
<a href="https://academysm.com">Academy SM</a>
```

Uma boa prática, como podem ver é informar todos os dados na URL, desde o protcolo (https), www e o domínio quando se fala sobre Links externos, diferentemente de Links Internos em que simplesmente informamos o nome do arquivo ao qual queremos acessar. 

### Escolhendo Onde Abrir o Link com o atributo `target`

O atributo `target` serve exatamente para informarmos ao HTML onde abrir cada Link, isso é especialmente útil quando utilizamos os links externos, pois por vezes não queremos cobrir a nossa página atual. Se eu estou em uma página do Canal Escola de Programação, para mim é mais do que óbvio que eu gostaria de abrir alguma página da Academy SM diretamente a partir de alguma outra aba. Vocês terão que lidar diretamente com esse tipo de link. Mas atualmente, se você clicar na nossa tag a, vamos abrir a página da Academy SM, correto? Nossa meta agora é justamente corrigir esse comportamento errôneo. Isso significa que por padrão, o target está como `_self`, crie o atributo `target` e coloque ele como `_blank` para que possamos abrir a página da Academy SM em outra página. 

``` html
<a href="https://academysm.com" target="_blank">Academy SM</a>
```

Como podes ver, agora a nossa página está abrindo em outra aba do navegador. 

#### Atributos Possíveis

1. `_self` - Semelhante ao input do `type='text'`, o target `_self` é o estado natural do nosso link, o que significa que por padrão o nosso link é configurado para abrir dentro da mesma aba, sobrepondo a nossa página atual. Uma recomendação é que você utilize esse atributo especialmente em páginas web em que nós estamos fazendo algum tipo de navegação interna. Mas claro, existem casos em que você pode utilizar `_self` com facilidade em links externos também, mas mantenha o foco em páginas internas. 
2. `_blank` - Ele faz com que o próximo link seja aberto em uma nova aba e não na aba atual. Como eu havia falado, ele é especialmente útil quando se fala de páginas externas. 
3. `_parent`, `_top` e `framename` - Eram úteis no passado em que as pessoas costumavam desenvolver com frequência utilizando frames, imagino que já não vamos mais utilizar isso nos tempos atuais, mas é um recurso bom para que vocês entendam que existe no HTML. Claro, fica de lição de casa para que vocês busquem entender um pouco mais sobre esses atributos. 

## Links de Download

Certamente você já fez algum download enquanto você navegava na Web, correto? Seja de uma imagem, um vídeo ou se algum outro tipo de mídia? Especialmente se você é um recrutador responsável por dirigir processos seletivos na sua empresa, essa prática tende a ser ainda mais comum pois você terá de fazer o Download ou até mesmo Upload de inúmeros currículos todos os dias. Mas muitas vezes você quer baixar um docuento de declaração de imposto de renda, ou alguma imagem no Facebook. Muitas vezes nós poderemos fazer isso por meio dos Links de Download. É exatamente por isso que vou disponibilizar o PowerPoint atual das nossas aulas de HTML e de CSS para que possamos repetir esse download. Digite o código abaixo para que você possa criar seu próprio link de download:

``` html
<a href="docs\Curso de HTML e CSS.pptx" download>Baixe o PDF!</a>
```

Para que isso funcione corretamente, é necessário que você baixe o PDF da aula [Aqui](<Power Point\Curso de HTML e CSS.pptx>)

A partir daí, você pode criar uma pasta docs dentro da aula 15 (se ela não existir ainda) e simplesmente colocar ali o nosso arquivo. 

Perceba, ao clicar no Link você receberá a Informação de que o arquivo foi devidamente baixado, como deve ser. 

![Arquivo Baixado](<imgs/15.2 - Download.png>) 

E pronto! A partir de agora, você criou seu próprio Link de Download. 

## Links para E-Mail e Telefone

Dentro do HTML você tabém pode construir Links que apontam para endereços de E-Mail, isso te dará a possibilidade de receber E-Mails diretamente. Isso pode ser feito por meio do HTML. Ao clicar no Link, é aberto o programa de E-Mail do seu computador. Claro, vamos fazer isso sem necessariamente um E-Mail real, até porque a ideia é justamente fugirmos de SPAM ou algum outro problema. 

``` html
<a href="mailto:gustavo@exemple.com">E-Mail</a>
```

No caso, o E-Mail "gustavo@exemple.com" é um E-Mail 100% fictício, o objetivo é justamente sermos didáticos. Um detalhe importante é que esses E-Mails são registrados por fins de documentação, de testes e de criação de aulas semelhantes à aula que estamos tendo agora. Isso significa que praticamente em qualquer exemplo se não para sempre, por muito tempo, vamos utilizar @exemple.com. 

### Mas Gustavo, e quanto aos Números de Telefone? 🤔

Os números de telefone funcionam de forma claramente diferente, para que possamos fazer a configuração de links de telefone, nós precisamos utilizar o `href=tel:<NUMERO-TELEFONE>`, justamente para que consigamos fazer ligações. Assim como o `mailto:` o `tel` é focado muito mais em fazer ligações e por isso ele abre o aplicativo de chamadas do seu celular para que ele funcione corretamente. 

``` html
<a href="tel:+5511">Telefone</a>
```

A grande questão aqui é que é mais do que claro que eu não colocaria um número de telefone que sequer possa ser real, o motivo é muito simples: ao fazermos isso, podemos acabar expondo em nossa página Web dados pessoais de um terceiro, ou até mesmo os nossos dados pessoais se utiliarmos links com `mailto:` ou `tel:`, é exatamente por isso que vamos fazer as coisas de uma outra forma, OK? 

### Alternativas Recomendadas

#### 1 - Formulário de Contato

Eu já uso com uma certa frequência Formulários de contato e na minha opinião, é a forma mais correta de fazermos o que temos que fazer no HTML sem utilizarmos informações pessoais, claro, o pessoal pode "encher o saco", mas pense pelo lado bom: não tem um idiota de ligando o dia inteiro querendo encher o seu saco. 

#### 2 - Uso de número Intermediário ou serviço VoIP.

Serviços VoIP servem exatamente para que a gente possa evitar esse tipo de problema, é como se fosse uma enorme secretária eletrônica em que fazemos uma ligação e a ligação é automaticamente transferida para o nosso número de telefone, mas é claro, tudo isso tem um custo. Se eu não me engano, a Twillio possui um serviço VoIP, creio que isso seja de suma importância para a sua privacidade. 

#### 3 - Serviço Telephony 

Serviços Telephony possuem um funcionamento parecido com serviços VoIP, a ideia é justamente transferir a ligação diretamente para o seu Back-End, a partir daí, o serviço conseguirá fazer uma ligação direto para o seu número de telefone. Esse é mais um serviço que exige um pagamento. 

## Oferecendo dicas para o usuário o atributo `title`

O atributo `title` possui um funcionamento interessante: por meio dele, nós podemos oferecer uma dica para o nosso usuário sobre o que o nosso Link faz e onde que ele vai clicar. Isso é bom especialmente para a questão semântica da nossa página, por meio dessa ferramenta, nós conseguiríamos melhorar ainda mais a experiência de usuário para potenciais usuários deficientes. 

``` html
<a href="https://academysm.com" target="_blank" title="Visitar a Academy SM">Academy SM</a>
```

Isso é especialmente útil quando se fala de acessibilidade, especialmente porque estamos criando um texto curto e otimizado para cada um dos nossos usuários. Isso garante uma acessibilidade maior dentro da página Web.

Mas claramente, estamos falando especialmente das relações entre os diferentes componentes e as diferentes páginas Web, nesse contexto, temos mais um atributo, o atributo `rel`.

## Estabelecendo melhores Relações entre Links utilizando o atributo `rel`

O atributo `rel` é importantíssimo, por meio dele, nós podemos estabelecer a relação entre a nossa página atual e a próxima página à qual nós estamos apontando. Assim como o `target`, esse atributo possui seus valores pré-definidos.

- `noopener` -> É um atributo importante por impedir que a página de destino consiga manipular a página de origem por meio de JavaScript, isso é uma questão de segurança. 
- `noreferrer` -> É importante para que a página de destino inclusive não saiba de onde o cliente veio, logo, se eu utilizar esse atributo em meu Link externo, o site da Academy SM não saberá que eu vim de uma página `localhost`.
- `nofollow` -> Utilizado especialmente quando se fala de ranqueamento, estamos indicando para buscadores como o Google e o Bing que eles não devem seguir esse link para ranqueamento. 