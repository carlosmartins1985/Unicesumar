# Peer to peer

**2.4 PARADIGMA PEER-TO-PEER**

    Discutimos o paradigma cliente-servidor no início do capítulo. Discutimos também algumas aplicações cliente-servidor padronizadas nas seções anteriores. Nesta seção, discutimos o paradigma peer-to-peer (também conhecido como par a par). O primeiro exemplo de compartilhamento de arquivos via peer-to-peer remonta a dezembro de 1987, quando Wayne Sino criou o WWIVnet, o componente de rede do Guerra Mundial Quatro (WWIV – World War Four), um Sistema de Quadro de Avisos (também conhecido como Bulletin Board System). Em julho de 1999, Ian Clarke proje-tou a Freenet, um sistema de armazenamento de dados descentralizado, distribuído e resistente a censuras, com o objetivo de fornecer liberdade de expressão através de uma rede peer-to-peer com forte proteção de anonimato. O paradigma peer-to-peer ganhou popularidade com o Napster (1999-2001), um serviço de compartilhamento de arquivos de música online criado por Shawn Fanning. Embora a cópia e distribuição livre de arquivos de música pelos usuários tenham levado a uma ação judicial contra o Napster por violação de direitos autorais, o que causou o fechamento do serviço, ele abriu o cami-nho para modelos de distribuição de arquivos baseados em peer-to-peer que surgiram mais tarde. O Gnutella foi lançado em março de 2000, seguido pelo Fast-Track (usado pelo Kazaa), BitTorrent, WinMX e GNUnet em março, abril, maio e novembro de 2001, respectivamente.

**2.4.1 Redes P2P**
Usuários da Internet que queiram compartilhar os seus recursos tornam-se peers e formam uma rede. Quando um peer na rede tem um arquivo (por exemplo, um arquivo de áudio ou de vídeo) para compartilhar, ele o deixa disponível para o restante dos peers. Um peer interessado pode se conectar ao computador onde o arquivo está armazenado e fazer o download. Depois de um peer obter um arquivo, ele pode deixá-lo disponível para outros peers para download. À medida que os peers se juntam à rede e obtêm o arquivo, mais cópias passam a ficar disponíveis para o grupo. Como as listas de peers podem crescer ou diminuir, a questão é como o paradigma rastreia os peers leais e a localização dos arquivos. Para responder a estas perguntas, precisamos primeiro dividir as redes P2P em duas categorias: centralizadas e descentralizadas.

**Redes centralizadas**
Em uma rede P2P centralizada, o sistema de diretórios – a lista dos peers e do que eles têm a ofere-cer – usa o paradigma cliente-servidor, mas o armazenamento e o download dos arquivos são feitos usando o paradigma peer-to-peer. Assim, uma rede P2P centralizada é muitas vezes denominada rede P2P híbrida. O Napster foi um exemplo de uma rede P2P centralizada. Nesse tipo de rede, um peer primeiro se registra junto a um servidor central. Em seguida, o peer fornece o seu endereço IP e uma lista de arquivos que ele tem para compartilhar. Para evitar o colapso do sistema, o Napster usava vários servidores para isso, apesar de mostrarmos apenas um na Figura 2.46.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2020-17-38.png)

    Um peer, ao procurar um determinado arquivo, envia uma consulta para um servidor central. O servidor procura em seu diretório e responde com os endereços IP dos nós que têm uma cópia do arquivo. O peer entra em contato com um dos nós e faz o download do arquivo. O diretório é constantemente atualizado à medida que os nós entram ou saem da rede. Redes centralizadas simplificam a manutenção dos diretórios, mas apresentam vários inconve-nientes. O acesso ao diretório pode gerar uma quantidade enorme de tráfego e deixar o sistema lento. Os servidores centrais são vulneráveis a ataques, e se todos eles falharem, o sistema inteiro deixa de funcionar. O componente central do sistema foi o principal responsável pelo Napster perder a ação judicial por violação de direitos autorais e pelo seu fechamento em julho de 2001. A Roxio trouxe de volta o Novo Napster em 2003; o Napster versão 2 é agora um site legal para venda de músicas.

Explicação IA

Este capítulo trata da transição e da coexistência de dois modelos fundamentais de comunicação na internet: o tradicional **Cliente-Servidor** e o inovador **Peer-to-Peer (P2P)**.

Abaixo, apresento uma explicação detalhada dividida pelos pontos principais abordados no texto:

---

## 1. O Conceito de Peer-to-Peer (P2P)

Diferente do modelo cliente-servidor, onde há uma hierarquia clara (um servidor centralizado que atende a vários clientes), no paradigma **P2P**, os dispositivos na rede — chamados de **peers** (pares) — atuam simultaneamente como **clientes e servidores**.

- **Compartilhamento de Recursos:** Cada peer disponibiliza parte de seus recursos (como arquivos de áudio, vídeo ou processamento) para outros membros da rede.

- **Escalabilidade Orgânica:** Quanto mais pessoas entram na rede e baixam um arquivo, mais cópias ficam disponíveis, o que tecnicamente torna a rede mais forte à medida que ela cresce.

---

## 2. Contexto Histórico

O texto traça uma linha do tempo importante para mostrar que o P2P não surgiu do nada:

- **WWIVnet (1987):** Um dos primeiros exemplos de troca de informações de forma distribuída.

- **Freenet (1999):** Focada em anonimato e resistência à censura.

- **Napster (1999):** O grande divisor de águas. Embora tenha sido fechado por questões de direitos autorais, ele provou que o modelo P2P era extremamente eficiente para distribuição de mídia em massa.

- **Gnutella, BitTorrent e outros (2000-2001):** Surgiram para preencher o vácuo deixado pelo Napster, muitas vezes com modelos ainda mais difíceis de derrubar (totalmente descentralizados).

---

## 3. Redes P2P Centralizadas (Híbridas)

O foco técnico da seção 2.4.1 é a **Rede Centralizada**, exemplificada pela Figura 2.46. Este modelo é chamado de "híbrido" porque mistura os dois paradigmas:

### Como funciona (O fluxo da imagem):

1. **Diretório Centralizado (Cliente-Servidor):** Existe um servidor central (Central de Diretórios) que mantém um "índice". Quando um peer entra na rede, ele informa ao servidor: *"Eu sou o IP X e tenho os arquivos A, B e C"*.

2. **A Busca:** Quando você quer um arquivo, você não pergunta para a rede toda. Você pergunta para o **servidor**. Ele te responde com uma lista de IPs de outros peers que possuem o que você busca.

3. **A Transferência (Peer-to-Peer):** O download real **não passa pelo servidor**. O seu computador conecta-se diretamente ao computador do outro peer para baixar o arquivo.

| **Elemento**        | **Papel no Sistema**                               |
| ------------------- | -------------------------------------------------- |
| **Linha Tracejada** | Informação de diretório (quem tem o quê).          |
| **Linha Cinza**     | Compartilhamento real do objeto (o arquivo em si). |

---

## 4. Vantagens e Desvantagens do Modelo Centralizado

O texto destaca que, embora o Napster tenha sido eficiente, ele tinha "calcanhares de Aquiles" (pontos fracos) fatais:

- **Vantagem:**
  
  - **Facilidade de Busca:** É muito rápido encontrar um arquivo porque o índice está em um só lugar.

- **Desvantagens:**
  
  - **Ponto Único de Falha:** Se o servidor central cair (por falha técnica ou ataque), ninguém consegue achar nada, mesmo que os arquivos ainda estejam nos computadores dos usuários.
  
  - **Gargalo de Tráfego:** Milhões de pessoas perguntando ao mesmo servidor podem deixá-lo extremamente lento.
  
  - **Vulnerabilidade Jurídica:** Como existe um "dono" do diretório (o servidor central), é fácil para a justiça identificar quem é o responsável pela rede e fechá-la, como aconteceu com o Napster original em 2001.

---

### <mark>Resumo Técnico</mark>

O capítulo explica que o P2P centralizado foi o estágio inicial da revolução dos arquivos compartilhados. Ele resolveu o problema de "onde encontrar os dados", mas falhou em ser verdadeiramente resiliente, o que levou ao desenvolvimento das redes **totalmente descentralizadas** (onde nem o índice fica em um servidor central), que provavelmente são o tema da sequência deste estudo.

---

### Rede descentralizada

Uma rede P2P descentralizada não depende de um sistema de diretórios centralizado. Nesse mo-delo, os peers se organizam em uma rede sobreposta (overlay network), uma rede lógica criada sobre uma rede física. Dependendo de como os nós da rede sobreposta são ligados, uma rede P2P descentralizada pode ser classificada como não estruturada ou estruturada.

### Redes não estruturadas

Em uma rede P2P não estruturada, os nós se ligam de forma aleatória. Uma busca em uma rede P2P não estruturada não é muito eficiente, pois uma consulta para localizar um arquivo deve inundar toda a rede (ou seja, ser enviada a todos os nós), o que produz uma quantidade significativa de tráfego e pode não retornar resultados. 

    Dois exemplos desse tipo de rede são Gnutella e Freenet. A seguir, discutimos a rede Gnutella como um exemplo.
    **Gnutella** -  A rede Gnutella é um exemplo de uma rede peer-to-peer descentralizada, porém não estruturada, no sentido de que o diretório é aleatoriamente distribuído entre os nós. Quando o nó A quer acessar um objeto (tal como um arquivo), ele entra em contato com um de seus vizinhos. Um vizinho, nesse caso, é qualquer nó cujo endereço seja conhecido pelo nó A. O nó A envia uma mensagem de consulta ao seu vizinho, o nó W. A consulta inclui o identificador do objeto (por exemplo, o nome do arquivo). Se o nó W sabe o endereço do nó X, que tem o objeto, ele envia uma mensagem de resposta, a qual inclui o endereço do nó X. O nó A agora pode usar os comandos definidos em um protocolo de transferência, como HTTP, para obter do nó X uma cópia do objeto. Se o nó W não sabe o endereço do nó X, ele inunda o pedido de A para todos os seus vizinhos. Por fim, um dos nós da rede responde à mensagem de consulta, e o nó A ganha acesso ao nó X. Discutiremos o mecanismo de inundação no Capítulo 4, quando discutimos protocolos de roteamento, mas é importante mencionar aqui que, embora as inundações no Gnutella sejam de certa forma controladas para evitar elevadas cargas de tráfego, uma das razões pelas quais o Gnutella apresenta baixa escalabilidade é o mecanismo de inundação. Uma das perguntas que ainda precisam ser respondidas é como, de acordo com o processo descrito anteriormente, o nó A sabe o endereço de pelo menos um vizinho. Isto é feito no momento da inicialização (bootstrap), quando o nó instala o software Gnutella pela primeira vez. O software inclui uma lista de nós (peers) que o nó A pode registrar como vizinhos. Mais tarde, o nó A pode usar duas mensagens, chamadas ping e pong, para tentar descobrir se um vizinho ainda está ativo. Conforme mencionado anteriormente, um dos problemas com a rede Gnutella é a falta de escalabilidade causada pelo mecanismo de inundação. Quando o número de nós aumenta, as inundações não levam a um bom resultado. Para tornar a consulta mais eficiente, uma nova versão do Gnutella implementou um sistema hierárquico de folhas e ultranós. Um nó entrante na rede torna-se uma folha, não se responsabilizando pelo roteamento; nós que são capazes de auxiliar no roteamento são promovidos a ultranós. Isto permite que as consultas propaguem-se até mais longe, aumentando a eficiência e a escalabilidade do sistema. O Gnutella adotou uma série de outras técnicas, como a inclusão do Protocolo de Roteamento de Consulta (QRP – Query Routing Protocol) e da Consulta Dinâmica (DQ – Dynamic Querying) para reduzir a carga de tráfego e tornar as pesquisas mais eficientes.

**<mark>Explicação IA</mark>**

Para entender as redes **P2P (Peer-to-Peer)**, a primeira coisa que você precisa esquecer é aquela ideia de um "servidor central" (como o Google ou o Facebook) que manda em tudo. Aqui, todo mundo é igual: seu computador é, ao mesmo tempo, um cliente e um servidor.

Vamos dividir o que você leu em três pilares principais:

---

### 1. O Conceito de "Overlay Network" (Rede Sobreposta)

Imagine que a internet física são as estradas e cabos que ligam as cidades. A **rede sobreposta** é como um clube exclusivo que criamos usando essas estradas.

- **A lógica:** Os nós (computadores) se conectam virtualmente. Para o sistema, o seu vizinho na rede P2P pode estar no Japão, mesmo que, fisicamente, ele esteja a milhares de quilômetros.

### 2. Redes Não Estruturadas: O Caos Organizado

O texto foca nas redes **não estruturadas**. Pense nelas como uma festa onde as pessoas chegam e conversam com quem estiver mais perto, sem lugares marcados.

- **O Problema da Busca:** Se você está procurando um livro nessa festa e não sabe quem o tem, você pergunta para o seu vizinho. Se ele não sabe, ele grita para os vizinhos dele. Isso é o que chamamos de **Inundação (Flooding)**.

- **Eficiência:** É baixa. Muita gente gritando ao mesmo tempo (tráfego de rede) e, às vezes, o livro está na festa, mas o seu grito não chegou até a pessoa que o tem.

---

### 3. O Exemplo do Gnutella

O Gnutella é o exemplo clássico dessa "festa". Vamos ver como ele funciona na prática:

| **Etapa**         | **O que acontece?**                                                                                                                                   |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bootstrap**     | Quando você instala o programa, ele já vem com uma "listinha de contatos" inicial para você não ficar sozinho.                                        |
| **Ping e Pong**   | São "oi" e "estou aqui". O nó manda um **Ping** para ver quem está vivo; quem responde com um **Pong** se torna seu vizinho ativo.                    |
| **A Busca**       | Você pergunta pelo arquivo "Musica.mp3". Se o vizinho não tem, ele repassa a pergunta. Quando alguém acha, te manda o endereço de quem tem o arquivo. |
| **Transferência** | A busca é feita pela rede P2P, mas o download em si geralmente usa protocolos comuns, como o **HTTP**.                                                |

---

### 4. A Evolução: Folhas e Ultranós

Como o sistema de "gritar para todo mundo" (inundação) não escala bem — ou seja, a rede trava se tiver milhões de usuários — o Gnutella evoluiu para um sistema **hierárquico**:

- **Folhas (Leaves):** São os usuários comuns. Eles apenas pedem coisas e não precisam se preocupar em passar mensagens de outros para frente.

- **Ultranós (Ultranodes):** São os "hubs". Computadores com internet rápida e mais potentes que organizam o tráfego das folhas, funcionando como pequenos centros de busca regionais.

> **Resumindo:** Uma rede P2P descentralizada não estruturada é como uma grande teia democrática onde a informação é encontrada no "boca a boca". É resiliente (se um nó sai, a rede continua), mas gasta muita energia e dados tentando achar o que você quer.

---

### Redes Estruturadas

    Uma rede estruturada utiliza um conjunto predefinido de regras para ligar nós para que as consultas sejam efetiva e eficientemente resolvidas. A técnica mais comum utilizada com essa finalidade é a Tabela de Hash Distribuída (DHT – Distributed Hash Table). A DHT é usada em muitas aplicações, incluindo Estrutura de Dados Distribuída (DDS – Distributed Data Structure), Sistemas de Conteúdos Distribuídos (CDS – Content Distributed Systems), Sistema de Nomes de Domínio (DNS – Domain Name System) e compartilhamento de arquivos P2P. Um protocolo de compartilhamento de arquivos P2P popular que usa DHT é o BitTorrent. Discutiremos o conceito de DHT independentemente na próxima seção como uma técnica que pode ser utilizada tanto em redes P2P estruturadas como em outros sistemas.

**2.4.2 Tabela de Hash Distribuída**
    Uma Tabela de Hash Distribuída (DHT – Distributed Hash Table) distribui dados (ou referências a dados) entre um conjunto de nós de acordo com algumas regras predefinidas. Cada peer em uma rede baseada em DHT torna-se responsável por uma série de dados. Para evitar a sobrecarga causada pelas inundações que discutimos no caso das redes P2P não estruturadas, redes baseadas em DHT permitem que cada peer tenha conhecimento parcial sobre a rede toda. Este conhecimento pode ser utilizado para rotear as consultas por itens até os nós responsáveis por eles, usando procedimentos eficazes e escaláveis que iremos discutir em breve.

**Espaço de endereços**
    Em uma rede baseada em DHT, cada peer e cada conjunto de dados é mapeado para um ponto em um grande espaço de endereços de tamanho 2 ^ m. O espaço de endereços é concebido usando aritmética modular, o que significa que podemos pensar nos pontos do espaço de endereços como se eles fossem distribuídos uniformemente sobre um círculo com 2 ^ m pontos (0 a 2 ^ m -1), em sentido horário, conforme apresentado na figura 2.47. A maioria das implementações de DHT usa m = 160.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2020-50-29.png)

**Calculando o hash do identificador do peer**
    O primeiro passo na criação do sistema DHT é colocar todos os peers sobre o anel que representa o espaço de endereços. Para isso, é usada uma função que calcula o hash do identificador do peer, normalmente seu endereço IP, mapeando-o para um inteiro de m bits chamado de ID de nó. 

*ID do nó = hash (Endereço IP do peer)*
    Uma função de hash é uma função matemática que cria uma saída a partir de uma entrada. No entanto, a DHT utiliza alguma das funções de hash criptográficas, como os algoritmos da família Algoritmo de Hash Seguro (SHA – Secure Hash Algorithm) que são resistentes à colisão, o que significa que a probabilidade de duas entradas serem mapeadas para a mesma saída é muito baixa. Discutiremos esses algoritmos de hash no Capítulo 10.

**Calculando o hash do identificador do objeto** 

    A função de hash também é aplicada sobre o nome do objeto (por exemplo, um arquivo) a ser com-partilhado, criando um inteiro de m bits no mesmo espaço de endereços. O resultado, no jargão da DHT, é chamado chave.
*chave = hash (Nome do objeto)*

    Na DHT, um objeto costuma ser identificado pelo par (chave, valor) no qual a chave é o hash do nome do objeto e o valor é o objeto ou uma referência ao objeto.

**Armazenando o objeto** 

    Existem duas estratégias para armazenar um objeto: o método direto e o indireto. No método direto, o objeto é armazenado no nó cujo ID seja de alguma forma o mais próximo à chave no anel. O termo mais próximo é definido de forma diferente em cada protocolo. Essa estratégia muito provavelmente envolve a transferência do objeto, que é movido do computador onde originalmente se encontrava. No entanto, a maioria dos sistemas de DHT utiliza o método indireto devido à sua maior eficiência. O peer que possui o objeto conserva esse objeto, mas uma referência para ele é criada e armazenada no nó cujo ID é o mais próximo ao ponto correspondente a sua chave. Ou seja, o objeto físico e a referência ao objeto são armazenados em dois locais distintos. Na estratégia direta, criamos um relacionamento entre o ID do nó que armazena o objeto e a chave dele; na indireta, criamos um relacionamento entre a referência (ponteiro) para o objeto e o nó que a armazena. Em ambos os casos, algum relacionamento é necessário para encontrar o objeto quando o nome do objeto é fornecido. Usaremos o método indireto no restante desta seção.

Embora o valor normal de m seja 160, para efeitos de demonstração, usamos m = 5 para facilitar o tratamento dos nossos exemplos. Na Figura 2.48, consideramos que vários peers já se juntaram ao grupo. O nó N5, cujo endereço IP é 110.34.56.20, tem um arquivo chamado Liberdade que quer compartilhar com seus pares. O nó calcula o hash do nome do arquivo, “Liberdade”, para obter a chave = 14. Como o nó mais próximo à chave 14 é o nó N17, o nó N5 cria uma referência para o nome do arquivo (chave), seu endereço IP, e o número da porta (e possivelmente algumas outras informações sobre o arquivo) e envia tal referência para ser armazenada no nó N17. Em outras palavras, o arquivo é armazenado em N5, a chave do arquivo é C14 (um ponto no anel DHT), mas a referência para o arquivo é armazenada no nó N17. Veremos mais adiante como os outros nós podem primeiramente encontrar N17, extrair a referência e então usá-la para acessar o arquivo Liberdade. Nosso exemplo mostra apenas uma chave no anel, mas em uma situação real, há milhões de chaves e nós no anel.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2020-54-23.png)

**Figura 2.48** *Esquema para o Exemplo 2.15.*

<mark>Explicação IA</mark>

Essa explicação detalha o funcionamento de uma **Rede Estruturada P2P** baseada em **DHT (Tabela de Hash Distribuída)**. Para entender esse conceito, imagine que em vez de uma lista centralizada de arquivos (como um servidor do Google), a "lista telefônica" da rede é picada em mil pedaços e espalhada entre todos os usuários.

Aqui está o resumo dos pontos principais para facilitar a compreensão:

---

## 1. O Espaço de Endereçamento (O Anel)

Imagine um círculo numerado de $0$ até $2^m - 1$.

- No exemplo da imagem, $m = 5$, então o círculo vai de **0 a 31**.

- Tudo na rede (tanto as pessoas/computadores quanto os arquivos) ganha um "endereço" dentro desse círculo através de uma função de **Hash**.

## 2. Identificação: Nós vs. Chaves

A DHT trata computadores e arquivos de forma matemática:

- **Nó (Node):** É o computador do usuário. O endereço dele no anel é o `hash(Endereço IP)`. Na imagem, o computador com IP `110.34.56.20` virou o **Nó N5**.

- **Chave (Key):** É o identificador do arquivo. O endereço dele no anel é o `hash(Nome do Arquivo)`. O arquivo "Liberdade" virou a **Chave 14**.

## 3. Quem guarda o quê? (A Regra da Proximidade)

Esta é a regra de ouro: **Um arquivo (ou sua referência) pertence ao nó cujo ID é o sucessor mais próximo da sua chave no sentido horário.**

No exemplo da Figura 2.48:

1. O arquivo "Liberdade" gerou a **Chave 14**.

2. Olhando o anel, o próximo nó ativo após o número 14 é o **N17**.

3. Portanto, o **N17** é o "bibliotecário" responsável por saber onde o arquivo "Liberdade" está.

## 4. Método Indireto (Eficiência)

O texto menciona que o arquivo físico não sai do computador original.

- O **N5** continua com o arquivo original.

- O **N5** envia apenas uma **referência** (um cartão de visita dizendo: "Eu tenho esse arquivo, meu IP é tal e minha porta é 5200") para o **N17**.

- Quando qualquer outro nó no mundo (como o N25 ou N2) quiser o arquivo "Liberdade", ele calculará o hash do nome, descobrirá que o responsável é o N17, perguntará a ele e receberá o IP do N5 para baixar o arquivo diretamente.

## 5. Como é feito o cálculo do hash

O cálculo do hash é o "coração" da DHT. Ele transforma dados de tamanhos variados (como um endereço IP curto ou um nome de arquivo longo) em um **número inteiro fixo** dentro daquele círculo de $0$ a $2^m-1$.

Aqui está como esse processo funciona tecnicamente:

---

### 1. A Escolha do Algoritmo

Na prática, a maioria das redes DHT (como o BitTorrent ou o IPFS) utiliza a família **SHA (Secure Hash Algorithm)**, especificamente o **SHA-1** ou o **SHA-256**.

- Essas funções são **determinísticas**: se você rodar o hash para o IP "192.168.1.1" mil vezes, o resultado será sempre o mesmo número.

- Elas são **resistentes a colisão**: é quase impossível que dois IPs diferentes resultem no mesmo número de hash.

### 2. O Cálculo para o Nó (Endereço IP)

O sistema pega o endereço IP do computador (e às vezes o número da porta para permitir múltiplos nós na mesma máquina) e o submete à função de hash.

ID*nó* = SH A1("110.34.56.20")  (mod 2 ^ m)

- **Entrada:** O texto ou os bytes do endereço IP.

- **Saída:** Um número binário enorme (160 bits no caso do SHA-1).

- **Ajuste ao Anel:** Como o nosso exemplo usa $m=5$ (espaço de 0 a 31), fazemos uma operação de **módulo** ($2^5 = 32$). O resto da divisão por 32 garante que o resultado caia exatamente em um dos pontos do círculo.

### 3. O Cálculo para o Objeto (Nome do Arquivo)

Para o arquivo, o processo é idêntico, mas a entrada muda. Em vez do IP, usa-se o **identificador único** do conteúdo.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-15-50.png)

- **Importante:** Se você mudar uma única letra no nome do arquivo (ex: "liberdade.mp3" com "l" minúsculo), o hash será um número completamente diferente, jogando o arquivo para outra posição no anel. Isso é chamado de **Efeito Avalanche**.

---

### Resumo do Processo de Mapeamento

Para visualizar como o dado vira o número na imagem que você enviou:

| **Tipo**    | **Dado de Entrada** | **Algoritmo (Exemplo)** | **Operação Módulo** | **Posição no Anel** |
| ----------- | ------------------- | ----------------------- | ------------------- | ------------------- |
| **Nó**      | `110.34.56.20`      | $Hash \to 1093$         | $1093 \pmod{32}$    | **5** (N5)          |
| **Arquivo** | `"Liberdade"`       | $Hash \to 2062$         | $2062 \pmod{32}$    | **14** (C14)        |

### Por que usar Hash e não o IP direto?

1. **Distribuição Uniforme:** O hash "espalha" os nós e arquivos de forma aleatória pelo anel. Isso evita que muitos arquivos fiquem acumulados em um único computador, equilibrando a carga da rede.

2. **Segurança:** Impede que um usuário escolha propositalmente um ID para tentar "roubar" o tráfego de um arquivo específico, já que o hash é imprevisível.

Ficou claro como a matemática "encaixa" cada elemento no seu lugar do círculo? Se quiser, posso explicar como o sistema lida quando dois nós acabam caindo muito perto um do outro!

---

### Por que isso é importante?

- **Escalabilidade:** Não existe um servidor central. Se 1 milhão de pessoas entrarem na rede, o "trabalho" de guardar referências é dividido entre 1 milhão de pessoas.

- **Rapidez:** Com regras matemáticas (como as *Finger Tables*, que o texto menciona que serão discutidas depois), você consegue encontrar qualquer arquivo na rede saltando por poucos nós, em vez de perguntar para todo mundo (inundação).

> **Resumo visual do exemplo:**
> 
> O **Nó 5** tem o arquivo. O arquivo tem o "nome" **14**. O **Nó 17** guarda o endereço do **Nó 5** porque o 17 vem logo após o 14 no círculo.

---

## Roteamento

    A função principal da DHT é rotear uma consulta até o nó responsável por armazenar a referência a um objeto. Cada implementação da DHT usa uma estratégia diferente para o roteamento, mas todas seguem a ideia de que cada nó precisa ter um conhecimento parcial sobre o anel para rotear uma consulta para um nó que esteja mais próximo do responsável.

**Chegada e saída de nós** 

    Em uma rede P2P, cada peer pode ser um desktop ou um laptop, ligado ou desligado. Quando um peer executa o software da DHT, ele entra na rede; quando o computador é desligado ou o peer fecha o software, ele sai da rede. Uma implementação de DHT precisa estabelecer uma estratégia clara e eficiente para lidar com a chegada e partida dos nós e com o efeito disso sobre o restante dos peers. A maioria das implementações de DHT trata a falha de um nó como se ele tivesse saído da rede.

**2.4.3 Chord** 

Existem vários protocolos que implementam sistemas de DHT. Nesta seção, apresentamos três deles: Chord, Pastry e Kademlia. Selecionamos o protocolo Chord por sua simplicidade e sua abordagem elegante para o roteamento de consultas. Em seguida, discutimos o protocolo Pastry porque ele usa uma abordagem diferente do Chord e sua estratégia de roteamento é muito próxima daquela do protocolo Kademlia, que é usado na rede de compartilhamento de arquivos mais popular atual-mente, o BitTorrent. O Chord foi publicado por Stoica et al., em 2001. A seguir, analisaremos brevemente as principais características desse algoritmo.

**Espaço de identificadores**
    Dados e nós no Chord são representados por identificadores de m bits que criam um espaço de identificadores contendo 2m pontos distribuídos em um círculo no sentido horário. Referimo-nos , o que significa que os identificadores são cíclicos, indo
à identificação de um dado como c (de chave) e ao identificador de um peer como N (de nó). A aritmética no espaço é feita em módulo 2m até 2m – 1 e de volta a 0. Embora algumas implementações usem uma função de hash resistente a colisões, como o SHA1 com m = 160, aqui usamos m = 5 para simplificar a discussão. O peer mais próximo para o qual N ≥ c é chamado de sucessor de c e armazena o valor (c, v), onde c é a chave (hash do objeto de dados) e v é o valor (informações sobre o peer servidor que possui o objeto). Ou seja, um objeto de dados, por exemplo, um arquivo, é armazenado no peer que possui aquele objeto, mas o valor do hash do objeto (chave c) e as informações sobre o peer (valor v) são armazenados no sucessor de c na forma do par (c, v). Isso significa que o peer que armazena o objeto de dados e o peer que detém o par (c, v) não são necessariamente os mesmos.

**Tabela de derivação**
    Um nó no algoritmo Chord deve ser capaz de resolver uma consulta: dada uma chave, o nó deve ser capaz de encontrar o identificador do nó responsável por aquela chave ou encaminhar a consulta para outro nó. O encaminhamento, contudo, requer que cada nó possua uma tabela de roteamento. O Chord exige que cada nó conheça m nós sucessores e um predecessor. Cada nó cria uma tabela de roteamento, chamada no Chord de tabela de derivação (finger table), que se parece com a Tabela 2.14. Note que a chave-alvo na linha i é N + 2i – 1. A Figura 2.49 mostra apenas a coluna de sucessores para um anel com alguns nós e chaves.
Perceba que a primeira linha (i = 1) efetivamente fornece o sucessor do nó. Também adicionamos o ID do nó predecessor, algo necessário, como veremos mais adiante.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-22-18.png)

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-22-57.png)

**Interface** 

    Para funcionar, o Chord precisa de um conjunto de operações conhecidas como a interface Chord. Nesta seção, discutimos algumas dessas operações para dar uma ideia do que está por trás do pro-tocolo Chord.

**Busca** 

    A operação mais usada no Chord é provavelmente a busca (lookup). O Chord foi projetado para permitir que seus peers compartilhem os serviços disponíveis. Para encontrar o objeto a ser compartilhado, um peer precisa saber qual é o nó responsável pelo objeto: o peer que armazena uma referência para ele. Mencionamos que, no Chord, um peer que é o sucessor de um conjunto de chaves no anel é o peer responsável por aquelas chaves. Encontrar o nó responsável corresponde, então, a encontrar o sucessor de uma chave. A Tabela 2.15 mostra o código usado para a operação de busca. A função de busca está escrita usando a abordagem top-down. Se o nó é responsável pela chave, ele retorna o seu próprio ID; caso contrário, invoca a função busca_sucessor. A função busca_sucessor invoca a função busca_predecessor. A última função invoca a função busca_predecessor_mais_próximo. A abordagem modular nos permite usar as três funções em outras operações em vez de redefini-las. Discutiremos mais a fundo a função de busca. Se o nó não é responsável pela chave, a função de busca invoca a função busca_sucessor para encontrar o sucessor do ID que lhe foi passado como parâmetro. A codificação da função busca_sucessor pode ser bastante simples se primeiramente encontrarmos o predecessor da chave. O nó predecessor pode facilmente nos ajudar a encontrar o próximo nó no anel, pois o primeiro valor na tabela de derivação do nó predecessor (derivação[1]) nos dá o ID do nó sucessor. Além disso, ter uma função para encontrar o nó predecessor de uma cha-ve pode ser útil para outras funções que escreveremos mais adiante. Infelizmente, um nó normal-mente não consegue encontrar o predecessor de uma chave de forma autônoma; a chave pode estar localizada longe do nó. Como explicamos anteriormente, um nó tem conhecimento limitado sobre os outros; a tabela de derivação contém um máximo de aproximadamente m outros nós (há algumas

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-28-09.png)

duplicações na tabela de derivação). Por isso, o nó precisa da ajuda de outros nós para encontrar o predecessor de uma chave. Isso pode ser feito com a função busca_predecessor_mais_próximo como uma Chamada de Procedimento Remoto (RPC – Remote Procedure Call). Uma RPC consiste em invocar uma função (procedimento) a ser executada em um nó remoto e retornar o resultado ao nó que iniciou a RPC. Utilizamos a expressão x.função no algoritmo, onde x é a identidade do nó remoto e função é o procedimento a ser executado. O nó usa essa função para encontrar outro nó que esteja mais próximo do predecessor do que ele mesmo. Então, passa a tarefa de encontrar o nó predecessor para o outro nó. Em outras palavras, se o nó A quer encontrar o nó X, ele encontra o nó B (um predecessor mais próximo) e passa essa tarefa para B. O nó B entra então em ação e tenta encontrar X, ou passa a tarefa para outro nó, C. O processo continua até que o nó que conhece o nó predecessor o encontra.
Considere que o nó N5 na Figura 2.49 queira encontrar o nó responsável pela chave c14. A Figura 2.50 mostra a sequência de 8 eventos que ocorrem nesse caso. Após o evento 4, no qual a função busca_predecessor_ mais_próximo retorna N10, a função busca_predecessor pede a N10 que retorne o valor de derivação[1], que é N12. Nesse momento, N5 descobre que N10 não é o predecessor de c14. O nó N5, então, pede a N10 que encontre o predecessor mais próximo de c14, que retorna como N12 (eventos 5 e 6). O nó N5 agora pede o valor de derivação[1] do nó N12, que retorna como N20. O nó N5, então, verifica e percebe que N12 é de fato o predecessor de c14. Essa informação é passada para a função busca_sucessor (evento 7). N5 agora pede o va-lor de derivação[1] do nó N12, recebendo como resultado N20. A busca é encerrada e N20 é o sucessor do c14.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-29-53.png)

Explicação IA

Com certeza. Esse assunto (DHT e Chord) parece assustador porque envolve muita "sopa de letrinhas" (N12, c14, RPC, m bits), mas o conceito por trás é muito elegante e simples.

Imagine que o **Chord** é como uma **agenda telefônica gigante em círculo**, onde ninguém tem o número de todo mundo, mas cada um sabe quem são os seus vizinhos e alguns "conhecidos estratégicos" mais distantes.

Aqui está o passo a passo para você nunca mais esquecer:

---

### 1. O Cenário: O Anel

Em vez de uma lista, imagine um relógio (o **Anel**).

- **Os Nós (N):** São os computadores (ex: N5, N10).

- **As Chaves (c):** São os arquivos ou dados que você quer encontrar (ex: c14).

- **A Regra de Ouro:** Quem guarda o arquivo `c14`? É o primeiro computador que vem **depois** dele no sentido horário. No seu desenho (Figura 2.49), o sucessor de `c14` é o `N20`.

### 2. O Problema: "Eu não conheço todo mundo"

Se o nó `N5` quer o arquivo `c14`, ele não sabe de cara que o arquivo está no `N20`. Ele só conhece quem está na sua **Tabela de Derivação (Finger Table)**.

A Tabela de Derivação é como um "atalho": o `N5` conhece quem está logo à frente, um pouco mais à frente, e bem longe do outro lado do anel.

### 3. A Lógica da Busca (O "Pulo do Gato")

Para achar o dono de uma chave, o Chord usa uma estratégia de **"cerco"**:

1. Eu não sei quem é o dono (Sucessor).

2. Então, eu tento achar quem vem **logo antes** do dono (o **Predecessor**).

3. Se eu achar quem vem antes, basta perguntar para esse cara: "Quem é o seu vizinho da direita?". Esse vizinho será, com certeza, o dono do arquivo.

---

### 4. Explicando o seu desenho (A busca de N5 por c14)

Vamos seguir os números da sua **Figura 2.50** como se fosse uma conversa:

- **Evento 1 e 2:** O `N5` quer achar o sucessor de `c14`. Ele começa a rodar a função `busca_predecessor`.

- **Evento 3 e 4:** `N5` olha sua tabela e pensa: *"Quem eu conheço que chega mais perto de c14 sem passar dele?"*. Ele vê que é o `N10`. Ele liga para o `N10` (isso é o tal do RPC) e pergunta: "Você é o cara que vem antes do c14?".

- **Evento 5 e 6:** O `N10` responde: *"Não sou eu, mas eu conheço o `N12`, que está mais perto do c14 do que eu!"*.

- **Evento 7:** O `N5` agora fala com o `N12`. Ele percebe que o `N12` é o último nó antes da chave `c14`. **Bingo!** Achamos o predecessor.

- **Evento 8:** Agora ficou fácil. Se o `N12` é o cara que vem antes, o `N5` pergunta ao `N12`: "Quem é o seu primeiro sucessor (derivação[1])?". O `N12` responde: "É o `N20`".

**Resultado:** O `N5` agora sabe que o arquivo `c14` está guardado no `N20`.

---

### Por que isso é bom?

- **Eficiência:** Você não precisa perguntar de um em um no círculo. Graças aos "atalhos" da tabela de derivação, você pula grandes partes do anel. É como procurar uma palavra no dicionário: você não lê da letra A até a Z, você pula direto para a letra desejada.

- **Escalabilidade:** Se entrarem 1 milhão de computadores, a tabela de cada um continua pequena e a busca continua rápida.

### Resumo das funções (Para a prova):

- **Busca (Lookup):** A pergunta geral ("Onde está o arquivo?").

- **Busca_Sucessor:** A resposta final ("O dono é o nó X").

- **Busca_Predecessor:** A estratégia ("Vou achar quem vem antes do dono").

- **Busca_Predecessor_Mais_Próximo:** O "GPS" ("Quem da minha lista de conhecidos está mais perto do alvo?").

Ficou mais claro agora? Se quiser, podemos detalhar como essa **Tabela de Derivação** é montada matematicamente ($N + 2^{i-1}$)!

---

**Estabilizar**
Antes de discutirmos como os nós entram e saem de um anel, é preciso enfatizar que qualquer alteração no anel (tal como a entrada e saída de um nó ou de um grupo de nós) pode desestabilizar o anel. Uma das operações definidas no Chord é chamada estabilizar. Cada nó no anel periodi-camente utiliza essa operação para validar as informações sobre o seu sucessor e para permitir que ele valide suas informações sobre o predecessor. O nó N usa o valor de derivação[1], S, para pedir ao nó S que retorne seu predecessor, P. Se o valor retornado por essa consulta, P, estiver entre N e S, significa que existe um nó cujo ID é igual a P e que se encontra entre N e S. Então, o nó N faz de P o seu sucessor e notifica P para que o nó N se torne seu antecessor. A Tabela 2.16 ilustra a operação de estabilizar.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-44-09.png)

**Restaurar_Tabela_Derivação**
Desestabilizações do anel podem alterar a tabela de derivação de até m nós. Outra operação definida no Chord é a chamada restaurar_tabela_derivação. Cada nó do anel deve invocar periodicamen-te essa função para manter a tabela de derivação atualizada. Para evitar elevação no tráfego do sistema, cada nó deve atualizar apenas uma das entradas da tabela em cada chamada. A entrada é escolhida aleatoriamente. A Tabela 2.17 mostra o código para a operação.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-45-08.png)

**Associação** 

Quando um peer entra no anel, ele usa a operação associar (join) e o ID de outro peer conhecido para buscar seu sucessor, definindo o predecessor como null (ou seja, vazio). Ele imediatamente invoca a função estabilizar para validar seu sucessor. O nó, então, pede ao seu sucessor que invoque a função mover-chave, que transfere as chaves pelas quais o novo peer será responsável. A Tabela 2.18 mostra o código para essa operação.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-46-05.png)

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-46-30.png)

É óbvio que, após essa operação, a tabela de derivação do nó que associou-se estará vazia e
as tabelas de derivação de até m predecessores estarão desatualizadas. As operações de estabilizar e restaurar_tabela_derivação que são executadas periodicamente após esse evento gradualmente estabilizarão o sistema.

Exemplo 2.17 Considere que o nó N17 associa-se ao anel na Figura 2.49 com a ajuda de N5. A Figura 2.51 mostra o anel após ele ser estabilizado. O processo é mostrado a seguir:

1. N17 usa o algoritmo Inicializar (5) para definir seu predecessor como null e seu sucessor (derivação[1]) como N20.
2. N17 pede, então, que N20 envie c14 e c16 para N17, pois N17 é agora responsável por essas chaves. 3. Após um intervalo limite, N17 usa a operação estabilizar para validar seu próprio sucessor (que é N20) e pede a N20 que mude seu predecessor para N17 (usando a função notificar).
3. Quando N12 usa a função estabilizar, o predecessor de N17 é atualizado para N12. 5. Finalmente, quando alguns nós usam a função restaurar_tabela_derivação, as tabelas de derivação dos nós N17, N10, N5 e N12 são alteradas.
4. **Saída ou falha**
   Se um peer deixa o anel ou se o peer (não o anel) falhar, a operação do anel será interrompida a menos que o anel se estabilize. Cada nó troca mensagens de ping e pong com os seus vizinhos para descobrir se eles estão ativos. Quando um nó não recebe uma mensagem de pong em resposta à sua mensagem de ping, sabe que o seu vizinho está inativo. Embora o uso das operações estabilizar e restaurar_tabela_derivação possam restaurar o anel depois de uma saída ou falha, o nó que detecta o problema pode imediatamente invocar essas operações sem esperar pelo tempo limite para fazê-lo. Um problema importante é que as funções estabilizar e restaurar_tabela_derivação podem não funcionar corretamente se vários nós deixa-rem o anel ou falharem ao mesmo tempo. Por essa razão, o Chord exige que cada nó monitore r sucessores (o valor de r depende da implementação). O nó pode sempre ir para o próximo sucessor se os anteriores não estiverem disponíveis. Outro problema nesse caso é que os dados gerenciados pelo nó que deixou o anel ou falhou já não estarão disponíveis. O Chord estipula que apenas um nó deve ser responsável por um conjunto de dados e referências, mas o Chord também exige que os dados e referências sejam duplicados em outros nós, nesse caso.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-47-41.png)

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-48-03.png)

O processo é mostrado a seguir:

1. O nó N5 percebe a saída de N10 quando não recebe uma mensagem de pong em resposta a sua mensagem de ping. O nó N5 muda seu sucessor (o valor de derivação [1]) para N12 (o segundo na lista de sucessores).
2. O nó N5 ativa imediatamente a função estabilizar e pede a N12 que mude seu predecessor para N5.
3. Com sorte, as chaves c7 e c9, que estavam sob a responsabilidade de N10, foram duplica-das em N12 antes da saída de N10.
4. Depois de algumas invocações à função restaurar_tabela_derivação, os nós N5 e N25 atualizam suas tabelas de derivação, conforme mostrado na figura.
   Aplicações
   O Chord é usado em diversas aplicações, incluindo o Sistema de Arquivos Colaborativo (CFS – Collaborative File System), Con-Chord e o Sistema de Nomes de Domínio Distributivo (DDNS – Distributive Domain Name System).
   2.4.4 Pastry Outro protocolo popular que segue o paradigma P2P é o Pastry, concebido por Rowstron e Druschel.
   O Pastry utiliza uma DHT, como descrito anteriormente, mas existem algumas diferenças funda-mentais entre o Pastry e o Chord no que diz respeito ao espaço de identificadores e ao processo de roteamento, que descreveremos a seguir.
   Espaço de identificadores
   No Pastry, assim como no Chord, os nós e os dados são representados por identificadores de m bits, criando um espaço de identificadores com 2m
   no sentido horário. Um valor comum para m é 128. O protocolo usa o algoritmo de hash SHA-1 com m = 128. No entanto, nesse protocolo, um identificador é visto como uma cadeia de n dígitos na base 2b
   de pontos distribuídos uniformemente em um círculo , onde b é normalmente 4 e n = (m/b). Em outras palavras, um identificador é um número de
   32 dígitos na base 16 (hexadecimal). Nesse espaço de identificadores, cada chave é armazenada no nó cujo identificador é numericamente mais próximo da chave, estratégia definitivamente diferente daquela utilizada pelo Chord. No Chord, uma chave é armazenada em seu nó sucessor; no Pastry, uma chave é armazenada no nó que for numericamente mais próximo da chave, podendo ser ele o nó sucessor ou predecessor.
   Roteamento
   Um nó no Pastry deve ser capaz de resolver uma consulta; dada uma chave, o nó deve encontrar o identificador do nó responsável por ela ou encaminhar a consulta para outro nó. Cada nó no Pastry usa duas entidades para fazer isso: uma tabela de roteamento e um conjunto de folhas.
   Tabela de roteamento O Pastry exige que cada nó mantenha uma tabela de roteamento com n linhas e (2b
   geral, quando m = 128 e b = 4, temos 32 (128/4) linhas e 16 colunas (2128 = 1632 ) colunas. Em ). Ou seja, temos
   uma linha para cada dígito do identificador e uma coluna para cada valor hexadecimal (0 a F). A Tabela 2.19 mostra a estrutura básica da tabela de roteamento para o caso geral. Na tabela para o nó N, a célula na linha i e coluna j (ou seja, o valor de Tabela [i, j]) fornece o identificador de um nó (caso ele exista) cujos i dígitos mais à esquerda coincidem com aqueles do identificador de N e cujo dígito na posição (i + 1) vale j. A primeira linha, 0, mostra a lista de nós ativos cujos identificadores não têm um prefixo em comum com N. A linha 1 mostra uma lista de nós ativos de mesmo dígito mais à esquerda que o identificador do nó N. De maneira similar, a linha 31 mostra a lista de todos os nós ativos que compartilham os 31 dígitos mais à esquerda com o nó N, tendo apenas o último dígito diferente.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-49-17.png)

Por exemplo, se N = (574A234B12E374A2001B23451EEE4BCD)16 , então o valor de Tabela
[2, D] pode ser o identificador de um nó tal como (57D...). Perceba que os dois dígitos mais à esquerda são 57, que coincidem com os dois primeiros dígitos de N, mas o próximo dígito é D, o valor correspondente à D-ésima coluna. Se houver mais nós com o prefixo 57D, o mais próximo, de acordo com a métrica de proximidade definida, é o escolhido, e seu identificador é inserido nesta célula. A métrica de proximidade é uma medida de distância determinada pela aplicação que usa a rede, e pode ser baseada no número de saltos entre os dois nós, no RTT entre os dois nós ou em outras métricas.
Conjunto de folhas Outra entidade utilizada no roteamento é um conjunto de 2b
identificadores (o tamanho de uma
linha na tabela de roteamento) chamado conjunto de folhas (leaf set). Metade do conjunto consiste em uma lista de identificadores numericamente menores do que o identificador do nó atual; a outra metade é uma lista de identificadores numericamente maiores do que o identificador do nó atual. Ou seja, o conjunto de folhas fornece os identificadores de 2b–1 nós que vêm depois do nó atual no anel.
nós ativos que antecedem o nó atual no anel e a lista de 2b–1
Exemplo 2.19 Consideremos que m = 8 bits e b = 2. Isto significa que pode haver até 2m
tificador tem m/b = 4 dígitos na base 2b = 256 identificadores, e cada iden-= 4. A Figura 2.53 mostra a situação em que há alguns nós ativos e
algumas chaves mapeadas para esses nós. A chave c1213 é armazenada em dois nós porque é equidistante em relação à deles. Isto fornece alguma redundância que pode ser usada se um dos nós falhar. A figura também mostra as tabelas de roteamento e os conjuntos de folhas para quatro nós selecionados utilizados nos exemplos descritos a seguir. Na tabela de roteamento para o nó N0302, por exemplo, escolhemos o nó 1302 para ser inserido em Tabela [0,1] porque consideramos que ele está mais próximo de N0302 de acordo com a métrica de proximidade empregada. Usamos a mesma estratégia para as outras entradas. Observe que uma célula em cada linha de cada tabela foi sombreada porque corresponde ao dígito do identificador do nó e, portanto, ne-nhum identificador de nó pode ser ali inserido. Existem também algumas células vazias porque não existem nós ativos na rede no momento que satisfaçam os requisitos para preenchê-la; quando alguns novos nós entrarem na rede, eles poderão ser inseridos nestas células.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-50-03.png)

Busca
Como discutido para o Chord, uma das operações utilizadas no Pastry é a busca (lookup): dada uma chave, é preciso encontrar o nó que armazena as informações sobre ela ou a própria chave. A Tabela 2.20 descreve a operação de busca em pseudocódigo. Nesse algoritmo, N é o identifica-dor do nó local, o nó que recebe uma mensagem e precisa encontrar o nó que armazena a chave definida na mensagem.
Exemplo 2.20 Na Figura 2.53, consideramos que o nó N2210 recebe uma consulta em busca do nó responsável pela chave 2008. Como ele não é responsável pela chave, ele primeiro verifica o seu conjunto de folhas. A chave 2008 não se encontra entre os valores em seu conjunto de folhas, de modo que o nó precisa utilizar a sua tabela de roteamento. Uma vez que o comprimento do prefixo em comum é 1, p = 1. O valor do dígito na posição 1 da chave é v = 0. O nó verifica o identificador em Tabela [1, 0], que é de 2013. A consulta é encaminhada para o nó 2013, que é de fato responsável pela chave. Ele envia sua informação para o nó que efetuou a consulta.
Exemplo 2.21 Na Figura 2.53, consideramos que o nó N0302 recebe uma consulta em busca do nó responsável pela chave 0203. Ele não é responsável pela chave, mas ela está em seu conjunto de folhas. O nó mais próximo nesse conjunto é o nó N0202. A consulta é enviada para esse nó, que é de fato responsável pela chave. O nó N0202 envia sua informação para o nó que efetuou a consulta.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-50-43.png)

**Associação**
O processo de entrada no anel do Pastry é mais simples e mais rápido do que no Chord. O novo nó, X, deve conhecer pelo menos um nó N0, que deve estar próximo de X (baseado na métrica de proxi-midade usada); isso pode ser feito por meio da execução de um algoritmo denominado Descoberta de Nó Vizinho (Nearby Node Discovery). O nó X envia uma mensagem de associação (join) para N0. Em nossa discussão, consideraremos que o identificador N0 não tem um prefixo em comum com o identificador X. Os passos a seguir mostram como o nó X cria sua tabela de roteamento e conjunto de folhas:

1. O nó N0 envia o conteúdo de sua linha 0 para o nó X. Como os dois nós não têm um prefixo comum, o nó X usa as partes apropriadas dessa informação para construir sua linha 0. O nó N0, então, trata a mensagem de associação como uma mensagem de busca, assumindo que o identificador X é uma chave. Ele encaminha a mensagem de associação a um nó, N1, cujo identificador é o mais próximo de X.
2. O nó N1 envia o conteúdo de sua linha 1 para o nó X. Como os dois nós têm um prefixo em comum, o nó X usa as partes apropriadas da informação para construir a sua linha 1. O nó N1, então, trata a mensagem de associação como uma mensagem de busca, assumindo que o identificador X é uma chave. Ele encaminha a mensagem de associação a um nó, N2, cujo identificador é o mais próximo de X.
3. O processo continua até que a tabela de roteamento do nó X esteja completa. 4. O último nó do processo, que tem o mais longo prefixo em comum com X, também envia seu conjunto de folhas para o nó X, o qual passa a ser o conjunto de folhas de X.
4. O nó X, então, troca informações com nós em sua tabela de roteamento e o conjunto de folhas para aprimorar a própria informação de roteamento e também para permitir que aqueles nós atualizem suas informações.

Exemplo 2.22 A Figura 2.54 mostra como um novo nó X cujo identificador é N2212 utiliza as informações de quatro nós da Figura 2.53 para criar a sua tabela de roteamento e conjunto de folhas iniciais, assim que ele se associa ao anel. Perceba que o conteúdo dessas duas tabelas se aproximará do esperado ao longo do processo de atualização. Nesse exem-plo, consideramos que o nó 0302 seja um nó próximo ao nó 2212 com base na métrica de proximidade utilizada.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-51-36.png)

Saída ou falha Cada nó do Pastry periodicamente testa se os nós em seu conjunto de folhas e em sua tabela de roteamento continuam ativos por meio de mensagens de sondagem (probe messages). Se um nó local descobre que um nó em seu conjunto de folhas não está respondendo às mensagens de sonda-gem, ele considera que o nó falhou ou deixou o anel. Para substituí-lo em seu conjunto de folhas, o nó local contacta o nó ativo de seu conjunto de folhas que tenha o identificador mais elevado, reparando seu conjunto de folhas com as informações provenientes daquele nó. Como existe uma sobreposição no conjunto de folhas de nós próximos, esse processo é bem-sucedido. Se um nó local descobre que outro em sua tabela de roteamento, Tabela [i, j], não responde às
mensagens da sondagem, ele envia uma mensagem a um nó ativo na mesma linha e pede o identi-ficador na posição Tabela [i, j] dele. Esse identificador substitui o nó que falhou ou deixou o anel.
Aplicação
O Partry é usado em algumas aplicações, incluindo PAST, um sistema de arquivos distribuído, e SCRIBE, um sistema descentralizado de publicação/assinatura.
2.4.5 Kademlia Outra rede peer-to-peer baseada em DHT é o Kademlia, concebido por Maymounkov e Mazières. O Kademlia, assim como o Pastry, roteia mensagens de acordo com a distância entre os nós, mas a interpretação da métrica de distância no Kademlia é diferente da adotada no Pastry, como descreve-remos a seguir. Na rede Kademlia, a distância entre dois identificadores (sejam eles nós ou chaves) é medida usando a operação de ou-exclusivo (XOR) bit a bit entre tais identificadores. Em outras palavras, se X e Y são dois identificadores, temos
distância (x, y) = x ⊕ y 

A métrica baseada em XOR tem quatro propriedades que esperamos obter quando usamos distâncias geométricas entre dois pontos, mostradas a seguir: 

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-52-29.png)

Espaço de identificadores
No Kademlia, nós e dados são representados usando identificadores de m bits que criam um espaço de identificadores contendo 2m
usa o algoritmo de hash SHA-1 com m = 160.
Exemplo 2.23 Por razões de simplicidade, consideremos que m = 4. Neste espaço, podemos ter 16 identificadores distribuídos pelas folhas de uma árvore binária. A Figura 2.55 mostra esse caso com apenas oito nós ativos e cinco chaves.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-52-57.png)

 c7 pareça numericamente equidistante de N6 e N8, ela é armazenada apenas em N6 porque 6 ⊕ 7 = 1, enquanto 6 ⊕ 8 = 14. Outro ponto interessante é que a chave c12 é numericamente mais próxima de N11, mas é armazenada em N15 porque 11 ⊕ 12 = 7, enquanto 15 ⊕ 12 = 3.

**Tabela de roteamento**
O Kademlia mantém apenas uma tabela de roteamento para cada nó; não existe um conjunto de folhas. Cada nó na rede divide a árvore binária em m subárvores que não incluem o próprio nó. A subárvore i inclui os nós que compartilham os i bits mais à esquerda (prefixo em comum) com o nó correspondente. A tabela de roteamento é composta por m linhas, mas apenas uma coluna. Durante nossa discussão, consideraremos que cada linha contém o identificador de um dos nós na subárvore correspondente, mas depois mostramos que o Kademlia permite até k nós em cada linha. A ideia é a mesma utilizada no Pastry, mas o comprimento do prefixo em comum baseia-se no número de bits em vez do número de dígitos na base 2b
. A Tabela 2.21 mostra a tabela de roteamento. 

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-53-34.png)

Exemplo 2.24 Encontraremos a tabela de roteamento para o Exemplo 2.23. Para simplificar o exemplo, consideramos que cada linha utiliza apenas um identificador. Como m = 4, cada nó possui quatro subárvores correspondentes às quatro linhas na tabela de roteamento. O identificador em cada uma representa o nó que está mais próximo do nó atual na subárvore correspondente. A Figura 2.56 mostra todas as tabelas de roteamento, mas apenas três das subárvores. Escolhemos apenas três, de um total de oito, para reduzir o tamanho da figura.
Explicaremos como foi feita a tabela de roteamento, por exemplo, para o nó 6, usando as subárvores correspon-dentes. As explicações para os outros nós são equivalentes.
a. Na linha 0, precisamos inserir o identificador do nó mais próximo na subárvore com prefixo em comum de comprimento p = 0. Há três nós nessa subárvore (N8, N11 e N15), mas N15 é o mais próximo de N6 porque N6 ⊕ N8 = 14, N6 ⊕ N11 = 13 e N6 ⊕ N15 = 9. N15 é inserido na linha 0.
b. Na linha 1, precisamos inserir o identificador do nó mais próximo na subárvore com prefixo em comum de comprimento p = 1. Há três nós nessa subárvore (N0, N1 e N3), mas N3 é o mais próximo de N6 porque N6 ⊕ N0 = 6, N6 ⊕ N1 = 7 e N6 ⊕ N3 = 5. N3 é inserido na linha 1.
c. Na linha 2, precisamos inserir o identificador do nó mais próximo na subárvore com prefixo em comum de comprimento p = 2. Há apenas um nó nessa subárvore (N5), que é aqui inserido.
d. Na linha 3, precisamos inserir o identificador do nó mais próximo na subárvore com prefixo em comum de comprimento p = 3. Não há nós nessa subárvore, então a linha fica vazia.
Exemplo 2.25 Na Figura 2.56, consideramos que o nó N0 (0000)2
responsável por c12 (1100)2 recebe uma mensagem de busca tendo como alvo o nó
. O comprimento do prefixo em comum entre os dois identificadores é 0. O nó N0 . O comprimento do prefixo em comum entre os dois iden-encaminha a mensagem para o nó na linha 0 de sua tabela de roteamento, o nó N8. Agora, o nó N8 (1000)2 precisa procurar o nó mais próximo de c12 (1100)2
tificadores é 1. O nó N8 encaminha a mensagem para o nó na linha 1 de sua tabela de roteamento, o N15, o qual é responsável por c12. O processo de roteamento se encerra. A rota é N0 → N8 → N15. É interessante notar que o nó N15, (1111)2
, e c12, (1100)2, têm um prefixo em comum de comprimento 2, mas a linha 2 de N15 está vazia, o que significa que o próprio N15 é responsável por c12.
Exemplo 2.26 Na Figura 2.56, consideramos que o nó N5 (0101)2
responsável por c7 (0111)2 recebe uma mensagem de busca tendo como alvo o nó . O comprimento do prefixo em comum entre os dois identificadores é 2. O N5 envia
a mensagem para o nó na linha 2 de sua tabela de encaminhamento, o N6, que é o responsável por c7. O processo de roteamento se encerra. A rota é N5 → N6.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-54-22.png)

Exemplo 2.27 

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-58-13.png)

k-bucket. Ter mais do que um nó em cada linha permite que o nó tenha alternativas quando outro deixa a rede ou falha. O Kademlia mantém em um balde os nós que ficaram conectados na rede por um longo tempo. Prova-se que os nós que estão conectados há um longo tempo provavelmente permanecerão conectados por um longo tempo.
Consulta em paralelo Como existem vários nós em um k-bucket, o Kademlia permite o envio de a consultas em paralelo para a nós no topo do k-bucket. Isto reduz o atraso se um nó falhar e não puder responder à consulta.
Atualização simultânea
Outra característica interessante do Kademlia é a atualização simultânea. Sempre que um nó recebe uma consulta ou uma resposta, ele atualiza seu k-bucket. Se várias consultas enviadas a um nó não apresentam resposta, o nó que enviou a consulta pode remover o nó destino do k-bucket correspondente.
Associação
Assim como no Pastry, um nó que deseja entrar na rede precisa conhecer pelo menos um outro nó. O nó ingressante envia seu identificador para o nó como se fosse uma chave a ser encontrada. A resposta recebida permite que o novo nó crie seus k-buckets.
Saída ou falha
Quando um nó deixa a rede ou falha, outros nós atualizam seus k-buckets usando o processo simul-tâneo descrito anteriormente.
2.4.6 Uma rede P2P popular: o BitTorrent O BitTorrent é um protocolo P2P projetado por Bram Cohen para compartilhar arquivos grandes entre grupos de peers. No entanto, o termo compartilhar nesse contexto é diferente daquele usado em outros protocolos de compartilhamento de arquivos. Em vez de um peer permitir que outro peer faça o download do arquivo completo, um grupo de peers participa do processo para propiciar a todos os peers do grupo uma cópia do arquivo. O compartilhamento de arquivos é feito por meio de um processo colaborativo chamado torrent. Cada peer participando em um torrent obtém pedaços do arquivo grande de outro peer que tenha tal arquivo e, ao mesmo tempo, fornece pedaços do arquivo para outros peers que não o possuem em uma espécie de tit-for-tat, um jogo de negociação jogado por crianças*
. O conjunto de todos os peers que participam em um torrent é denominado
swarm, ou enxame. Um peer com arquivo de conteúdo completo de um enxame é chamado seed, ou semente; um peer que tem apenas parte do arquivo e quer obter o restante do mesmo é chamado leech, ou sanguessuga. Em outras palavras, um enxame é uma combinação de seeds e leeches. O BitTorrent passou por várias versões e apresenta muitas implementações. Em primeiro lugar, descreveremos a versão original, que utiliza um nó central chamado tracker, ou rastreador. Em se-guida, mostraremos como algumas novas versões eliminam o tracker por meio do uso de uma DHT.
BitTorrent com um tracker
O BitTorrent original apresenta outra entidade em um torrent, chamada tracker (ou rastreador), que, como o nome sugere, monitora a operação enxame, conforme descrito mais adiante. A Figura 2.57 mostra um exemplo de um torrent com seeds, leeches e o tracker. Na figura, o arquivo a ser compartilhado, o arquivo de conteúdo, é dividido em cinco partes (conhecidas como pedaços, ou chunks). Os peers 2 e 4 já têm todos os pedaços, enquanto os

* N. de T.: O tit-for-tat refere-se a negociações no estilo “olho por olho”, ou “é dando que se recebe”.

![](/home/carlos/Imagens/Capturas%20de%20tela/Captura%20de%20tela%20de%202026-04-09%2021-58-58.png)

outros têm apenas alguns deles. Os pedaços que cada peer já possui estão sombreados. O upload e o download de pedaços são contínuos. Alguns peers podem deixar o torrent, enquanto novos peers podem passar a participar dele. Agora, considere que um novo peer quer obter esse mesmo arquivo de conteúdo. O novo peer acessa o servidor BitTorrent e fornece o nome do arquivo de conteúdo; recebe um metarquivo com o nome do arquivo de torrent, o qual contém as informações sobre os pedaços do arquivo de con-teúdo e o endereço do tracker que gerencia esse torrent em específico. O novo peer, então, acessa o tracker e recebe os endereços de alguns peers no torrent, normalmente chamados vizinhos. O novo peer é agora parte do torrent e pode obter e enviar partes do arquivo de conteúdo. Quando tiver todos os pedaços, ele pode abandonar o torrent ou permanecer nele com o intuito de ajudar outros peers, incluindo os novos que entraram no enxame depois dele, a obter todos os pedaços do arquivo de conteúdo. Nada impede que um peer abandone o torrent antes de obter todos pedaços e depois volte a participar do enxame mais tarde ou de não voltar novamente. Embora os processos de entrar, compartilhar e deixar um torrent possam parecer simples, o
protocolo BitTorrent aplica uma série de políticas com o objetivo de garantir equidade, para incen-tivar os peers a trocar pedaços com outros peers, evitar a sobrecarga de um peer com os pedidos dos outros e permitir que um peer encontre outros que forneçam melhores serviços. Para evitar a sobrecarga de um peer e garantir equidade na rede, cada peer precisa limitar o
número de conexões simultâneas com seus vizinhos; o valor tipicamente adotado é quatro. Um peer marca um vizinho como unchoked (desbloqueado) ou choked (bloqueado), e também os classifica como interessados ou desinteressados. Em outras palavras, um peer divide suas listas de vizinhos em dois grupos distintos: unchoked
e choked. Também os divide nos grupos interessado e desinteressado . O grupo unchoked refere-se à lista dos peers aos quais o peer atual está simultaneamente conectado; ele envia e recebe pedaços desse grupo sem parar. O grupo choked refere-se à lista de vizinhos aos quais o peer não está atual-mente conectado, mas aos quais ele pode se conectar no futuro. A cada 10 segundos, o peer atual conecta-se a um peer do grupo interessado que esteja choked, na esperança de conseguir uma melhor taxa de transferência de dados. Se o novo peer fornece uma er bloqueado, passando, então, para o grupo choked. Assim, os peers no grupo unchoked sempre têm a maior taxa de transferência de dados dentre os peers testados. A aplicação dessa estratégia divide os vizinhos em subgrupos, de modo que os vizinhos com taxas de transferência de dados compatíveis comuniquem-se uns com os outros. A ideia da estratégia de negociação tit-for-tat descrita anterior-mente pode ser observada nessa política, que segue o estilo “é dando que se recebe”. Para permitir que um peer recém-chegado, sem pedaços para compartilhar, também seja capaz de receber pedaços de outros, a cada 30 segundos um peer aleatoriamente desbloqueia um único peer do grupo interessado (ou seja, promove-o do grupo choked para o grupo unchoked) independentemente de sua taxa de upload. Essa ação é chamada optimistic unchoking, ou desbloqueio otimista. O protocolo BitTorrent tenta proporcionar um equilíbrio entre o número de pedaços que cada peer pode ter a cada instante usando uma estratégia chamada rarest-first (o mais raro primeiro). Nela, um peer tenta primeiro fazer o download dos pedaços com o menor número de cópias repeti-das dentre seus vizinhos; assim, os pedaços são distribuídos mais rapidamente.

BitTorrent sem tracker
No projeto original do BitTorrent, se o tracker falhar, novos peers não podem se conectar à rede e o processo de atualização dos nós é interrompido. Existem várias implementações do BitTorrent que eliminam a necessidade de um tracker centralizado. Na implementação que descrevemos aqui, o protocolo ainda usa o tracker, mas ele não é centralizado. A tarefa de rastreamento é distribuída dentre alguns nós na rede. Nesta seção, mostramos como a DHT do Kademlia pode ser usada para atingir esse objetivo, mas evitamos mostrar em detalhes o protocolo em específico. No BitTorrent com um tracker central, a tarefa do tracker é fornecer uma lista de peers em um
enxame dado um arquivo de metadados que define o torrent. Se pensarmos no hash dos metada-dos como sendo a chave e no hash da lista de peers em um enxame como sendo o valor, podemos deixar alguns nós em uma rede P2P desempenhar o papel de trackers. Um novo peer que entra no torrent envia o hash dos metadados (chave) para o nó que ele conhece. A rede P2P usa o protocolo Kademlia para encontrar o nó responsável pela chave. Este envia o valor, que na verdade é a lista de peers no torrent correspondente, para o peer entrante. Agora, o peer entrante pode usar o proto-colo BitTorrent para compartilhar o arquivo de conteúdo com os peers presentes na lista recebida.
