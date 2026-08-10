# Resumo — Aula 01: Introdução aos Sistemas Operacionais

**Disciplina:** Sistemas Operacionais
**Professor:** Me. Deivison S. Takatu
**Contato:** deivison.takatu@fatec.sp.gov.br

---

## 1. O que é um Sistema Operacional?

Um **Sistema Operacional (SO)** é o software essencial que **gerencia o hardware e o software** de um computador. Ele funciona como uma **interface entre o usuário e a máquina**, permitindo que os programas se comuniquem com os componentes físicos do computador.

**Exemplos de SOs:** Windows, macOS, Linux, Android, iOS.

---

## 2. Estrutura Interna: Camadas e Modelos

Os sistemas operacionais são organizados internamente de forma hierárquica para garantir modularidade.

- **Estrutura em Camadas:** organização hierárquica que separa as funções do SO em níveis, facilitando manutenção e organização.
- **Monolítica vs. Modular:** duas abordagens diferentes de projetar o núcleo do sistema — a monolítica concentra tudo em um bloco só, enquanto a modular divide as funções em partes independentes.

### O Kernel (núcleo do SO)
- É o coração do sistema operacional.
- Tem acesso direto ao hardware.
- Gerencia os recursos vitais da máquina (processador, memória, dispositivos).

### Modos de Operação
| Modo | Descrição |
|---|---|
| **Modo Usuário** | Onde rodam os programas comuns, com acesso restrito |
| **Modo Kernel** | Modo com privilégios elevados e acesso total ao hardware |

---

## 3. Escalonamento de Processos

É a forma como o SO decide **qual processo executar e por quanto tempo**.

- **Objetivos:** eficiência, justiça (fairness) e bom tempo de resposta.
- **Algoritmos comuns:** FIFO (primeiro a chegar, primeiro a ser atendido), Round Robin (tempo igual para cada processo) e Prioridade (processos mais importantes são executados primeiro).
- **Impacto:** afeta diretamente o desempenho geral do sistema.

---

## 4. Gerenciamento de Memória

### Memória Principal (RAM)
- Alocação dinâmica de espaço para os programas.
- Proteção de memória, evitando que um programa interfira em outro.

### Memória Virtual
- Funciona como uma **expansão lógica da RAM**, usando o disco quando a memória física não é suficiente.
- Utiliza técnicas de **paginação e segmentação**.
- Aumenta a segurança e a flexibilidade do sistema.

---

## 5. Dispositivos, Arquivos, Segurança e Virtualização

- **Gerenciamento de E/S (Entrada/Saída):** controla os dispositivos periféricos (teclado, mouse, impressora etc.).
- **Sistemas de Arquivos:** organizam e permitem o acesso aos dados armazenados.
- **Segurança em SO:** mecanismos de proteção contra ameaças e acessos indevidos.
- **Virtualização:** permite otimizar o uso dos recursos do computador, criando ambientes flexíveis e isolados (máquinas virtuais).

---

## 6. Avaliação da Disciplina

A nota final segue a fórmula:

```
Nota = (P1 × 0.25) + (P2 × 0.25) + ((PJ + AT) × 0.25)
```

- **P1** – Prova 1
- **P2** – Prova 2
- **PJ** – Projeto
- **AT** – Atividades

---

## 7. Atividade Proposta (Aula 01)

1. Formar grupos de **3 a 5 integrantes** (a mesma composição deve ser usada em todas as atividades semanais).
2. Enviar arquivo com os nomes completos do grupo na primeira atividade da disciplina.
3. Criar um **repositório no GitHub** para todas as entregas do semestre, incluindo um arquivo `.md` com o resumo da Aula 01.
4. Criar uma **linha do tempo (mapa mental)** sobre os anos de lançamento de diferentes sistemas operacionais, feita de forma colaborativa no **Miro**, e depois convertida em `.md` para o repositório.

---

## 8. Por que ter um portfólio de projetos?

- Demonstra habilidades práticas e domínio das ferramentas.
- Serve como evidência do aprendizado.
- Facilita a avaliação pelo professor.
- Amplia oportunidades em estágios e empregos.
- Estimula organização e melhoria contínua.

---

## Referências Bibliográficas

- TANENBAUM, A. S.; BOS, H. *Sistemas Operacionais Modernos*. 4. ed. São Paulo: Pearson, 2016.
- SILBERSCHATZ, A.; GALVIN, P. B.; GAGNE, G. *Fundamentos de Sistemas Operacionais*. 9. ed. Rio de Janeiro: LTC, 2015.
- STALLINGS, W. *Sistemas Operacionais: Conceitos e Projetos*. 8. ed. São Paulo: Pearson, 2015.
- DENARDIN, G. W.; BARRIQUELLO, C. H. *Sistemas Operacionais de Tempo Real e sua Aplicação em Sistemas Embarcados*. Porto Alegre: Editora da UFRGS, 2014.
- AWASTHI, A.; RAWAT, V. *Ramificação e Tarefas do Sistema Operacional*. Edições Nosso Conhecimento, 2023.
- DOWNEY, A. B. *Think OS: A Brief Introduction to Operating Systems*. Green Tea Press, 2015.
- RED HAT. *Red Hat Enterprise Linux – System Administration Guide*. Documentação Oficial.
- DOCKER INC. *Docker Documentation*. Disponível em: https://docs.docker.com
