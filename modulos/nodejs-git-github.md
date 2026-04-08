# Node.js & Git/GitHub — Módulo 5

> Backend básico, controle de versão e colaboração.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Fullstack 12 Meses#fase 2 Especializacao Circular](cursos/fullstack-12-meses#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — Controle de Versão e Git Básico

**Conteúdo:**
- Por que controle de versão existe (problema que resolve)
- Git vs GitHub (local vs nuvem)
- Instalação e configuração inicial (`git config --global`)
- Fluxo básico: `git init`, `git status`, `git add`, `git commit`
- Mensagens de commit: boas práticas e padrões (conventional commits)
- `git log` e `git diff`
- `.gitignore`: o que ignorar e por quê
- Desfazendo coisas: `git restore`, `git reset`

**Exercícios práticos (escolha um):**
1. Versionar o projeto do módulo HTML/CSS: init, adicionar arquivos, 3 commits significativos com mensagens descritivas
2. Criar um diário de aprendizado em markdown, versionar cada entrada como um commit separado
3. Simular o histórico de um projeto: criar 5 arquivos em momentos diferentes, commitar cada etapa com mensagem adequada

**Recursos:**
- [Git Official Docs](https://git-scm.com/doc)
- [Conventional Commits](https://www.conventionalcommits.org/pt-br/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Oh My Git!](https://ohmygit.org/) — jogo para aprender Git

**Tarefas de casa (escolha uma ou mais):**
1. Versionar todos os projetos feitos nos módulos anteriores com commits organizados
2. Criar um `.gitignore` para um projeto Node.js e explicar cada linha adicionada
3. Pesquisar sobre "git blame" e "git bisect", documentar para que servem e quando usar
4. Praticar `git reset` (soft, mixed, hard) em um repositório de teste e documentar as diferenças
5. Criar um repositório com pelo menos 10 commits e usar `git log --oneline --graph` para visualizar o histórico

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — GitHub e Trabalho em Equipe

**Conteúdo:**
- Criando conta e repositório no GitHub
- `git remote`, `git push`, `git pull`, `git clone`
- Fork e o conceito de contribuição open source
- Branches: `git branch`, `git checkout`, `git switch`
- Merge: fast-forward vs merge commit
- Resolvendo conflitos de merge
- Pull Requests: criando, revisando e aprovando
- GitHub Flow (branch → PR → review → merge)

**Exercícios práticos (escolha um):**
1. Em duplas: um cria o repositório, o outro faz fork, ambos adicionam arquivos em branches separadas e abrem PRs
2. Simular um conflito de merge: dois branches editando a mesma linha, resolver o conflito manualmente
3. Criar um repositório com README completo, fazer contribuição em branch, abrir PR para si mesmo e fazer merge

**Recursos:**
- [GitHub Docs - Hello World](https://docs.github.com/pt/get-started/quickstart/hello-world)
- [GitHub Flow](https://docs.github.com/pt/get-started/quickstart/github-flow)
- [Learn Git Branching](https://learngitbranching.js.org/?locale=pt_BR) — visual interativo

**Tarefas de casa (escolha uma ou mais):**
1. Contribuir com um repositório open source no GitHub (mesmo que seja só corrigir um typo no README)
2. Criar um perfil profissional no GitHub com README personalizado (usando badges, GIFs, stats)
3. Organizar todos os projetos do curso em repositórios públicos bem documentados no GitHub
4. Explorar o GitHub de alguém que admira e listar 3 boas práticas observadas nos repositórios deles
5. Criar um repositório colaborativo com um colega: cada um faz uma branch com uma feature, abre PR e faz code review do outro

**Tempo:** 4h (1h teoria + 2h prática em dupla + 1h apresentação)

---

### Aula 3 — Introdução ao Node.js

**Conteúdo:**
- O que é Node.js e como ele funciona (event loop, non-blocking I/O)
- Diferença entre JavaScript no navegador e no Node
- Instalando Node.js e usando o terminal
- `node arquivo.js` — executando scripts
- Módulos nativos: `fs` (ler/escrever arquivos), `path`, `os`
- `require` e `module.exports` (CommonJS)
- `import`/`export` (ES Modules)
- NPM: o que é, `npm init`, `package.json`
- Instalando pacotes: `npm install`, `dependencies` vs `devDependencies`

**Exercícios práticos (escolha um):**
1. Script de organização de arquivos: ler uma pasta com `fs`, listar todos os arquivos e separar por extensão
2. Gerador de relatório: ler um array de dados hardcoded, processar e escrever um arquivo `.txt` com relatório formatado
3. CLI simples: script que recebe argumentos (`process.argv`) e executa ações diferentes (ex: `node app.js --help`, `node app.js --list`)

**Recursos:**
- [Node.js Official Docs](https://nodejs.org/pt-br/docs/)
- [MDN - CommonJS Modules](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules)
- [NPM Official Docs](https://docs.npmjs.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar um script que lê um arquivo `.csv` de notas de alunos e gera um relatório com média, aprovados e reprovados
2. Criar um script de backup: copiar todos os arquivos de uma pasta para outra com `fs`
3. Construir um gerador de senhas via CLI: `node senha.js --tamanho 12 --especiais`
4. Criar um script que busca todos os arquivos `.js` em uma pasta (recursivamente) e conta quantas linhas cada um tem
5. Explorar o `package.json`: criar scripts npm customizados (`npm run dev`, `npm run build`, `npm run test`)

**Tempo:** 4h (1h teoria + 2h prática + 1h exercícios)

---

### Aula 4 — Express.js: Rotas e Middlewares

**Conteúdo:**
- O que é um servidor HTTP e como funciona
- Instalando e configurando o Express.js
- Criando o primeiro servidor: `app.listen()`
- Rotas: `app.get()`, `app.post()`, `app.put()`, `app.delete()`
- `req` e `res`: request e response
- `req.params`, `req.query`, `req.body`
- Middlewares: o que são e para que servem
- `express.json()` e `express.urlencoded()`
- Middlewares de erro e `next()`
- `app.use()` e ordem dos middlewares

**Exercícios práticos (escolha um):**
1. Servidor de frases motivacionais: GET `/frases` retorna array, GET `/frases/:id` retorna uma específica, GET `/frases/aleatoria` retorna uma aleatória
2. API de calculadora: rotas para soma, subtração, multiplicação e divisão recebendo valores via query params
3. Servidor de informações: GET `/`, GET `/sobre`, GET `/contato` respondendo com JSONs de informações do "site"

**Recursos:**
- [Express.js Official Docs](https://expressjs.com/pt-br/)
- [MDN - HTTP Overview](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Overview)
- [Insomnia](https://insomnia.rest/) ou [Thunder Client](https://www.thunderclient.com/) — para testar APIs

**Tarefas de casa (escolha uma ou mais):**
1. Criar uma API de filmes com: listar todos, buscar por ID, filtrar por gênero (query param), retornar filmes aleatórios
2. Construir uma API de piadas: retornar piada aleatória, listar por categoria, buscar por palavra-chave
3. Criar um servidor com middleware de log: registrar em arquivo toda requisição (método, rota, hora, status)
4. Implementar uma API com rate limiting manual: contador por IP, bloquear após 10 requisições por minuto
5. Desenvolver uma API de quiz: listar perguntas, submeter resposta, retornar resultado com pontuação

**Tempo:** 4h (1h teoria + 2h prática + 1h teste com Insomnia/Thunder Client)

---

### Aula 5 — REST API: CRUD Completo

**Conteúdo:**
- O que é REST (Representational State Transfer)
- Verbos HTTP e seus significados semânticos
- Status codes: 200, 201, 400, 401, 403, 404, 500
- Recursos e URIs: boas práticas de nomenclatura
- CRUD: Create, Read, Update, Delete
- Persistência em memória (array) vs arquivo JSON
- Salvando e lendo dados de arquivo com `fs`
- Validação básica de dados de entrada
- Organização do projeto: separando rotas em arquivos (Router)

**Exercícios práticos (escolha um):**
1. API de tarefas completa: CRUD de tarefas com persistência em arquivo JSON (id, titulo, descricao, completo, criadoEm)
2. API de produtos: CRUD completo com dados persistidos em JSON, status codes corretos e validação básica
3. API de usuários: criar, listar, buscar por ID, atualizar nome/email, deletar — com persistência em arquivo

**Recursos:**
- [REST API Design Best Practices](https://restfulapi.net/)
- [MDN - HTTP Status Codes](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)
- [JSON Placeholder](https://jsonplaceholder.typicode.com/) — API fake para referência

**Tarefas de casa (escolha uma ou mais):**
1. Criar uma API de biblioteca: CRUD de livros (titulo, autor, ano, disponivel), com rota para emprestar e devolver
2. Construir uma API de receitas: CRUD completo com campos: nome, ingredientes (array), modo de preparo, tempo, dificuldade
3. Desenvolver uma API de estoque: produtos com quantidade, rota para entrada e saída de estoque, alerta quando quantidade < 5
4. Criar uma API de agenda de contatos: CRUD + busca por nome (parcial) + filtro por cidade
5. Implementar paginação manual em uma rota de listagem: `?page=1&limit=10`

**Tempo:** 4h (1h teoria + 2h prática + 1h code review em dupla)

---

### Aula 6 — Autenticação com JWT

**Conteúdo:**
- O que é autenticação e autorização (diferença)
- Sessões vs Tokens
- JWT (JSON Web Token): header, payload, signature
- Fluxo de autenticação: login → token → requisições autenticadas
- `jsonwebtoken` — instalação e uso
- Gerando token no login
- Middleware de verificação de token
- Protegendo rotas
- Armazenando senhas com hash: `bcryptjs`
- Variáveis de ambiente com `dotenv`

**Exercícios práticos (escolha um):**
1. Sistema de login e rotas protegidas: POST `/register`, POST `/login` (retorna JWT), GET `/perfil` (requer token)
2. API com níveis de acesso: usuário comum (acessa GET) e admin (acessa POST/PUT/DELETE), verificados pelo payload do JWT
3. Sistema de autenticação completo: cadastro com senha hasheada, login com JWT, rota protegida, rota de refresh token

**Recursos:**
- [JWT.io](https://jwt.io/) — decodificar e entender tokens JWT
- [NPM - jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
- [NPM - bcryptjs](https://www.npmjs.com/package/bcryptjs)
- [MDN - HTTP Authentication](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Authentication)

**Tarefas de casa (escolha uma ou mais):**
1. Adicionar autenticação JWT na API criada na aula anterior (tarefas ou produtos)
2. Implementar expiração de token (ex: 1h) e retornar erro adequado quando expirado
3. Criar sistema de refresh token: token de acesso (15min) + token de renovação (7 dias)
4. Adicionar proteção de rotas por role: rota `/admin` só acessível para usuários com `role: 'admin'` no payload do JWT
5. Pesquisar sobre OAuth2 e redigir um texto explicando o fluxo de autenticação com Google/GitHub

**Tempo:** 4h (1h teoria + 2h prática + 1h revisão de segurança)

---

### Aula 7 — Organização e Boas Práticas de API

**Conteúdo:**
- Estrutura de projeto escalável (Controllers, Routes, Services, Models)
- Separação de responsabilidades (MVC simplificado)
- Tratamento de erros centralizado (error handler middleware)
- Validação de dados com `Joi` ou `zod`
- Logging com `morgan`
- CORS: o que é e como configurar
- Variáveis de ambiente: `.env`, `.env.example`
- Versionamento de API: `/api/v1/`
- Documentação básica com comentários e README

**Exercícios práticos (escolha um):**
1. Refatorar a API de tarefas usando a estrutura Controllers/Routes/Services
2. Adicionar validação com Zod em todas as rotas de uma API existente (campos obrigatórios, tipos, tamanhos)
3. Criar um middleware de tratamento de erros que retorna sempre o mesmo formato: `{ error: true, message: '', code: '' }`

**Recursos:**
- [Zod Docs](https://zod.dev/)
- [NPM - morgan](https://www.npmjs.com/package/morgan)
- [Express Error Handling](https://expressjs.com/pt-br/guide/error-handling.html)
- [The Twelve-Factor App](https://12factor.net/pt_br/) — boas práticas de aplicações

**Tarefas de casa (escolha uma ou mais):**
1. Reestruturar completamente uma API anterior usando a arquitetura Controllers/Routes/Services
2. Criar um `.env.example` documentado para um projeto, explicando cada variável
3. Adicionar logging em arquivo: erros vão para `logs/error.log`, requisições para `logs/access.log`
4. Implementar versionamento na API: `/api/v1/` e simular uma `/api/v2/` com uma resposta diferente
5. Escrever um README completo para uma API: endpoints, autenticação, exemplos de request/response, como rodar localmente

**Tempo:** 4h (1h teoria + 2h prática + 1h apresentação)

---

### Aula 8 — Projeto: API REST Completa

**Conteúdo:**
- Revisão dos conceitos do módulo
- Planejamento de uma API: definindo recursos, rotas e regras de negócio
- Estrutura final do projeto
- Persistência final com arquivo JSON (simulando banco de dados)
- Testes manuais com Insomnia/Thunder Client
- Deploy simples no Render ou Railway
- Documentação da API no README

**Exercício prático:**
1. Construir uma API REST completa do zero: autenticação JWT + CRUD de pelo menos 2 recursos relacionados + validação + tratamento de erros + deploy

**Desafio extra (para rápidos):**
1. Adicionar testes automatizados básicos com `jest` e `supertest`
2. Implementar upload de arquivos com `multer`
3. Criar um webhook simples que notifica uma URL ao criar um novo recurso

**Recursos:**
- [Render.com](https://render.com/) — deploy gratuito de APIs Node.js
- [Railway.app](https://railway.app/) — alternativa de deploy
- [Jest Docs](https://jestjs.io/pt-BR/)

**Tarefas de casa (escolha uma ou mais):**
1. Fazer o deploy da API na Render ou Railway e testar todos os endpoints no ar
2. Criar uma coleção no Insomnia/Thunder Client com todas as rotas documentadas e exportar como arquivo
3. Adicionar testes com Jest: testar pelo menos 3 rotas (status code + corpo da resposta)
4. Escrever um artigo no Notion/LinkedIn sobre o que aprendeu no módulo (solidifica o conhecimento)
5. Conectar o frontend (To-Do List do módulo JavaScript 2) com a API criada neste módulo

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação e deploy)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Repositório no GitHub com histórico de commits organizado
2. API REST com autenticação JWT
3. Pelo menos 2 recursos com CRUD completo
4. Validação de dados e tratamento de erros
5. Deploy funcionando (URL pública)
6. README com documentação dos endpoints

---

## Próximo módulo

→ [Reactjs](modulos/reactjs.md)

---

#modulo #nodejs #express #git #github #api #rest #jwt #fullstack
