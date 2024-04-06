# Mas como a Internet Funciona? 

Antes de tudo, temos que entender como o computador funciona.

## E como o computador funciona?

O computador funciona de uma forma um tanto quanto exótico. Ele funciona com um monte de zeros e uns, ligado e desligado, é como se os dados fossem pequenos circuitos elétricos que alimentam o computador. Cada um desses zeros e uns são um bit. 8 bytes geram um bit.

É importante citar o seguinte: um computador opera de uma forma realmente exótica, pois muitas pessoas tendem a pensar que 1KB por exemplo é 1024 Bytes e não é bem assim. 1 KiloByte por exemplo, nada mais é do que 1024 Bytes. Por que disso? Pense comigo! Assim como o computador opera com uma série de zeros e uns, ele opera na base binária. E vale lembrar que 2 elevado a 10 é igual a 1024, exatamente por isso que 1 KiloByte nada mais é do que 1024 Bytes.

Tabela de conversão:

| Valor | Quantidade |
| -------- | -------- |
| 1 Byte | 8 bits |
| 1 KiloByte | 1024 Bytes |
| 1 MegaByte | 1024 KiloBytes |
| 1 GigaByte | 1024 MegaBytes |
| 1 TeraByte | 1024 GigaBytes |

### Detalhe: Dados de Transmissão

Em placas de Rede e para medir a velocidade de conexão com a Internet, nós não checamos a velocidade por meio de Bytes, mas de Bits. Por conta disso, temos que nos lembrar que devemos tomar MUITO cuidado quando medimos a velocidade da Internet.

MB em maiúsculo - MegaByte
Mb com o b em minúsculo - Megabit.

# Comunicação Entre Computadores

Uma rede pequena ou uma LAN é um conjunto de computadores conectados por meio de um switch. Os switchs nada mais são do que pequenos aparelhos com um monte de cabos que tem por objetivo fazer com que os computadores possam se comunicar entre si. 

Digamos que tenhamos uma rede pequena com apenas 7 computadores, quando o computador um por exemplo quer se comunicar com o computador 3, ele simplesmente vai enviar uma mensagem para o roteador, dentro dessa mensagem vão ter alguns dados bem importantes, como **a hora da mensagem**, **a data da mensagem**, **o computador mensageiro** e o **computador de destino**. Essas informações serão importantes para que o roteador entenda para onde ele tem que enviar essa comunicação.

# Como Funciona a transmissão de dados por meio da Internet - Roteadores

No meio da Internet a comunicação ocorre de uma forma muito parecida como no funcionamento das LANs, mas ao invés de você mandar um pacote diretamente para outro computador no meio da rede, você vai enviar diretamente para a Internet. Por isso, o switch vai pegar esses dados da mensagem ou do pacote que você está enviando e direcionar esse pacote para o roteador.

Antes de começarmos a fazer essa transmissão dos nossos dados para a Internet, primeiro nós temos que traduzir esses dados. O computador não consegue transferir diretamente seus dados por meio da Internet. Por isso, os dados que você envia do seu celular ou do seu computador passam por um pequeno aparelho chamado Modem. O processo de traduzir as ondas elétricas que fazem seu computador funcionar é para a Internet, ou seja, para o meio telefónico é chamado de Modulação. O processo de recebimento de dados e de tradução desses dados é chamado de demodulação.

# Afinal de Contas, o que é a Internet?

Certamente, agora você deve estar se perguntando: O que é a Internet? Pois bem, agora vou de fato explicar essa dúvida. A Internet nada mais é do que a conexão entre um roteador e outro roteador, a conexão entre um serviço e outro. A conexão é 100% decentralizada, justamente para balancear a carga dos computadores dentro da Internet. O objetivo da Internet ser decentralizada é justamente para que caso haja algum problema em algum rotador que esse problema não impacte nenhuma rede.

Deixo aqui uma lição para vocês: pesquisar como são feitas as conexões internacionais e como funcionam os cabos marítimos. Muitas das informações que temos em mãos estão acessíveis por um servidor dos Estados Unidos. O acesso não é feito apenas via Wireless ou via satélite, o acesso muitas vezes é feito por meio de cabos de rede que passam no fundo do mar. Eu mesmo tenho um site hospedado numa máquina do AWS dos Estados Unidos o acesso àquela máquina só é possível graças ao que a Internet se transformou.

A única forma de acabar de fato com a Internet é derrubar todos os computadores, todos os roteadores e todos os switchs ao mesmo tempo. 

Logo, podemos perceber o seguinte: **A Internet é a Rede das Redes**

# Como acessamos um site? 

Antes de tudo, eu gostaria de fazer uma pergunta para vocês, principalmente para vocês que acompanharam a aula passada: como acessamos um site? Melhor ainda: como os sites se diferenciam? Se você está pensando no número IP pois bem, você está certo, mas ao mesmo tempo você está errado. Ao desligar o seu computador ou o seu modem de Internet o seu computador muda de endereço IP. Imagine a bagunça que seria você tentar se comunicar com um DataCenter do YouTube e não poder se comunicar porque o DataCenter mudou de endereço IP, isso tornaria a Internet praticamente inviável não tornaria? Pensando nisso, começaram a surgir os Domain Name Service, serviço de nome de domínio, os chamados endereços DNS, são eles que permitem que você simplesmente Digite a URL do YouTube ou no caso do último projeto que desenvolvi um [www.alisonsilvapoeta.com.br](www.alisonsilvapoeta.com.br) e consigam acessar normalmente esse site. Recomendo que pesquisem um pouco mais sobre DNS, com certeza esse é um tema extremamente interessante.

Basicamente, endereços DNS traduzem nomes compreensíveis para meros humanos em endereços IPv4 ou IPv6. O computador não entende letras, apenas bits e mais bits.

# E como nós chegamos ao site que queremos acessar?

Os dados após chegarem no seu roteador são enviados por meio daquele cabo de Internet ao servidor do seu provedor de Internet. O provedor de Internet, no caso o meu a Vivo ajuda a indicar a melhor rota para se chegar ao servidor onde você quer enviar ou receber dados. Eu por exemplo, tenho uma aplicação hospedada no Amazon AWS de um amigo meu lá nos Estados Unidos, basicamente o roteador vai pegar os dados que quero transferir para aquela aplicação e decidir qual a melhor forma de se fazer isso. Esse é exatamente o trabalho de um provedor de Internet, escolher a melhor rota para transferirmos os nossos pacotes. Cada uma dessas empresas, contam com uma informação importante chamada **Tabela de Roteamento**, a função da **Tabela de Roteamento** é verificar qual rota é a mais viável para nos comunicarmos com outro ponto da Internet e verificar a viabilidade dessa rota.

A forma como os dados transacionam remete muito à forma como nós transacionamos dentro da cidade. Imagine que você more num lugar onde você possa ir para o trabalho de carro, moto, ônibus ou trem. O roteador funciona exatamente como você, ele vai escolher a melhor rota e o melhor caminho para se chegar ao seu destino. Num dia que estivermos com as ruas congestionadas provavelmente ele vai escolher ir de trem. Num dia de feriado em que os ônibus estiverem vazios ele vai de ônibus, até porque você pode economizar muito mais tempo indo de ônibus ao invés de ir de carro se você parar para pensar, visto que você pode jogar, ou até mesmo assistir as minhas aulas no ônibus.

Ah Gustavo, mas o meu ônibus dá a volta ao mundo. Não interessa! Nem sempre o caminho mais eficiente é o caminho mais rápido. Imagine num dia em que o trem esteja lotado e o trânsito congestionado mas ao mesmo tempo, que você consiga sentar no ônibus em horário de pico. O que em São Paulo é praticamente impossível né? Sem sombra de dúvidas em 90% dos casos, se você for uma pessoa pouco apressada vai compensar ir de ônibus e não de carro ou trem. É por isso que por muitas vezes demora muito para você carregar uma página Web e em outras vezes é realmente rápido carregar uma página. Assim como no trânsito, na Internet acontecem picos de tráfego. Lembre-se: nada na computação é de graça, tudo custa recursos computacionais e recursos de rede o que nós programadores temos que fazer é aproveitar ao máximo cada um desses recursos disponíveis.

## Exemplo claro: transferência de dados para um servidor dos Estados Unidos

Na hora de transferir ou transacionar dados lá para os Estados Unidos, o seu roteador teria a seguinte lógica de funcionamento: suponhamos que você tenha uma aplicação hospedada no Norte da Virgínia lá nos Estados Unidos e que um usuário de São Paulo, SP vai se comunicar com essa aplicação, vamos fazer o passo a passo na prática OK?

Primeiramente, o pacote requisitando acessar aquela aplicação será enviado por meio da Internet, ele sairá do seu computador no primeiro momento em que você digitar o www e der enter. O pacote sairá do seu computador e irá direto para o roteador, que vai transformar o código binário enviado pelo seu computador pessoal em ondas telefónicas. Essas ondas irão para o seu provedor de Internet que terá um aparelho muito semelhante ao seu Modem e ele vai escolher as seguintes opções, todas as opções são meramente ilustrativas, portanto, não precisa ilustrar isso.

| Roteador | A quantos KM |
| -------- | ------------ |
| Rio de Janeiro | 200 KM |
| Cuiabá | 500 KM |
| Belo Horizonte | 300 KM |

Nesse caso, os dados irão diretamente para uma sede da Vivo lá no Rio de Janeiro. 

| Roteador | A quantos KM |
| -------- | ------------ |
| Miami - Via Marítima | 2000KM |
| Belo Horizonte | 100 KM |

Como sabemos, as vias marítimas envolvem fibras óricas, logo, isso torna muito mais fácil a transação de dados. Mas suponhamos que um monte de gente queira comprar alguma coisa lá no Mercado Livre e essas pessoas estão acessando diversos sites hospedados nos servidores ali em Belo Horizonte o que torna o caminho mais curto menos eficiente do que transacionar dados via linha marítima. Logo, Os dados vão direto para um roteador em Miami. Lembrem-se: rota mais rápida e eficiente.

| Roteador | A quantos KM |
| -------- | ------------ |
| Carolina do Sul | 200KM |
| Tennesse | 300KM |
| Texas | 1000 KM |

Novamente, meu pacote de dados será enviado para a Carolina do Sul, que logicamente é o lugar mais próximo. A partir daí, meu pacote foi para um dos roteadores da Amazon lá do Norte da Virgínia seguindo com sucesso e exibindo a página Web que finalmente eu desenvolvi:

![Exemplo: Meu portfólio](<2.1 - Imagem de Exemplo.png>)

Essa página foi colocada apenas como um exemplo do tipo de página que vocês vão desenvolver com esse curso, a página é hospedada no Github Pages. Mas isso é um exemplo unicamente didático.

Isso é feito em questão de milissegundos, é muito rápido!

# Transferência de Dados

A transferência de dados na Internet é uma coisa extremamente interessante. Ao invés de você conseguir acessar necessariamente uma página Inteira, quando você faz o download ou o acesso à uma imagem por exemplo, você consegue ir acessando ela aos poucos. Se você conversar com uma pessoa que tem mais de 40 anos, facilmente essa pessoa vai falar sobre a Internet Discada. O princípio é quase o mesmo, o servidor vai cortando a informação em pequenos pacotes para que ela chegue até você.

Futuramente, talvez em cursos de JavaScript, vamos entrar no mérito das Streamings que são extremamente interessantes. Onde os dados são carregados aos poucos e disponibizados sob demanda. Se você ainda não entende de HTML não recomendo que você pesquise sobre isso ainda. Ao final do Curso de JavaScript acredito fazer muito mais sentido.

Para resumir o que que é um Streaming, pense em um vídeo no YouTube. O vídeo nunca é totalmente disponibilizado para você, ele é disponibilizado aos poucos para você, isso é uma forma de streaming. Isso funciona com vídeos, músicas, enfim. O Streaming vai funcionar dependendo da qualidade da Internet que você vai ter. É aqui que entram os chamados servidores que nada mais são do que máquinas muito mais potentes e rápidas do que a sua máquina que tem por objetivo armazenar dados, vídeos, imagens, enfim...

Imagine por exemplo o YouTube. O YouTube é um grande exemplo de streaming de vídeos. E é bem lógico pensar que o YouTube não tem apenas um servidor, o YouTube tem vários servidores, inclusive alguns deles aqui em São Paulo onde estou gravando esse vídeo. O YouTube replica os vídeos para cada um desses servidores afim de que caso um servidor caia o serviço todo não caia. Isso se chama na computação de balanceamento de carga. 

# Privacidade na Internet

Não entrarei em detalhes muito técnicos aqui, mas existem diversas formas de aumentar a sua privacidade e a segurança na Internet, imagine o seguinte cenário: você quer fazer uma compra mas você tem medo que alguém acabe interceptando dados importantes, como é o caso de dados de cartão de crédito, conta bancária, enfim. A maioria dos sites hoje em dia vem com aquele cadeadinho no navegador que indicam que a conexão estabelecida entre a sua máquina e o servidor Web é uma conexão segura. O que significa que os dados de cartão de crédito são encriptados na sua máquina e quando eles chegam de fato ao servidor eles são desencriptados. Isso garante a segurança dos seus dados. O nome dessas conexões são conexões HTTPS e elas são muito importantes e tornam muitas vezes mais seguro fazer uma compra na Internet do que comprar fisicamente. 

Saber disso é utilidade pública visto que as tiazonas de Facebook costumam adorar falar merdas. Vi um comentário outro dia de uma velha que disse que não tem nada a esconder. Se você não tem nada a esconder velha, manda aí nos comentários do vídeo os números do seu cartão. Manda também o código de segurança, o nome na frente e a data de expiração. Estou querendo comprar um MacBook se você fizer isso você vai facilitar o meu trabalho. 

Se você caro amigo leigo ou amigo desenvolvedor quiser se aprofundar no fantástico mundo da privacidade, recomendo que você comece estudando coisas como WANs, VPNs e a lógica de funcionamento desse tipo de aplicação. Tenho certeza que isso será bem prazeroso e acredito que todo o usuário minimamente inteligente, estou claramente excluíndo velhas que falam merdas no Facebook deveria ter acesso a VPNs.

Não sei se isso vai de fato ser algo importante para os próximos tópicos do nosso curso de HTML, mas eu precisava expressar a minha revolta quanto a certas falas. 

# Como nos Comunicamos com Outras Partes do Mundo?

Nos comunicamos por meio de Serviços Provedores de Internet. Temos que entender que existem provedores locais, regionais e globais. Os provedores locais são pequenos e se interessam em conectar um bairro ou até mesmo uma cidade pequena. Os regionais pretendem conectar um país ou um Estado como São Paulo. E os Globais que serão responsáveis por esses cabos de Infraestrutura que mostrei para vocês, eles conectam países ou continentes. 

Voltando aquele exemplo da comunicação com um servidor dos Estados Unidos, você mandaria um pacote para o provedor do seu bairro, esse pacote seria enviado para o provedor da sua cidade ou estado e depois para o provedor do seu país, que enviaria para outro provedor lá nos Estados Unidos, que enviaria para um provedor na Carolina do Sul e que enviaria para o Norte da Virgínia. Recomendo que pesquisem mais sobre provedores se tiverem curiosidade sobre isso, é um tema realmente interessante. 

Eles existem especialmente para manter a Internet funcional e evitar que a complexidade na Internet aumente muito.

A Internet é tão interessante que por mais que a gente tente se conectar a um site hospedado lá nos Estados Unidos, ele carregou facilmente e em questão de segundos. Mais interessantes, são as técnicas que as empresas utilizam para aumentar a experiência de usuário. Sabe a sua Internet da Vivo? Então, muitas vezes ela é conectada diretamente com os roteadores e servidores do Google, para que a experiência de assistir YouTube seja uma esperiência extremamente amigável. 

# O futuro da Internet

Existem empresas hoje em dia, trabalhando todo o santo dia para tornar a Internet cada vez mais acessível, recomendo pesquisarem sobre conexões à Internet via Satélite, o projeto Loon da Google e o projeto Starlink da SpaceX, todos essas são excelentes projetos que vão ajudar a difundir a internete cada vez mais.

# Conclusão

A Internet é sem sombra de dúvidas fascinante e acima de tudo, a Internet não é das empresas, nem tampouco dos governos, mas de todo o povo. 

Caso você queira aprender mais sobre o tema, deixarei alguns links para alguns vídeos que serviram de referências para mim. Ao mesmo tempo, pesquise sobre Peering, WANs, VPNs e privacidade caso você queira se aprofundar no assunto.

Muito obrigado pela atenção.

# Bibliografias:

[Curso em Vídeo - Como a Internet Funciona](https://youtu.be/nlO5hySqJFA?si=yUVVkCsw9GICvXaT)
[Vox - How Internet Works](https://youtu.be/TNQsmPf24go?si=P0W2k6WFVOQD3Q0h)
[FreeCodeCamp - How does the Internet Work](https://youtu.be/zN8YNNHcaZc?si=P4syj8Pg8vO0WI_W)
[Fábio Akita - Como a Sua Internet Funciona | Introdução a Redes Parte 3](https://youtu.be/gcv5hXyTcIo?si=1AVIiczbRCGaahK4)