# 🖥️ Resumo: Conceitos, Funções e Tipos de Sistemas Operacionais & Git

---

## 📌 1. Tipos de Sistemas Operacionais

* 🏢 **Mainframes (Grande Porte):**
  * Alta capacidade de Entrada/Saída (E/S) e processamento massivo de transações (TPS).
  * Foco em confiabilidade e processamento em lote (*batch*).
  * *Exemplos:* OS/360, OS/390, Linux e UNIX em servidores bancários e corporativos.

* 🌐 **Sistemas de Servidor:**
  * Múltiplos usuários simultâneos e serviços de rede (web, arquivos, bancos de dados, autenticação).
  * Alta estabilidade e escalabilidade.
  * *Exemplos:* Linux, Windows Server.

* ⚡ **Sistemas de Multiprocessadores:**
  * Suporte a múltiplos núcleos/CPUs e paralelismo.
  * Desafios: balanceamento de carga, sincronização (*locks*, semáforos) e coerência de cache.

* 💻 **Computadores Pessoais (PCs):**
  * Interface gráfica intuitiva, foco no usuário final, suporte multimídia e multiprogramação.
  * *Exemplos:* Windows, macOS, Linux.

* 📱 **Sistemas Portáteis (Mobile):**
  * Gestão de energia rigorosa, APIs para sensores e isolamento de segurança (*sandboxing*)[cite: 1].
  * *Exemplos:* Android, iOS[cite: 1].

* 🔌 **Sistemas Embarcados (*Embedded*):**
  * Hardware dedicado com recursos restritos (ROM/Flash), sem instalação direta pelo usuário[cite: 1].
  * *Aplicações:* Eletrodomésticos, sistemas automotivos[cite: 1].
  * *Exemplos:* Embedded Linux, QNX, VxWorks[cite: 1].

* 📡 **Nós Sensores:**
  * Dispositivos diminutos com bateria limitada, orientados a eventos e redes sem fio[cite: 1].
  * *Exemplos:* TinyOS, Contiki[cite: 1].

* ⏱️ **Sistemas de Tempo Real (*Real-Time*):**
  * **Hard Real-Time:** Prazos rígidos; falhas temporais causam danos catastróficos (ex.: controle de voo)[cite: 1].
  * **Soft Real-Time:** Tolera pequenas degradações/atrasos ocasionais (ex.: streaming de mídia)[cite: 1].

* 💳 **Cartões Inteligentes (*Smart Cards*):**
  * Memória restrita, segurança avançada/criptografia e isolamento por *applets*[cite: 1].

---

## 🐙 2. Controle de Versão com Git & GitHub

* 🛠️ **Git:** Sistema de controle de versão local via linha de comando para rastreamento de mudanças e sincronização de repositórios[cite: 1].
* ⚙️ **Configuração Inicial:**
  ```bash
  git config --global user.name "<Nome>"
  git config --global user.email "<Email>"