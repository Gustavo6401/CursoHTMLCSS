# Inserindo Imagens no HTML

Certamente, a maioria dos sites que você olha e que acha bonito utilizam imagens na página, correto? É exatamente por isso que hoje vou te ensinar como você pode não apenas inserir imagens em sua página Web, como também a redimensionar as imagens para que você possa pegar as imagens de um tamanho ideal, além disso, veremos como redimensionar uma imagem.

## Mas Gustavo, Por que Redimensionar uma Imagem? 🤔

Bom, nosso maior gasto sem sombra de dúvidas são serviços em nuvem, exatamente por isso que eu acho que a melhor ideia seria redimensionar uma imagem de acordo com o dispositivo do usuário, imagine que seu site é um sucesso e que você recebe milhões de visitantes por mês, você sabia que em serviços como o AWS e o Azure você paga inclusive pela transferência de dados? Um arquivo de 2 MB pode não parecer muito para o seu armazenamento interno, porém, quando se fala sobre servidores a situação é bem diferente. Geralmente, na Web, as imagens são projetadas para terem entre 600 e 400 pixels de largura justamente por isso! Uma imagem de 600 pixels por exemplo pode ocupar um espaço de por exemplo uns 100 KB. Voltando à questão da transferência de dados, imagine que 1 milhão de usuário acessem seu site no mês, desses 1 milhão, se você for expôr a imagem de 2MB, sua transferência de dados será de 2TBs por mês. Num cenário otimista, isso geraria um custo de cerca de US$ 225,00. Enquanto isso, ao transferir a imagem de 600 pixels e 100KB, você teria uma economia de 20x, gastando apenas US$ 11,00. É exatamente por isso que o nosso objetivo aqui é de redimensionar a imagem. 

Para redimencionarmos, utilizaremos um aplicativo chamado Gimp, o objetivo é tornar que tudo fique da forma mais funcional possível e econômica para você desenvolvedor Web. 

O Gimp pode ser baixado pelo seguinte Link: [Download Gimp](https://www.gimp.org/downloads/)

Nosso objetivo é que nossas imagens tenham no máximo 600 pixels de largura. Para isso, farei a modelagem dessa imagem aqui:

![Bonequinho de Palito](imgs/9.1%20-%20Bonequinho%20de%20Palito.png)

### Instalando o Gimp 🎨

#### Primeiramente, clique em Download direto:

![Download Gimp](imgs/9.2%20-%20Download%20Gimp.jpeg)

#### 2 - Clique em Instalar Só para Mim:

![Clique em Instalar Só Para Mim](imgs/9.3%20-%20Instalar%20Só%20para%20Mim.png)

#### 3 - Clique em Instalar:

![Clique em Instalar](imgs/9.4%20-%20Clique%20em%20Instalar.png)

#### 4 - Inicie o GIMP:

![Inicie o GIMP](imgs/9.5%20-%20Inicie%20o%20GIMP.png)

### E agora que Instalamos, Começaremos a Dimensionar a Imagem 🖼️

Primeiramente, quero que a nossa imagem tenha as seguintes larguras: o Tamanho original, 600px, 400px e 300px de largura. 

#### 1 - Abra o Gimp.

Após abrir o GIMP, sua tela deve estar da seguinte forma:

![GIMP - Página Inicial](imgs/9.6%20-%20Página%20Inicial%20do%20Gimp.png)

#### 2 - No canto Superior Esquerdo, Clique em Arquivo:

![Arquivo](imgs/9.7%20-%20Clique%20em%20Arquivo.png)

#### 3 - Clique em Abrir:

Clique em Abrir e vá até o diretório que você deseja.

![Abrir](imgs/9.8%20-%20Clique%20em%20Abrir.png)

#### 4 - Clique em Imagem:

![Imagem](imgs/9.10%20-%20Imagem.png)

#### 5 - Redimensionar Imagem:

![Redimensionar Imagem](imgs/9.11%20-%20Redimensionar%20Imagem.png)

#### 6 - Digite a Altura e a Largura:

Digite a Largura e a Altura desejadas, quando você mexe na largura, para que a sua imagem não fique estranha o GIMP automaticamente mexe na altura também, isso faz com que a sua imagem fique bonita mesmo que em resoluções menores.

![Digite a Largura](imgs/9.12%20-%20Digite%20a%20Altura%20e%20a%20Largura%20Desejadas.png)

#### 7 - Por Fim, Clique em Redimensionar:

![Clique em Redimensionar](imgs/9.13%20-%20Clique%20em%20Redimensionar.png)

#### 8 - Clique em Arquivo:

![Arquivo](imgs/9.14%20-%20Clique%20em%20Arquivo.png)

#### 9 - Clique em Exportar Como:

![Exportar Como](imgs/9.15%20-%20Clique%20em%20Exportar%20Como.png)

#### Pronto!

#### Exercício:

Repita o processo com as resoluções de 400 e 300 pixels de largura.

## Exibindo a Imagem em Nossa Página.

Após tudo o que fizemos, exibir uma imagem no HTML é algo relativamente simples, nós podemos fazer isso por meio da tag img, uma tag dedicada a exibir exatamente algumas imagens em uma página Web, a exibição é muito simples:

``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagens no HTML</title>
</head>
<body>
    <img src="image.png" />
</body>
</html>
```

Viu como é simples? com uma simples tag nós conseguimos exibir qualquer imagem em nosso site.

**Ah Gustavo, a Imagem Está Grande em Meu Site 😬**

Sem problemas, existe uma forma de lidar com esse tipo de imagens no HTML!

Dentro da tag img e até mesmo no CSS nós podemos definir propriedades para a altura e para a largura da imagem:

``` html
<img src="image.png"
        width="600"
        height="338" />
```

Como pode perceber, a imagem ficou visivelmente mais funcional e a página está menos poluída, a palavra width é a palavra inglesa para "largura" e height para "altura". 

## Exibindo Diferentes Imagens para Diferentes Dispositivos 📱💻🖥️

Como sabemos, celulares e computadores possuem resoluções diferentes, com isso, nós podemos redimensionar as imagens por meio de regras CSS ou até mesmo o HTML moderno nos oferece um recurso que permite enviarmos sob demanda uma imagem para o usuário de acordo com o dispositivo dele. Isso pode ser feito por meio do parâmetro `srcset` e do parâmetro sizes:

``` html
<img 
    src="image-300px.png"   
    srcset="
        image-300px.png 300w,
        image-400px.png 400w,
        image-600px.png 600w,
        image.png 1280w
    "
    sizes="
        (max-width: 400px) 300px,
        (max-width: 600px) 400px,
        (max-width: 1279px) 600px,
        1280px
    "
    alt="Imagem responsiva"
/>
```

O nome disso é responsividade, sejamos sinceros também, seu site e seu bolso agradecem e muito! 

### Mas Gustavo, Esse Site Ficou Complicado, Ajuda a Entender! 😶‍🌫️

Então eu vou explicar linha a linha para que vocês entendam. A primeira coisa que eu fiz foi criar várias imagens com nomes bem auto-explicativos, basicamente eu peguei aquela imagem do bonequinho de palitos e recriei ela em diferentes tamanhos, especialmente para caber em cada dispositivo e para que eu não tenha que pagar um absurdo em transferência de dados. 

Após criar esses arquivos, deixei todos em nomes muito auto-explicativos como image-300px.png e image-400px.png. O objetivo é representar a quantidade de pixels em largura que cada imagem ocupa. Como visto anteriormente, eu coloquei essas pastas ao lado do meu arquivo `index.html`:

![Imagens](imgs/9.16%20-%20Pasta%20com%20as%20Imagens.png)

Basicamente o que eu fiz foi importar cada uma dessas imagens em meu site normalmente. 

``` html
<img 
    src="image-300px.png"   
    srcset="
        image-300px.png 300w,
        image-400px.png 400w,
        image-600px.png 600w,
        image.png 1280w
    "
    sizes="
        (max-width: 400px) 300px,
        (max-width: 600px) 400px,
        (max-width: 1279px) 600px,
        1280px
    "
    alt="Imagem responsiva"
/>
```

Basicamente, esse número ao lado do arquivo é uma forma de informar ao navegador a largura da imagem. 

### Mas Gustavo, e Quanto aos Sizes? 🤔

Os sizes possuem uma filosofia muito parecida, eles são responsáveis pela forma que a imagem será exibida na tela 

``` html
<img 
    src="image-300px.png"   
    srcset="
        image-300px.png 300w,
        image-400px.png 400w,
        image-600px.png 600w,
        image.png 1280w
    "
    sizes="
        (max-width: 400px) 300px,
        (max-width: 600px) 400px,
        (max-width: 1279px) 600px,
        1280px
    "
    alt="Imagem responsiva"
/>
```

Nesse contexto, quando a tela tiver até 400px, a imagem a ser renderizada será a de 400px e ela ocupará 300 pixels na tela, se o seu dispositivo possuir 600 pixels de largura, a imagem vai ocupar 400 pixels e sinceramente, se a sua tela tiver mais que 1200 pixels a imagem vai ocupar a tela inteira, claro que vou ajustar para que isso não aconteça e para que a imagem tenha no máximo 1280 pixels como ela foi feita para ser feita.

``` html
<img 
    src="image-300px.png"   
    srcset="
        image-300px.png 300w,
        image-400px.png 400w,
        image-600px.png 600w,
        image.png 1280w
    "
    sizes="
        (max-width: 400px) 300px,
        (max-width: 600px) 400px,
        (max-width: 1279px) 600px,
        1280px
    "
    alt="Imagem responsiva"
/>
```

## Bom, Temos Muitas Imagens, Como Lidar Com Isso? 😔

A melhor forma de lidar com essas imagens é colocar todas elas em uma pasta separada, a importação delas é extremamente simples, e a partir daí vocês já vão aprendendo a organizar arquivos CSS:

Primeiro, peguei as imagens todas e transferi para a pasta imgs:

![Pasta Imagens](imgs/9.17%20-%20Explicação%20Pasta%20img.png)

### Mas Gustavo, e Quanto a Importar Essas Imagens? 🤔

Bom, fazer isso é uma coisa relativamente muito simples, para isso, é só colocar o nome da pasta, da mesma forma como fazemos no Markdown:

``` html
<img 
    src="imgs/image-300px.png"   
    srcset="
        imgs/image-300px.png 300w,
        imgs/image-400px.png 400w,
        imgs/image-600px.png 600w,
        imgs/image.png 1280w
    "
    sizes="
        (max-width: 400px) 300px,
        (max-width: 600px) 400px,
        (max-width: 1279px) 600px,
        1280px
    "
    alt="Imagem responsiva"
/>
```

## Já que o Assunto é Sobre Escovação de Bits. 🪥

Uma excelente forma de economizar dinheiro no seu sistema é o Lazy Loading. Experiência própria pessoal, uma boa parte do público não vai rolar a sua página a ponto de ver todas as imagens presentes nela, como dito anteriormente, experiência própria. Para evitar esse problema, vamos fazer uma eficiente escovação de bits chamada lazy loading. Isso vai fazer com que a sua imagem seja carregada sob demanda, ou seja, quando o seu usuário acessar a parte da página à qual ela está inserida. 

### E como garantir que isso vai acontecer? 🤔

Bom, como esse curso é de HTML inicialmente, eu vou ensinar uma gambiarra para vocês. Abra o arquivo HTML e acima do Componente de Imagens, digitem `br*300`.

Apertem Enter, a partir daí sua página agora possui 300 espaços em branco. 

É relativamente bem simples fazer isso:

![300 BR](imgs/9.18%20-%20Muitos%20Espaços%20em%20Branco.png)

E o Resultado também é bem legal, (ou não) 😁:

![300 BR](imgs/9.19%20-%20Muitos%20BRS.png)