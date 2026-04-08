# AWS & Git — Módulo 3 (Data Science)

> Infraestrutura em nuvem e controle de versão para Data Science.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Data Science#fase 1 Fundamentos Linear](../cursos/data-science#fase-1--fundamentos-linear.md)

---
## Aulas
### Aula 1 — Git e GitHub para Data Science

**Conteúdo:**
- Controle de versão no contexto de Data Science
- Por que versionar notebooks e scripts
- Git básico: init, add, commit, push, pull
- Mensagens de commit semânticas para projetos de dados
- `.gitignore` para Data Science (datasets grandes, .env, __pycache__)
- GitHub: repositórios, branches, PRs
- Git LFS: versionando datasets grandes
- DVC (Data Version Control): introdução
- Boas práticas: nunca commitar credenciais ou dados sensíveis
- GitHub Actions: CI para notebooks

**Exercícios práticos (escolha um):**
1. Versionar projeto Python existente: estrutura de pasta data science, commits por etapa (EDA, limpeza, modelo)
2. Criar repositório público de análise com README profissional e notebook organizado
3. Configurar DVC em um projeto: rastrear dataset no S3, versionar com Git

**Recursos:**
- [DVC Official Docs](https://dvc.org/doc)
- [Conventional Commits](https://www.conventionalcommits.org/pt-br/)
- [Git LFS](https://git-lfs.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Organizar todos os projetos Python em repositórios GitHub públicos com README
2. Criar template de repositório Data Science: estrutura de pastas, gitignore, README padrão
3. Explorar repositórios Data Science no GitHub e listar 3 boas práticas observadas
4. Configurar pre-commit hooks: verificar formatação antes de commitar
5. Criar GitHub Actions que roda notebook Jupyter a cada push e salva outputs

**Tempo:** 4h (1h teoria + 2h prática + 1h configuração)

---

### Aula 2 — AWS: IAM, EC2 e S3 para Dados

**Conteúdo:**
- IAM: usuário, grupos e políticas para Data Science
- S3: armazenamento de datasets, modelos e outputs
- Estrutura de bucket para dados: raw/, processed/, models/, outputs/
- Boto3: SDK Python para AWS
- Upload/download de datasets com Boto3
- EC2 para notebooks: instâncias com GPU (introdução)
- SageMaker Studio (visão geral)
- Boas práticas de custo: só ligar quando usar
- Lifecycle policies para dados antigos
- Presigned URLs para compartilhar datasets

**Exercícios práticos (escolha um):**
1. Criar estrutura de bucket S3 para projeto DS, fazer upload de dataset, acessar via Boto3 no Python
2. Script Python de ingestão: ler CSV local, processar com pandas, salvar processado no S3
3. EC2 com Jupyter: criar instância, instalar Jupyter, acessar no browser via SSH tunnel

**Recursos:**
- [Boto3 Docs](https://boto3.amazonaws.com/v1/documentation/api/latest/)
- [AWS SageMaker](https://docs.aws.amazon.com/pt_br/sagemaker/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar pipeline de dados: download de fonte pública → limpeza → upload S3 processado
2. Script de backup: sincronizar pasta local de datasets com S3 automaticamente
3. Explorar AWS SageMaker Studio e criar notebook conectado a dados no S3
4. Configurar ciclo de vida no S3: datasets com mais de 90 dias vão para Glacier
5. Calcular custo de armazenar 100GB de dados no S3 por 1 ano (diferentes classes)

**Tempo:** 4h (1h teoria + 2h prática + 1h exercícios)

---

### Aula 3 — AWS Glue e ETL na Nuvem

**Conteúdo:**
- O que é ETL (Extract, Transform, Load)
- AWS Glue: ETL serverless
- Glue Data Catalog: metadados dos dados
- Glue Crawlers: descoberta automática de schemas
- Glue Jobs: scripts PySpark para transformação
- AWS Glue vs EMR vs Lambda para ETL
- Particionamento de dados no S3
- Formatos de dados: CSV vs Parquet vs JSON (performance)
- Monitoramento de jobs Glue
- Custo: comparando abordagens

**Exercícios práticos (escolha um):**
1. Criar Glue Crawler para catalogar dataset no S3, inspecionar schema descoberto
2. Criar Glue Job simples: ler CSV do S3, transformar com PySpark, salvar como Parquet
3. Pipeline ETL: dados brutos → Glue Crawler → Glue Job → dados processados → Athena

**Recursos:**
- [AWS Glue Docs](https://docs.aws.amazon.com/pt_br/glue/)
- [PySpark Docs](https://spark.apache.org/docs/latest/api/python/)

**Tarefas de casa (escolha uma ou mais):**
1. Converter dataset grande de CSV para Parquet com Glue e comparar tamanho e velocidade de query
2. Criar Glue Job que faz join de duas fontes de dados e salva resultado
3. Configurar trigger de Glue Job: rodar automaticamente toda vez que arquivo chegar no S3
4. Implementar particionamento por ano/mês/dia nos dados processados
5. Pesquisar sobre Delta Lake e documentar diferença em relação ao Parquet puro

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 4 — Athena: Consultas SQL no S3

**Conteúdo:**
- O que é AWS Athena: SQL direto no S3
- Configurando Athena: workgroup, S3 output
- Criando tabelas externas com MSCK REPAIR TABLE
- Queries SQL no Athena: SELECT, WHERE, GROUP BY
- Performance: particionamento e formatos colunares
- Custo: paga por dado escaneado (Parquet economiza)
- Athena com Python (boto3)
- Conectando Power BI ao Athena (ODBC)
- Athena + Glue Catalog: integração
- Salvando queries frequentes

**Exercícios práticos (escolha um):**
1. Criar tabela Athena sobre dados no S3, executar queries analíticas, comparar custo CSV vs Parquet
2. Conectar Power BI ao Athena via ODBC e criar visualizações em tempo real
3. Script Python que executa queries no Athena e salva resultados localmente

**Recursos:**
- [AWS Athena Docs](https://docs.aws.amazon.com/pt_br/athena/)
- [Athena ODBC Driver](https://docs.aws.amazon.com/athena/latest/ug/connect-with-odbc.html)

**Tarefas de casa (escolha uma ou mais):**
1. Criar análise completa de vendas usando apenas Athena + S3 (sem banco relacional)
2. Comparar performance e custo: mesma query em CSV vs Parquet particionado
3. Conectar Jupyter ao Athena via PyAthena e criar análise exploratória
4. Criar views no Athena para queries complexas frequentes
5. Montar pipeline: Glue ETL → Parquet no S3 particionado → Athena → Power BI

**Tempo:** 4h (1h teoria + 2h prática + 1h exercícios)

---

### Aula 5 — Lambda para Processamento de Dados

**Conteúdo:**
- Lambda no contexto de Data Engineering
- Processamento event-driven
- Trigger S3: processar arquivo ao chegar
- Lambda + pandas: lightweight processing
- Lambda Layers: dependências Python pesadas
- Limitações do Lambda: timeout, memória, tamanho de payload
- Quando usar Lambda vs Glue vs EC2
- Orquestração com Step Functions (introdução)
- CloudWatch para monitoramento de pipelines
- SNS: notificações de sucesso/falha de pipeline

**Exercícios práticos (escolha um):**
1. Lambda trigger S3: novo CSV chega → Lambda processa e salva Parquet → notifica SNS
2. Lambda de validação de dados: verificar schema, tipos e nulos, rejeitar arquivos inválidos
3. Orquestrar 3 Lambdas sequenciais com Step Functions: ingest → transform → load

**Recursos:**
- [AWS Lambda Docs](https://docs.aws.amazon.com/pt_br/lambda/)
- [AWS Step Functions](https://docs.aws.amazon.com/pt_br/step-functions/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar pipeline serverless completo: API externa → Lambda ingestion → S3 → Glue → Athena
2. Lambda de alerta: monitorar métrica e enviar email via SNS quando threshold for atingido
3. Criar Step Functions workflow para pipeline de ML: prep data → train → evaluate → deploy
4. Implementar retry logic no Lambda para lidar com erros transitórios
5. Comparar custos de pipeline: Lambda vs EC2 always-on para 1M eventos/mês

**Tempo:** 4h (1h teoria + 2h prática + 1h arquitetura)

---

### Aula 6 — RDS e Redshift

**Conteúdo:**
- RDS para dados transacionais (OLTP)
- PostgreSQL no RDS: criação e conexão
- psycopg2: conectando Python ao PostgreSQL
- SQLAlchemy + RDS
- AWS Redshift: data warehouse (OLAP)
- Diferença entre OLTP (RDS) e OLAP (Redshift)
- Redshift Serverless (Free Tier)
- Carregando dados no Redshift via COPY do S3
- Consultas analíticas otimizadas para Redshift
- Redshift Spectrum: queries S3 a partir do Redshift

**Exercícios práticos (escolha um):**
1. Criar RDS PostgreSQL, conectar com psycopg2, carregar dataset e executar queries analíticas
2. Pipeline RDS → S3 → Redshift: exportar dados transacionais para análise histórica
3. Comparar performance e custo: mesma query analítica no RDS vs Redshift vs Athena

**Recursos:**
- [AWS Redshift Docs](https://docs.aws.amazon.com/pt_br/redshift/)
- [psycopg2 Docs](https://www.psycopg.org/docs/)

**Tarefas de casa (escolha uma ou mais):**
1. Migrar dados de SQLite local para RDS PostgreSQL
2. Criar pipeline de carga incremental: novos registros RDS → S3 → Redshift diariamente
3. Comparar arquiteturas: Data Lake (S3+Athena) vs Data Warehouse (Redshift) — quando usar cada
4. Explorar Redshift ML: treinar modelo dentro do Redshift com dados do warehouse
5. Criar dashboard Power BI conectado ao Redshift via ODBC

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão de arquitetura)

---

### Aula 7 — CloudWatch e Monitoramento de Pipelines

**Conteúdo:**
- CloudWatch: logs, métricas e alertas
- Log Groups e Log Streams
- Métricas customizadas: instrumentando o código
- CloudWatch Alarms: notificações por email/SNS
- CloudWatch Dashboards: painel operacional
- AWS X-Ray: rastreamento de requests
- Cost Explorer: analisando e otimizando custos
- AWS Budgets: alertas de orçamento
- Tagging: organizando recursos por projeto/time
- Boas práticas de FinOps para Data Science

**Exercícios práticos (escolha um):**
1. Criar dashboard CloudWatch: monitorar Lambda invocations, errors, duration, S3 storage
2. Adicionar métricas customizadas ao pipeline: registrar registros processados, erros e latência
3. Configurar alertas: email quando Lambda falhar ou custo diário ultrapassar $2

**Recursos:**
- [AWS CloudWatch Docs](https://docs.aws.amazon.com/pt_br/cloudwatch/)
- [AWS Cost Explorer](https://docs.aws.amazon.com/pt_br/cost-management/latest/userguide/ce-what-is.html)

**Tarefas de casa (escolha uma ou mais):**
1. Instrumentar todo o pipeline de dados com CloudWatch custom metrics
2. Criar runbook: documento com procedimentos para incidentes comuns
3. Configurar Cost Anomaly Detection: alerta automático de gastos inesperados
4. Criar relatório semanal automático de custos com Lambda + SNS
5. Pesquisar OpenTelemetry e como integrar com AWS X-Ray

**Tempo:** 4h (1h teoria + 2h prática + 1h FinOps)

---

### Aula 8 — Projeto: Pipeline de Dados na AWS

**Conteúdo:**
- Revisão da arquitetura
- Planejando o pipeline de dados
- Implementação: ingestão → processamento → armazenamento → consulta → visualização
- Deploy e automação
- Documentação de arquitetura
- Apresentação final

**Exercício prático:**
1. Pipeline completo: ingestão de dados de API pública → S3 (raw) → Lambda/Glue (transform) → S3 (processed) → Athena (query) → Power BI (visualização)

**Sugestões de projeto:**
1. Pipeline de dados climáticos: API de weather → processamento diário → dashboard
2. Análise de redes sociais: API Twitter/Reddit → ETL → análise de sentimentos → dashboard
3. Pipeline financeiro: cotações de ações → cálculo de indicadores → alertas → visualização
4. Dados governamentais: portal de dados abertos → ETL → análise → relatório Power BI

**Desafio extra:**
1. Implementar orquestração com Apache Airflow no MWAA (Managed Airflow)
2. Adicionar MLflow para rastreamento de experimentos de ML no pipeline
3. Criar IaC com Terraform ou AWS CDK

**Tarefas de casa (escolha uma ou mais):**
1. Criar diagrama de arquitetura completo do pipeline com custos estimados
2. Escrever LinkedIn post ou artigo documentando o pipeline construído
3. Adicionar testes automatizados para validação de dados em cada etapa
4. Criar documentação técnica: data catalog descrevendo cada dataset
5. Pesquisar sobre certificação AWS Data Engineer e criar plano de estudos

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Pipeline de dados rodando na AWS
2. Dados organizados no S3 (raw + processed)
3. Pelo menos uma transformação (Glue ou Lambda)
4. Consultas via Athena
5. Visualização no Power BI ou similar
6. Diagrama de arquitetura
7. README com instruções e custos estimados

---

## Materiais do Professor

- [Pasta GIT E AWS > AWS — Google Drive](https://drive.google.com/drive/folders/131Bv-q7A4QPLl53dSEOrQJ8tsvp6nFyW)
- [AWS_01.pptx](https://drive.google.com/file/d/1fdy7ZJGLlEJdcC79jSWDAUetuYzOeoEl/view)
- [AWS _ Aula 2.pptx](https://drive.google.com/file/d/14TjI4tF_YVA9uiKzSvPePuCwowA0-2kH/view)
- [AWS _ Aula 3.pptx](https://drive.google.com/file/d/1mJ1ZDzmJ4mH1nOHjFQXISaYGpnAC-bPy/view)
- [AWS _ Aula 4.pptx](https://drive.google.com/file/d/1deNAJoNuf-ahv71jPZ_u42suhFoTXlCB/view)
- [AWS _ Aula 6.pptx](https://drive.google.com/file/d/1hIStpindf52EEMjE3k7l-IC7t4uFb5PU/view)
- [AWS _ Aula X.pptx](https://drive.google.com/file/d/16serq5WTfBV097N5Fssz59sloPfwEj_-/view)

---

## Próximo módulo

→ [Power Bi](../modulos/power-bi.md)

---

#modulo #aws #cloud #s3 #lambda #glue #athena #datascience #dataengineering
