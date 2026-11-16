<p align="center">
  <img src="./assets/banner.svg" alt="Caroline Brunheti — Backend Developer" width="100%" />
</p>

<p align="center">
  <!-- Troque o link abaixo pelo endereço do seu portfólio quando ele estiver publicado -->
  <a href="https://carolinebrunheti.netlify.app/"><img src="https://img.shields.io/badge/Portfólio-8b5cf6?style=for-the-badge&logo=netlify&logoColor=white" alt="Portfólio" /></a>
  <a href="https://www.linkedin.com/in/carolinebrunheti/"><img src="https://img.shields.io/badge/LinkedIn-6366f1?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:caroline.brunheti@outlook.com"><img src="https://img.shields.io/badge/E--mail-06b6d4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="E-mail" /></a>
</p>

---

### Sobre mim

Sou desenvolvedora backend na **Solinftec**, onde trabalho com **Java, Spring Boot e Kafka**, persistência em **Oracle** e **PostgreSQL/PostGIS** e aplicações rodando em **Kubernetes** com observabilidade na **AWS**. Estou me aprofundando em arquitetura de sistemas distribuídos, não só em como construir aplicações mas em como projetá-las para escalar, evoluir e se manter confiáveis.

<p align="center">
  <img src="./assets/terminal.svg" alt="Terminal: whoami, stack e o que estou estudando" width="760" />
</p>

### Stack

<p>
  <img src="https://img.shields.io/badge/Java-8b5cf6?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring%20Boot-8b5cf6?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/Spring%20Security-8b5cf6?style=flat-square&logo=springsecurity&logoColor=white" alt="Spring Security" />
  <img src="https://img.shields.io/badge/Quarkus-8b5cf6?style=flat-square&logo=quarkus&logoColor=white" alt="Quarkus" />
  <img src="https://img.shields.io/badge/Go-8b5cf6?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <br />
  <img src="https://img.shields.io/badge/Apache%20Kafka-6366f1?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka" />
  <img src="https://img.shields.io/badge/RabbitMQ-6366f1?style=flat-square&logo=rabbitmq&logoColor=white" alt="RabbitMQ" />
  <img src="https://img.shields.io/badge/GraphQL-6366f1?style=flat-square&logo=graphql&logoColor=white" alt="GraphQL" />
  <img src="https://img.shields.io/badge/Microsserviços-6366f1?style=flat-square" alt="Microsserviços" />
  <img src="https://img.shields.io/badge/Clean%20Architecture-6366f1?style=flat-square" alt="Clean Architecture" />
  <br />
  <img src="https://img.shields.io/badge/PostgreSQL-06b6d4?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Oracle-06b6d4?style=flat-square" alt="Oracle" />
  <img src="https://img.shields.io/badge/AWS-06b6d4?style=flat-square" alt="AWS" />
  <img src="https://img.shields.io/badge/Azure-06b6d4?style=flat-square" alt="Azure" />
  <img src="https://img.shields.io/badge/Docker-06b6d4?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-06b6d4?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-06b6d4?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" />
</p>

### Projeto principal: PetServices

Sistema de clínica veterinária com **3 microsserviços** que conversam por eventos no **Kafka**, rodando em **Kubernetes (AKS)** com deploy automático e rollback no GitHub Actions. Passou por testes de caos (Kafka, Postgres e pods derrubados) e de carga com k6, que levaram a **Outbox, Dead Letter Topic, idempotência e falha rápida com 503**.

```mermaid
flowchart LR
    C["Cadastros + login JWT"] -- Kafka --> A["Agendamento"] -- Kafka --> H["Histórico"]
```

| Repositório | Papel | Stack |
|---|---|---|
| [**PetServices**](https://github.com/carolinebrunheti/PetServices) | Cadastros, login JWT e eventos via Outbox | Java 17 · Spring Boot 4 · Spring Security · Kafka |
| [**PetAgendamentoApi**](https://github.com/carolinebrunheti/PetAgendamentoApi) | Agendamento de consultas, com DLT e idempotência | Java 17 · Spring Boot 4 · Kafka · PostgreSQL |
| [**HistoricoPetApi1**](https://github.com/carolinebrunheti/HistoricoPetApi1) | Histórico de consultas, alimentado por eventos | Java 17 · Spring Boot 4 · Kafka · PostgreSQL |
| [**PetServicesK8s**](https://github.com/carolinebrunheti/PetServicesK8s) | Kubernetes, CI/CD e testes de carga | AKS · GitHub Actions · k6 |

**0** falhas com 150 usuários simultâneos · **0** dados perdidos com o Kafka fora do ar · **239** testes automatizados com Testcontainers

### Outros projetos

| Projeto | Sobre | Stack |
|---|---|---|
| [**AgendamentoAPI**](https://github.com/JavaPosTech/AgendamentoAPI) | Microsserviço de agendamento hospitalar com autenticação JWT e comunicação assíncrona | Java 21 · Spring Security · PostgreSQL |
| [**NotificacaoAPI**](https://github.com/JavaPosTech/NotificacaoAPI) | Consome eventos do RabbitMQ e notifica pacientes por e-mail, com retentativa automática | Spring Boot · RabbitMQ · Spring Retry |
| [**HistoricoAPI**](https://github.com/JavaPosTech/HistoricoAPI) | Histórico de consultas via GraphQL com 100% de cobertura de testes | Spring for GraphQL · JUnit 5 · JaCoCo |
| [**RestauranteAPI v2**](https://github.com/JavaPosTech/V2-RestauranteAPI) | Sistema de gestão de restaurantes reescrito com Clean Architecture | Spring Boot · Clean Architecture |
| [**ApiRestGo**](https://github.com/carolinebrunheti/ApiRestGo) | API REST de clientes em Go com router chi e PostgreSQL via Docker Compose | Go · chi · PostgreSQL · Docker |

<sub>Os projetos da FIAP foram desenvolvidos em grupo na pós-graduação.</sub>

### Contribuições

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/carolinebrunheti/carolinebrunheti/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/carolinebrunheti/carolinebrunheti/output/github-snake.svg" />
  <img alt="Cobrinha percorrendo o gráfico de contribuições" src="https://raw.githubusercontent.com/carolinebrunheti/carolinebrunheti/output/github-snake.svg" />
</picture>

---

<p align="center">
  <sub> Sempre aberta a trocar ideias sobre backend, arquitetura e sistemas distribuídos</sub>
</p>
