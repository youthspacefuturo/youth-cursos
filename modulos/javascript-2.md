# JavaScript 2 — Módulo 3

> Lógica avançada: arrays, loops e funções.

## Informações do Módulo

- **Aulas:** 6 (de 4h cada)
- **Carga horária:** 24h
- **Posição na trilha:** [Fullstack 12 Meses#fase 1 Fundamentos Linear](cursos/fullstack-12-meses#fase-1--fundamentos-linear.md)

---
## Aulas
### Aula 1 — Arrays: Criação e Acesso

**Conteúdo:**
- O que é um array (vetor)
- Criando arrays: `[]` e `new Array()`
- Acessando elementos por índice (começa em 0!)
- `.length` — tamanho do array
- Alterando e adicionando elementos (push, pop, shift, unshift)
- Arrays multidimensional (matriz simples)
- spread operator: `...array`

**Exercícios práticos (escolha um):**
1. Lista de compras: criar array, adicionar itens, remover o último, mostrar a lista completa
2. Gerenciador de notas: criar array de notas, calcular média, mostrar a maior e a menor
3. Cadastro de personagens: criar array de objetos com nome, idade e hobby de 3 personagens

**Recursos:**
- [MDN - Arrays](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [MDN - Array Methods](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array#instanciações)

**Tarefas de casa (escolha uma ou mais):**
1. Agenda de contatos: criar array de objetos com nome e telefone, listar todos e buscar por nome
2. Sorteio de amigo secreto: criar array de nomes e sortear um aleatório
3. Lista de tarefas: permitir adicionar, marcar como concluída e remover tarefas
4. Estatísticas de time de futebol: array de jogadores com nome e gols, mostrar artilheiro e total de gols
5. Inventário de jogo RPG: array de itens com nome, tipo e dano, permitir listar e buscar por tipo

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Métodos de Array

**Conteúdo:**
- `.map()` — transformar cada elemento
- `.filter()` — filtrar elementos
- `.reduce()` — reduzir a um único valor
- `.find()` e `.findIndex()` — encontrar elemento
- `.includes()` e `.indexOf()` — verificar existência
- `.sort()` — ordenar
- `.slice()` e `.splice()` — copiar e remover
- Encadeando métodos (method chaining)
- Destructuring de arrays: `const [a, b] = array`

**Exercícios práticos (escolha um):**
1. Processador de vendas: array de objetos {produto, preco, quantidade}, usar map para calcular total, filter para produtos > R$50, reduce para total geral
2. Filtro de candidatos: array de objetos {nome, idade, experiencia}, filtrar quem tem ≥18 anos e experiência > 2 anos
3. Gerenciador de playlist: array de músicas {titulo, artista, duracao}, filtrar por artista, ordenar por duração, mostrar total de duração

**Recursos:**
- [MDN - Map](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [MDN - Filter](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [MDN - Reduce](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
- [Exercism - Array Exercises](https://exercism.org/tracks/javascript/exercises)

**Tarefas de casa (escolha uma ou mais):**
1. Dashboard de vendas: array de vendas {produto, valor, categoria}, gerar relatório com total por categoria usando reduce
2. Sistema de/library: array de livros, filtrar por autor, ordenar por ano, buscar por título com includes
3. Analisador de temperatura: array de temperaturas por dia, usar map para converter Celsius→Fahrenheit, filter para dias quentes (>30°C), reduce para média
4. Classificador de produtos: array de produtos com preço e categoria, usar filter para promoções (>20% desconto), map para aplicar desconto
5. Gerenciador de equipes: array de equipes com membros, usar reduce para contar total de membros, find para buscar equipe por nome

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 3 — Objetos e JSON

**Conteúdo:**
- O que são objetos: `{ chave: valor }`
- Acessando propriedades: `.` vs `[]`
- Adicionando e removendo propriedades
- Métodos em objetos
- `this` — referenciando o próprio objeto
- Objetos dentro de arrays (array de objetos)
- JSON: o que é e para que serve
- `JSON.stringify()` e `JSON.parse()`
- Desestruturação de objetos: `const { nome, idade } = pessoa`

**Exercícios práticos (escolha um):**
1. Cartão de visita interativo: objeto com nome, cargo, empresa, email, criar função que exibe formatted
2. Calculadora de IMC com histórico: array de objetos {nome, peso, altura, data}, calcular IMC de cada um e classificar
3. Sistema de veículos: objeto com marca, modelo, ano, preço, criar método que aplica desconto

**Recursos:**
- [MDN - Objects](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [MDN - JSON](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON)
- [MDN - Destructuring](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)

**Tarefas de casa (escolha uma ou mais):**
1. Perfil de rede social: objeto com nome, bio, seguidores, posts (array de objetos), calcular engajamento (comentários/seguidores)
2. Catálogo de filmes: array de objetos {titulo, diretor, ano, generos (array)}, buscar por gênero, ordenar por ano
3. Registrador de transações: objeto com {id, tipo (entrada/saida), valor, descricao, data}, usar filter para separar entradas e saídas, reduce para saldo
4. Agenda de compromissos: array de objetos {id, titulo, descricao, data, categoria}, filtrar por categoria, ordenar por data
5. Configurador de personagem (RPG): objeto com atributos {nome, classe, nivel, vida, mana, forca}, criar método de level up que aumenta atributos

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 4 — DOM: Seleção de Elementos e Eventos

**Conteúdo:**
- O que é o DOM (Document Object Model)
- `document.getElementById()` e `document.querySelector()`
- `document.querySelectorAll()` e NodeList
- `.textContent` e `.innerHTML` (diferenças e segurança)
- Selecionando elementos pai, filho e irmão
- Criando elementos: `.createElement()`
- Adicionando ao DOM: `.appendChild()` e `.append()`
- Eventos: `.addEventListener('click', function)`
- Eventos comuns: click, submit, keyup, keydown, change, mouseover
- Event object: `e.target`, `e.preventDefault()`
- Delegação de eventos

**Exercícios práticos (escolha um):**
1. Contador de cliques: botão que incrementa, decrementa e reseta um número na tela
2. Lista de tarefas interativa: input para adicionar tarefa, lista que exibe, botão de remover ao lado de cada item
3. Formulário de cadastro: inputs para nome, email e idade, ao submeter mostrar os dados no console

**Recursos:**
- [MDN - DOM Introduction](https://developer.mozilla.org/pt-BR/docs/Web/API/Document_object_model/Introduction)
- [MDN - querySelector](https://developer.mozilla.org/pt-BR/docs/Web/API/Document/querySelector)
- [MDN - addEventListener](https://developer.mozilla.org/pt-BR/docs/Web/API/EventTarget/addEventListener)
- [DOM Playground](https://chrome developer tools → Elements panel)

**Tarefas de casa (escolha uma ou mais):**
1. Simulador de loteria: input para número apostado, botão para sortear, exibir resultado (acertou ou não)
2. Accordion/FAQ: lista de perguntas, clicar na pergunta expande/recolhe a resposta
3. Trocador de tema: botão que alterna entre tema claro e escuro, salvando preferência no localStorage
4. Galeria de imagens: miniaturas que, ao clicar, mostram imagem grande em modal
5. Quiz interativo: perguntas com 4 opções, ao selecionar mostrar se acertou ou errou
6. Timer/Pomodoro: display com segundos, botões iniciar, pausar e resetar

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 5 — DOM: Manipulação de Estilos e Renderização

**Conteúdo:**
- Alterando CSS via JavaScript: `.style`
- Classe `.classList` (.add, .remove, .toggle, .contains)
- Alterando atributos: `.setAttribute()`, `.getAttribute()`
- Renderização condicional: mostrando/escondendo elementos com base em condições
- Renderização de listas: loop dentro do innerHTML ou createElement
- Template literals para gerar HTML dinâmico
- Separando dados (objeto) da visualização (HTML/CSS)
- Limpando conteúdo: `.innerHTML = ''`

**Exercícios práticos (escolha um):**
1. Painel de métricas: cards que mostram dados de um objeto, com botões para trocar entre visualizações (cards/tabela/lista)
2. Seletor de personagens: dropdown com nomes, ao selecionar mostra card com foto, stats e descrição do personagem
3. Mural de cards de produtos: array de produtos renderizados como cards, com filtro por categoria usando botões

**Recursos:**
- [MDN - Changing styles](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/Howto/Change_elements)
- [MDN - Template literals](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Template_literals)
- [MDN - classList](https://developer.mozilla.org/pt-BR/docs/Web/API/Element/classList)

**Tarefas de casa (escolha uma ou mais):**
1. Dashboard financeiro: receber receitas e despesas, renderizar cards com saldo total, total de receitas e total de despesas
2. Feed de posts: array de posts com autor, texto, data e likes, renderizar como feed com botão de like
3. Seletor de планeta: dropdown com opções (Mercúrio, Vênus, etc.), ao selecionar mostrar card com peso, gravidade e temperatura média
4. Comparador de smartphones: array de celulares, renderizar cards comparativos, filtrar por faixa de preço
5. Lista de compras com totales: itens com quantidade e preço, renderizar lista com subtotal por item e total geral

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 6 — Projeto: To-Do List Completa

**Conteúdo:**
- Estruturando o HTML: input, botão, lista
- Estilizando com CSS (card, shadows, cores)
- Modelando dados: array de objetos {id, texto, completo}
- Funções: adicionar, completar, remover, editar
- Persistência com localStorage (JSON.stringify/parse)
- Contadores dinâmicos: total, completados, pendentes
- Filtros: mostrar todos / ativos / completados
- Código organizado: separação de dados, DOM e eventos
- Boas práticas de organização de código

**Exercício prático:**
1. Construir uma To-Do List completa com: adicionar tarefa, marcar como concluída (riscada), remover, editar (ao clicar no texto), filtros (todos/pendentes/completos), persistência no localStorage e contador de tarefas

**Desafio extra (para rápidos):**
1. Adicionar categorias/tag às tarefas e filtrar por categoria
2. Adicionar data de prazo e destacar tarefas vencidas
3. Implementar arrastar-e-soltar para reordenar tarefas

**Recursos:**
- [MDN - localStorage](https://developer.mozilla.org/pt-BR/docs/Web/API/Window/localStorage)
- [MDN - Working with objects](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Working_with_Objects)
- [TodoMvc Example](https://todomvc.com/) (referência de projeto to-do)

**Tarefas de casa (escolha uma ou mais):**
1. Calculadora de IMC completa: input de peso/altura, exibir resultado com classificação e histórico de medições salvas no localStorage
2. Gerenciador de contatos: CRUD completo (criar, ler, atualizar, deletar) com persistência no localStorage
3. app de anotações: criar, editar e deletar notas, salvar no localStorage, com busca por texto
4. Lista de desejos: adicionar itens com link, preço e prioridade, marcar como comprado, filtrar por comprado/disponível
5. Rastreador de hábitos: marcar dias que praticou um hábito, mostrar streak atual e histórico semanal

**Tempo:** 4h (30min revisão + 3h projeto guiado + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. To-Do List completa e funcional (ou app equivalente)
2. Dados persistidos no localStorage
3. Código organizado (sem código inline no HTML)
4. pelo menos um filtro funcional
5. Uso de funções para organizar a lógica

---

## Próximo módulo

→ [Html Css Avancado](modulos/html-css-avancado.md)

---

#modulo #javascript #logica #dom #arrays #objetos #fullstack
