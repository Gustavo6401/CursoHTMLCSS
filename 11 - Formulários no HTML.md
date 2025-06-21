# Formulários no HTML

Os formulários são uma das ferramentas mais importantes do HTML, eles são utilizados em vários contextos, desde a sua compra em algum site de e-commerce até uma postagem em sua rede social favorita. Vamos ficar por dentro da teoria por trás disso, pois mais para a frente, em cursos sobre API Rest e especialmente sobre JavaScript, entenderemos um pouco mais a fundo sobre o funcionamento dos Forms.

# A tag `<form>`

A tag form é a tag que serve para a criação de formulários no HTML, por meio dela, podemos construir toda a parte de interação do nosso usuário com a nossa página Web. O que a torna uma tag extremamente importante. Dentro dela, podemos incluir diversas outras tags, como `<input>`, `<label>`, `<button>`, `<fieldset>`, `<select>`, `<textarea>`, `<fieldset>` e `<legend>`. A partir daí, os dados serão enviados diretamente para o nosso servidor, onde processaremos os dados e os armazenaremos numa base de dados. Esse conceito é extremamente importante para os nossos próximos cursos: armazenamento no Servidor. A arquitetura da Internet é justamente baseada nisso: o usuário baixa os arquivos HTML, CSS e JavaScript diretamente em seu computador e esses arquivos conterão informações como as "portas" ou as rotas para o servidor para que possamos enviar os nossos dados. Uma URL é exatamente isso, um endereço ao qual visitamos na Internet, para que possamos receber os dados do usuário. Você está aqui provavelmente por ter acessado o site YouTube.com, correto? Por conta disso, você recebeu os vídeos diretamente no seu navegador.

Mas tenha em mente também que você precisa enviar dados, senão, o YouTube fica chato, não é mesmo? É exatamente por isso que existe a tag `form`, para que possamos enviar os nossos dados, nossas imagens, vídeos e absolutamente tudo até o servidor. 

## Mas Gustavo, como esse processo é feito? 🤔

Dentro do Form, esse processo é feito utilizando um atributo chamado `action` e um atributo chamado `method`. O atributo `action` tem a função de determinar o local para onde vamos enviar os nossos dados. O servidor utilizará uma linguagem de programação e por meio dela, fará o processamento e download dos nossos dados. Esse é o nosso método de entrada de dados. Quando estamos falando sobre o atributo chamado `method`, estamos falando justamente sobre a forma como esses dados serão enviados. O atributo chamado `method` possui dois valores possíveis: GET e POST. GET determina que os dados devem ser enviados diretamente na URL e POST determina que os valores devem ser ocultos da URL, o que é excelente especialmente para dados pessoais, como e-mail e senha. 

``` html
<form action="" method="post">
    <label for="nome">Nome</label>
    <input type="text" id="nome" name="nome" placeholder="Seu Nome" />

    <button>Cadastrar Dados.</button>
</form>
```

Galera, eu tenho planos de que no futuro, que a gente possa consumir esses dados aos quais estamos criando aqui por meio de uma API Rest em C#, mas para isso, pretendo ensinar para vocês Bancos de Dados SQL Server, Asp.Net Core e JavaScript para que possamos nos aprofundar no tema. Se tudo der certo, será um conteúdo bem interessante. 

## Inputs e Tipos de Campos.

Imagino que você deva ter se perguntado: 🤔 Um, então para isso, precisamos finalmente criar uma página Interativa, onde temos campos aos quais podemos digitar qualquer valor, correto? E você não poderia estar mais certo! Essa é a função das nossas tags `<input>`, `<select>` e `<textarea>`. Tags essas em que o usuário possa digitar e enviar dados diretamente para o nosso servidor.

Nós podemos criar inputs de diversas formas possíveis com os mais diversos valores, enviando desde dados como nome e senha, até cores e imagens! Mostrarei para vocês cada um dos atributos `type`. O nome de cada um dos tipos é bastante auto-explicativo, eu garanto para vocês!

### Tipos de Caracteres.

| Tipo        | Função                                                           |
| ----------- | ---------------------------------------------------------------- |
| text        | Tipo padrão, voltado para strings normais.                       |
| password    | Voltado para senhas, os caracteres permanecem ocultos.           |
| email       | Voltado para campos de e-mail e inclusive exige um arroba @      |
| search      | Voltado para permitir que os usuários façam buscas em sua página |
| tel         | Voltado para dados de Telefones                                  |
| url         | Recebe URLs.                                                     |

Esses tipos de caracteres podem utilizar diversos tipos de texto, como senhas, telefones, urls etc. Eles também podem ser validados por meio de diversos valores, como `required`, `maxlength`, `placeholder` e `pattern.`

| Tipo           | Função                                                                   |
| -------------- | ------------------------------------------------------------------------ |
| required       | Mostra que o preenchimento do input é obrigatório.                       |
| maxlength      | Indica o tamanho máximo de caracteres no input.                          |
| placeholder    | Coloca um texto simples enquanto seu input estiver vazio.                |
| pattern        | Insere um Regex diretamente no HTML                                      |

A partir daqui, conseguiremos validar e criar inputs maduros e consistentes no HTML. 

### Números e Datas

| Tipo           | Função                                                                   |
| -------------- | ------------------------------------------------------------------------ |
| number         | Número simples começando a partir do zero.                               |
| range          | Muito semelhante ao tipo number utilizando min e max, mas é deslizante   |
| date           | Voltado para campos de data.                                             |
| time           | Voltado para campos de hora.                                             |
| datetime-local | Possibilita ao usuário selecionar uma data e uma hora.                   |
| month          | Possibilita ao usuário escolher um mês                                   |

Assim como os caracteres, os inputs de tipos numéricos também possuem seus próprios atributos:

| Tipo           | Função                                                                   |
| -------------- | ------------------------------------------------------------------------ |
| min            | Indica o valor mínimo que deve ser exibido no input.                     |
| max            | Indica o valor máximo que deve ser exibido no input.                     |
| step           | É importante para determinar intervalos de valores                       |

### Checkbox

Certamente você se lembrou também de valores booleanos, correto? Como verdadeiro ou falso, maior ou menor de idade, possui deficiência ou não. Pois é, existem inputs igualmente semelhantes! O nome dele é checkbox e o valor enviado para o servidor é sempre verdadeiro ou falso. 

``` html
<label for="maior">Maior de Idade?</label>
<input id="maior" type="checkbox" name="maior" />
```

### Radio Buttons

Cartamente, você também está pensando em alguma forma de cadastrar múltiplas opções pré-definidas, correto? Como é o caso do Sexo ou do Estado do Usuário. Para isso servem os Radio Buttons:

``` html
<label>
    <input type="radio" name="sexo" value="masculino" />
    Masculino
</label>
<label>
    <input type="radio" name="sexo" value="Feminino" />
    Feminino
</label>
```

### Arquivos e Cores

Os inputs também servem para que nós possamos enviar ao servidor arquivos e cores para os usuários. isso pode ser de grande ajudar para que existam alguns tipos de sistemas, tais como as redes sociais ou qualquer tipo de sistema de upload de arquivo. 

``` html
<div>
    <label for="foto">Sua Foto de Perfil</label>
    <input type="file" name="foto" id="foto" />
</div>
```

E quanto às cores, o princípio de utilização é bem parecido:

``` html
<div>
    <label for="favColor">Cor Preferida</label>
    <input type="color" name="favColor" id="favColor" />
</div>
```

### Select

Mas imagine ter que selecionar o estado dessa forma, não é mesmo? Ficaria terrível para o usuário! É exatamente por isso que existe um campo muito semelhante ao input chamado select. 

``` html
<select name="estado">
    <option value="SP">São Paulo</option>
</select>
```

Por meio disso, você poderá simplesmente criar vários e vários campos sem cansar os olhos do usuário. Claro, haverá um trabalho para construir Drop Down Lists, no entanto, o select melhora muito esse trabalho.

### Textarea

E se eu quiser escrever um texto um pouco mais longo? 🤔 Para isso, existe o textarea. Uma ferramenta que possibilita que você escreva um texto multi-linha diretamente em seu navegador. 

``` html
<label>Outras Considerações</label>
<textarea></textarea>
```

### Envio do Formulário e Limpeza do Formulário

O envio do formulário é feito por meio de um botão, ou até mesmo um Input! Exatamente, existe um input com o tipo submit, justamente para isso! Mas para personalizar um pouco mais, criamos um botão do tipo submit para que possamos enviar os dados diretamente do formulário para o servidor. 

``` html
<button type="submit">Cadastrar Dados.</button>
```

Quanto à limpeza do formulário, podemos utilizar o `button` do tipo reset, a função dele é limpar todos os dados previamente preenchidos em nosso formulário. 

``` html
<button type="reset">Limpar Formulário</button>
```

# Label e a Semântica dos Formulários.

As tags label são textos que acompanham o nosso formulário, inicialmente, podemos incluir textos em nossos formulários simplesmente por colocarmos textos comuns, mas isso não ficaria viável, nem tampouco adaptável para deficientes visuais. Por isso, creio que a melhor forma de lidar com esse problema fosse exatamente a utilização da tag label. 

``` html
<label for="nome">Nome</label>
<input type="text" id="nome" name="nome" placeholder="Seu Nome" />
```

O atributo `for` serve que o label seja apontado especialmente para o input com o id chamado `nome`. Isso é necessário para a configuração dos nossos inputs. 

# Fieldsets

Em formulários muito longos, é comum nos depararmos com campos muito diferentes que existem poucas relações entre si, nesse contexto, existem os fieldsets e especialmente o elemento legend.

## Fieldset

Fieldset é uma separação semântica do seu formulário, especialmente das suas partes principais para as suas partes secundárias. 

``` html
<fieldset>
    <label for="nome">Nome</label>
    <input type="text" id="nome" name="nome" placeholder="Seu Nome" />

    <label for="maior">Maior de Idade?</label>
    <input id="maior" type="checkbox" name="maior" />

    <label>
        <input type="radio" name="sexo" value="masculino" />
        Masculino
    </label>
    <label>
        <input type="radio" name="sexo" value="Feminino" />
        Feminino
    </label>
</fieldset>
```

## Legend

Legend é um elemento que serve para indicar para o usuário exatamente cada um desses fieldsets. Como o próprio nome já diz, o elemento serve como uma espécie de legenda para cada um desses campos. 

``` html
<form action="" method="post">
    <fieldset>
        <legend>Dados Pessoais</legend>
        <label for="nome">Nome</label>
        <input type="text" id="nome" name="nome" placeholder="Seu Nome" />

        <label for="maior">Maior de Idade?</label>
        <input id="maior" type="checkbox" name="maior" />

        <label>
            <input type="radio" name="sexo" value="masculino" />
            Masculino
        </label>
        <label>
            <input type="radio" name="sexo" value="Feminino" />
            Feminino
        </label>
    </fieldset>

    <label>Outras Considerações</label>
    <textarea></textarea>

    <fieldset>
        <select name="estado">
            <option value="SP">São Paulo</option>
        </select>
    </fieldset>

    <button type="submit">Cadastrar Dados.</button>
    <button type="reset">Limpar Formulário</button>
</form>
```

Ao abrir o formulário, percebemos que somos capazes de fazer algo muito parecido com o que fazemos em formulários tradicionais, mas 100% no HTML. 

## Finalizando ✅

O objetivo dessa aula foi introduzir vocês aos formulários no HTML e no CSS. Posteriormente, minha meta é justamente criar um curso sobre API Rest em C# e de desenvolvimento Front-End utilizando JavaScript com os conhecimentos mostrados aqui. 

# Fontes:

[Seu Primeiro Formulário](<https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Extensions/Forms/Your_first_form>)

[Tag form](<https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/form>)

[Tag Input](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/input>)

[Tag textarea](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/textarea>)

[Tag select](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/select>)

[Tag label](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/label>)

[Tag fieldset](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/fieldset>)

[Tag legend](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/legend>)