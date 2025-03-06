# O que São as Tags?

As tags são utilizadas no HTML para que possamos abrir e fechar o conteúdo da nossa aplicação, especialmente da seguinte forma:

``` html
<!DOCTYPE html>
<html lang="pt-Br">
    <head>
        
    </head>
    <body>
        
    </body>
</html>
```

O caracter de menor `<` abre uma tag e o caracter maior `>` é responsável por fechar. O objetivo do HTML é manter todo o conteúdo dentro das tags. 

### Tags autônomas

Algumas tags não demandam outra tag para serem fechadas, chamamos essas tags de tags autônomas, exemplos de tags autônomas são `<img />`, `<input />` ou `<link />`.

## E por que utilizamos os símbolos de maior `<` e menor `>`? 🤔

Pense comigo! Se você assistiu ao nosso curso de C# sabe que a linguagem C veio antes, correto? Assim como o HTML não foi a primeira linguagem de marcação existente! 

Antes do HTML, existiu uma linguagem de marcação chamada SGML, o objetivo dela era óbvio: ela era voltada para estruturar grandes volumes de dados, seja numa base de dados ou alguma outra coisa.

O GML foi uma linguagem criada pela IBM especialmente sobre isso e ao invés de servir como estruturação de páginas Web, como o HTML, o GML e o SGML foram utilizados muito mais para facilitar a leitura humana e ao mesmo tempo a leitura das máquinas. Digamos que eu tenha que lidar com um banco de dados ou algo nesse gênero, seria ideal que eu estruturasse os meus dados da seguinte forma:

``` sgml
<documnto>
    <titulo>4 - Tags no HTML</titulo>
    <paragrafo>Oi, tudo bem? Sejam bem-vindos a mais um capítulo do curso do canal escola de programação!</paragrafo>
</documento>
```

## E por que então não usarmos simplesmente SGML? 🤔

O SGML carrega diversos problemas, especialmente porque o nome das Tags SGML é completamente livre e aberto para a criação das pessoas. 

Como eu faria então que um navegador possa entender um pouco mais sobre o que estou escrevendo? Foi nesse contexto que nasceu o HTML e tags como `<p>` ou tags autônomas como `<input />`. Essa imposição de regras do HTML originou ao que conhecemos como Web hoje em dia.

## Lição de casa 🧠📖

A lição de casa de hoje é pesquisar um pouco mais sobre o funcionamento das tags e sobre outras linguagens como Markdown, XML e JSON que também podem servir para marcação.

Agradeço especialmente ao ChatGPT, por ter me ajudado bastante nesse aula, além disso, há muito conteúdo adicional aqui:

[Curso de HTML em uma Hora da Rafaella Ballerini](https://youtu.be/Fhy-5CtVkiM?si=w-IwpFXky707VDn5)
[Curso do Gustavo Guanabara](https://youtube.com/playlist?list=PLHz_AreHm4dkZ9-atkcmcBaMZdmLHft8n&si=w5tH5inHzg9DdOYr)
[O que são Linguagens de Marcação - Thiago Gaelzer](https://thiagogaelzer.com/o-que-sao-linguagens-de-marcacao/)