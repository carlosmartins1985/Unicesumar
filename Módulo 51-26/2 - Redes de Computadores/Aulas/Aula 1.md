# Aula 1 - Redes de Computadores

*Fundamentos, Protocolos e Comunicação*

Objetivos da aula

**Compreeder o conceito** - Entender o que são redes e com elas funcionam no dia-dia;

**Conhecer os Modelos** - Explorar OSI, TCP/IP e os principais protocolos de comunicação;

**Aplicaçõe**s - Reconhecer os componentes de rede e associa-los a situações reais da TI.

Ao final desta aula, seremos capazes de...

* Explicar o que é uma rede;

* Identificas os principais componentes e topologias;

* Distinguir os modelos OSI  e TCP/IP;

* Reconhecer os protocolos mais utilizados no cotidiano.

O que é uma rede de computadores?

    Qualquer conjunto de dispositivos, sendo computador, tablet, smartphone que esteja conectados e trocando dados temos uma rede de computadores.

    Temos dois conceitos, internet é uma coisa e rede de computadores. Por exemplo, para se ter internet em casa precisamos ter rede de computadores, mas para que computadores se comuniquem não precisamos ter internt. Podemos ter equipamentos transmitindo dados entre si sem ter internet. Nas redes de computadores trocamos dados e compartilhamos recursos.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-03-31%2020-23-53.png)

    Esses dispositivos se comunicam por meios fisicos cabos ou sem fio, wifi, utilizando regras chamadas protocolos. Protocolos são regras que fazer com que um dispositivo no ponta A se comunique a outro dispositivo no ponto B. É como se fosse a linguagem que as máquinas usam para se comunicar. Isso a 60 anos atrás era impossível, pois cada máquina tinha um protocolo diferênte, cada fabricante adotava um protocolo diferênte. Hoje temos o modelo OSI e o modelo TCP/IP que ajudam os dispositivos a se comunicar.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img2.png)

* Empresas utilizam a rede para compartilhar recursos, como impressoras e arquivos;

* Podemos ter aulas online, pois a rede provem comunicação;

* IOT - Lâmpada, máquina de lavar;

* Bluetooth também é uma rede de computadores;

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img3.png)

        O profissional pode atuar em várias áreas, como infraestrutura, cabeamento, proxy, várias áreas, pois hoje qualquer empresa precisa estar conectado a uma rede ou a internet.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img4.png)

    No inicio as redes eram majoritariamente militar, os EUA criaram as redes de computadores para trocar informações a nível militar, isso por conta da disputa espacial.

    Em 1980 foi criada a padronização, para que equipamentos de diversos fabricantes conseguissem trocar informações entre si.

    A popularização começou quando a internet chegou as universidades, e essas controlavam as empresas que forneciam internet, para as residências, por exemplo, essas empresas precisavam ter uma altorização das universidades para o fornecimento de interne. Elas montados provedores, pediam uma conceção para ter um link de dados, e esse link era transmitido para as residências. Fibra ótica é uma tecnologia dos anos 70, que se popularizou na década de 90.

    Em 2000 tivemos a convergencia para o wifi.

IOT, tudo hoje pode estar conectado a internet. Podemos ter um lápis com leitor de movimentos, ou uma roupa que detecta a sua tempetatura corporal.

    Serviços em nuvem como google, amazon, azurre, são servidores que oferecem o serviço de hospedagem e armazenamento para grandes empresas.

Aplicações

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img5.png)

    Podemos acessar dados de qualquer conectados a internet. Uma empresa pode ter uma intranet, que só conecta internamente. Temos também a extranet, que permite que acessamos a rede de uma empresa remotamente, tendo acesso a documentos e recursos.

    E a internet são os vários dispositivos conectados. Quando acessamos a netflix, estamos acessando um servidos que está nos EUA. Algo publicado no Brasil pode ser acessado por alguém no Japão.

    Aplicação distribuida - Hoje não conseguimos fazer um PIX se não tivermos o conceito de aplicação distribuida.

    Podemos ter 10 servidores conectados, se um falhar tem o segundo, se falhar tem outro, isso chamamos de redundancia. Por exemplo, se um servidor estiver recebendo muita carga podemos, através de configuração, dividir a carga de trabalho para outro servidor. 

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img6.png)

**Topologia de rede**

    Irá dizer o contexto de como está arquitetado uma rede em determinado ambiente, como é a distribuição de dados e como é distribuida essa informação.

    O primeiro deles e o mais utilizado é o modelo estrela, que também pode ser representado como em uma linha reta, com conexões para um suit ou um hub, que são concentradores, o cocentrador é um dispositivo que recebe a conexão de vários computadores, que irão trocar dados, hub e suit são dispositivos da topologia estrela.     A vantagem é que se um cair, o outro assume, não prejudicando a rede, podemos conectar vários equipamentos na rede. Atualmente a grande maioria dos computadores estão na topologia estrela.

**Topologia anel**

    Não é mais utilizada, trata-se de um circuito fechado, como por exemplo cinco computadores, onde a informação passa em um único sentido, utilizando uma chave, tokem, para que a informação possa ser passada para o outro computador da rede.

    Todo mundo ouve o conteúdo que foi passado para os demais. Um dado do ponto A para o B, irá passar para os outros também, a informação anda em um único sentido, diferente da topologia estrela que envia a informação para apenas um destinatário.

**Topologia em barra**

    Imagine uma linha com vários dispositivos conectados, a desvantagem é que se o cabo se romper a conexão fica comprometida, pois todos usam o mesmo cabo de comunicação, um único barramento, ainda é usado em tecnologia de câmeras.

**Topologia em malha**

    Onde um dispositivo pode se comunicar com vários ao mesmo tempo, por exemplo, o A pode se conectar com o B, C, D e E, calcula que em uma rede em malha, é o total de dispositivos menos um, se a rede tem 5 dispositivos, cada nó se comunica com 4 dispositivos, um com um link para cada, cada um com 4 ramificações. Por exemplo, em  um reunião, com 3 participantes, podemos montar uma rede em malha, onde cada um poderá se comunicar com o outro e compartilhar recursos de rede. E uma aplicação barata.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img7.png)

    Roteador - Serve para dar uma rota, se queremos acessar o site da netflix, ele irá passar por vários roteadores até chegar ao destino final.

Teste prático no pronpt;

```bash
carlos@cs-ubuntu:~$ traceroute www.google.com
traceroute to www.google.com (142.251.154.119), 30 hops max, 60 byte packets
 1  _gateway (192.168.1.1)  6.360 ms  3.851 ms  3.861 ms
 2  10.85.161.32 (10.85.161.32)  4.050 ms  8.293 ms  8.412 ms
 3  * * *
 4  10.10.0.9 (10.10.0.9)  8.789 ms  8.467 ms  8.639 ms
 5  10.200.0.52 (10.200.0.52)  17.468 ms  17.141 ms  17.576 ms
 6  142.251.154.119 (142.251.154.119)  17.790 ms  15.137 ms  15.133 ms
carlos@cs-ubuntu:~$ 
```

    Aqui temos os roteadores onde a requisição passa até chegar ao servidor do google. Passou por seis roteadores. Pode variar a quantidade de roteadores dependendo do tráfego da rede.

    Pode levar vários passos, dependendo do tráfego na rede. Ou seja a função do roteador é escolher a melhor rota do ponto a ao ponto b.

Switch - Distribuir a internet para vários dispositivos, podendo conter várias portas, para empresas podem ter mais de 20 portas, conseguindo distribuir internet para mais de 20 computadores ao mesmo tempo.

    Access Point - Amplificador de sinal.

Firewall - Barreira, monitora as entradas e saídas da rede, monitora o tréfego, para proteger a rede, saber o que está entrando e o que está saindo.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img8.png)

**Protocolos** 

    São regras, padrões, na qual, indempendento do dispositivo de rede, seja notebook, celular, e indempendente do meio de transmissão, seja fibra ótica, par trançado seguem a mesma regra. São as regras usadas para a conexão entre os dispositivos.

    A padronização é muito importante em uma rede de computadores.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img9.png)

**Cliente-Servidor** 

    Por exemplo, quando acessamos a netflix trata-se de um modelo cliente servidor, onde a minha máquina é a cliente, e a net, tem uma ou várias máquinas servidores que enviam o que estou querendo assistir.

**Peer-to-peer**

    Trata-se de um modelo onde todos os dispositivos são clientes e servidores, exemplo u-torrent, onde minha máquina pode ser cliente e servidor ao mesmo tempo, Pois ao mesmo tempo em que a minha pode compartilhar arquivos pelo torrent, pode também acessar um streaming, como netflix, a assim agir como cliente ao mesmo tempo. Outras aplicações com blockchain, que trocam pares de chaves para fazer transações financeiras com criptomoedas, podendo ser computador um servidor para gerar as chavez, sendo o padrão do bitcoin, permitindo trasações financeiras de maneira confiável. Outro exemplo são chamadas via watsapp e telegram, os dados que trafegam na rede não são visiveis, são criptografados, quando uma mensagem é enviada ela é critpografada, e enviado chavez públicas e privadas, e o dispositivo que recebe a mensagem faz a mesma coisa de forma inversa. Descriptografa a informação recebida. Essa criptografia quem cria é o própio dispositivo smartphone.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img10.png) 

**Comutação de redes**

    E a maneira que os dados podem ser fragmentados e enviados por pacotes, um pacote é quebrado em várias partes, até chegar em binário, e depois é remontado, como se fosse um quebracabeça. Ou seja;

* Quebra a informação em vários pedaços, e vai com outras informações;

* Vai encapsulando até chegar no nível físico;

* Quando chega no físico vai binário pela rede;

* Já no destino é feito o processo inverso até montar os pedaços do arquivo novamente, e receber a informação como foi enviada.

    Esses pacotes quebrados podem ir por vários caminhos, e não necessáriamente por um só roteador, podendo ser por vários roteadores.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img11.png)    Modelo OSI e TCP/IP são modelos que garantem que, independente do fabricante do computador ou da placa de rede, a informação chegue até o destino.

O modelo TCP/IP continua fazendo as mesmas coisas do modelo OSI, porém foi encurtado. Na figura temos as mudanças que foram aplicadas, com alterações nas nomenclaturas. No modelo osi temos 7 camadas, e no modelo tcp temos 4 camadas.

    Quando enviamos uma mensagem, ela parte da camada mais alta, no caso camada de aplicação, percorre até a camada física, e é enviada, chegando ao destino ela faz o processo inverso, chega pela camada física e percorre até a camada de aplicação e é mostrada ao destinatário.

**Camada de Aplicação**

    É a camada mais alta, é por exemplo, onde acessamos o navegador, ou seja, o navegador está na camada de aplicação.

    Quando torna-se valor binário, camada física, essa envia o dado na rede, seja por cabo, ou wifi, via física ou ar, chega no destino, a camada física recebe, e passa por todas as camadas até a camada de aplicação novamente.

    Cada camada tem uma função específica, por exemplo;

* **Camada de aplicação** - Enviamos um E-mail, no gmail estamos na camada de aplicação;

* **Camada de apresentação** - Temos 3 pilares, que são a criptografia, que irá embaralhar as informações, a compactação, que deixa os arquivos com peso menor, por exemplo se temos uma imagem que tem vários pixels iguais, eles são igualados, com dados binários, para serem enviados, e também é feita a tradução, de decimal para tabela ascii 2, pega um texto e converte para este modelo.

* **Camada de seção** - Ela é responsável por iniciar e encerrar uma sessão, por exemplo, quando enviamos um e-mail, ela abre a sessão, salva, sinaliza que estão se comunicando, indica o canal, envia o dado, e posteriormente fecha a sessão.

`TCP/IP - É um modelo de comunicação, onde tcp, é, protocolo de controle de transporte, junto com ip que é internt protocol, responsável pelo endereçamento de máquinas na rede.`

`IOT - São equipamentos que enviam dados através da internt, e assim tem um funcinamento conectado, por exemplo, sensores de irrigação de solo, onde o sensor faz a irrigação ativar dependendo da umidade, pulseiras que medem o batimento cardiáco em pacientes, relógios inteligentes que monitoram atividades físicas, por exemplo`

    Dois computadores conectados por rede, através de um cabo, não necessáriamente são uma intranet. Podemos ter duas máquinas conectadas por par trançado, sendo um crossover, entre os dois, eles estariam em uma rede LAN. Para uma intranet, geralmente faz uso de senha, onde computadores de fora não tem acesso a essa rede.

    A topologia mais vantajosa hoje seria a rede malha ou a topologia em estrela, que usamos hoje em casa, e lá possuimos dispositivos conectados a essa rede, temos uma topologia em estrela.

    O problema no claude code teve haver com redes, vale lembrar que sistemas pix de bancos, que geralmente tem seus sistemas hospedados na nuvem, como amazom ou azurre, salvo o banco do Brasil, que possui um sistema legado, com seus própios servidores, e não dependem de um servidor externo.

    Como funciona uma VPN - Nada mais que alugar um canal de comunicação, onde esse canal será privado entre origem e destino, um Virtual Private Network.

    Porque o modelo tcp tem só quatro camadas e o modelo osi tem 7 - Nada mais é que uma simplificação do modelo OSI, fez se essa simplificação porque percebeu-se que a camada de aplicação, apresentação e sessão fazem práticamente a mesma coisa e estão mais próxima do usuário. Conseguimos visualisar nas camadas 7, 6 e 5 o que estã na camada de aplicação.

**Transporte** 

    Nessa camada temos dois protocolos importântes, o protocolo tcp, que garante que a informação chegue ao destino final, e a udp, que ó protocolo que utiliza datagramas, ele não precisa garantir que o dado chegue, pois por exemplo, em transmissões de vídeo pode-se perder dados, e não teria problema no protocolo udp, que não precisa garantir que o dado chegue no usuário final, diferênte do protocolo tcp que precisa garantir que o dado chegue até o destinatário.

**Camada de rede**

    Na camada do modelo OSI e no modelo tcp é chamado de internet, onde temos a parte dos roteadores e a parte dos ip's, os roteadores escolhem a melhor rota para o dado e os endereçõ  ip's é o endereço lógico da máquina na rede. 192.168.0.50, por exemplo, podemdo repetir, pois cada usuário usa uma rede diferênte do outro, quem endereça o ip é o modem, o papel do modem é dividir a rede telefonica, que manda a fibra ótica até o modem, faz a converção do sinal digital para analógico e vice versa, o roteador/modem faz a enderezação ip para cada dispositivo.

**Camada de enlace**

    Está atrelada a camada de acesso a rede, temos a formatação desses dados em endereço MAC, diferente do endereço lógico, o endereço MAC é o endereço físico de acesso a rede. Cada endereço MAC é único no munco.

**Camada Física**

    Pega todos esses dados e converte para sinal digital binário para ser transmitido pela rede, podendo ser enviado por cabos fibra-ótica, wifi.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img12.png)    Serviços em uma rede

    Primeiramente temos o endereçamento ip, o endereço lógico da máquina na rede, onde cada endereço é único na rede, sendo definido pela faixa de ip da rede local.     Cada dispositivo tem seu endereço ip, como o roteador, terá o seu endereço ip, no meio do camiho pode ter outro roteador com outro endereço ip, acessando um servidor, que pode ser um site, por exemplo, www.unicesumar.com que estará hospedado em um servidor com um domínio, entrando no DNS, que para nós humanos é mais fácil digitar o nome do site do que seu endereço ip, ele faz a converção de um dominio em um endereço ip, então no servidor tem uma tabela que define qual ip o site ficará hospedado, por exemplo, isso é atrelado ao dominio de uma rede, de um site no caso. Por exemplo se falarmos um CEP aleatório provavelmente não saberemos a qual rua se refere, porém se falarmos o nome da rua saberemos, pois não temos o cep decorado, então o DNS faz essa converção de endereço.

**DHCP** - é um protocolo que distribui um automáticamente um ip.

**ARP** - É um protocolo que atrela um IP a um endereço MAC, resolve endereços IP em endereços MAC na rede, faz a associação do endereço MAC, que é único no mundo, com o endereço IP na rede.

    Uma coisa importante, porque pedem para reiniciar o roteador quando a net trava, provavelmente conflito de ip com outro dispositivo na rede, e reiniciando ele busca outro ip para disponibilizar, ou seja, não podemos ter dois ips iguais na mesma rede.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img13.png)    Protocolo TCP um protocolo mais confiável, pois garante que o dado será entregue, controla os erros, ordena os pacotes, quebra em vários pedaços,e depois monta novamente, desvantagem, é mais lento.

**UDP** - Não tem garantia que o dado irá chegar, em jogo pode travar, pois não precisa de confirmação, não precisa de uma confirmação de entrega, entrega mais rápida.

**HTTP/HTTPS** - Acessar sites e para transmissões seguras, porta 8

**FTP/SFTP** - Transmissão de arquivos, envio e recebimento, porta 21 e 22.

**SMTP** - Protocolo para envio de e-mail, porta 25.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img14.png)    Resumo do foi visto, as aplicações, estudando cada camada do modelo OSI, enenderemos as camadas do modelo TCP.

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img15.png)

<mark>Lembrando que DNS não é um protocolo, e sim um serviço.</mark>

![](/home/carlos/Unicesumar/Módulo%2051-26/Redes%20de%20Computadores/imagens/img16.png)
