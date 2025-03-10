# Metadados no HTML e a Tag `title`

Como você sabe, metadados são uma das ferramentas mais importantes do HTML, eles podem ser representados pela Tag meta e contém todos os metadados de qualquer arquivo que você busca importar em sua página. Eles podem ser utilizados para diversas configurações como o relacionamento com motores de busca como o Google e o Bing, o compartilhamento de um bom link em suas redes sociais, com direito a uma descrição detalhada e fotos de sua página. 

## Poderoso! O que mais podemos fazer com a tag `meta`? 🔥

Muitas coisas, dentre elas:

### 1 - Definir a Codificação de Caracteres

``` html
<meta charset="UTF-8">
```

A codificação UTF-8 como mencionado anteriormente permite a utilização de caracteres especiais e acentos, inclusive, ela é bastante utilizada mesmo nos Estados Unidos. (Ao menos nos tutoriais que eu vi).

### 2 - Tornar o site Responsivo:

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Esse código será lido especialmente por dispositivos móveis, inclusive, isso pode ser consultado por meio da documentação do Mozilla.

### 3 - Definir Descrições para SEO:

``` html
<meta name="description" content="Esta é uma página incrível sobre tecnologia.">
```

Essa descrição será exibida após a busca do seu site no Google ou no Bing. 

### 4 - Definir Palavras-Chave para a Sua Página:

``` html
<meta name="keywords" content="tecnologia, programação, HTML">
```

### 5 - Configurar a Compatibilidade de Navegadores Antigos:

``` html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

### 6 - Redirecionamentos

``` html
<meta http-equiv="refresh" content="5; url=https://www.exemplo.com">
```

O primeiro parâmetro é o número de segundos, o segundo é uma URL de redirecionamento.

### 7 - Definir Informações para Redes Sociais:

``` html
<meta property="og:title" content="Título da minha página">
<meta property="og:description" content="Descrição legal para redes sociais">
<meta property="og:image" content="https://www.exemplo.com/imagem.jpg">
```

Você pode configurar a sua página para mostrar o que será visto quando o usuário estiver acessando do Facebook, do WhatsApp, do Telegram ou de qualquer outra Rede Social.

### 8 - Impedir Indexação

``` html
<meta name="robots" content="noindex, nofollow">
```

### 9 - Impedir Potenciais Ataques

``` html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
```

É muito provável, que você já saiba o que é um script ou um estilo, correto? Dadas essas informações, é exatamente por isso que utilizamos a CSP. A função dela é bloquear os potenciais Cookies de terceiros que tendem a prejudicar o funcionamento da sua página Web ou até mesmo tentam roubar informações confidenciais, como Cookies ou Tokens de Acesso. 

Minha recomendação é que a partir de agora vocês já tomem isso com vocês e que passem a bloquear os potenciais scripts maliciosos em suas páginas Web. 

### 10 - Autor

Podemos por meio dos metadaados informar quem criou de fato aquela página Web:

``` html
<meta name="author" content="Gustavo da Silva Oliveira">
```

## E quanto à Tag `title`? ✒️

A função da tag `title` além de estar relacionada com a questão de SEO ela também está relacionada com uma boa experiência de usuário. Seu título deve resumir bem o que a sua página se propõe a fazer e ao mesmo tempo, ele é importante para potencializar a sua experiência de usuário. Certamente, você já viu um site que tinha a determinada estrutura:

1. Página Inicial
2. Sobre Nós
3. Contato

A partir de agora, você já pode incluir alguns bons títulos para cada uma dessas páginas:

``` html
<title>Página Inicial</title>
```

É importante que o título da página reflita o conteúdo que está presente dentro de sua página, mesmo em momentos onde o usuário comete erros dentro do seu site, isso ajuda a manter seu site funcional e acessível para pessoas que sofrem algum tipo de deficiência:

``` html
<title>Página Inicial - Erro - Formulário de Contato</title>
```

Mais para frente, num curso de JavaScript, explicarei para vocês um pouco mais sobre o funcionamento e a alteração da nossa tag de títulos. 

## Muito bom né? 😁

Meta descrições são um recurso extremamente eficaz para que você possa escrever uma página Web com eficiência e qualidade. A lição de casa para vocês é simples: Colocarem uma imagem legal para o seu site nas redes sociais, criarem um título e uma descrição que contenha até 180 caracteres e implementar a Content Secure Policy.