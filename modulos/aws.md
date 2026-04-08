# AWS — Módulo 6

> Computação em nuvem com Amazon Web Services.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Fullstack Python#fase 2 Especializacao Circular](../cursos/fullstack-python#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — Cloud Computing e AWS Fundamentos

**Conteúdo:**
- O que é Cloud Computing: IaaS, PaaS, SaaS
- Por que as empresas migraram para a nuvem
- AWS: principais serviços e regiões
- Criando conta AWS (Free Tier)
- AWS Console: navegando pela interface
- IAM (Identity and Access Management): usuários, grupos, roles, policies
- Princípio do menor privilégio
- Criando usuário IAM para uso diário (nunca usar root)
- AWS CLI: instalação e configuração
- Billing Dashboard: controlando custos

**Exercícios práticos (escolha um):**
1. Criar conta AWS, configurar MFA na conta root, criar usuário IAM admin e configurar AWS CLI
2. Criar grupos IAM com permissões específicas: Developer (EC2+S3), DataEngineer (S3+Glue+Athena)
3. Explorar AWS Free Tier e documentar o que pode usar gratuitamente para um projeto real

**Recursos:**
- [AWS Free Tier](https://aws.amazon.com/pt/free/)
- [AWS Documentation](https://docs.aws.amazon.com/)
- [AWS Skills Builder](https://skillbuilder.aws/) — cursos gratuitos

**Tarefas de casa (escolha uma ou mais):**
1. Completar um módulo do AWS Cloud Practitioner Essentials (gratuito no Skills Builder)
2. Criar política IAM customizada para um cenário específico com apenas permissões necessárias
3. Configurar AWS Budget Alarm: notificar por email se custo ultrapassar $5
4. Pesquisar e documentar os 10 serviços AWS mais usados no mercado
5. Criar organização de tags para rastrear custos por projeto

**Tempo:** 4h (1h teoria + 2h prática + 1h exploração)

---

### Aula 2 — EC2: Servidores na Nuvem

**Conteúdo:**
- O que é EC2 (Elastic Compute Cloud)
- Tipos de instâncias: famílias (t, m, c, r), tamanhos
- AMIs: imagens de máquina pré-configuradas
- Security Groups: firewall da instância
- Key Pairs: acessando via SSH
- Criando e acessando instância EC2 (Ubuntu)
- Instalando e configurando aplicação na EC2
- Elastic IP: IP fixo para a instância
- User Data: scripts de inicialização
- Monitoramento básico com CloudWatch

**Exercícios práticos (escolha um):**
1. Criar instância EC2 t2.micro, conectar via SSH, instalar Python + Flask, subir API simples com acesso público
2. Criar EC2 com User Data: instância já inicializa com Nginx + app configurado
3. Subir o projeto Flask do módulo anterior na EC2, configurar domínio com IP elástico

**Recursos:**
- [AWS EC2 Getting Started](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/EC2_GetStarted.html)
- [SSH Guide](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)

**Tarefas de casa (escolha uma ou mais):**
1. Subir o projeto Flask completo na EC2 com Gunicorn + Nginx
2. Configurar auto-start do app via systemd (app reinicia se a instância reiniciar)
3. Criar snapshot da instância e restaurar em nova EC2
4. Monitorar a instância com CloudWatch e criar alarme de CPU alta
5. Pesquisar diferença entre EC2, ECS e Lambda: quando usar cada um

**Tempo:** 4h (1h teoria + 2h prática + 1h deploy ao vivo)

---

### Aula 3 — S3: Armazenamento de Objetos

**Conteúdo:**
- O que é S3 e casos de uso
- Buckets e objetos: estrutura hierárquica simulada
- Criando bucket com configurações corretas
- Upload, download e delete de objetos
- Permissões: bucket policy vs ACL
- Hosting de site estático no S3
- Versionamento de objetos
- Ciclo de vida: mover para classes de storage mais baratas
- CloudFront: CDN + HTTPS para S3
- Pré-signed URLs: acesso temporário a objetos privados
- Boto3: manipulando S3 com Python

**Exercícios práticos (escolha um):**
1. Criar bucket, configurar hosting estático, fazer upload do frontend React e acessar pela URL do S3
2. Script Python com Boto3: upload de múltiplos arquivos, listar objetos, gerar pre-signed URL
3. Configurar CloudFront na frente do S3 para servir assets com HTTPS e cache

**Recursos:**
- [AWS S3 Docs](https://docs.aws.amazon.com/pt_br/s3/)
- [Boto3 S3 Docs](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3.html)

**Tarefas de casa (escolha uma ou mais):**
1. Script de backup automático: comprimir pasta local e enviar para S3 diariamente
2. Implementar upload de arquivos do Flask direto para S3 (em vez de servidor local)
3. Configurar ciclo de vida: mover objetos com mais de 30 dias para Glacier
4. Hospedar o portfólio pessoal no S3 + CloudFront com HTTPS
5. Criar versioning no bucket e simular recuperação de versão anterior de um arquivo

**Tempo:** 4h (1h teoria + 2h prática + 1h exercícios)

---

### Aula 4 — RDS: Banco de Dados Gerenciado

**Conteúdo:**
- O que é RDS (Relational Database Service)
- Engines suportadas: PostgreSQL, MySQL, MariaDB, Aurora
- Free Tier: PostgreSQL db.t3.micro
- Criando instância RDS PostgreSQL
- Grupos de segurança: permitindo acesso
- Conectando com DBeaver ou pgAdmin
- Backup automático e snapshots
- Multi-AZ: alta disponibilidade
- Read Replicas: escalabilidade de leitura
- Conectando aplicação Flask ao RDS
- Migrações em produção

**Exercícios práticos (escolha um):**
1. Criar RDS PostgreSQL, conectar com DBeaver, criar banco, usuário e tabelas, migrar dados do SQLite local
2. Conectar a API Flask ao RDS, configurar via variáveis de ambiente, fazer deploy na EC2
3. Criar script de migração: exportar dados do SQLite local e importar no PostgreSQL na AWS

**Recursos:**
- [AWS RDS Docs](https://docs.aws.amazon.com/pt_br/rds/)
- [DBeaver Community](https://dbeaver.io/)

**Tarefas de casa (escolha uma ou mais):**
1. Migrar projeto Flask completo para usar RDS PostgreSQL em produção
2. Configurar backup automático diário e testar restore de snapshot
3. Criar usuário de banco com permissões mínimas para a aplicação
4. Monitorar RDS com CloudWatch: conexões, CPU, storage
5. Pesquisar Aurora Serverless: quando faz sentido economicamente

**Tempo:** 4h (1h teoria + 2h prática + 1h migração)

---

### Aula 5 — Lambda e Serverless

**Conteúdo:**
- O que é Serverless e quando usar
- Lambda: funções sem servidor
- Criando função Lambda com Python
- Triggers: API Gateway, S3, CloudWatch Events, SQS
- Variáveis de ambiente no Lambda
- Layers: dependências compartilhadas
- Cold start: o que é e como mitigar
- API Gateway: criando HTTP API
- Lambda + API Gateway: API serverless completa
- Monitoramento com CloudWatch Logs
- Custo: comparando Lambda vs EC2

**Exercícios práticos (escolha um):**
1. Criar Lambda + API Gateway: função Python que retorna dados JSON, acessível via HTTP
2. Lambda trigger de S3: toda vez que arquivo é enviado ao S3, função processa e salva metadados no DynamoDB
3. Migrar endpoints simples da API Flask para Lambda (CRUD básico serverless)

**Recursos:**
- [AWS Lambda Docs](https://docs.aws.amazon.com/pt_br/lambda/)
- [Serverless Framework](https://www.serverless.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar API serverless completa (CRUD) com Lambda + API Gateway + DynamoDB
2. Criar Lambda de processamento de imagens: trigger S3 → redimensionar e salvar em outro bucket
3. Agendar Lambda com CloudWatch Events: rodar relatório todo dia às 8h
4. Criar Lambda de envio de email: trigger SQS → processar fila e enviar emails
5. Comparar custos: mesma API em EC2 t2.micro vs Lambda (simular 100k requisições/mês)

**Tempo:** 4h (1h teoria + 2h prática + 1h debate serverless vs tradicional)

---

### Aula 6 — DynamoDB e Serviços de Mensageria

**Conteúdo:**
- DynamoDB: NoSQL gerenciado
- Conceitos: tabelas, itens, atributos, partition key, sort key
- Criando tabela e inserindo dados
- Queries e scans: diferenças e performance
- GSI (Global Secondary Index)
- Boto3 + DynamoDB
- SQS (Simple Queue Service): filas de mensagens
- Criando fila e publicando/consumindo mensagens com Python
- SNS (Simple Notification Service): pub/sub
- Casos de uso: desacoplar sistemas, processar em background
- Dead Letter Queues

**Exercícios práticos (escolha um):**
1. Criar tabela DynamoDB de sessões de usuário: chave por user_id, expiração automática com TTL
2. Fila SQS + Lambda: simular sistema de notificações por email (publicar na fila, Lambda consome e "envia")
3. API com resposta assíncrona: POST cria job na fila, GET /job/:id retorna status (PENDING/DONE)

**Recursos:**
- [AWS DynamoDB Docs](https://docs.aws.amazon.com/pt_br/dynamodb/)
- [AWS SQS Docs](https://docs.aws.amazon.com/pt_br/sqs/)

**Tarefas de casa (escolha uma ou mais):**
1. Migrar sessões de usuário da aplicação Flask para DynamoDB
2. Criar sistema de tarefas em background com SQS: relatório pesado processado de forma assíncrona
3. Implementar fan-out com SNS: um evento notifica múltiplos serviços via subscriptions
4. Criar Dead Letter Queue para capturar mensagens que falharam e processar novamente
5. Comparar DynamoDB vs PostgreSQL RDS: quando usar cada um com exemplos práticos

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 7 — CI/CD com GitHub Actions e CodePipeline

**Conteúdo:**
- O que é CI/CD (Continuous Integration / Delivery)
- GitHub Actions: workflows, jobs, steps
- Criando workflow de CI: testes automáticos a cada push
- Deploy automático no Render/EC2 via GitHub Actions
- AWS CodePipeline: pipeline nativo da AWS
- CodeBuild: build automatizado
- CodeDeploy: deploy em EC2
- Variáveis de ambiente e secrets no GitHub
- Docker + ECR (Elastic Container Registry)
- Boas práticas de CI/CD

**Exercícios práticos (escolha um):**
1. Criar workflow GitHub Actions: push → rodar pytest → se passou, deploy automático no Render
2. Pipeline completo com AWS: CodePipeline → CodeBuild (testes+build Docker) → ECR → EC2
3. CI para múltiplos ambientes: push na main → staging, tag de versão → produção

**Recursos:**
- [GitHub Actions Docs](https://docs.github.com/pt/actions)
- [AWS CodePipeline Docs](https://docs.aws.amazon.com/pt_br/codepipeline/)

**Tarefas de casa (escolha uma ou mais):**
1. Configurar CI para todos os projetos do módulo
2. Criar pipeline de deploy para produção com aprovação manual obrigatória
3. Adicionar notificação no Slack/Telegram ao fazer deploy (webhook)
4. Criar badge de CI no README: status do último build
5. Pesquisar sobre GitOps e ArgoCD: documentar a diferença de abordagem

**Tempo:** 4h (1h teoria + 2h prática + 1h configuração ao vivo)

---

### Aula 8 — Projeto: Deploy Completo na AWS

**Conteúdo:**
- Revisão da arquitetura completa
- Planejando a infraestrutura do projeto
- Implementação: EC2 + RDS + S3 + Lambda (conforme necessidade)
- CI/CD com GitHub Actions
- Monitoramento com CloudWatch
- Documentação da arquitetura (diagrama)
- Estimativa de custos
- Apresentação final

**Exercício prático:**
1. Deploy completo do projeto Flask: EC2 + RDS PostgreSQL + S3 para uploads + CI/CD com GitHub Actions

**Desafio extra:**
1. Adicionar Lambda para processamento assíncrono
2. Configurar Auto Scaling Group na EC2
3. Criar diagrama de arquitetura com AWS Architecture Diagrams

**Tarefas de casa (escolha uma ou mais):**
1. Criar diagrama de arquitetura AWS do projeto com draw.io ou Lucidchart
2. Calcular estimativa mensal de custos com AWS Pricing Calculator
3. Adicionar CloudWatch Dashboard monitorando EC2, RDS e Lambda
4. Criar runbook: documento com procedimentos de operação do sistema
5. Estudar para AWS Cloud Practitioner (certificação de entrada)

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Aplicação deployada na AWS (EC2 ou Lambda)
2. Banco de dados no RDS
3. Arquivos estáticos no S3
4. CI/CD com GitHub Actions
5. Diagrama de arquitetura
6. README com URL de produção

---

## Materiais do Professor

- [Pasta GIT E AWS > AWS — Google Drive](https://drive.google.com/drive/folders/131Bv-q7A4QPLl53dSEOrQJ8tsvp6nFyW)
- [AWS_01.pptx](https://drive.google.com/file/d/1fdy7ZJGLlEJdcC79jSWDAUetuYzOeoEl/view)
- [AWS _ Aula 2.pptx](https://drive.google.com/file/d/14TjI4tF_YVA9uiKzSvPePuCwowA0-2kH/view)
- [AWS _ Aula 3.pptx](https://drive.google.com/file/d/1mJ1ZDzmJ4mH1nOHjFQXISaYGpnAC-bPy/view)
- [AWS _ Aula 4.pptx](https://drive.google.com/file/d/1deNAJoNuf-ahv71jPZ_u42suhFoTXlCB/view)
- [AWS _ Aula 6.pptx](https://drive.google.com/file/d/1hIStpindf52EEMjE3k7l-IC7t4uFb5PU/view)
- [AWS _ Aula X.pptx](https://drive.google.com/file/d/16serq5WTfBV097N5Fssz59sloPfwEj_-/view)
- [kahoot_aws.csv](https://drive.google.com/file/d/1mOsxvZO9lAlaGIU9iPFtcWqGVXYthxdh/view)

---

## Próximo módulo

→ [Projeto Final Python](../modulos/projeto-final-python.md)

---

#modulo #aws #cloud #ec2 #s3 #lambda #rds #serverless #cicd
