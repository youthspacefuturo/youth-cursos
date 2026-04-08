# Projeto Final — Módulo 8

> Desenvolvimento completo do projeto full stack — cada aluno escolhe seu tema.

## Informações do Módulo

- **Aulas:** 6 (de 4h cada)
- **Carga horária:** 24h
- **Posição na trilha:** [Fullstack 12 Meses#fase 3 Projeto Final](cursos/fullstack-12-meses#fase-3--projeto-final.md)

---
## Aulas
### Aula 1 — Kickoff: Git, GitHub e Definição de Projeto

**Conteúdo (fixo — todos passam por aqui):**
- Revisão de Git e GitHub: fluxo completo (branch → commit → PR → merge)
- Criar/organizar repositório do projeto
- GitHub Projects: criando board com colunas (A Fazer, Em Progresso, Revisão, Feito)
- Levantamento de requisitos: o que o projeto precisa ter
- Definindo MVP (Minimum Viable Product): o mínimo que o projeto precisa fazer
- Separando funcionalidades em tasks no GitHub Projects
- Alinhamento de expectativas: o que é possível fazer em 6 aulas

**Exercício prático:**
1. Criar repositório no GitHub com README do projeto (nome, descrição, funcionalidades planejadas)
2. Criar GitHub Project com board de tarefas
3. Listar pelo menos 10 tarefas no board (features do MVP)

**Recursos:**
- [GitHub Projects - Official Guide](https://docs.github.com/pt/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)
- [MoSCoW Method](https://www.agilebusiness.org/page/ProjectManagement14) — priorização de requisitos

**Tempo:** 4h (1h revisão Git/GitHub + 1h GitHub Projects + 2h planejamento)

---

### Aula 2 — Setup: Node.js + React + Arquitetura

**Conteúdo (fixo — todos passam por aqui):**
- Criar projeto backend (Node/Express) com estrutura organizada
- Criar projeto frontend (React + Vite)
- Configurar ESLint e Prettier em ambos
- Conectar frontend e backend (CORS configurado)
- Criar estrutura de pastas: controllers, routes, services, models
- Primeira rota funcionando: GET /health
- Deploy inicial (mesmo que seja "Hello World") — garantir que funciona
- Configurar variáveis de ambiente (.env) em ambos
- Versionar no GitHub com branches corretas

**Exercício prático:**
1. Ter dois repositórios no GitHub: `meu-projeto-backend` e `meu-projeto-frontend`
2. Backend rodando localmente com pelo menos uma rota e deploy no Render
3. Frontend com Vite rodando e conseguindo fazer request para o backend
4. README de ambos com instruções de como rodar localmente

**Recursos:**
- [Vite - Create Project](https://vitejs.dev/guide/)
- [Express Generator](https://expressjs.com/en/starter/generator.html)
- [Render - Deploy Node.js](https://render.com/docs/deploy-node-express-app)

**Tempo:** 4h (1h teoria + 3h hands-on)

---

### Aula 3 — Tira-Dúvidas: Autenticação e Persistência

**Conteúdo (planejado — ajustar conforme necessidade da turma):**
- JWT: teoria + prática ( refresher)
- Estrutura de usuário no banco de dados
- Rotas protegidas: middleware de autenticação
- Persistência: JSON (simples) ou SQLite (intermediário)
- Quando usar array em memória vs arquivo vs banco
- Validação de dados de entrada
- Tratamento de erros consistente

**Exercício prático:**
1. Implementar autenticação no próprio projeto (se aplicável)
2. Ou: estruturar dados e rotas de forma que autenticação possa ser adicionada depois

**Recursos:**
- [JWT.io](https://jwt.io/)
- [bcryptjs](https://www.npmjs.com/package/bcryptjs)

**Tempo:** 4h (30min teoria específica + 3h projeto individual com suporte)

---

### Aula 4 — Tira-Dúvidas: Frontend e Integração

**Conteúdo (planejado — ajustar conforme necessidade da turma):**
- Organizando componentes React (pages, components, hooks, context)
- Context API: quando usar e como estruturar
- React Router: rotas, parâmetros, navegação
- Consumindo a própria API (fetch ou axios)
- Estados: loading, error, data — padronizando
- CSS: organização (CSS Modules, BEM, variáveis)
- Responsividade: mobile-first

**Exercício prático:**
1. Implementar 2-3 páginas do frontend integradas ao backend
2. Ou: revisar e melhorar estrutura de arquivos do frontend existente

**Recursos:**
- [React.dev](https://react.dev/)
- [React Router Docs](https://reactrouter.com/)

**Tempo:** 4h (30min teoria específica + 3h projeto individual com suporte)

---

### Aula 5 — Tira-Dúvidas: Deploy, SEO e Polish

**Conteúdo (planejado — ajustar conforme necessidade da turma):**
- Deploy do backend: Render, Railway ou Vercel
- Deploy do frontend: Vercel ou Netlify
- Variáveis de ambiente no production
- HTTPS e domínio customizado (opcional)
- SEO básico: meta tags, title dinâmico, sitemap
- Performance: lazy loading de imagens, code splitting
- Boas práticas de UI/UX: revendo o que foi feito em UX/UI
- Acessibilidade: проверка básica

**Exercício prático:**
1. Fazer deploy de ambos (frontend + backend) em produção
2. Testar tudo no celular ou DevTools mobile
3. Rodar Lighthouse e verificar score

**Recursos:**
- [Vercel - Deploy](https://vercel.com/docs)
- [Lighthouse](https://developer.chrome.com/docs/lighthouse/)

**Tempo:** 4h (30min teoria específica + 3h projeto individual com suporte)

---

### Aula 6 — Apresentação Final e Encerramento

**Conteúdo (fixo — todos apresentam):**
- Cada aluno apresenta seu projeto (5-7 minutos cada)
- Demonstração ao vivo (ou demo gravado)
- Explicar: o que é, tecnologias usadas, principais desafios e como superou
- Code review final: o que poderia melhorar
- Lições aprendidas: o que levar para projetos futuros
- Próximos passos: como continuar evoluindo o projeto
- Encerramento do curso: celebração! 🎉

**Formato de apresentação:**
1. Nome do projeto + tagline (30s)
2. Demo ao vivo (3-4min)
3. Tecnologias escolhidas e por quê (30s)
4. Maior desafio + como resolveu (30s)
5. O que faria diferente (30s)
6. Perguntas da turma (1-2min)

**Critérios de avaliação (sugestão):**
1. Funcional: o projeto faz o que se propôs?
2. Código: organizado, legível, com boas práticas?
3. Git: histórico de commits, uso de branches?
4. Deploy: funcionando em produção?
5. Apresentação: clareza e organização?

**Tempo:** 4h (30min por aluno × ~8 alunos = ~4h)

---

## Estrutura Resumida

| Aula | Tipo | Conteúdo |
|------|------|----------|
| 1 | **Fixa** | Git/GitHub review + Definição de projeto + GitHub Projects |
| 2 | **Fixa** | Setup Node + React + Arquitetura + Deploy inicial |
| 3 | **Variável** | Autenticação e persistência (ajustar conforme necessidade) |
| 4 | **Variável** | Frontend e integração com API (ajustar conforme necessidade) |
| 5 | **Variável** | Deploy, SEO, performance, polish (ajustar conforme necessidade) |
| 6 | **Fixa** | Apresentação final + Encerramento |

---

## Projetos Sugeridos

1. Clone simplificado do Twitter (feed, postar, perfil)
2. App de tarefas com colaboração (convidar amigos)
3. Marketplace simples (cadastro de produtos, carrinho, checkout simulado)
4. Blog com painel admin (criar, editar, deletar posts)
5. Gerenciador de finanças pessoais
6. Clone do GitHub user finder (mas com mais features)
7. App de quiz colaborativo (criar quiz, compartilhar link, ver resultados)
8. Plataforma de anotações com tags e busca
9. Gerador de flashcards para estudos
10. Clone do Linktree personalizado

---

## Requisitos Mínimos do Projeto

11. Frontend responsivo (React)
12. Backend com API REST (Node/Express)
13. Persistência de dados (JSON, SQLite ou PostgreSQL)
14. Interface funcional
15. GitHub com commits organizados e branches
16. Deploy funcionando (URL pública)

---

#modulo #projeto-final #fullstack #integracao
