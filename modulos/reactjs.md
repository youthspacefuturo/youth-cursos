# React.js — Módulo 6

> Biblioteca para construção de interfaces reativas.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Fullstack 12 Meses#fase 2 Especializacao Circular](cursos/fullstack-12-meses#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — O que é React e Primeiros Componentes

**Conteúdo:**
- O que é React e por que foi criado
- DOM Virtual vs DOM Real
- Criando projeto com Vite: `npm create vite@latest`
- Estrutura de arquivos do Vite + React
- JSX: HTML dentro do JavaScript
- Componentes: o que são e por que usar
- Criando seu primeiro componente funcional
- Props: passando dados para componentes
- Componentes dentro de componentes
- Renderização de listas com `.map()`

**Exercícios práticos (escolha um):**
1. Card de perfil: componente que recebe nome, cargo e foto, renderiza um card estilizado
2. Lista de redes sociais: componente que recebe um array de redes (nome, url, ícone) e renderiza uma lista de links
3. Componente de produto: receber dados de produto (nome, preço, imagem) e renderizar um card de e-commerce

**Recursos:**
- [React Official Docs](https://react.dev/)
- [Vite - Getting Started](https://vitejs.dev/guide/)
- [MDN - JSX](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Property_accessors)
- [React Playground](https://playcode.io/react) — testar React online

**Tarefas de casa (escolha uma ou mais):**
1. Criar uma galeria de personagens: array de 5 personagens com nome, descrição e imagem, renderizados como cards usando `.map()`
2. Componente Header reutilizável: receber título e Logo (props), renderizar header com navegação
3. Construir um componente de Pricing Table: receber plano, preço e features, renderizar card de preço
4. Criar uma lista de tarefas simples: array de tarefas renderizadas como itens de lista
5. Componente de Resenha de filme: receber título, nota (0-5 estrelas), review e renderizar card completo

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Estado com useState e Interatividade

**Conteúdo:**
- O que é estado (state) e por que é necessário
- `useState`: declarando e atualizando estado
- Estado com tipos primitivos (string, number, boolean)
- Estado com arrays e objetos
- Eventos no React: `onClick`, `onChange`, `onSubmit`
- Formulários controlados (controlled components)
- Estado baseado em estado anterior (`setState` com função)
- Separando lógica e apresentação (componente vs página)

**Exercícios práticos (escolha um):**
1. Contador interativo: botões para incrementar, decrementar e resetar, com estado visual de contagem
2. Formulário de cadastro: inputs para nome, email e idade, ao submeter mostrar os dados na tela
3. Toggle de tema: botão que alterna entre tema claro e escuro, salvando preferência

**Recursos:**
- [React.dev - useState](https://react.dev/reference/react/useState)
- [React.dev - Managing State](https://react.dev/learn/managing-state)
- [MDN - Events](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/Building_blocks/Events)

**Tarefas de casa (escolha uma ou mais):**
1. Jogo de par ou ímpar: usuário escolhe, computador escolhe aleatoriamente, resultado exibido
2. Formulário de login: inputs de usuário e senha, validação básica, feedback de sucesso/erro
3. Simulador de votômetro: input para número de votos, botões +1 e -1, total exibido
4. Trocador de frase: array de frases motivacionais, botão "próxima frase" que muda o estado
5. Seletor de idioma: botões para PT/EN/ES, texto que muda de acordo com o estado selecionado

**Tempo:** 4h (1h teoria + 2h prática + 1h desafios)

---

### Aula 3 — Renderização Condicional e Listas

**Conteúdo:**
- Renderização condicional: `&&`, `? :`, early return
- Exibindo ou ocultando elementos com base em estado
- `if/else` vs operadores ternários vs `&&`
- keys em listas: por que são importantes e como usar
- Index como key (quando não há ID único)
- Lidando com lista vazia
- Filtros e ordenação com base no estado
- Separando componentes de item e lista

**Exercícios práticos (escolha um):**
1. Lista de tarefas com filtro: array de tarefas, input de busca, botões "todas/pendentes/completas", renderização condicional
2. Filtro de produtos por categoria: array de produtos com categoria, botões de filtro, renderização da lista filtrada
3. Dashboard de métricas: estado com dados de vendas, renderizar cards diferentes baseado no valor (positivo/negativo/neutro)

**Recursos:**
- [React.dev - Conditional Rendering](https://react.dev/learn/conditional-rendering)
- [React.dev - Lists and Keys](https://react.dev/learn/rendering-lists)
- [React.dev - Thinking in React](https://react.dev/learn/thinking-in-react)

**Tarefas de casa (escolha uma ou mais):**
1. Agenda de contatos com busca: array de contatos, input de busca, renderizar apenas nomes que contêm o texto digitado
2. Carrinho de compras: lista de produtos, checkbox para selecionar, valor total calculado e exibido
3. Quiz com progresso: array de perguntas, mostrar só a pergunta atual, avançar ao responder, tela de resultado no final
4. Galeria com ordenação: array de imagens, botões para ordenar por nome/data/tamanho, re-renderização atualizada
5. Paginação simulada: array grande de itens, mostrar apenas 10 por vez, botões anterior/próxima

**Tempo:** 4h (1h teoria + 2h prática + 1h exercício guiado)

---

### Aula 4 — useEffect e Ciclo de Vida

**Conteúdo:**
- Efeitos colaterais: o que são e quando ocorrem
- `useEffect`: executando código após a renderização
- `useEffect` com array de dependências vazio (`[]`)
- `useEffect` com dependências específicas
- Cleanup de effect: retornando função
- Buscando dados com `useEffect` (fetch básico)
- Carregamento de dados e estados de loading/error
- Renderização após efeito colateral
- Diferença entre effect e event handler

**Exercícios práticos (escolha um):**
1. Componente que busca dados de usuário via API ao carregar: https://api.github.com/users/{username}, exibe avatar, nome e bio
2. Timer com useEffect: display de segundos que atualiza a cada segundo, botão para iniciar/pausar
3. Lista de posts buscando de API: https://jsonplaceholder.typicode.com/posts, renderizar títulos em lista

**Recursos:**
- [React.dev - useEffect](https://react.dev/reference/react/useEffect)
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) — API fake para testes
- [MDN - Fetch API](https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API)

**Tarefas de casa (escolha uma ou mais):**
1. Perfil de weather: input de cidade, buscar temperatura via API open-meteo (gratuita), exibir clima atual
2. Relógio mundial: selecionar timezone, usar `setInterval` com cleanup adequado
3. Lista de Pokémon: buscar lista de https://pokeapi.co/api/v2/pokemon/, renderizar cards com nome e imagem
4. To-Do com persistência: toda mudança de estado salva no localStorage via useEffect
5. Auto-save: textarea que salva automaticamente no localStorage após 2 segundos sem digitação

**Tempo:** 4h (1h teoria + 2h prática com APIs + 1h debugging)

---

### Aula 5 — Context API e Estado Global

**Conteúdo:**
- O problema de prop drilling
- Context API: criando e usando contexto
- `createContext` e `useContext`
- Provider: envolvendo componentes
- Múltiplos contextos vs contexto único
- Padrão de estado global: ThemeContext, AuthContext
- Atualizando contexto (estado + funções)
- Quando usar Context vs estado local
- Performance: evitando re-renderizações desnecessárias

**Exercícios práticos (escolha um):**
1. ThemeContext: criar toggle de tema claro/escuro, componente que consome o tema e altera cores globalmente
2. AuthContext: criar contexto de usuário logado, componentes Header e Profile que exibem dados diferentes baseado em estar logado ou não
3. CartContext: contexto de carrinho de compras, adicionar/remover itens de qualquer componente, total exibido no header

**Recursos:**
- [React.dev - Context](https://react.dev/reference/react/createContext)
- [React.dev - Scaling Up with Reducer and Context](https://react.dev/learn/scaling-up-with-reducer-and-context)
- [Kent C. Dodds - Context is not composition](https://kentcdodds.com/blog/context-is-not-a-state-management-solution)

**Tarefas de casa (escolha uma ou mais):**
1. LanguageContext: contexto de idioma, componentes que renderizam textos diferentes baseado na seleção
2. NotificationsContext: contexto de notificações, adicionar notificação de qualquer lugar, componente que lista todas
3. UserContext + AuthContext: criar contexto de usuário com dados e também boolean de autenticação
4. Criar um "Settings Context": preferências do app (tema, fonteSize, notificações) acessíveis em qualquer lugar
5. Refatorar o carrinho da aula prática para separar actions (add, remove, clear) do estado

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão de patterns)

---

### Aula 6 — Hooks Customizados e React Router

**Conteúdo:**
- Hooks customizados: extraindo lógica reutilizável
- Convenções de nomenclatura: `useNomeDoHook`
- Hooks customizados com estado e efeitos
- Exemplos: `useLocalStorage`, `useFetch`, `useToggle`
- React Router: o que é e para que serve
- Instalação: `react-router-dom`
- `BrowserRouter`, `Routes`, `Route`
- `Link` e `NavLink` (navegação sem reload)
- Parâmetros de URL: `useParams`
- Query params: `useSearchParams`

**Exercícios práticos (escolha um):**
1. App com 3 páginas: Home, Sobre, Contato — navegação com React Router sem reload
2. Blog com posts: lista na home, clique leva para página individual (`/posts/:id`)
3. Dashboard com sidebar: menu lateral com links para diferentes seções da aplicação

**Recursos:**
- [React Router Official Docs](https://reactrouter.com/)
- [React.dev - Reusing Logic with Custom Hooks](https://react.dev/learn/reusing-logic-with-custom-hooks)
- [useHooks.com](https://usehooks.com/) — galeria de hooks customizados

**Tarefas de casa (escolha uma ou mais):**
1. App de notas com navegação: lista de notas na home, clique abre nota para edição em outra rota
2. E-commerce com rotas: Home, Produtos, Produto individual (`/produto/:id`), Carrinho
3. Criar hook `useDebounce`: atrasa a atualização de um valor (útil para busca)
4. Criar hook `useOnClickOutside`: detecta clique fora de um elemento (útil para menus dropdown)
5. App de personagens: home com lista, página individual com detalhes completos do personagem selecionado

**Tempo:** 4h (1h teoria + 2h prática + 1h debugging de rotas)

---

### Aula 7 — Requisições HTTP e Boas Práticas

**Conteúdo:**
- fetch vs axios: diferenças e quando usar cada
- Instância do axios com headers padrão
- Interceptadores (interceptors): requests e responses
- Hook customizado `useFetch` reutilizável
- Estados de loading, data e error
- Cancelamento de requisições com AbortController
- Boas práticas de структура de projeto React
- Componentes inteligentes vs presentacionais
- Lidando com erros de API gracefulmente

**Exercícios práticos (escolha um):**
1. Componente UserList: buscar lista de usuários de API, renderizar cards com loading state e error state
2. Componente de busca de CEP: input para CEP, ao digitar buscar via API (viacep.com.br), exibir endereço
3. Dashboard de dados: buscar múltiplos endpoints, combinar dados, renderizar métricas

**Recursos:**
- [Axios Docs](https://axios-http.com/ptbr/docs/intro)
- [MDN - AbortController](https://developer.mozilla.org/pt-BR/docs/Web/API/AbortController)
- [ViaCEP](https://viaceep.com.br/) — API gratuita de CEP

**Tarefas de casa (escolha uma ou mais):**
1. Cloninha do GitHub user finder: input de username, buscar dados do usuário, renderizar perfil com avatar, bio, seguidores
2. App de previsão do tempo: buscar clima por cidade, exibir temperatura atual, mínima, máxima e ícone do clima
3. Criar hook `useApi`: hook genérico que recebe URL, retorna { data, loading, error } com AbortController
4. Componente de lista infinita: ao scrollar para o bottom, buscar mais dados (pagination com useEffect)
5. Criar um "Image Search" com a API do Unsplash ou Pexels, buscar imagens por termo

**Tempo:** 4h (1h teoria + 2h prática + 1h refatoração)

---

### Aula 8 — Projeto Final: Aplicação Completa

**Conteúdo:**
- Revisão dos conceitos do módulo
- Definindo o escopo do projeto
- Arquitetura: rotas, contextos, componentes, API
- Implementação guiada passo a passo
- Testes e debugging
- Boas práticas de organização de código
- Preparação para deploy
- Deploy no Vercel ou Netlify
- Apresentação final

**Exercício prático:**
1. Construir uma aplicação React completa do zero: autenticação (login/logout com Context), listagem de dados de API, formulários, rotas, estados de loading/error e deploy

**Sugestões de projetos:**
1. App de gerenciamento de tarefas com usuário logado (autenticação fake via Context, backend na aula anterior)
2. GitHub user finder: buscar usuário, ver repositórios, favoritar repositórios (salvos em localStorage)
3. Blog pessoal com posts (API fake), criação de post, comentários
4. E-commerce simplificado: lista de produtos, carrinho com Context, checkout simulado

**Desafio extra (para rápidos):**
1. Implementar testes com React Testing Library
2. Adicionar animações com Framer Motion
3. Criar um tema dark/light com persistência

**Recursos:**
- [Vercel.com](https://vercel.com/) — deploy gratuito
- [Netlify](https://www.netlify.com/) — alternativa
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)

**Tarefas de casa (escolha uma ou mais):**
1. Fazer deploy do projeto no Vercel e testar em produção
2. Adicionar persistência: tudo que o usuário faz é salvo no localStorage e restaurado ao recarregar
3. Escrever testes para pelo menos 2 componentes com React Testing Library
4. Criar um README completo do projeto: como rodar, funcionalidades, screenshots
5. Gravar um vídeo curto (2-3 min) explicando uma funcionalidade interessante do projeto

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Aplicação React com pelo menos 3 páginas (React Router)
2. Contexto para estado global (auth ou theme ou cart)
3. Dados de API com estados de loading/error
4. Hooks customizados para lógica reutilizável
5. Código organizado (componentes em pastas, separação de responsabilidades)
6. Deploy funcionando (URL pública)

---

## Próximo módulo

→ [Ux Ui Figma](modulos/ux-ui-figma.md)

---

#modulo #react #frontend #hooks #jsx #routing #fullstack
