# Plano de Estudos — Deivyd Garcez

> Objetivo: consolidar título de Analista Sênior no mercado de software e infraestrutura.
> Baseado no que já domino e nos gaps identificados em julho/2026.

---

## Prioridade 1 — Alta (gaps que travam entrevistas)

### Docker
O mercado espera que qualquer backend rode em container. Hoje entrego como `.exe`; a expectativa é `docker-compose up`.

| Recurso | Tipo | Custo |
|---|---|---|
| [Docker — documentação oficial (Get Started)](https://docs.docker.com/get-started/) | Leitura / labs | Grátis |
| [Play with Docker](https://labs.play-with-docker.com/) | Laboratório online | Grátis |
| [Curso Docker — Matheus Battisti (YouTube)](https://www.youtube.com/watch?v=RE31GWJGkwA) | Vídeo PT-BR | Grátis |
| [Docker & Kubernetes: The Practical Guide — Udemy](https://www.udemy.com/course/docker-kubernetes-the-practical-guide/) | Vídeo + labs | Pago (~R$30 promoção) |

**Meta prática:** dockerizar o backend do Invec (FastAPI + variáveis de ambiente via `.env`).

---

### PostgreSQL (banco mainstream)
Firebird é nicho. Entrevistas cobram índices, transactions, EXPLAIN ANALYZE em Postgres ou MySQL.

| Recurso | Tipo | Custo |
|---|---|---|
| [PostgreSQL Tutorial](https://www.postgresqltutorial.com/) | Leitura | Grátis |
| [CS50's Introduction to Databases (Harvard)](https://cs50.harvard.edu/sql/2024/) | Vídeo + exercícios | Grátis |
| [pgAdmin](https://www.pgadmin.org/) | Ferramenta GUI | Grátis |
| [Curso Banco de Dados — Bóson Treinamentos (YouTube)](https://www.youtube.com/playlist?list=PLucm8g_ezqNqzXyP1BxZgpSTDLZFKFhg7) | Vídeo PT-BR | Grátis |
| [PostgreSQL Bootcamp — Udemy](https://www.udemy.com/course/postgresqlmasterclass/) | Vídeo + labs | Pago (~R$30 promoção) |

**Meta prática:** recriar as tabelas do Invec em Postgres; comparar queries com Firebird.

---

### Linux CLI
Seus servidores de clientes são Windows. O mercado de backend/DevOps é majoritariamente Linux.

| Recurso | Tipo | Custo |
|---|---|---|
| [Linux Journey](https://linuxjourney.com/) | Interativo | Grátis |
| [The Linux Command Line (livro online)](https://linuxcommand.org/tlcl.php) | Leitura | Grátis |
| [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) | Desafios práticos (SSH) | Grátis |
| [Linux para Desenvolvedores — DIO](https://www.dio.me/courses/linux-para-desenvolvedores) | Vídeo PT-BR | Grátis |

**Meta prática:** subir uma EC2 Amazon Linux, instalar Python + uvicorn, rodar o servidor Invec sem Windows.

---

### Git avançado + Fluxo de time
Você usa git mas o mercado cobra: branch strategy, rebase vs merge, PR com code review, conventional commits.

| Recurso | Tipo | Custo |
|---|---|---|
| [Pro Git (livro oficial)](https://git-scm.com/book/pt-br/v2) | Leitura PT-BR | Grátis |
| [Learn Git Branching (interativo)](https://learngitbranching.js.org/?locale=pt_BR) | Interativo visual | Grátis |
| [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/) | Referência | Grátis |

**Meta prática:** criar um branch `feature/`, abrir PR com descrição, fazer squash merge no próprio inventario-app.

---

## Prioridade 2 — Média (separa pleno de sênior)

### CI/CD completo (deploy automático)
Você já tem GitHub Actions rodando pytest. O próximo nível é deploy automático ao dar push.

| Recurso | Tipo | Custo |
|---|---|---|
| [GitHub Actions — documentação oficial](https://docs.github.com/pt/actions) | Leitura | Grátis |
| [GitHub Actions — Full Course (TechWorld with Nana, YouTube)](https://www.youtube.com/watch?v=R8_veQiYBjI) | Vídeo inglês | Grátis |
| [CI/CD com GitHub Actions — Rocketseat (YouTube)](https://www.youtube.com/watch?v=IKs7GI84oGk) | Vídeo PT-BR | Grátis |

**Meta prática:** pipeline que, ao dar push em master, sobe o servidor no EC2 Linux automaticamente.

---

### Terraform (Infraestrutura como código)
Sua infra AWS foi criada pelo console. IaC é exigido em vagas DevOps/Cloud sênior.

| Recurso | Tipo | Custo |
|---|---|---|
| [Terraform — Get Started AWS (HashiCorp)](https://developer.hashicorp.com/terraform/tutorials/aws-get-started) | Hands-on oficial | Grátis |
| [Terraform em 1 hora — Fernanda Kipper (YouTube)](https://www.youtube.com/watch?v=bIPF_hzmQGE) | Vídeo PT-BR | Grátis |
| [Terraform: Do Zero ao Avançado — Udemy](https://www.udemy.com/course/terraform-do-zero-ao-avancado/) | Vídeo PT-BR | Pago (~R$30 promoção) |

**Meta prática:** escrever o `.tf` que sobe uma EC2 + security group + Elastic IP — o que você faz hoje no console.

---

### Redis
Cache, sessões, filas — aparece em toda stack de produto escalável.

| Recurso | Tipo | Custo |
|---|---|---|
| [Redis University (redis.io)](https://university.redis.io/) | Cursos oficiais | Grátis |
| [Redis em 100 segundos (Fireship, YouTube)](https://www.youtube.com/watch?v=G1rOthIU-uo) | Vídeo inglês | Grátis |
| [Redis com Python — Real Python](https://realpython.com/python-redis/) | Tutorial | Grátis |

**Meta prática:** adicionar cache de token JWT no Invec usando Redis em vez de dicionário em memória.

---

### Observabilidade (logs estruturados + métricas)
CloudWatch básico não conta. Mercado quer correlation ID, dashboards, alertas.

| Recurso | Tipo | Custo |
|---|---|---|
| [Grafana — documentação + playground](https://play.grafana.org/) | Playground grátis | Grátis |
| [OpenTelemetry para Python](https://opentelemetry.io/docs/languages/python/) | Documentação | Grátis |
| [Logging estruturado com Python — Real Python](https://realpython.com/python-logging/) | Tutorial | Grátis |
| [Datadog — trial 14 dias](https://www.datadoghq.com/) | Ferramenta comercial | Trial grátis |

---

## Prioridade 3 — Certificação (valida tudo e abre faixa salarial)

### AWS Solutions Architect Associate

Valida o que você já faz na prática e preenche os gaps de VPC, RDS, ALB, Auto Scaling.

| Recurso | Tipo | Custo |
|---|---|---|
| [AWS Skill Builder — cursos oficiais](https://skillbuilder.aws/) | Vídeo oficial | Grátis (maioria) |
| [Stephane Maarek — SAA-C03 (Udemy)](https://www.udemy.com/course/aws-certified-solutions-architect-associate-saa-c03/) | Mais recomendado do mercado | Pago (~R$30 promoção) |
| [Simulados — Tutorials Dojo](https://tutorialsdojo.com/courses/aws-certified-solutions-architect-associate-practice-exams/) | Simulado (6 provas completas) | Pago (~US$15) |
| [AWS Whitepapers](https://aws.amazon.com/whitepapers/) | Leitura oficial | Grátis |
| [Exame oficial — AWS](https://aws.amazon.com/certification/certified-solutions-architect-associate/) | Prova (Pearson VUE) | Pago (~US$150) |

**O que focar** (com base na sua infra atual):
- VPC customizada: subnets privadas, NAT Gateway, route tables
- RDS: Multi-AZ, Read Replicas, Aurora
- ALB / NLB + Auto Scaling Groups
- ElastiCache, SQS, CloudFront
- EC2, Lambda, S3, IAM — já domina na prática, só revisar o que o exame cobra

---

## Ordem sugerida de execução

```
Mês 1-2   → Docker + Linux CLI  (resolve o gap mais visível em entrevistas)
Mês 2-3   → PostgreSQL          (dominar queries, índices, explain)
Mês 3-4   → CI/CD completo      (pipeline de deploy real no EC2 Linux)
Mês 4-5   → Terraform           (IaC da infra que já existe na AWS)
Mês 5-6   → AWS SAA-C03         (estudo + simulados + prova)
Paralelo  → Git avançado        (aplicar em todo commit do inventario-app)
```

---

## Plataformas que concentram o conteúdo

| Plataforma | Tipo | Obs |
|---|---|---|
| [YouTube](https://youtube.com) | Vídeo | PT-BR disponível para quase tudo |
| [Udemy](https://udemy.com) | Vídeo + labs | Promoções frequentes (~R$27-35) |
| [DIO](https://dio.me) | Vídeo PT-BR | Grátis com certificado |
| [Alura](https://alura.com.br) | Vídeo PT-BR | Pago (~R$100/mês), qualidade alta |
| [Linux Foundation Training](https://training.linuxfoundation.org/) | Cursos + certs | Grátis e pago |
| [Real Python](https://realpython.com) | Texto/tutorial | Inglês, profundidade técnica |
| [AWS Skill Builder](https://skillbuilder.aws) | Oficial AWS | Grátis (maioria) |
