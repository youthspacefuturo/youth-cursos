# Projeto Final — Módulo 7 (Python Full Stack)

> Desenvolvimento completo do projeto full stack com Python — aluno escolhe o tema.

## Informações do Módulo

- **Aulas:** 6 (de 4h cada)
- **Carga horária:** 24h
- **Posição na trilha:** [Fullstack Python#fase 3 Projeto Final](cursos/fullstack-python#fase-3--projeto-final.md)

---
## Aulas
### Aula 1 — Kickoff: Git, GitHub e Definição de Projeto

**Conteúdo (fixo — todos passam por aqui):**
- Revisão de Git e GitHub: fluxo completo
- Criar repositório e configurar .gitignore Python
- GitHub Projects: board de tasks (A Fazer, Em Progresso, Revisão, Feito)
- Levantamento de requisitos do projeto
- MVP: o mínimo viável para o projeto ser entregue
- Definindo banco de dados: modelagem básica
- Estrutura de pastas Python profissional
- Alinhamento de expectativas: o que cabe em 6 aulas

**Exercício prático:**
1. Criar repositório, README com descrição, GitHub Projects com 10+ tasks do MVP
2. Rascunhar diagrama ER do banco de dados no dbdiagram.io

**Recursos:**
- [GitHub Projects Guide](https://docs.github.com/pt/issues/planning-and-tracking-with-projects/)
- [dbdiagram.io](https://dbdiagram.io/)

**Tempo:** 4h (1h revisão + 1h GitHub Projects + 2h planejamento)

---

### Aula 2 — Setup: Flask + PostgreSQL + Arquitetura

**Conteúdo (fixo — todos passam por aqui):**
- Criar projeto Flask com Application Factory
- Configurar Flask-SQLAlchemy com PostgreSQL local
- Criar modelos conforme planejado
- Migrações com Flask-Migrate
- Configurar variáveis de ambiente (.env)
- Primeiro endpoint funcionando: GET /health
- CORS configurado para o frontend (se necessário)
- Deploy inicial no Render (mesmo que "Hello World")
- Versionar no GitHub com branch `main` e `develop`

**Exercício prático:**
1. Backend Flask rodando com PostgreSQL e pelo menos 1 modelo criado
2. Deploy inicial no Render com URL funcionando
3. README com instruções de como rodar localmente

**Tempo:** 4h (1h teoria + 3h hands-on)

---

### Aula 3 — Tira-Dúvidas: Backend e Banco de Dados

**Conteúdo (planejado — ajustar conforme necessidade):**
- CRUD completo dos recursos principais
- Relacionamentos entre modelos
- Validação de dados de entrada
- Tratamento de erros padronizado
- Autenticação JWT (se necessário)
- Queries avançadas com SQLAlchemy
- Migrations para alterações no banco
- Seeds com dados de exemplo

**Exercício prático:**
1. Implementar pelo menos 2 recursos completos com CRUD
2. Testar todas as rotas com Insomnia/Postman

**Tempo:** 4h (30min teoria específica + 3h projeto + 30min revisão)

---

### Aula 4 — Tira-Dúvidas: Frontend ou Integração

**Conteúdo (planejado — ajustar conforme necessidade):**

**Se projeto Flask + Jinja2 (frontend monolítico):**
- Templates Jinja2 para todas as páginas
- Flask-Login: autenticação via sessão
- Formulários WTForms com validação
- Upload de arquivos
- CSS responsivo

**Se projeto Flask API + React (separado):**
- Consumindo a API Flask com axios
- Context API para estado global
- React Router para navegação
- Estados de loading/error
- Deploy do frontend no Vercel

**Exercício prático:**
1. Implementar pelo menos 2 páginas/fluxos completos
2. Integração frontend ↔ backend funcionando

**Tempo:** 4h (30min teoria específica + 3h projeto + 30min revisão)

---

### Aula 5 — Tira-Dúvidas: Deploy, Testes e Polish

**Conteúdo (planejado — ajustar conforme necessidade):**
- Deploy completo no Render (backend + banco)
- Variáveis de ambiente em produção
- Testes básicos com pytest
- Validação final de todas as rotas
- Ajustes de UX/UI
- Lighthouse: acessibilidade e performance
- README completo com screenshots
- Preparação para apresentação

**Exercício prático:**
1. Deploy funcionando com URL pública
2. Todas as funcionalidades do MVP implementadas

**Tempo:** 4h (30min teoria específica + 3h projeto + 30min apresentação)

---

### Aula 6 — Apresentação Final

**Conteúdo (fixo — todos apresentam):**
- Cada aluno apresenta o projeto (5-7 minutos)
- Demo ao vivo da aplicação em produção
- Explicar: o que é, tecnologias, desafios e como superou
- Próximos passos: o que adicionaria com mais tempo
- Celebração! 🎉

**Formato de apresentação:**
1. Nome e tagline do projeto (30s)
2. Demo ao vivo (3-4min)
3. Stack escolhida e por quê (30s)
4. Maior desafio + solução (30s)
5. Perguntas (1-2min)

**Critérios de avaliação (sugestão):**
1. Funcional: o projeto faz o que prometeu?
2. Código: organizado e com boas práticas?
3. Banco de dados: modelagem correta?
4. Deploy: funcionando em produção?
5. Git: histórico organizado?

**Tempo:** 4h (apresentações de 5-7min por aluno)

---

## Estrutura Resumida

| Aula | Tipo | Conteúdo |
|------|------|----------|
| 1 | **Fixa** | Git/GitHub + Planejamento + GitHub Projects |
| 2 | **Fixa** | Setup Flask + PostgreSQL + Deploy inicial |
| 3 | **Variável** | Backend: CRUD, Banco, Auth |
| 4 | **Variável** | Frontend/Integração: Jinja2 ou React |
| 5 | **Variável** | Deploy + Testes + Polish |
| 6 | **Fixa** | Apresentação final 🎉 |

---

## Projetos Sugeridos

1. Blog com painel admin (CRUD de posts, categorias, autores)
2. E-commerce básico (produtos, carrinho, pedidos)
3. Sistema de agendamento (serviços, clientes, agenda)
4. Rede social simplificada (perfil, posts, follows)
5. Gerenciador de finanças pessoais (receitas, despesas, relatórios)
6. Plataforma de cursos (cursos, aulas, progresso)
7. Sistema de tarefas por projeto (estilo Trello)

## Requisitos Mínimos

8. Backend Flask com pelo menos 2 recursos e CRUD
9. Banco de dados PostgreSQL com relacionamentos
10. Autenticação (Flask-Login ou JWT)
11. Interface funcional (Jinja2 ou React separado)
12. Deploy no Render
13. GitHub com histórico organizado

---

#modulo #projeto-final #python #flask #postgresql #deploy
