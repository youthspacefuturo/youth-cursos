# REST API & Git — Módulo 3

> Criação de APIs REST com Python e controle de versão.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Fullstack Python#fase 1 Fundamentos Linear](../cursos/fullstack-python#fase-1--fundamentos-linear.md)

---
## Aulas
### Aula 1 — Git Básico

**Conteúdo:**
- Por que controle de versão existe
- Git vs GitHub
- Instalação e configuração inicial (`git config --global`)
- Fluxo básico: `init`, `status`, `add`, `commit`
- Mensagens de commit: conventional commits
- `git log`, `git diff`
- `.gitignore` para projetos Python
- Desfazendo coisas: `git restore`, `git reset`

**Exercícios práticos (escolha um):**
1. Versionar o projeto do módulo anterior com pelo menos 5 commits significativos
2. Criar diário de aprendizado em markdown, commitar cada entrada separadamente
3. Criar repositório com estrutura de projeto Python organizada e documentada

**Recursos:**
- [Git Official Docs](https://git-scm.com/doc)
- [Conventional Commits](https://www.conventionalcommits.org/pt-br/)
- [Oh My Git!](https://ohmygit.org/)

**Tarefas de casa (escolha uma ou mais):**
1. Versionar todos os projetos anteriores com commits organizados
2. Criar `.gitignore` Python completo e explicar cada regra
3. Praticar `git reset` (soft, mixed, hard) e documentar as diferenças
4. Explorar `git log --oneline --graph` em um repositório com vários commits
5. Criar repositório com 10+ commits e usar `git bisect` para encontrar um "bug" simulado

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — GitHub e Colaboração

**Conteúdo:**
- Criando conta e repositório no GitHub
- `git remote`, `git push`, `git pull`, `git clone`
- Fork e contribuição open source
- Branches: `git branch`, `git checkout`, `git switch`
- Merge e resolução de conflitos
- Pull Requests: criando, revisando, aprovando
- GitHub Flow
- README profissional com Markdown

**Exercícios práticos (escolha um):**
1. Em duplas: fork, branch separada, PR e revisão cruzada
2. Simular conflito de merge e resolver manualmente
3. Criar repositório com README completo (badges, screenshots, instruções)

**Recursos:**
- [GitHub Docs](https://docs.github.com/pt)
- [Learn Git Branching](https://learngitbranching.js.org/?locale=pt_BR)

**Tarefas de casa (escolha uma ou mais):**
1. Criar perfil profissional no GitHub com README customizado
2. Organizar todos os projetos do curso em repos públicos bem documentados
3. Contribuir com um repo open source (mesmo que correção de typo)
4. Criar repositório colaborativo com colega: branch por feature, PR e code review
5. Explorar Actions do GitHub: criar workflow simples de CI

**Tempo:** 4h (1h teoria + 2h prática em dupla + 1h apresentação)

---

### Aula 3 — HTTP e REST com Flask

**Conteúdo:**
- O que é HTTP: verbos, status codes, headers
- O que é REST: princípios e constraints
- Instalando Flask: `pip install flask`
- Primeiro servidor Flask
- Rotas e métodos: `@app.route()`, `methods=['GET', 'POST']`
- `request`: acessando dados da requisição
- `jsonify`: retornando JSON
- Status codes corretos: 200, 201, 400, 404, 500
- Testando com Postman ou Thunder Client
- CORS com `flask-cors`

**Exercícios práticos (escolha um):**
1. API de frases motivacionais: GET /frases (lista), GET `/frases/<id>`, GET `/frases/aleatoria`
2. API de calculadora: rotas para soma, subtração, multiplicação, divisão via query params
3. API de consulta de CEP (simular com dados hardcoded): GET `/cep/<cep>` retorna cidade e estado

**Recursos:**
- [Flask Official Docs](https://flask.palletsprojects.com/)
- [MDN - HTTP Status](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)
- [Insomnia](https://insomnia.rest/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar API de filmes: listar, buscar por ID, filtrar por gênero
2. API de piadas: retornar piada aleatória, listar por categoria
3. Servidor com middleware de log: registrar em arquivo toda requisição
4. API de quiz: listar perguntas, submeter resposta, retornar pontuação
5. API de receitas: buscar por nome parcial, filtrar por dificuldade

**Tempo:** 4h (1h teoria + 2h prática + 1h teste com Insomnia)

---

### Aula 4 — CRUD Completo com Flask

**Conteúdo:**
- Estrutura de projeto Flask organizada
- Blueprints: separando rotas por recurso
- CRUD com persistência em arquivo JSON (simulando banco)
- Validação de dados de entrada
- Tratamento de erros centralizado
- IDs automáticos e timestamps
- Serialização de objetos Python para JSON
- Boas práticas de nomenclatura de endpoints

**Exercícios práticos (escolha um):**
1. API de tarefas completa: CRUD com persistência JSON (id, titulo, descricao, status, criado_em)
2. API de produtos: CRUD completo com validação e status codes corretos
3. API de usuários: criar, listar, buscar por ID, atualizar, deletar

**Recursos:**
- [Flask Blueprints](https://flask.palletsprojects.com/blueprints/)
- [REST API Design](https://restfulapi.net/)

**Tarefas de casa (escolha uma ou mais):**
1. API de biblioteca: CRUD de livros com rotas de emprestar/devolver
2. API de estoque: produtos com quantidade, rotas de entrada/saída
3. Implementar paginação manual: `?page=1&limit=10` em rota de listagem
4. API de agenda: CRUD de contatos com busca por nome parcial
5. API de receitas: CRUD completo com ingredientes (array) e instruções

**Tempo:** 4h (1h teoria + 2h prática + 1h code review)

---

### Aula 5 — Flask + SQLAlchemy

**Conteúdo:**
- Flask-SQLAlchemy: integrando ORM ao Flask
- Modelos como classes Python
- Migrações com Flask-Migrate / Alembic
- Relacionamentos em modelos
- Queries dentro de rotas Flask
- Serialização de modelos para JSON
- Separando models, routes e services
- Variáveis de ambiente com python-dotenv
- Configurações por ambiente (dev, prod)

**Exercícios práticos (escolha um):**
1. Refatorar API de tarefas (aula 4) usando Flask-SQLAlchemy com SQLite
2. API de blog: modelos User, Post, Comment com Flask-SQLAlchemy
3. API de escola: modelos Aluno, Disciplina, Nota com relacionamentos

**Recursos:**
- [Flask-SQLAlchemy Docs](https://flask-sqlalchemy.palletsprojects.com/)
- [Flask-Migrate Docs](https://flask-migrate.readthedocs.io/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar migração para adicionar nova coluna em tabela existente
2. Adicionar seed script que popula banco com dados fictícios usando Faker
3. Implementar soft delete: campo `deleted_at` em vez de deletar de verdade
4. Criar query complexa: busca com múltiplos filtros e ordenação
5. Documentar todos os endpoints da API com exemplos de request/response no README

**Tempo:** 4h (1h teoria + 2h prática + 1h refatoração)

---

### Aula 6 — Autenticação JWT com Flask

**Conteúdo:**
- Autenticação vs Autorização
- JWT: header, payload, signature
- `flask-jwt-extended`: instalação e configuração
- Rota de registro com senha hasheada (werkzeug)
- Rota de login retornando JWT
- `@jwt_required()`: protegendo rotas
- `get_jwt_identity()`: acessando dados do token
- Roles e permissões no payload
- Refresh tokens
- Variáveis de ambiente para secrets

**Exercícios práticos (escolha um):**
1. Sistema de autenticação completo: /register, /login, /me (rota protegida)
2. API com níveis de acesso: admin vs usuário comum
3. Adicionar autenticação à API de tarefas anterior (tarefas por usuário logado)

**Recursos:**
- [Flask-JWT-Extended Docs](https://flask-jwt-extended.readthedocs.io/)
- [JWT.io](https://jwt.io/)

**Tarefas de casa (escolha uma ou mais):**
1. Implementar expiração de token (1h) com retorno de erro adequado
2. Criar sistema de refresh token
3. Adicionar proteção de rotas por role no projeto existente
4. Pesquisar sobre OAuth2 e documentar o fluxo com Google/GitHub
5. Implementar "change password" e "forgot password" simulado

**Tempo:** 4h (1h teoria + 2h prática + 1h revisão de segurança)

---

### Aula 7 — Boas Práticas e Testes

**Conteúdo:**
- Estrutura profissional de projeto Flask
- Separação de responsabilidades: routes, controllers, services, models, schemas
- Validação com Marshmallow ou Pydantic
- Testes com `pytest`
- Testes de integração com `pytest-flask`
- Test fixtures e factories
- Coverage: `pytest-cov`
- Documentação automática com Flask-Swagger-UI
- Logging com Python `logging` module
- Deploy para produção: Gunicorn

**Exercícios práticos (escolha um):**
1. Reestruturar API existente com arquitetura routes/services/models
2. Criar testes para 3 endpoints: sucesso, 404 e validação de erro
3. Adicionar documentação Swagger à API criada

**Recursos:**
- [pytest Docs](https://docs.pytest.org/)
- [Marshmallow Docs](https://marshmallow.readthedocs.io/)
- [Flask Testing](https://flask.palletsprojects.com/testing/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar suite de testes para todos os endpoints da API
2. Adicionar CI com GitHub Actions: rodar testes a cada push
3. Documentar API completa com Swagger/OpenAPI
4. Configurar Gunicorn + nginx localmente para simular produção
5. Escrever README profissional com badges de CI, cobertura de testes e versão

**Tempo:** 4h (1h teoria + 2h prática + 1h apresentação)

---

### Aula 8 — Projeto: API REST Completa com Deploy

**Conteúdo:**
- Revisão dos conceitos do módulo
- Planejamento da API: recursos, rotas, regras de negócio
- Implementação guiada
- Deploy no Render ou Railway
- Configurando PostgreSQL em produção (introdução)
- Testando tudo em produção

**Exercício prático:**
1. API REST completa: autenticação JWT + CRUD de 2 recursos relacionados + SQLAlchemy + testes + deploy

**Sugestões de projeto:**
1. API de blog com posts, comentários e usuários
2. Sistema de eventos com inscrições
3. API de produtos com categorias e pedidos
4. Gerenciador de projetos com tarefas e membros

**Desafio extra:**
1. Conectar frontend React (módulo anterior) com esta API
2. Implementar upload de imagens com Flask
3. Adicionar WebSockets com Flask-SocketIO

**Tarefas de casa (escolha uma ou mais):**
1. Fazer deploy e testar todos os endpoints em produção
2. Adicionar rate limiting com Flask-Limiter
3. Implementar cache com Flask-Caching
4. Criar Postman/Insomnia collection completa da API
5. Conectar a API ao frontend do módulo anterior

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação e deploy)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Repositório no GitHub organizado
2. API REST com autenticação JWT
3. SQLAlchemy como ORM
4. Testes automatizados (mínimo 3)
5. Deploy funcionando (URL pública)
6. README com documentação dos endpoints

---

## Materiais do Professor

- [Pasta GIT + NODE.JS — Google Drive](https://drive.google.com/drive/folders/1QXe9Pq4K1Fc-L8dQXmHXtdWCllCIOVjk)
- [Pasta GIT — Google Drive](https://drive.google.com/drive/folders/1y8GQBN54XOIxwg_mFIsPURMsSlNwyNdF)
- [git & github - aula1.pptx](https://drive.google.com/file/d/1JzcvmJwl0ylSGLyLVdgIqMkKT2MGc7uo/view)
- [Git & github - aula2.pptx](https://drive.google.com/file/d/1wxKLk19yltb1LLsP1KcmIy0EWDR2CSwe/view)
- [Git & github - aula3.pptx](https://drive.google.com/file/d/12mBBNm5Qi0tJUE9fuc0bUR8l3KQj4SjJ/view)
- [Git & github - aula4.pptx](https://drive.google.com/file/d/1kQtnZbjbw5uXOPvqrmeBD16gWnbsYrA/view)
- [CRUD COMPLETO.docx](https://drive.google.com/file/d/1_WceKxmufMz0_kDe2syKv3vWUEqTGT4e/view)

---

## Próximo módulo

→ [Flask](../modulos/flask.md)

---

#modulo #python #flask #api #rest #git #github #jwt
