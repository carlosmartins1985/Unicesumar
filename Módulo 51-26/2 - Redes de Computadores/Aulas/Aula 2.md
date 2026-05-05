# Aula 2 - Redes de Computadores

**Modelos de referência OSI e TCP/IP**

A base para entender como as redes de computadores funcionam, na teorÍa e na prática

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2020-01-22.png)

    Nesta aula faremos algumas simulações para entender o funcionamento dos modelos osi e tcp.

    Tanto o modelo OSI e TCP/IP são padrões para que as máquinas consigam fazer a ligação entre si, a conexão.

    Eles precisam de protocolos para funcionar, e esses protocolos são meios que as máquinas usam para conseguir se comunicar independente do fabricante.

Mas como vemos isso na prática?

Um computador tem as camadas, da origem ao destino e vice versa.

    Mas como as mensagens são trocadas entre as máquinas?

Podemos fazer uma análogia como se fosse uma viagem, por exemplo.

    Quando vamos viajar, primeiro compramos a passagem, depois despachamos a bagagem, e depois entramos no ônibus. Posteriormente temos o trajeto, que  são as rodovias, que podem ser compreendidos como a ***Camada Física*** , que seriam os meios que os dados utilizam para percorrer o trajeto até o destino. E quando chegamos ao nosso destino, precisamos fazer o processo reverso. Descer do ônibus, pegar a bagagem e sair da rodoviária. Esso processo passa pela camada de aplicação até a camada física, e depois o processo reverso.

    É isso que os modelos de referência fazem quando estamos nos comunicando na rede.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2020-12-46.png)

    Quais são os tipos de referência que esses modelos fazem?

    Tanto o modelos OSI quanto o TCP/IP tem camadas, que tem a função de organizar esses dados para que tenham inicio meio e fim, durante a comunicação origem/destino. Uma padronização, que indenpendete do fabricante da máquina irá funcinar, Interoperabilidade, que permite que um computador com linux consiga mandar mensagem para um smartphone Android, por exemplo, indenpendente do sistema operacional que estejamos utilizando. Diagnostico, que é a possíbilidade de entender onde estão ocorrendo os problemas, da rede, do pc ou da empresa, o que facilita o diagnostico, para identificar um possível gargalo, por exemplo.

 ![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2020-21-18.png)

    Aqui temos as sete camadas do modelo OSI, onde a camada de Aplicação, camada 7 é a que está mais próxima do usuário, e a camada física é a que está mais abstrata para o usuário, mais distante.

**Aplicação** - Nesta camada temos os protocolos, como o HTTP, POP3, FTP, UTFTP cada aplicação dessa existe um protocolo e serviço, com o DNS.

**Apresentação** - Temos a criptográfia, a tradução a compactação de dados.

**Seção** - Temos a abertura e fechamento de seção, é onde se inicia a comunicação, e quando essa comunicação e encerrada a seção é fechada.

**Transporte** - Temos dois protocolos conhecidos, o tcp e o udp, sendo o tcp o mais confiável, pois contém uma garantia de entrega dos pacotes, e o udp, que não possui garantia de entrega dos pacotes mas é mais rápido que o TCP, usamos  por exemplo para uma transmissão ao vivo, pois não precisamos de uma confirmação de entrega desse pacote, apenas rapidez.

**Rede** - A camada de rede é responsável pelo endereçamento das máquinas na rede.

**Enlace** - Responsável pelo endereçamento físico da máquina, da placa de rede do computador ou qualquer dispositivo que esteja na rede.

**Física** - Por onde os dados trafegam, do ponto de origem até o ponto de destino.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2020-34-50.png)

    Com o avanço da tecnologia o modelo OSI foi simplificado para o modelo TCP/IP com 4 camadas. Ná prática a diferênça em cada camada dessa está na junção, onde a camada de **Aplicação** do modelo TCP/IP aborda **Aplicação, Apresentação e Seção,** essas três camadas foram compactadas para a camada de **Aplicação**. A camada de **Transporte** continuou igual. A camada de **Rede** e de **Enlace** ficaram na camada de **Internet**, e a camada **física** ficou conhecida como **Enlace**, que é apenas a parte física do computador.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2020-42-38.png)

**Wireshark**

    Com o Wireshark conseguimos capturar dados que estão trafegando na rede, seja em casa, na empresa.

    Iniciamos a captura dos dados clicando na Nadadeira do shark.

Na inicialização qual é o tipo de conexão que queremos visualizar no pc.

Importante usao o sudo para abrir o wireshark.

Podemos acessar várias conexões, como wifi e cabeada.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2021-09-31.png)

    Colocando o mouse encima da conexão nos é mostrado o endereço IP da máquina, no ipv4, e também mostra no ipv6.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2021-14-33.png)

Dando dois cliques na conexão wifi, o wire já começa a capturar os pacotes na rede. Cada linha dessa é um pacote que foi trafegado na rede.

Na tela do wire temos;

Na *primeira coluna*, o número em ordem crescente, que é a sequência em que os dados trafegaram na rede.

Na segunda coluna - O tempo em milisegundos, que o pacote levou para sair do meu pc até o endereço de destino.

Na terceira coluna - Temos o IP de de origem, que é o ip da minha máquina;

Na quarta coluna - Temos o IP de destino do pacote;

Na quinta coluna - Temos os protocolos, TCP e UDP;

Na sexta coluna - O tamanho do pacote;

Na última coluna - A informação do que esse dado levou e o que trouxe como resposta.

**Capturando pacotes**

Acessamos o site do uol, para teste;

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2021-39-44.png)

E temos a captura do pacote, notamos na direita uma série de caracteres que não são intendiveis pelo ser humano, pois foram convertidos para hexadecimal e também para binário. Quando estamos acessando o navegador, enviando um e-mail para alguém, estamos na camada de Aplicação. Se estamos usando o html, estamos usando o protocolo http, e se for um e-mail, https, se estamos baixando um arquivo da internet, estamos usando o protocolo FTP.

    Na camada de apresentação temos a tradução a compactação e a compressão. Provávelmente esse dado que passou pelo wire, que foi enviado, foi traduzido e criptografado.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2021-46-04.png)

Na esquerda temos a tradução, hexadecimal, e na direita a criptografia. Não conseguimos saber qual dado passou pela rede, porém existem ferramentas que fazem a engenharia reversa desses dados, onde conseguimos fazer a descriptografia do dado que está na camada de apresentação. O dado na camada de apresentação é traduzido para hexadecimal, e quando chega na camada física se transforma em dado binário.

**DNS**

Na camada de aplicação conseguimos também visualizar o serviço de DNS.

    No prompt de comando conseguimos visualizar o serviço DNS, sabemos que as máquinas na rede se comunicão através de endereço ip, então, se criarmos um site, e colocassemos um ip de identificação, 192.168.5.9, por exemplo, ficaria muito difícil para alguém consegir sempre digitar o endereço do site, ou mesmo decorar o endereço. Podemos testar enviando um ping para um site e ver o retorno;

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-07%2022-01-38.png) 

    Podemos tentar outro site para ver se teremos uma resposta;

```bash
carlos@cs-ubuntu:~$ ping www.uol.com
PING amazonas.uol.com.br (200.147.35.224) 56(84) bytes of data.
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=1 ttl=242 time=17.4 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=2 ttl=242 time=20.0 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=3 ttl=242 time=20.3 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=4 ttl=242 time=17.7 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=5 ttl=242 time=19.5 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=6 ttl=242 time=19.3 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=7 ttl=242 time=20.3 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=8 ttl=242 time=18.1 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=9 ttl=242 time=19.2 ms
^L64 bytes from pagueuol.net (200.147.35.224): icmp_seq=10 ttl=242 time=17.6 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=11 ttl=242 time=20.3 ms
64 bytes from pagueuol.net (200.147.35.224): icmp_seq=12 ttl=242 time=20.4 ms
^C
--- amazonas.uol.com.br ping statistics ---
12 packets transmitted, 12 received, 0% packet loss, time 11015ms
rtt min/avg/max/mdev = 17.396/19.168/20.392/1.126 ms
carlos@cs-ubuntu:~$ 
```

    Testando com o site do uol temos o retorno, e esse é o ip do site uol (200.147.35.224). 

Podemos ter por exemplo um servidor, que será uma máquina mais robusta, esse servidor terá uma tabela DNS, que será responsável por resolver a requisição, quando acessamos um site, por exemplo, www.google.com, a table recebe essa requisição, busca o endereço ip correspondente a esse endereço e devolve a página htmo correspondente ao site. Podemos testar o ping no site da unicesumar, usando o -4 para que seja retornado o ipv4;

```bash
carlos@cs-ubuntu:~$ ping -4 www.unicesumar.edu.br
PING www.unicesumar.edu.br (172.66.150.187) 56(84) bytes of data.
64 bytes from 172.66.150.187: icmp_seq=1 ttl=58 time=31.2 ms
64 bytes from 172.66.150.187: icmp_seq=2 ttl=58 time=4.53 ms
64 bytes from 172.66.150.187: icmp_seq=3 ttl=58 time=4.55 ms
64 bytes from 172.66.150.187: icmp_seq=4 ttl=58 time=4.38 ms
```

Testando o ip no navegador não carregou, provávelmente por conta de alguma segurança na rede.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-13%2021-35-02.png)

Desse modo que funciona a invasão de redes, através do ip, podendo utilizar /admin,  por exemplo, e conseguindo invadir o sistema.

Testamos com o site do professor;

```bash
carlos@cs-ubuntu:~$ ping -4 www.jalyson.tec.br
PING www.jalyson.tec.br (82.25.67.187) 56(84) bytes of data.
64 bytes from 82.25.67.187: icmp_seq=1 ttl=56 time=17.0 ms
64 bytes from 82.25.67.187: icmp_seq=2 ttl=56 time=50.6 ms
64 bytes from 82.25.67.187: icmp_seq=3 ttl=56 time=20.4 ms
^C
```

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-13%2021-38-00.png)

Se tentar-mos pelo dominio conseguimos acessar.

O ping serve para testar se um equipamento está conectado a internet, ou ao nosso equipamnto, podemos testar com nosso próprio smartphone;

```bash
carlos@cs-ubuntu:~$ ping -4 192.168.1.7
PING 192.168.1.7 (192.168.1.7) 56(84) bytes of data.
64 bytes from 192.168.1.7: icmp_seq=1 ttl=64 time=377 ms
64 bytes from 192.168.1.7: icmp_seq=2 ttl=64 time=99.6 ms
64 bytes from 192.168.1.7: icmp_seq=3 ttl=64 time=217 ms
64 bytes from 192.168.1.7: icmp_seq=4 ttl=64 time=42.6 ms
64 bytes from 192.168.1.7: icmp_seq=5 ttl=64 time=65.5 ms
64 bytes from 192.168.1.7: icmp_seq=6 ttl=64 time=87.9 ms
64 bytes from 192.168.1.7: icmp_seq=7 ttl=64 time=207 ms
64 bytes from 192.168.1.7: icmp_seq=8 ttl=64 time=134 ms
64 bytes from 192.168.1.7: icmp_seq=9 ttl=64 time=252 ms
64 bytes from 192.168.1.7: icmp_seq=10 ttl=64 time=275 ms
64 bytes from 192.168.1.7: icmp_seq=11 ttl=64 time=98.7 ms
^C
--- 192.168.1.7 ping statistics ---
12 packets transmitted, 11 received, 8.33333% packet loss, time 11016ms
rtt min/avg/max/mdev = 42.593/168.618/377.484/99.718 ms
```

E temos informações como tempo de envio, quantidade de pacotes enviados, recebidos.

Existe o ping exaustivo, faz várias vezes o ping, ao desligar o wifi do aparelho destino ele perde a conexão, não faz mais o ping, se ligar novamente volta ao normal.

Ping é um teste para para verificar se a nossa máquina está se conectando a rede, em algum dispositivo, sendo outra máquina na mesma rede ou um servidor remoto.

Podemos testar rede wifi, rede cabeada.

Também é um teste que os provedores de internet também fazem, quando pedem para reiniciar o roteador, quando liga novamente o técnico faz o teste do ping no roteador para saber se reconectou.

**Camada de Transporte**

O protocolo **TCP** garante que um dado chegue no destino final, já no **UDP** não garante que o dado chegue no destino final.

O TCP/IP exige uma quantidade maior de informações para o dado que será entregue, toda vez que a informação é enviada, ele garante que a informação será entregue.

Para sabermos que a informação foi entregue existe o ACK (acknowledgment) trata-se de uma confirmação que o dado foi entregue no destino.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-13%2021-57-27.png)

Aqui temos;

Source Port - Porta de Saída = 58062;

Destination Port - Porta de Destino - 443

ACK - acknowledgment - Uma confirmação que o dado foi recebido pela máquina destino.

Se pegar-mos um protocolo UDP não temos o ACK, pois esse protocolo não precisa de confirmação de entrega, ele só pega o dado, compacta e manda.

Esses dois protocolos estão na camada de transporte.

**Camada de Rede**

A camada de rede define o endereço lógico do computador na rede. Os ip's podem ser iguais, tanto em nossas casas, quanto na casa de alguém que mora em outra cidada. Digamos por exemplo que o provedor de internet colocou o ip padrão para o roteador em uma residência como:

Rede casa Carlos - SC - Blumenau

Modem (VIVO) 200.70.25.111

 {IP notebook 192.168.1.128}

{IP smartphone 192.168.1.222}

Rede casa Fernando - SP

Modem(Nio): 202.41.111.75

{IP notebook 192.168.1.222}

{IP smartphone 192.168.1.40}

Aqui vemos que os podem coincidir, pois fazem parte de uma rede distinta, o que não pode ser igual é o endereço ip do roteador.

    Sabemos que a informação passa por vários roteadores até chegar ao destino, por exemplo, para mandar algo para Fernando, o dado poderia passar por pelo menos três roteadores diferêntes:

R1: 172.20.45.70

R2: 196.77.100.200

R3: 172.50.45.60

    Primeiro a máquina se comunica com o roteador mais próximo, que é o roteador 1, e vai se comunicar com o ip do Fernando, isso é possível pois ambos estão em uma rede LAN, que são redes internas, os roteadores estão em uma rede WAN, alguns roteadores já vem com uma fixa de IP fixo de fábrica, 168.1.alguma coisa, e outra pessoa pode ter o mesmo aparelho, com a mesma faixa de IP, e apesar disso não ocorre conflito pois estão em redes diferêntes.

Conflitos de IPs em uma rede podem acontecer por causa do DHCP, que distribui os ips de forma automática. 



<mark>Roteadores não podem ter o mesmo IP na rede externa. Gera conflito</mark>

    Pode acontecer uma coincidencia de dois roteadores terem o mesmo IP na rede, então quem concerta esse cenário é a operadora através da tabela de IP's.



    Segue a mesma lógica do CEP da residência, que quando mudamos de cidade é sempre outro, os IP's também, para cada estado temos ips diferêntes.

Cada modem tem um ip externo atrelado a operadora, e quando mudamos de operadora ou de cidade o ip também muda.

    Diferente da telefonia móvel, que podemos mudar de cidade, estado ou país que o número permanece o mesmo. Isso vale para a interne 4g, 5g e etc... Por exemplo, quando conectamos o celular ao 4g é passado uma faixa de IP da operadora, e não de uma rede interna, a doméstica, por exemplo, é assim que conseguimos rotear internet através do celular, pois quando fazemos isso, todos os dispositivos que se conectam a nossa rede móvel formam, aí sim, uma rede interna, pois o celular faz o papel de roteador, mas para a rede externa, para se comunicar com a operadora segue o mesmo conceito de um roteador comum que se conecta com o provedor de internet.

    Temos então Ips da operadora e ips internos, duas faixas de ips, ou seja, ips para a rede LAN e ip para a rede WAN.



    Imaginamos por exemplo uma empresa, onde temos 100 computadores para enumera-los, para isso temos duas opções:

* Usando IP fixo - Que seria numerando manualmente, se tivermos 100 máquinas, precisaremos enumerar cada um deles, 192.168.1.1 até o 192.168.1.100.

* Usando o DHCP  - Que podemos marcar a tabela e o sistema distribui os ips para os computadores, a desvantagem é que como as máquinas ficam se conectando constantemente a rede pode acontecer um conflito de ip, por exemplo, um computador na rede tentar acessar o computador com mesmo endereço ip, ips duplicados, mas mesmo assim ainda é indicado para ser usado ao configurar máquinas domésticas,pois mesmo que haja algum conflito, podemos apenas reiniciar o roteador que será realencado os ips para cada máquina.

    Já para empresas que tem 100 computadores, por exemplo, aconselha-se usar o ip fixo, pois sabemos que cada computador terá um ip fixo na rede, o que facilita a manutenção, por exemplo, se precisamos fazer algum monitoramento para descobrir se está sendo feito algo ilicito na empresa, com o ip fixo a máquina é rapidamente identificada, conseguimos monitorar essa rede pelo própio wireshark, com ele conseguimos ver o que a pessoa está assistindo, e quais dados estão passando por ele.

    Porque quando reiniciamos o roteador o tráfego melhora?

    Precismos entender que cada provedor de internet tem uma tabela de clientes:

```
Tabela de Clientes
José Francisco da Rocha 201.89.100.57
Maria de Fátima 201.89.100.58
Pedro Francisco 201.89.100.59
```

    Como vemos, trata-se de uma sequência, que em algum momento esse endereçamento estará saturado, cheio, e assim começará a travar o sistema, e digamos que algum cliente reclame, eles podem pegar esse cliente e simplismente passar para uma outra faixa de IP que não esteja congestionado, por exemplo, enviando Pedro para outra faixa de ip de rede:

```
Pedro Francisco 205.74.85.96
```

    É mudado o chaveamento, que é tirar uma pessoa de uma rede e coloca-la em outra rede, e também sempre que reiniciamos o modem é fornecido um IP diferênte do que estava sendo usado antes, sempre é alterado a faixa de IP, mas por exemplo, para fins de investigação, o roteador guarda um histórico dos IP's anteriores, caso seja necessário.



**Mascara de sub-rede**

    Define quantas máquinas podemos ter na rede e em que faixa de ip estará.

    Temos as classificações A, B, C.

    Todos os dispositivos que estiverem conectados a mesma LAN compartilham a mesma máscara de sub-rede.

    Por exemplo, temos a máscara:

255.255.255.0 que nada mais é que octetos binários, pois convertendo 255 para binário temos: `1111.1111`.

    Octetos são conjuntos de 8 bits, que representamos em cada ponto da máscara de sub-rede:

Mascara de sub-rede: 255.255.255.0 

Representação binária: 11111111.11111111.11111111.00000000 

Tudo que for um representa rede e tudo que for zero representa host, que é cada dispositivo conectado a rede, computador, celular, tv...

Essa é uma rede de classe C, e através dessa máscara conseguimos saber quantas máquinas conseguimos conectar a essa rede. Para calcular quantos hosts podemos ter conectado a rede, efetuamos o cálculo através dos zeros, ou seja, são oito zeros, então:

```
2 ^ 8 = 256
```

Ou seja, podemos ter 256 máquinas conectadas a essa rede.

Para a faixa de ip, quando temos tudo 1 na mascara de sub-rede, significa que a faixa 192.168.1 nunca será alterada, será sempre fixo, todos os hosts terão essa mesma faixa, a única que muda é o último octeto, onde tem zero, porém não utilizamos o ip zero, 192.168.1.0, sendo:

* 192.168.1.0 - O primeiro IP que nunca é usado, é só uma referência para qual será a faixa de ip.

* 192.168.1.255 - O último IP é o broadcast, que envia mensagem aos dispositivos na rede para saber se estão conectados, sendo endereço de máquina e não endereço ip.

* 192.168.1.1 - A primeira máquina da rede;

* 192.168.1.254 - A última máquina da rede;

Temos então 2 elevado a 8, que teremos o valor de 256, então a faixa vai de 0 a 255, sendo 256 hosts para conexão.

Então sempre que formos fazer o calculo para quantos dispositivos podemos conectar na rede usamos 2 ^ 8 - 2, pois dois ips nunca são usados.

    Tudo isso para a classe C.



`Classe B`

    Na classe C temos:

255.255.0.0 - Onde os dois primeiros octetos são endereços de rede e os últimos dois são endereços de hosts para conexão.

No cálculo:

255.255            .0.0                256 ^ 2 = 65.536 hosts aproximadamente

--rede--           -hosts-



Classe A 

255.0.0.0 - Cálculo - podemos ter até 16.777.216, dezesseis milhões de hosts, dentro de uma mesma rede.



Aplicações para a classes;

    Quantas máquinas podem ser conectadas naquela rede, para não desperdiçar endereço ip.

    Para casos em que precisamos de poucos endereços ips podemos usar o semdr, que usa uma máscara de subrede endereçamento.



Ipv4 tem 32 bits, 8 x 4 = 32. São 4 bits.



Definimos o ip através do roteador ou servidor de ip, montamos um servidor de ip.



Quando hopedamos um site recebemos um ip que nos comunicamos através de um app, choreftp e o firezila, que quando criamos o site, recebemos um ip ao qual enviamos o doc html do site para ser carregado. Um endereço ip com user e password.



Firewal - é um servidor que monitora o que entra e sai da rede. 








