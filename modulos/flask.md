# Flask — Módulo 4

> Framework web leve e flexível para Python.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Fullstack Python#fase 2 Especializacao Circular](../cursos/fullstack-python#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — Flask e Templates Jinja2

**Conteúdo:**
- Revisão de Flask: rotas, request, response
- Templates com Jinja2: `render_template()`
- Sintaxe Jinja2: `{{ variavel }}`, `{% if %}`, `{% for %}`
- Template inheritance: `{% extends %}`, `{% block %}`
- Arquivos estáticos: CSS, JS, imagens com `url_for('static', ...)`
- Passando dados do Python para o template
- Filtros Jinja2: `| upper`, `| date`, `| truncate`
- Macros: componentes reutilizáveis no template
- Flash messages: `flash()` e `get_flashed_messages()`

**Exercícios práticos (escolha um):**
1. Blog estático: listar posts de um array Python, cada post tem página própria via template herança
2. Catálogo de produtos: template base, página de listagem e página de detalhe
3. Dashboard de notas: receber lista de alunos, renderizar tabela com situação colorida

**Recursos:**
- [Flask Docs - Templates](https://flask.palletsprojects.com/templating/)
- [Jinja2 Docs](https://jinja.palletsprojects.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar site pessoal multi-página com Jinja2: home, sobre, projetos, contato
2. Template de email em HTML com Jinja2 (simular envio por arquivo)
3. Dashboard de métricas usando dados de uma lista Python
4. Criar macro de paginação reutilizável para qualquer listagem
5. Portfólio com dados vindo de arquivo JSON e renderizados via Jinja2

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Formulários com WTForms

**Conteúdo:**
- Flask-WTF: instalação e configuração
- Definindo formulários como classes Python
- Campos: `StringField`, `EmailField`, `PasswordField`, `SelectField`, `TextAreaField`
- Validadores: `DataRequired`, `Email`, `Length`, `EqualTo`
- CSRF protection: o que é e como funciona no Flask-WTF
- Renderizando formulários no template
- Processando submissão: `form.validate_on_submit()`
- Exibindo erros de validação
- Formulários de edição: pré-populando campos

**Exercícios práticos (escolha um):**
1. Formulário de contato com validação: nome (required), email (valid), mensagem (min 20 chars)
2. Formulário de cadastro de produto: nome, categoria (select), preço (decimal), descrição, validação completa
3. Formulário de login + cadastro com senhas iguais e email único

**Recursos:**
- [Flask-WTF Docs](https://flask-wtf.readthedocs.io/)
- [WTForms Validators](https://wtforms.readthedocs.io/en/3.0.x/validators/)

**Tarefas de casa (escolha uma ou mais):**
1. Formulário de pedido: produto (select), quantidade (number), endereço, telefone — com todas as validações
2. Formulário multi-step: 3 etapas (dados pessoais, endereço, confirmação)
3. Formulário de busca avançada com múltiplos filtros opcionais
4. Criar formulário de upload de arquivo (imagem) com validação de tipo e tamanho
5. Formulário com campo dinâmico: adicionar/remover itens via JavaScript + Flask

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 3 — Flask-Login e Autenticação

**Conteúdo:**
- Flask-Login: instalação e configuração
- `UserMixin` e `@login_required`
- `login_user()`, `logout_user()`, `current_user`
- `LoginManager` e `user_loader`
- Hashing de senhas com Werkzeug
- Sessões: como o Flask mantém o usuário logado
- Redirecionamento após login
- "Remember me" functionality
- Proteção de rotas por role (manual)
- Mensagens de boas-vindas e feedback

**Exercícios práticos (escolha um):**
1. Sistema de autenticação: registro, login, logout, página protegida com perfil do usuário
2. Blog com autenticação: visitante vê posts, logado pode criar e editar os próprios
3. Painel admin: apenas usuários com role 'admin' acessam rotas /admin/*

**Recursos:**
- [Flask-Login Docs](https://flask-login.readthedocs.io/)
- [OWASP Authentication](https://owasp.org/www-project-web-security-testing-guide/)

**Tarefas de casa (escolha uma ou mais):**
1. Adicionar "esqueci minha senha": gerar token por email (simular com print)
2. Implementar "perfil do usuário": editar nome, email e avatar (upload)
3. Criar sistema de 2FA básico: gerar código de 6 dígitos e verificar
4. Adicionar log de acessos: registrar IP, data/hora e rota de cada login
5. Implementar bloqueio após 5 tentativas de login falhas

**Tempo:** 4h (1h teoria + 2h prática + 1h revisão de segurança)

---

### Aula 4 — Flask-SQLAlchemy Avançado

**Conteúdo:**
- Relacionamentos: 1:N, N:N, 1:1
- `backref` e `back_populates`
- Lazy loading vs eager loading
- Migrações com Flask-Migrate: `flask db init`, `migrate`, `upgrade`
- Queries avançadas: join, filter, order, paginate
- Paginação com `paginate()`
- Eventos SQLAlchemy: `@event.listens_for`
- Transações e rollback
- Validações a nível de modelo
- Soft delete: campo `deleted_at`

**Exercícios práticos (escolha um):**
1. Sistema de blog completo: User → Posts → Comments (1:N e N:N com tags)
2. E-commerce básico: User, Product, Category (N:N), Order, OrderItem
3. Rede social: User, Post, Like (N:N), Follow (self-referential)

**Recursos:**
- [Flask-SQLAlchemy Docs](https://flask-sqlalchemy.palletsprojects.com/)
- [Flask-Migrate Docs](https://flask-migrate.readthedocs.io/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar migração para adicionar tabela nova em projeto existente
2. Implementar busca full-text simples com `LIKE` e múltiplos campos
3. Adicionar timestamps automáticos (`created_at`, `updated_at`) a todos os modelos
4. Criar seed completo com Faker para popular banco com dados realistas
5. Documentar diagrama ER do projeto com dbdiagram.io

**Tempo:** 4h (1h teoria + 2h prática + 1h modelagem)

---

### Aula 5 — Blueprints e Estrutura de Projeto

**Conteúdo:**
- Application Factory: `create_app()` pattern
- Blueprints: organizando rotas por módulo
- Separação em pastas: `auth/`, `blog/`, `admin/`
- Config por ambiente: `DevelopmentConfig`, `ProductionConfig`
- Extensions: inicializando SQLAlchemy, Login, etc. fora do app
- Error handlers: `@app.errorhandler(404)`
- Custom Jinja2 filters e context processors
- Logging configurado
- Estrutura profissional final

**Exercícios práticos (escolha um):**
1. Refatorar projeto existente com Application Factory + Blueprints
2. Criar novo projeto já na estrutura profissional desde o início
3. Criar Blueprint de admin completo: dashboard, listagem e edição de entidades

**Recursos:**
- [Flask Application Factory](https://flask.palletsprojects.com/patterns/appfactories/)
- [Flask Large App Guide](https://flask.palletsprojects.com/patterns/packages/)

**Tarefas de casa (escolha uma ou mais):**
1. Refatorar todos os projetos anteriores usando Application Factory
2. Criar Blueprint de API (JSON) separado do Blueprint de views (HTML)
3. Implementar config por variáveis de ambiente com fallbacks seguros
4. Criar middleware de logging que registra tempo de cada requisição
5. Criar blueprint de health check: GET /health retorna status e versão

**Tempo:** 4h (1h teoria + 2h prática + 1h apresentação)

---

### Aula 6 — Upload, Email e Tarefas Background

**Conteúdo:**
- Upload de arquivos com Flask: `request.files`, `secure_filename`
- Validação de tipo e tamanho de arquivo
- Armazenando arquivos localmente e na nuvem (S3 básico)
- Enviando emails com Flask-Mail
- Templates de email em HTML
- Tarefas assíncronas com Celery + Redis (introdução)
- Agendamento de tarefas: Celery Beat
- Notificações: email de boas-vindas, reset de senha
- Webhooks: o que são e como implementar

**Exercícios práticos (escolha um):**
1. Sistema de avatar: upload de foto de perfil, validar tipo (png/jpg) e tamanho (<2MB), salvar e exibir
2. Formulário de contato com envio de email: preencher form → Flask-Mail → receber email real
3. Sistema de notificações: ao criar usuário, disparar email de boas-vindas (pode ser só print em dev)

**Recursos:**
- [Flask-Mail Docs](https://flask-mail.readthedocs.io/)
- [Celery Docs](https://docs.celeryq.dev/)
- [Boto3 - AWS S3](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3.html)

**Tarefas de casa (escolha uma ou mais):**
1. Implementar reset de senha por email: gerar token, enviar link, validar e atualizar senha
2. Upload de múltiplos arquivos: galeria de imagens com thumbnail gerado automaticamente (Pillow)
3. Criar tarefa Celery de relatório: gerar PDF com dados e enviar por email
4. Implementar importação de dados via CSV upload
5. Webhook de pagamento: simular recebimento e processar evento

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 7 — Docker e Deploy

**Conteúdo:**
- O que é Docker e por que usar
- Dockerfile para aplicação Flask
- `docker build` e `docker run`
- Docker Compose: Flask + PostgreSQL + Redis
- Variáveis de ambiente no Docker
- Volumes para persistência
- Diferença entre dev e prod no Docker
- Deploy no Render com Docker
- PostgreSQL em produção (Render PostgreSQL)
- Nginx como reverse proxy (introdução)
- Gunicorn: servidor WSGI de produção

**Exercícios práticos (escolha um):**
1. Dockerizar projeto Flask existente: Dockerfile + docker-compose com PostgreSQL
2. Deploy completo no Render: Flask + PostgreSQL, variáveis de ambiente configuradas
3. Criar ambiente de desenvolvimento com Docker Compose: Flask + PostgreSQL + PgAdmin

**Recursos:**
- [Docker Official Docs](https://docs.docker.com/)
- [Render - Flask Deploy](https://render.com/docs/deploy-flask)
- [Real Python - Docker Flask](https://realpython.com/docker-in-action-faq/)

**Tarefas de casa (escolha uma ou mais):**
1. Dockerizar todos os projetos do módulo
2. Configurar GitHub Actions para build e push de imagem Docker
3. Configurar domínio customizado no Render
4. Implementar health check no container Docker
5. Pesquisar sobre Kubernetes e documentar diferença com Docker Compose

**Tempo:** 4h (1h teoria + 2h prática + 1h deploy ao vivo)

---

### Aula 8 — Projeto Final do Módulo

**Conteúdo:**
- Revisão de todos os conceitos
- Definição e planejamento do projeto
- Implementação guiada
- Deploy com Docker + PostgreSQL
- Apresentação final

**Exercício prático:**
1. Web app Flask completo: autenticação, CRUD, templates Jinja2, upload, deploy Docker no Render

**Sugestões de projeto:**
1. Blog com admin panel (CRUD de posts, categorias, comentários, usuários)
2. E-commerce básico (produtos, carrinho, pedidos, painel de vendas)
3. Rede social (perfil, posts, follows, likes, notificações)
4. Sistema de agendamento (serviços, clientes, calendário)

**Desafio extra:**
1. Implementar API REST + Jinja2 no mesmo projeto (híbrido)
2. Adicionar WebSockets com Flask-SocketIO para chat ou notificações em tempo real
3. Integrar com API externa (pagamento, mapas, etc.)

**Tarefas de casa (escolha uma ou mais):**
1. Fazer deploy e testar em produção
2. Adicionar testes de integração com pytest
3. Criar case study do projeto: processo, desafios, aprendizados
4. Publicar no GitHub com README profissional e screenshots
5. Escrever artigo sobre o projeto em blog pessoal ou LinkedIn

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentações)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Web app Flask funcional com autenticação
2. Templates Jinja2 responsivos
3. SQLAlchemy + migrações
4. Blueprint structure (Application Factory)
5. Deploy no Render com Docker e PostgreSQL
6. README profissional com screenshots

---

## Materiais do Professor

- [Pasta FAST API — Google Drive](https://drive.google.com/drive/folders/1BQruvUzAc08bT9uqT0fZEwTjSegIfJau)
- [Mod 3- Aula 1 DFS Python POO.pptx](https://drive.google.com/file/d/1M7t8pVgV9Xbh1ouIhsqma_T0RAyUJshI/view)
- [Mod 3- Aula 2 DFS Python POO.pptx](https://drive.google.com/file/d/1ViTYd3ioIp8x2BxTQpp6XnuyyNhYIQ2Y/view)
- [Mod 3- Aula 03 DFS Python Tratamento Erro.pptx](https://drive.google.com/file/d/1PfULeV4HWuGSPD8YRVN_h5MVFVZLHAGM/view)
- [Mod 3- Aula 4 DFS Python.pptx](https://drive.google.com/file/d/1G2kqn8ZgQWcnoYxEy3jmjEXT8j3wSFcF/view)
- [Mod 3- Aula 5 DFS Python.pptx](https://drive.google.com/file/d/1xBIENckW7AyUpa3NSgeIgUjJLP1XnpAb/view)
- [Mod3 Python - Aula 6.pptx](https://drive.google.com/file/d/1kTVpFmbmlMyIzVVxpNv21yDN1b0rezco/view)

---

## Próximo módulo

→ [Power Bi](../modulos/power-bi.md)

---

#modulo #flask #python #backend #templates #docker #deploy
