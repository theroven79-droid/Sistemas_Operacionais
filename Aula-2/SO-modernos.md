# 🖥️ A Evolução dos Sistemas Operacionais 🚀


## 📚 Resumo Profundo: Das Válvulas aos Smartphones 📱


**Baseado em:** *Sistemas Operacionais Modernos (4ª Edição)* — Andrew S. Tanenbaum e Herbert Bos (Seções 1.2.1 a 1.2.5).


---

### 📜 Pré-História da Computação


Antes mesmo de dividirmos a história dos sistemas operacionais (e da computação em si) em gerações formais, é estritamente necessário voltarmos ao século XIX.


* **Charles Babbage (1792-1871):**

  * O matemático inglês projetou o que é considerado o primeiro computador verdadeiramente digital, chamado de *máquina analítica*.

  * Ele gastou grande parte da sua vida e da sua fortuna tentando construí-la.

  * Infelizmente, a máquina nunca funcionou de verdade. O motivo? Ela era puramente mecânica e a tecnologia de manufatura da época simplesmente não conseguia produzir as engrenagens e rodas com a altíssima precisão necessária.


* **A Primeira Programadora:**

  * Babbage, sendo um visionário, percebeu que sua máquina precisaria de *software*.

  * Ele contratou Ada Lovelace (filha do poeta Lord Byron).

  * Ada tornou-se a primeira programadora do mundo.

  * Hoje, a linguagem de programação de alto nível `Ada®` carrega o seu nome como homenagem.


* **Sistemas Operacionais nesta época:**

  * Totalmente inexistentes.


---

## 🔥 1.2.1 A Primeira Geração (1945-1955): Válvulas


A Segunda Guerra Mundial estimulou uma explosão de atividade na área computacional, devido à necessidade de cálculos balísticos complexos e quebra de códigos de criptografia inimigos.


### 💡 A Tecnologia


Os primeiros computadores funcionais utilizavam válvulas termiônicas e relés eletromagnéticos. Eles eram colossais e consumiam enormes quantidades de energia.


### 🏢 Pioneiros e Máquinas Históricas


Vários projetos independentes surgiram ao redor do mundo de forma quase simultânea:


1. **John Atanasoff e Clifford Berry:** Construíram o primeiro computador digital funcional (Iowa, EUA) usando cerca de 300 válvulas.

2. **Konrad Zuse:** Construiu o computador Z3 em Berlim usando relés eletromagnéticos.

3. **Equipe de Bletchley Park:** Com a presença ilustre de Alan Turing, construíram o *Colossus* na Inglaterra.

4. **Howard Aiken:** Criou o Mark I na Universidade de Harvard.

5. **William Mauchley e J. Presper Eckert:** Construíram o icônico ENIAC na Universidade da Pensilvânia.


### ⌨️ A Rotina de Programação


* A computação engatinhava. Um único grupo de engenheiros projetava, construía, programava, operava e mantinha cada máquina.

* **Linguagens:** Desconhecidas. Nem o Assembly existia.

* **Operação:** A programação era feita em código de máquina absoluto ou conectando manualmente milhares de cabos em painéis de ligações.

* **Processo:** O engenheiro reservava um bloco de tempo em uma ficha na parede, descia até a sala de máquinas, inseria seu painel e cruzava os dedos para que as dezenas de milhares de válvulas não queimassem durante o processo.

* Apenas no início da década de 1950 surgiram os **cartões perfurados**, permitindo que os programas fossem escritos em cartões e depois lidos pela máquina.


---

## 🖲️ 1.2.2 A Segunda Geração (1955-1965): Transistores e Sistemas em Lote


A invenção do transistor mudou o mundo. Os computadores se tornaram confiáveis o suficiente para serem produzidos em escala e vendidos para grandes corporações, universidades e agências governamentais.


### 🏢 O Nascimento dos Mainframes


* Essas máquinas gigantes ficavam isoladas em salas exclusivas e fortemente climatizadas.

* Ocorreu a primeira grande **divisão do trabalho**: projetistas, construtores, operadores, programadores e mantenedores passaram a ter papéis separados.

* O programador escrevia o código (em *FORTRAN* ou *Assembly*) no papel, perfurava em cartões e entregava ao operador da máquina.


### ⏳ O Grande Gargalo: Tempo Desperdiçado


Dado o altíssimo custo das máquinas (como o famoso IBM 7094), o tempo de CPU era precioso.

Sempre que uma tarefa acabava, a CPU ficava totalmente ociosa enquanto o operador andava até a impressora, pegava a saída, procurava a fita do compilador FORTRAN, carregava a próxima pilha de cartões... etc.


### 📦 A Invenção do Sistema em Lote (Batch)


Para eliminar o tempo ocioso humano, criou-se o **Sistema em Lote**.


A ideia genial foi usar um computador menor e barato (como o **IBM 1401**), que era ótimo para leitura de cartões e impressão, para preparar fitas para o computador principal e caro (**IBM 7094**), que era ótimo para cálculos.


#### 📊 O Fluxo do Sistema em Lote (Referência: Figura 1.3)


| Etapa | Máquina | Ação Realizada |

| :---: | :--- | :--- |

| **1** | Nenhuma | O programador entrega o maço de cartões na sala de entrada. |

| **2** | **IBM 1401** | Lê os cartões de dezenas de programadores e grava tudo em uma única Fita Magnética de Entrada. |

| **3** | Humano | O operador carrega fisicamente a fita de entrada para a sala principal. |

| **4** | **IBM 7094** | Processa os lotes sequencialmente sem parar. Grava os resultados em uma Fita de Saída. |

| **5** | Humano | O operador leva a Fita de Saída de volta para a máquina mais barata. |

| **6** | **IBM 1401** | Imprime os resultados no papel de forma *off-line*. |


### 🗂️ A Estrutura de uma Tarefa Típica (Referência: Figura 1.4)


Para automatizar a transição entre tarefas na fita, surgiram os primeiros rudimentos de controle do SO. Uma tarefa do sistema **FMS** (Fortran Monitor System) tinha os seguintes cartões de controle:


```text

1. $JOB       -> Especifica o tempo máximo, conta a ser debitada e nome do programador.

2. $FORTRAN   -> Instrui o SO a carregar o compilador FORTRAN da fita do sistema.

3. [Código]   -> O programa FORTRAN em si.

4. $LOAD      -> Instrui o SO a carregar o programa-objeto recém-compilado.

5. $RUN       -> Inicia a execução do programa.

6. [Dados]    -> Dados que o programa consumirá.

7. $END       -> Marca o fim da tarefa.

```


Nesta geração, os cálculos eram puramente científicos/engenharia. Os sistemas operacionais de destaque eram o **FMS** e o **IBSYS** da IBM.


---

## 💽 1.2.3 A Terceira Geração (1965-1980): CIs e Multiprogramação


No início dos anos 1960, fabricantes enfrentavam um dilema: mantinham duas linhas de produtos totalmente incompatíveis.

1. Computadores Científicos (orientados a palavras, ex: 7094).

2. Computadores Comerciais (orientados a caracteres, para ordenação bancária, ex: 1401).


### 🦖 O IBM System/360 e o OS/360


A IBM revolucionou o mercado lançando o **System/360**. Usava **Circuitos Integrados (CIs) de pequena escala**, combinando ambas as necessidades em uma única família de computadores com a mesma arquitetura de software.


O problema? O sistema operacional prometido, o **OS/360**, precisava agradar a todos. O resultado foi um monstro: milhões de linhas de Assembly, escrito por milhares de pessoas e repleto de dezenas de milhares de *bugs*.

*(Isso inspirou Fred Brooks a escrever o icônico livro "O Mítico Homem-Mês").*


### 🔄 A Revolução da Multiprogramação


Até então, quando uma tarefa realizava E/S (como ler uma fita magnética), a CPU parava completamente e ficava ociosa.

A **multiprogramação** dividiu a memória em partições para abrigar múltiplas tarefas. Se a Tarefa 1 for bloqueada esperando a fita, o SO passa a CPU imediatamente para a Tarefa 2.


#### 📊 Mapa de Memória na Multiprogramação (Referência: Figura 1.5)


| Endereçamento da Memória Física |

| :--- |

| **[ Partição 3 ]** Tarefa 3 (Pronta ou Aguardando) |

| **[ Partição 2 ]** Tarefa 2 (Pronta ou Aguardando) |

| **[ Partição 1 ]** Tarefa 1 (Em Execução na CPU) |

| **[ Protegido  ]** Sistema Operacional |


> *Nota: Essa técnica exige hardware especial para proteger a memória de um programa contra invasões do outro.*


### 🚀 Spooling e Timesharing


* **Spooling:** (*Simultaneous Peripheral Operation On Line*). Com a popularização dos discos magnéticos, o SO podia ler os cartões e gravá-los no disco assim que chegassem à sala. O uso de fitas e dos IBMs 1401 deixou de ser necessário para E/S.

* **Timesharing:** O processamento em lote causava um problema: tempo de resposta demorado. Uma vírgula errada custava um dia de trabalho. O Tempo Compartilhado permitiu que vários usuários acessassem o sistema via terminais interativos online. A CPU alternava rapidamente entre eles, dando a ilusão de que cada um possuía o computador inteiro para si.


### 🌟 O MULTICS


Inspirados pelo timesharing (como o CTSS), o M.I.T., a Bell Labs e a GE uniram-se para criar o **MULTICS** (*Multiplexed Information and Computing Service*).

A visão era insana para a época: criar um "computador utilitário" central que forneceria processamento para toda a cidade de Boston, da mesma forma que a concessionária de energia fornece eletricidade.


O MULTICS era tão ambicioso (e escrito em PL/I) que sofreu atrasos enormes. A Bell Labs e a GE abandonaram o projeto. O M.I.T. continuou, mas o MULTICS nunca tomou o mundo comercialmente. Porém, ele **moldou a história** por sua influência acadêmica.


### 🐧 Do UNIX ao Linux


Com a desistência da Bell Labs no MULTICS, o pesquisador **Ken Thompson** encontrou um minicomputador PDP-7 encostado. Ele decidiu escrever uma versão minimalista e para usuário único baseada nos conceitos do MULTICS.


O resultado foi o **UNIX**.


* O UNIX popularizou-se absurdamente.

* O código fonte aberto permitiu bifurcações (System V da AT&T, BSD de Berkeley).

* Para arrumar a fragmentação, o IEEE criou o padrão **POSIX**.

* Andrew Tanenbaum (o autor do livro que estamos resumindo) criou um clone enxuto do UNIX chamado **MINIX**, para fins educacionais.

* O código do MINIX inspirou diretamente um estudante finlandês chamado **Linus Torvalds** a criar um kernel próprio: O **Linux**. Hoje, o Linux domina os servidores mundiais, nuvens, sistemas embarcados e smartphones (via Android).


---

## 💻 1.2.4 A Quarta Geração (1980-Presente): Computadores Pessoais


Com o desenvolvimento do **LSI** (*Large Scale Integration*), foi possível colocar milhares de transistores num único centímetro quadrado de silício.

Isso deu origem aos microprocessadores e à era do Computador Pessoal (Microcomputador).


### 📜 O Início da Era do PC


* A Intel lançou o processador **8080**.

* **Gary Kildall** criou o primeiro controlador para disco flexível e escreveu um sistema operacional chamado **CP/M** (*Control Program for Microcomputers*). O CP/M dominou por cinco anos absolutos o mercado incipiente.


### 🪟 A Escolha que Mudou o Mundo: IBM e Microsoft


Quando a gigantesca IBM decidiu criar o "IBM PC", procurou Bill Gates para o interpretador BASIC. A IBM perguntou a Gates sobre um SO.

Gates recomendou Gary Kildall. Em um dos episódios mais bizarros da história corporativa, Kildall esnobou os executivos da IBM (mandou a esposa negociar e o advogado recusou assinar o contrato de confidencialidade).


A IBM voltou a Gates. Gates não tinha um SO, mas sabia que Tim Paterson (da Seattle Computer Products) tinha um chamado **QDOS**.

Gates comprou o QDOS por meros US$ 75.000, renomeou-o para **MS-DOS**, contratou Paterson para adaptá-lo e o licenciou para a IBM. A Microsoft exigiu manter os direitos e vender para outros clones do PC. O resto é história.


### 🖱️ A Revolução da Interface Gráfica do Usuário (GUI)


Até o início dos anos 80, os computadores usavam a temida *Linha de Comando* (CLI).


* **O Pioneiro:** Doug Engelbart (Stanford) inventou o mouse, janelas e ícones.

* **O Berço:** A Xerox PARC refinou a ideia.

* **A Explosão Apple:** Steve Jobs visitou o PARC, percebeu que aquilo era o futuro, e criou o **Apple Macintosh** (após o fracasso do caro modelo Lisa). O Mac popularizou a GUI para usuários totalmente leigos.

  *(Hoje, o macOS X utiliza um núcleo avançado UNIX baseado no micronúcleo Mach e BSD).*.

* **A Resposta Microsoft:** Para não ficar para trás, a Microsoft lançou o **Windows**. De 1985 a 1995, o Windows era apenas uma "casca" visual que rodava por cima do MS-DOS.

* Com o **Windows 95**, tornou-se um SO independente.

* A linha seguiu para o **Windows NT** (uma reescrita total, 32-bits, feita por David Cutler), Windows 2000, XP, Vista, 7, e o Windows 8 focado em toques.


### 🌐 Redes e Sistemas Distribuídos


Ainda nesta geração, as redes locais (LAN) surgiram.

1. **Sistemas Operacionais de Rede:** Cada máquina tem seu SO e os usuários acessam os servidores de forma consciente e remota.

2. **Sistemas Operacionais Distribuídos:** Aglomerados de múltiplos processadores e máquinas que aparecem para o usuário final como se fossem um único e colossal computador centralizado.


---

## 📱 1.2.5 A Quinta Geração (1990-Presente): Computadores Móveis


O sonho de Dick Tracy com seu "rádio relógio de pulso" (década de 1940) virou realidade.

Telefonia e computação se fundiram na palma da mão.


### 📈 A Caminhada Histórica Mobile


* **1946:** O primeiro "telefone móvel" pesava 40 quilos e ia no porta-malas do carro.

* **1970:** Surgiu o "tijolo", o primeiro celular portátil (ainda com 1 kg).

* **1990:** O primeiro verdadeiro smartphone, combinando PDA (*Personal Digital Assistant*) com telefonia (Nokia N9000). O termo *smartphone* só veio em 1997 pela Ericsson.


### ⚔️ O Trono de Ferro Mobile e a Guerra dos Sistemas


O mercado móvel provou ser o mais dinâmico e feroz da história da tecnologia. Os líderes são derrubados com extrema velocidade.


#### A Era dos Antigos Reis

* **Symbian OS:** O monarca absoluto da primeira década. Adotado maciçamente por gigantes como Nokia, Sony Ericsson, Samsung e Motorola.

* **Blackberry OS (RIM):** Dominava o segmento corporativo com seus teclados físicos e e-mails hiper-seguros.


#### A Disrupção Definitiva

Em apenas dois anos (2007-2008), o mundo mudou, e o Symbian desabou, forçando a Nokia a migrar desesperadamente para o Windows Phone.


* 🍏 **O Choque do iOS (2007):**

  * Lançado pela Apple no iPhone 1.

  * Eliminou o teclado físico, introduziu uma UI perfeita para multitoque (capacitiva).

  * Focou em segurança, fluidez e no conceito matador das "App Stores".


* 🤖 **A Contraofensiva Android (2008):**

  * O Google lançou o Android, montado sobre o *Kernel Linux*.

  * O diferencial: O Google ofereceu o sistema sob uma licença **permissiva e aberta**.

  * Todos os fabricantes que entraram em pânico com o lançamento do iPhone (Samsung, HTC, Motorola) adotaram o Android de imediato.

  * Criou uma comunidade global gigantesca com programação em Java (Dalvik/ART).


### 🌍 O Cenário Atual


Hoje, o mercado vive um **duopólio** massivo entre o Android (Google) e o iOS (Apple). Os sistemas operacionais pararam de ser apenas pontes entre hardware e software local para se tornarem ecossistemas interconectados na nuvem. Sensores (GPS, acelerômetros, câmeras 4K) e a integração pesada com Inteligência Artificial ditam o design interno dos SOs modernos.


A história nos ensina que a glória de um Sistema Operacional não é eterna. A tecnologia dita os rumos, e o próximo salto (seja computação quântica, vestíveis invisíveis ou bio-computação) certamente dará início a uma **Sexta Geração**.


---

## 📚 Apêndice e Glossário de Conceitos Retirados do Texto


Para consolidar os eventos descritos de 1945 até hoje, aqui está um reforço dos conceitos vitais citados nas páginas da obra de Tanenbaum e Bos:


* **Assembly:** Linguagem de montagem muito próxima da linguagem de máquina, utilizada logo que as linguagens de programação nasceram. Poupava a memória preciosíssima dos primeiros sistemas.

* **FORTRAN e PL/I:** Linguagens de programação primordiais. O FORTRAN foi imensamente usado para cálculos científicos no IBM 7094. O PL/I foi escolhido (e causou dores de cabeça) para o projeto MULTICS.

* **O Mítico Homem-Mês (Fred Brooks):** Livro clássico escrito por um dos criadores do OS/360, apontando que "adicionar mais programadores a um projeto atrasado o atrasará ainda mais".

* **Kernel / Núcleo:** O cerne do sistema operacional. O Linux e o UNIX possuem kernels bem robustos, o Mac OS usa variações do Mach, e o Windows usa o NT.

* **POSIX:** *Portable Operating System Interface*. Um padrão da IEEE para garantir que os programas pudessem ser compilados e executados em qualquer vertente do UNIX, organizando a bagunça deixada pelas diversas distribuições comerciais.


---
<br>

<div align="center">

  <p><em>Fim do Documento</em></p>

</div>


## 🕰️ Linha do Tempo Cronológica Detalhada


Para facilitar a visualização de todos os marcos computacionais referenciados nas seções 1.2.1 a 1.2.5, observe a seguinte progressão temporal baseada no texto:


### Décadas de 1940 e 1950

* **1944:** Howard Aiken constrói o Mark I na Universidade de Harvard.

* **1945 (aprox.):** O famoso ENIAC é finalizado por William Mauchley e J. Presper Eckert na Universidade da Pensilvânia.

* **1946:** Surge o primeiro telefone móvel, uma unidade monstruosa de 40 kg adaptada para carros.

* **Anos 50 (Início):** Introdução e disseminação dos cartões perfurados na computação, abandonando a necessidade de conectar cabos físicos manualmente (Plugboards).


### Década de 1960

* **1961:** O DEC PDP-1 lança a semente da era dos minicomputadores, custando uma fração (US$ 120.000) do valor dos Mainframes.

* **Início dos Anos 60:** A General Motors, a Ford e a NSA adotam a computação baseada no revolucionário CTSS (M.I.T.), que implementou o *Timesharing*.

* **1964:** A IBM introduz o System/360 e unifica as linhas científica e comercial.

* **Final dos Anos 60:** O Instituto de Pesquisa de Stanford (Doug Engelbart) cria os primeiros protótipos de interfaces visuais e do mouse.

* **1969:** A Bell Labs e a GE abandonam o projeto MULTICS, deixando o M.I.T. desenvolvê-lo isoladamente. Ken Thompson encontra o PDP-7 ocioso e começa a base do UNIX.


### Década de 1970

* **Anos 70:** Surge o Motorola apelidado de "tijolo", o primeiro celular verdadeiramente manual de 1kg.

* **1974:** A Intel lança o 8080, o primeiro processador de 8 bits para uso geral. O cenário dos microcomputadores ganha tração.

* **1977:** A Digital Research adapta e espalha o sistema CP/M de Gary Kildall para uma infinidade de microcomputadores.


### Década de 1980

* **Início dos Anos 80:** A IBM lança o "IBM PC" usando o sistema MS-DOS comprado de Bill Gates e Tim Paterson (QDOS).

* **1984:** Lançamento do IBM PC/AT (processador 80286) e o histórico Apple Macintosh introduzindo a GUI para as massas.

* **1985:** A Microsoft introduz a primeira versão do Windows, que operava ainda como um simples ambiente gráfico sobre o MS-DOS.

* **1987:** Andrew S. Tanenbaum lança o MINIX para ensinar o funcionamento de sistemas similares ao UNIX para seus alunos universitários.


### Década de 1990

* **1990:** Lançamento do Nokia N9000, o primeiro aparelho a fundir telefonia móvel e recursos de PDA.

* **1991:** O estudante Linus Torvalds, inspirado pelo MINIX, inicia o desenvolvimento do Linux, transformando-o no mais popular kernel open-source do mundo.

* **1995:** A Microsoft lança o Windows 95, que finalmente deixava de ser apenas uma camada do MS-DOS para integrar diversas características de um Sistema Operacional real de 32 bits.

* **1997:** A fabricante Ericsson oficializa a terminologia "Smartphone".

* **1999:** A Apple reformula a base do seu macOS adotando um kernel híbrido derivado do BSD UNIX e do micronúcleo Mach.


### Anos 2000 em Diante

* **Anos 2000 (Primeira Metade):** Domínio irrestrito do Symbian OS nos dispositivos móveis em escala global. Surgimento do BlackBerry.

* **2007:** A Apple desestabiliza o mercado lançando o primeiro iPhone com a interface iOS (então iPhone OS), focado no multitoque e no usuário final.

* **2008:** O Google lança oficialmente o sistema Android, apostando na distribuição open-source permissiva.

* **2011:** Em desespero pela perda do mercado, a Nokia assina parceria e abandona o Symbian em favor do Windows Phone.

* **Tempos Atuais:** Sistemas como o Windows 8 e posteriores reformulam o uso de PCs prevendo o multitoque nativo em telas. Nos dispositivos móveis, consolida-se o duopólio hegemônico global do Android e iOS.


---

## 📖 Conclusão Analítica


Observar as transições abordadas pelas gerações 1 a 5 deixa uma lição imensa para os profissionais e estudiosos de ciência da computação. As raízes das abstrações (arquivos, diretórios, processos, timesharing) nasceram não da noite para o dia, mas pela exigência dolorosa e criativa de driblar gargalos de hardware.


A necessidade de processar cartões de maneira eficiente levou ao **Spooling**. A necessidade de debugar códigos sem esperar dias gerou o **Timesharing**. A frustração com telas textuais pretas culminou na criação da **GUI**. E o desejo pela portabilidade culminou no ecossistema de **Smartphones**, cujos sistemas operacionais carregam no seu cerne os exatos mesmos fundamentos arquitetônicos dos mainframes da década de 60, escalados e otimizados.


Os Sistemas Operacionais são entidades orgânicas. O UNIX, por exemplo, originou-se das cinzas de um projeto frustrado (MULTICS) e hoje rege silenciosamente o planeta na forma de Linux e derivados, mantendo os mesmos padrões POSIX. 

Ao ler as seções 1.2.1 a 1.2.5, torna-se nítido que hardware é passageiro, mas uma arquitetura de software bem idealizada sobrevive a décadas de avanços tecnológicos.