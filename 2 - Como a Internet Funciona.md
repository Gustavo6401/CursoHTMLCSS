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

# Como Funciona a transmissão de dados por meio da Internet

Antes de começarmos a fazer essa transmissão dos nossos dados para a Internet, primeiro nós temos que traduzir esses dados. O computador não consegue transferir diretamente seus dados por meio da Internet. Por isso, os dados que você envia do seu celular ou do seu computador passam por um pequeno aparelho chamado Modem. O processo de traduzir as ondas elétricas que fazem seu computador funcionar é para a Internet, ou seja, para o meio telefónico é chamado de Modulação. O processo de recebimento de dados e de tradução desses dados é chamado de demodulação.

# Como acessamos um site? 

Antes de tudo, eu gostaria de fazer uma pergunta para vocês, principalmente para vocês que acompanharam a aula passada: como acessamos um site? Melhor ainda: como os sites se diferenciam? Se você está pensando no número IP pois bem, você está certo, mas ao mesmo tempo você está errado. Ao desligar o seu computador ou o seu modem de Internet o seu computador muda de endereço IP. Imagine a bagunça que seria você tentar se comunicar com um DataCenter do YouTube e não poder se comunicar porque o DataCenter mudou de endereço IP, isso tornaria a Internet praticamente inviável não tornaria? Pensando nisso, começaram a surgir os Domain Name Service, serviço de nome de domínio, os chamados endereços DNS, são eles que permitem que você simplesmente Digite a URL do YouTube ou no caso do último projeto que desenvolvi um [www.alisonsilvapoeta.com.br](www.alisonsilvapoeta.com.br) e consigam acessar normalmente esse site. Recomendo que pesquisem um pouco mais sobre DNS, com certeza esse é um tema extremamente interessante.

# E como nós chegamos ao site que queremos acessar?

Os dados após chegarem no seu roteador são enviados por meio daquele cabo de Internet ao servidor do seu provedor de Internet. O provedor de Internet, no caso o meu a Vivo ajuda a indicar a melhor rota para se chegar ao servidor onde você quer enviar ou receber dados. Eu por exemplo, tenho uma aplicação hospedada no Amazon AWS de um amigo meu lá nos Estados Unidos, basicamente o roteador vai pegar os dados que quero transferir para aquela aplicação e decidir qual a melhor forma de se fazer isso. 

A forma como os dados transacionam remete muito à forma como nós transacionamos dentro da cidade. Imagine que você more num lugar onde você possa ir para o trabalho de carro, moto, ônibus ou trem. O roteador funciona exatamente como você, ele vai escolher a melhor rota e o melhor caminho para se chegar ao seu destino. Num dia que estivermos com as ruas congestionadas provavelmente ele vai escolher ir de trem. Num dia de feriado em que os ônibus estiverem vazios ele vai de ônibus, até porque você pode economizar muito mais tempo indo de ônibus ao invés de ir de carro se você parar para pensar, visto que você pode jogar, ou até mesmo assistir as minhas aulas no ônibus.

Ah Gustavo, mas o meu ônibus dá a volta ao mundo. Não interessa! Nem sempre o caminho mais eficiente é o caminho mais rápido. Imagine num dia em que o trem esteja lotado e o trânsito congestionado mas ao mesmo tempo, que você consiga sentar no ônibus em horário de pico. O que em São Paulo é praticamente impossível né? Sem sombra de dúvidas em 90% dos casos, se você for uma pessoa pouco apressada vai compensar ir de ônibus e não de carro ou trem. É por isso que por muitas vezes demora muito para você carregar uma página Web e em outras vezes é realmente rápido carregar uma página. Assim como no trânsito, na Internet acontecem picos de tráfego. Lembre-se: nada na computação é de graça, tudo custa recursos computacionais e recursos de rede o que nós programadores temos que fazer é aproveitar ao máximo cada um desses recursos disponíveis.

# Transferência de Dados

A transferência de dados na Internet é uma coisa extremamente interessante. Ao invés de você conseguir acessar necessariamente uma página Inteira, quando você faz o download ou o acesso à uma imagem por exemplo, você consegue ir acessando ela aos poucos. Se você conversar com uma pessoa que tem mais de 40 anos, facilmente essa pessoa vai falar sobre a Internet Discada. O princípio é quase o mesmo, o servidor vai cortando a informação em pequenos pacotes para que ela chegue até você.

Futuramente, talvez em cursos de JavaScript, vamos entrar no mérito das Streamings que são extremamente interessantes. Onde os dados são carregados aos poucos e disponibizados sob demanda. Se você ainda não entende de HTML não recomendo que você pesquise sobre isso ainda. Ao final do Curso de JavaScript acredito fazer muito mais sentido.

# O futuro da Internet

Existem empresas hoje em dia, trabalhando todo o santo dia para tornar a Internet cada vez mais acessível, recomendo pesquisarem sobre conexões à Internet via Satélite, o projeto Loon da Google e o projeto Starlink da SpaceX, todos essas são excelentes projetos que vão ajudar a difundir a internete cada vez mais.