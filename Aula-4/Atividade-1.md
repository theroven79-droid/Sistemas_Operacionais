# Atividade: Formatação e Instalação de um Sistema Operacional Windows

## Objetivo

O objetivo desta atividade é que os alunos **pesquisem, descrevam e apresentem o processo de formatação e instalação do Windows em um computador**, relacionando cada etapa aos conceitos estudados sobre **Estrutura e Arquitetura de Sistemas Operacionais**.

A atividade tem como foco desenvolver conhecimentos sobre:

- Sistemas Operacionais
- Componentes de um Sistema Operacional
- Kernel
- Modos de execução
- Processos
- Programa × Processo × Thread
- Sistema de arquivos
- Entrada/Saída
- Drivers de dispositivos
- Formatação e instalação de um Sistema Operacional

---

# Estrutura da Atividade

A atividade será dividida em **duas etapas**.

## 1️⃣ Aula Teórica – Preparação da Atividade

Durante a aula, os alunos deverão:

- Pesquisar sobre o processo de **formatação e instalação do Windows**;
- Descrever as principais etapas do processo;
- Identificar os componentes do Sistema Operacional envolvidos;
- Relacionar o processo de instalação aos conceitos estudados;
- Preparar o **documento da atividade em Markdown**.

Durante esse período o professor estará disponível para orientar dúvidas sobre:

- Formatação;
- Instalação do Windows;
- Estrutura do Sistema Operacional;
- Kernel;
- Processos;
- Sistema de arquivos;
- Entrada/Saída;
- Drivers.

---

# 2️⃣ Atividade Prática – Descrição do Processo

Os alunos deverão imaginar que receberam um computador que precisa ser **formatado e preparado para uma nova instalação do Windows**.

A atividade deverá descrever o processo **desde o momento em que o computador é ligado até o Windows estar instalado e pronto para utilização**.

### Processo geral

Primeiramente, é necessário preparar um **pendrive de instalação do Windows**, utilizando a mídia oficial do sistema operacional.

Após preparar o pendrive, o computador é desligado e iniciado novamente para acessar a **BIOS/UEFI**. Nessa etapa, o usuário seleciona o pendrive como dispositivo de inicialização (*boot*), salva as alterações e reinicia o computador.

Após o *boot* pelo pendrive, o computador carrega o ambiente de instalação do Windows. O instalador reconhece os dispositivos disponíveis e apresenta ao usuário as opções para escolher a unidade em que o sistema será instalado.

Dependendo da instalação escolhida, o usuário pode excluir, criar ou formatar partições. Após a preparação da unidade, os arquivos de instalação são copiados para o armazenamento e o Windows começa a ser instalado e configurado.

Durante esse processo, o sistema utiliza recursos como **CPU, memória RAM, armazenamento e dispositivos de entrada e saída**. O kernel e os drivers são responsáveis por permitir o gerenciamento e a comunicação adequada entre o software e o hardware.

Ao final, o computador reinicia, carrega o Windows instalado e realiza as configurações iniciais. Depois disso, o sistema estará pronto para utilização.

A explicação deverá abordar obrigatoriamente os seguintes conceitos:

---

## Componentes do Sistema Operacional

Durante a instalação e configuração do Windows, diversos componentes do sistema operacional participam do processo.

Os principais recursos que precisam ser gerenciados são:

- **CPU:** responsável pela execução das instruções dos processos;
- **Memória RAM:** utilizada para armazenar temporariamente dados e instruções dos processos;
- **Armazenamento:** utilizado para ler e gravar os arquivos do sistema;
- **Dispositivos de entrada e saída:** permitem a interação entre o usuário, o sistema e os dispositivos;
- **Processos:** representam os programas que estão sendo executados;
- **Sistema de arquivos:** organiza e permite o acesso aos dados armazenados;
- **Drivers:** permitem a comunicação adequada entre o sistema operacional e determinados dispositivos de hardware.

O **kernel** é o principal responsável pelo gerenciamento desses recursos, enquanto outros componentes, como drivers e sistemas de arquivos, realizam funções específicas necessárias para o funcionamento do sistema.

---

## Kernel: O Núcleo do Sistema

O **kernel** é a parte central do sistema operacional e possui a função de gerenciar os recursos do computador e intermediar a comunicação entre software e hardware.

### Quando o kernel passa a atuar?

O kernel passa a atuar quando o sistema operacional é carregado durante o processo de inicialização. Após o *boot* e o carregamento do sistema, o kernel é colocado na memória e começa a controlar e gerenciar os recursos disponíveis.

Durante o ambiente de instalação do Windows, também existe um ambiente operacional próprio que utiliza componentes do sistema para controlar o hardware e executar o instalador.

### Como ele gerencia os recursos do computador?

O kernel distribui e controla os recursos entre os diferentes processos.

Ele gerencia, por exemplo:

- CPU;
- Memória RAM;
- Processos;
- Dispositivos de entrada e saída;
- Armazenamento;
- Outros recursos de hardware.

Esse gerenciamento permite que diferentes tarefas sejam executadas de forma organizada, evitando conflitos entre os processos.

### Como ele faz a comunicação entre software e hardware?

Os programas não precisam conhecer diretamente os detalhes de funcionamento de cada componente de hardware.

Quando uma aplicação precisa utilizar um recurso, ela realiza uma solicitação ao sistema operacional. O kernel gerencia essa solicitação e, quando necessário, utiliza os drivers para realizar a comunicação com o dispositivo.

De forma simplificada:

**Aplicação → Sistema Operacional → Kernel → Driver → Hardware**

Durante a instalação, recursos como CPU, memória, armazenamento, teclado, mouse, monitor e pendrive precisam ser controlados para que o processo ocorra corretamente.

---

## Modos de Execução

Os sistemas operacionais utilizam diferentes níveis de privilégio para proteger o sistema e controlar o acesso aos recursos.

### Modo Usuário

O **Modo Usuário** é utilizado normalmente pelas aplicações executadas pelo usuário.

Nesse modo, os programas possuem acesso limitado aos recursos do computador e não podem acessar diretamente áreas protegidas da memória ou controlar livremente o hardware.

Durante a instalação, o usuário interage com aplicações e interfaces, por exemplo:

- Preparando a mídia de instalação;
- Acessando a BIOS/UEFI;
- Selecionando o dispositivo de *boot*;
- Interagindo com o instalador;
- Escolhendo a unidade de instalação;
- Selecionando opções de formatação.

### Modo Kernel

O **Modo Kernel** possui privilégios elevados e é utilizado para executar operações críticas do sistema operacional.

Nesse modo, o kernel pode gerenciar:

- CPU;
- Memória;
- Processos;
- Dispositivos;
- Armazenamento;
- Comunicação com o hardware.

O usuário não possui acesso irrestrito ao Modo Kernel, pois isso poderia comprometer a segurança e a estabilidade do sistema.

### Identificação dos modos durante a instalação

Os dois modos estão envolvidos no processo.

No **Modo Usuário**, ocorre principalmente a interação do usuário com as ferramentas e interfaces utilizadas para preparar e instalar o sistema.

No **Modo Kernel**, são realizadas operações de baixo nível relacionadas ao gerenciamento dos recursos e à comunicação com o hardware.

É importante observar que **acessar a BIOS/UEFI não significa estar no Modo Usuário ou no Modo Kernel do Windows**, pois a BIOS/UEFI é um firmware executado antes do sistema operacional ser carregado.

### Por que o sistema operacional não permite que qualquer programa tenha acesso direto e irrestrito ao hardware?

O acesso irrestrito poderia causar problemas de **segurança, estabilidade e gerenciamento de recursos**.

Um programa poderia, por exemplo:

- Alterar dados pertencentes a outro processo;
- Acessar informações que deveriam estar protegidas;
- Interferir na memória de outros programas;
- Utilizar recursos do hardware de forma inadequada;
- Causar travamentos ou falhas no sistema.

Por isso, o sistema operacional controla o acesso aos recursos e utiliza diferentes níveis de privilégio para impedir que aplicações comuns comprometam o funcionamento do computador.

---

## Processos

Durante a instalação do Windows, diversos processos são executados para realizar as tarefas necessárias.

### O que caracteriza um processo?

Um **processo é um programa em execução**.

Quando um programa é iniciado, o sistema operacional cria um processo e fornece a ele recursos necessários para sua execução, como memória e tempo de processamento da CPU.

Um processo possui seu próprio estado de execução e pode conter uma ou várias threads.

### Quais programas/processos são executados?

Durante o processo de instalação e configuração podem existir processos relacionados a:

- Instalador do Windows;
- Serviços do ambiente de instalação;
- Gerenciamento de dispositivos;
- Configuração do sistema;
- Drivers;
- Processos relacionados ao armazenamento;
- Serviços de inicialização;
- Serviços de segurança do Windows, quando aplicável.

Não é necessário que todos esses processos sejam executados exatamente da mesma forma em todas as instalações, pois isso pode variar de acordo com a versão do Windows e o ambiente utilizado.

### Quais recursos eles precisam?

Os processos utilizam diferentes recursos do computador, principalmente:

- **CPU:** para executar instruções;
- **Memória RAM:** para armazenar temporariamente dados e instruções;
- **Armazenamento:** para ler e gravar arquivos;
- **GPU:** quando são necessárias operações gráficas;
- **Dispositivos de entrada e saída:** para comunicação com periféricos.

### Como o sistema operacional gerencia esses processos?

O kernel gerencia os processos e distribui os recursos disponíveis entre eles.

Ele controla o uso da CPU, memória e dispositivos, permitindo que diferentes processos sejam executados de maneira organizada e evitando conflitos.

---

## Processo × Programa × Thread

Um exemplo relacionado à instalação do Windows pode ser utilizado para compreender a diferença entre esses três conceitos.

### Qual é o programa?

O **programa** é o conjunto de instruções armazenadas que possui a finalidade de realizar determinada tarefa.

Um exemplo é o **programa instalador do Windows**, responsável por realizar as etapas necessárias para a instalação do sistema operacional.

### Quando ele se torna um processo?

O programa se torna um **processo quando é executado**.

Por exemplo:

**Programa:** instalador armazenado na mídia de instalação.

**Processo:** instalador sendo executado naquele momento.

Quando o processo é criado, o sistema operacional fornece os recursos necessários para sua execução.

### Onde podem existir threads?

As **threads existem dentro dos processos**.

Durante a instalação, um processo pode possuir múltiplas threads para realizar diferentes tarefas. Por exemplo, uma thread pode estar envolvida com leitura de dados enquanto outra participa de alguma etapa de processamento ou gravação.

### Por que utilizar múltiplas threads pode ser útil?

Múltiplas threads permitem dividir o trabalho de um processo em diferentes unidades de execução.

Isso pode permitir que tarefas sejam executadas de forma concorrente, melhorando o aproveitamento dos recursos do processador e tornando determinadas operações mais eficientes.

### Resumo

**Programa → conjunto de instruções armazenadas**

**Processo → programa em execução**

**Thread → unidade de execução dentro de um processo**

---

## Sistema de Arquivos

O **sistema de arquivos** é responsável por organizar, armazenar e permitir o acesso aos arquivos presentes em um dispositivo de armazenamento.

Durante a formatação e instalação do Windows, ele possui um papel fundamental.

### O que acontece com os dados existentes?

Os dados existentes **não são necessariamente apagados apenas por iniciar a instalação**.

Isso depende das ações realizadas pelo usuário.

Se uma partição for formatada ou excluída durante uma instalação limpa, os dados existentes nela poderão ser removidos.

Por isso, antes de uma formatação, é importante verificar qual partição está sendo selecionada e realizar um backup dos dados importantes.

### Formatação da unidade

A formatação prepara uma partição para utilizar um determinado sistema de arquivos.

Na instalação do Windows, a partição selecionada pode ser preparada para receber o sistema operacional. Em instalações modernas do Windows, o **NTFS** é normalmente utilizado na partição principal do sistema.

### Criação e organização das estruturas necessárias

O sistema de arquivos fornece estruturas que permitem organizar e localizar os arquivos armazenados.

Durante a instalação, o Windows cria as pastas, arquivos e estruturas necessárias para o funcionamento do sistema operacional.

### Cópia dos arquivos de instalação

Os arquivos presentes na mídia de instalação, como o pendrive, são lidos e copiados para a unidade de armazenamento escolhida pelo usuário.

Assim, os arquivos necessários deixam de depender do pendrive e passam a fazer parte da instalação no armazenamento interno.

### Criação dos arquivos necessários para inicialização

Durante a instalação, também são configuradas as estruturas necessárias para que o computador consiga localizar e iniciar o Windows durante o processo de *boot*.

Isso permite que, após a instalação, o computador consiga iniciar o sistema a partir da unidade interna.

### Organização dos arquivos do Windows após a instalação

Após a instalação, os arquivos do Windows ficam organizados no armazenamento de acordo com as estruturas do sistema de arquivos.

Entre as principais pastas encontradas em uma instalação do Windows estão:

- `Windows`
- `Program Files`
- `Users`

Além delas, existem outros arquivos e estruturas necessários para inicialização, configuração e funcionamento do sistema.

### Diferença entre apagar, particionar e formatar

É importante diferenciar esses conceitos:

- **Apagar dados:** significa remover arquivos existentes.
- **Particionar:** significa dividir ou organizar uma unidade de armazenamento em partições.
- **Formatar:** significa preparar uma partição para utilizar um determinado sistema de arquivos.

Portanto, **particionar uma unidade não é a mesma coisa que formatá-la**, e formatar uma partição não deve ser confundido simplesmente com apagar arquivos individualmente.

---

## Entrada/Saída e Drivers de Dispositivos

Durante o processo de instalação, diversos dispositivos de entrada, saída e armazenamento são utilizados.

| Dispositivo | Tipo | Como o Windows consegue se comunicar com ele? |
|---|---|---|
| **Teclado** | Entrada | O Windows utiliza drivers e interfaces de entrada para receber os comandos das teclas. |
| **Mouse** | Entrada | O driver permite que o sistema receba os movimentos e cliques do mouse. |
| **Monitor** | Saída | O driver de vídeo permite que o sistema envie informações gráficas para o monitor. |
| **SSD/HD** | Armazenamento | O Windows utiliza controladores, drivers e o sistema de arquivos para ler e gravar dados. |
| **Pendrive** | Entrada/Armazenamento | O computador utiliza a interface USB e seus drivers para reconhecer e acessar os arquivos do pendrive. |
| **Rede** | Entrada/Saída | O driver do adaptador de rede permite enviar e receber dados através da rede. |
| **Áudio** | Saída | O driver de áudio permite que o sistema envie sinais sonoros para caixas de som ou fones. |

### Como o Windows consegue se comunicar com esses dispositivos?

O Windows utiliza **drivers**, interfaces e mecanismos do sistema operacional para se comunicar com o hardware.

Os drivers funcionam como uma camada de software que permite ao sistema operacional utilizar determinados dispositivos sem precisar conhecer todos os detalhes específicos do funcionamento de cada componente.

Por exemplo:

**Windows → Driver de vídeo → GPU → Monitor**

**Windows → Driver de áudio → Dispositivo de áudio → Fone/Caixa de som**

**Windows → Driver de rede → Placa de rede → Rede/Internet**

### Por que os drivers são importantes?

Os drivers são importantes porque permitem que o sistema operacional **reconheça, controle e utilize corretamente os dispositivos de hardware**.

Durante a instalação, o Windows pode utilizar drivers básicos para conseguir funcionar com os principais componentes. Após a instalação, drivers específicos podem ser instalados ou atualizados para oferecer suporte completo ao hardware.

---

# 🔎 Parte Principal da Atividade

Depois de explicar o processo, construam uma **linha do tempo da instalação do Windows**.

Para cada etapa, indiquem **qual conceito estudado está envolvido e por que ele é importante**.

| Etapa | O que acontece? | Conceito envolvido | Por que é importante? |
|---|---|---|---|
| **1. Inicialização** | O computador é ligado e inicia o processo de *boot*. O firmware verifica e inicializa os componentes necessários. | **Inicialização / Hardware** | Prepara o computador para encontrar e carregar o ambiente de inicialização. |
| **2. Inicialização do instalador** | O computador inicia pelo pendrive selecionado como dispositivo de *boot* e carrega o ambiente de instalação do Windows. | **Entrada/Saída / Sistema Operacional** | Permite acessar os arquivos necessários para iniciar a instalação. |
| **3. Reconhecimento do hardware** | O ambiente de instalação identifica componentes como armazenamento, teclado, mouse, monitor e outros dispositivos. | **Drivers / Entrada e Saída** | Permite que o instalador utilize os dispositivos necessários para continuar a instalação. |
| **4. Seleção da unidade** | O usuário escolhe o SSD/HD e a partição onde o Windows será instalado. | **Armazenamento / Sistema de Arquivos** | Define o local onde os arquivos do sistema serão armazenados. |
| **5. Particionamento/formatação** | O usuário pode criar, excluir ou formatar partições de acordo com a instalação desejada. | **Sistema de Arquivos** | Prepara o armazenamento e estabelece as estruturas necessárias para organizar os dados. |
| **6. Cópia dos arquivos** | Os arquivos de instalação são lidos do pendrive e copiados para o armazenamento interno. | **Entrada/Saída / Sistema de Arquivos** | Permite transferir e armazenar os arquivos necessários para a instalação. |
| **7. Instalação do Windows** | O instalador aplica os arquivos e configura os componentes necessários para o funcionamento do Windows. | **Processos / Kernel / Sistema de Arquivos** | Organiza os componentes do sistema e prepara o Windows para ser inicializado. |
| **8. Instalação/configuração de drivers** | Drivers necessários são instalados ou configurados para que os dispositivos funcionem corretamente. | **Drivers / Entrada e Saída** | Permite a comunicação adequada entre o sistema operacional e o hardware. |
| **9. Inicialização do sistema** | O computador reinicia e carrega o Windows instalado a partir da unidade interna. | **Kernel / Processos / Boot** | O sistema operacional é carregado e começa a gerenciar os recursos do computador. |
| **10. Windows pronto para utilização** | O usuário acessa o Windows e pode utilizar aplicativos, arquivos e dispositivos. | **Gerenciamento de Recursos / Processos / Drivers** | O sistema passa a gerenciar continuamente CPU, RAM, armazenamento, processos e dispositivos. |

---

# 🧩 Desafio Final

Ao final da atividade, respondam:

> **Se não existisse um Sistema Operacional, quais partes desse processo precisariam ser realizadas diretamente pelo usuário ou pelos programas?**

Se não existisse um **Sistema Operacional**, muitas tarefas precisariam ser realizadas diretamente pelo usuário ou pelos próprios programas.

Seria necessário controlar manualmente recursos como:

- CPU;
- Memória;
- Armazenamento;
- Dispositivos de entrada e saída;
- Comunicação com o hardware;
- Organização dos arquivos;
- Execução dos programas.

Cada programa também precisaria conhecer detalhes específicos de funcionamento dos componentes do computador para conseguir utilizá-los.

Isso tornaria o uso do computador muito mais complexo, pois não existiria uma camada responsável por **abstrair o hardware, gerenciar os recursos e controlar o acesso aos dispositivos**.

O Sistema Operacional facilita esse processo ao fornecer serviços e mecanismos que permitem aos programas utilizar o hardware de forma organizada e controlada.

---

E:

> **Qual dos conceitos estudados vocês consideram mais importante para que o computador consiga passar de um conjunto de componentes de hardware para um sistema capaz de executar aplicações? Justifique.**

Consideramos o **kernel** e o **sistema de arquivos** dois dos conceitos mais importantes para que o computador consiga passar de um conjunto de componentes de hardware para um sistema capaz de executar aplicações.

O **kernel** é responsável por gerenciar os principais recursos do computador, como CPU, memória, processos e dispositivos, além de intermediar a comunicação entre software e hardware.

Já o **sistema de arquivos** é responsável por organizar e controlar o armazenamento dos dados, permitindo que o sistema operacional encontre, leia, grave e gerencie os arquivos.

Sem o kernel, os recursos do hardware não seriam gerenciados de forma adequada e os processos não teriam um mecanismo centralizado para utilizar CPU e memória.

Sem um sistema de arquivos, os dados armazenados não teriam uma estrutura adequada para serem organizados e localizados pelo sistema.

Portanto:

> **O kernel gerencia os recursos e faz a intermediação entre software e hardware, enquanto o sistema de arquivos organiza os dados armazenados. Juntos, eles são fundamentais para transformar os recursos físicos do computador em um ambiente capaz de executar aplicações.**

---

# 📦 Entrega

Produza um documento em **Markdown** contendo:

1. **Descrição do processo de formatação e instalação do Windows**;
2. **Explicação dos 7 conceitos solicitados**;
3. **Linha do tempo do processo**;
4. **Tabela relacionando cada etapa aos conceitos estudados**;
5. **Respostas do desafio final**.

A atividade deve demonstrar **a relação entre os conceitos**, e não apenas apresentar definições isoladas.

---

# 🎯 Questão Central da Atividade

> **"Ao formatar e instalar o Windows, onde o Sistema Operacional está trabalhando e por que cada um desses componentes é necessário?"**

Durante a instalação, o Sistema Operacional está envolvido no **gerenciamento dos recursos, execução dos processos, comunicação com o hardware, organização dos arquivos e controle dos dispositivos**.

Cada conceito possui uma função diferente, mas todos trabalham em conjunto:

**Hardware → Drivers → Kernel → Sistema Operacional → Processos/Aplicações**

Essa relação permite que o computador deixe de ser apenas um conjunto de componentes físicos e passe a oferecer um ambiente capaz de executar aplicações de maneira organizada e segura.

---

# 📊 Rubrica de Avaliação

| Critério | Descrição | Pontos |
|---|---|---:|
| **Descrição do processo** | Explicação clara e organizada das etapas de formatação e instalação do Windows | 2 |
| **Componentes do Sistema Operacional** | Identificação e explicação dos componentes envolvidos no processo | 2 |
| **Relação entre os conceitos** | Relação adequada entre kernel, modos de execução, processos, threads, sistema de arquivos, I/O e drivers | 3 |
| **Linha do tempo e tabela** | Organização das etapas e identificação da importância de cada conceito | 1 |
| **Desafio final** | Capacidade de analisar a importância do Sistema Operacional no processo | 1 |
| **Organização e Markdown** | Estrutura, clareza e organização do documento entregue | 1 |
| **Total** |  | **10 pontos** |

---

# ⚠️ Observações

- A atividade deve ser desenvolvida com base nos **conceitos apresentados em aula**.
- Não basta apenas descrever os passos da instalação do Windows.
- É necessário **explicar onde cada conceito estudado aparece no processo**.
- Destaque principalmente **por que aquele componente é importante** naquela etapa.
- Utilize termos técnicos corretamente.
- Organize o material utilizando títulos, subtítulos, listas e tabelas em **Markdown**.
- A atividade deve demonstrar a relação entre **software, Sistema Operacional e hardware**.
- Diferencie corretamente **BIOS/UEFI, boot, kernel, sistema de arquivos, processos, threads, drivers e hardware**.
- Lembre-se de que **formatar uma partição não é o mesmo que simplesmente apagar arquivos**, e que a formatação pode resultar na perda dos dados existentes naquela partição.