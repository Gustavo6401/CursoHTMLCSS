# Vídeos no HTML

Certamente, você já pensou como aplicativos como YouTube, Vimeo e até mesmo os sites de conteúdo adulto se popularizaram na Internet e as ferramentas que eles utilizavam. Por conta disso, hoje vou ensinar para vocês uma forma de incorporar vídeos em sua página Web. 

## Tag `<video>` 🎥

A tag `video` é uma tag que permite a incorporação e o download de vídeos diretamente para o seu navegador de forma simples e rápida, sendo sem sombra de dúvidas uma das tags responsáveis pelo Fim do Flash. Essa foi de longe uma das melhores tecnologias suportadas pelo HTML. 

Para colocar um vídeo em sua página Web, você pode fazer algo muito simples, como:

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls></video>
```

Como mostrado anteriormente, o atributo *src* ou *source* é voltado especialmente para que você busque o caminho (relativo ou absoluto) até o arquivo que você deseja importar em seu site. *Width* é voltado para mostrar a largura do componente de vídeo e *controls*, voltado para exibir esses controles, como a barra de progresso, o botão de reprodução e pausa e a quantidade em minutos (ou horas) do vídeo. 

## Principais Atributos da tag `<video>` 🎞️

A tag `video` conta com os seguintes atributos:

### *autoplay*

*autoplay* é um atributo que determina se o vídeo será reproduzido assim que o usuário abrir a página. Alguns navegadores permitem, outros não, digite o seguinte código em sua tag de vídeos:

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls autoplay></video>
```

### *height*

Bastante semelhante ao width, é um atributo focado em determinar a altura do vídeo.

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls height="400"></video>
```

### *loop*

Ao acabar o vídeo, o vídeo voltará a ser reproduzido infinitamente. 

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls loop></video>
```

### *muted*

Determina se o vídeo permanecerá mudo enquanto ele for executado em sua página Web.

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls muted></video>
```

### *poster*

Serve como uma espécie de *Thumbnail* para o seu vídeo, em resumo, será uma espécie de "capa" a ser mostrada enquanto o vídeo não for carregado:

``` html
<video src="videos/Estrutura Básica do HTML.mp4" width="600" controls poster="imgs/Estrutura Básica do HTML.png"></video>
```

### *preload*

Será responsável por mostrar se o componente de vídeo deve ser carregado logo no início da página ou se ele vai ser carregado no começo ou apenas quando o usuário mandar. O vídeo que eu incorporei na página possui aproximadamente 50 MB. Imagine então se você tem uma empresa e o seu site recebe 1 milhão de acessos todos os meses, o custo de transferência de dados será de 50 TB e aproximadamente 5.000 dólares mensais. Pense que agora, apenas metade dos seus usuários rolam a página a ponto de assistir o vídeo, daí você vai e me pergunta: Será que realmente faz sentido tanto dinheiro e tantos recursos gastos na transferência de dados? Eu posso afirmar com clareza que não! É exatamente por isso que temos essa forma de Lazy Loading e até mesmo de Streaming no caso de arquivos pesados. Streaming é algo que requer JavaScript, nesse caso, não vale a pena que eu explique sobre o tema agora.

O atributo *preload* por padrão recebe três valores: 

1. *auto* - Comportamento Padrão, ele indica que o vídeo será baixado junto com o resto da página;
2. *metadata* - Baixa Apenas os Metadados do vídeo, enquanto o resto é baixado sob demanda, no caso, se o usuário acessar a parte da página onde está o vídeo aí sim o vídeo será baixado.
3. *none* - Indica que nem o vídeo nem os metadados serão baixados. 

## Finalizando ✅

O objetivo dessa aula foi dar uma introdução a respeito do funcionamento dos vídeos no HTML5. Diferentemente das imagens, a lição de casa é pesquisarem um pouco sobre o Flash e sobre como ele influenciou o HTML5. Sobre como a Apple praticamente extinguiu o Flash e sobre as origens do HTML5. Formatos de vídeos também são um assunto muito interessante, pesquisem sobre `mp4`, `ogg` e `webm`. Por hoje é só pessoal, claro que deixarei com vocês a excelente documentação do Mozilla que devo lembrar que gosto muito mais que a do W3C que é o consórcio oficial que cuida da Web.

[Tag video](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/video)