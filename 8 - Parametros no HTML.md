# Parâmetros no HTML

Parâmetros são uma parte importante da visibilidade e da leitura do HTML, tanto para o navegador quanto para nós seres humanos, um parâmetro basicamente é uma forma de incluirmos informações no nosso HTML sem necessariamente prejudicarmos o conteúdo. Pense nas configurações de cada componente da tela, elas são importantes, correto? Um exemplo muito claro que não foi visto até agora seria a tag `<img>` que conta especialmente com a importação de uma imagem na página: 

``` html
<img src="../2.1 - Imagem de Exemplo.png"
    width="1342"
    height="3796"/>
```

O objetivo do HTML é muito simples: Apenas o conteúdo no centro, nada fora. 

Um exemplo melhor certamente seriam tags de meta descrições:

``` html
<meta>name=viewport content=width=device-width initial-scale=1.0</meta>
```

Ou pior, ler um código assim:

``` html
<meta "viewport" "width=device-width initial-scale=1.0" />
```

Se você for testar isso na Visual Studio, nem irá funcionar.

Como mencionado anteriormente, muitas vezes os atributos servem como uma configuração para o componente, o que está dentro das tags sempre é o conteúdo. Quando ensinarmos sobre CSS isso ficará cada vez mais claro para vocês.

## História dos Parâmetros ⏳

Antes de entendermos sobre a história dos parâmetros, temos que entender especialmente sobre a história da impressão como um todo. Cada documento possui diversos parâmetros de acordo com o conteúdo presente nele. Por exemplo, certas coisas devem ser pensadas como:

1. Tamanho da Fonte
2. Está em Negrito ou Itálico
3. Cor da Fonte

Os parâmetros nas linguagens de marcação vieram **como uma forma de representar essas características do texto**. É como se o que estivesse dentro da tag fosse o conteúdo e o parâmetro, a característica. Exemplo:

``` html
<h1 class="titulo">Olá, Mundo!</h1>
```

Entre as linguagens que vieram antes do GML como o RUNOFF, isso não poderia ser diferente e o mesmo se aplica ao próprio GML. 

Como citado anteriormente, Tim Berners Lee inspirou-se no SGML para criar os parâmetros e no SGML não era diferente, os parâmetros eram representados de forma muito semelhante ao HTML. 

## Lição de Casa 📖

Pesquisem um pouco sobre como parâmetros eram representados em linguagens mais antigas como o GML e o SGML, usem bastante o ChatGPT e peçam para que ele sugira uma boa fonte para vocês.

Algumas Fontes:

[Raízes das Linguagens de Marcação](<https://cacm.acm.org/research/tracing-the-roots-of-markup-languages/#F2>)

[História do Runoff](<https://bxriver.net/obscure/runoff/>)

[Curso de HTML Gustavo Guanabara](<https://youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n&si=a3PhTqm5Mv-aEqKK>)

[Curso de HTML da Rafealla Ballerini](<https://youtu.be/Fhy-5CtVkiM?si=2oHVY1Rcvm0pkWYQ>)

[Curso de HTML da Free Code Camp](<https://youtu.be/kUMe1FH4CHE?si=YAxL9P07b0CA-h6x>)