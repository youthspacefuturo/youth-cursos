# HTML & CSS — Módulo 1

> Fundamentos da construção de páginas web.

## Informações do Módulo

- **Aulas:** 4 (de 4h cada)
- **Carga horária:** 16h
- **Posição na trilha:** [Fullstack 12 Meses#fase 1 Fundamentos Linear](cursos/fullstack-12-meses#fase-1--fundamentos-linear.md)

---
## Aulas
### Aula 1 — O Mundo Web e Primeiras Tags

**Conteúdo:**
- Como a web funciona (navegador ↔ servidor ↔ HTTP)
- Diferença entre frontend e backend
- Editores de código (VS Code + extensões úteis)
- Estrutura básica HTML (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)
- Tags essenciais: `<h1>` a `<h6>`, `<p>`, `<strong>`, `<em>`
- Criando seu primeiro arquivo HTML

**Exercícios práticos (escolha um):**
1. Criar página "Sobre Mim" com nome, título, parágrafo sobre hobbies e uma lista de skills
2. Criar uma página "Currículo" com nome, cargo desejado, contato e resumo profissional
3. Montar uma página "Perfil de Personagem" (fictício ou real) com nome, história e características

**Recursos:**
- [MDN - HTML Basics](https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/HTML_basics)
- [MDN - Estrutura de Documentos](https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Howto)

**Tarefas de casa (escolha uma ou mais):**
1. Criar uma página "Currículo" com nome, cargo desejado, contato e resumo profissional
2. Fazer uma lista de seus 10 filmes/séries favoritos usando listas ordenadas
3. Escrever um texto sobre seu hobby favorito usando pelo menos 5 tags diferentes de formatação (`<strong>`, `<em>`, `<mark>`, `<small>`, etc.)
4. Explorar o código fonte de um site famoso (ex: wikipedia.org) e identificar as tags principais

**Tempo:** 4h (1h teoria + 2h prática + 1h correção coletiva)

---

### Aula 2 — Listas, Links e Imagens

**Conteúdo:**
- Listas ordenadas (`<ol>`) e não ordenadas (`<ul>`)
- Listas aninhadas
- Links com `<a href="">` (absolutos vs relativos)
- Atributos de links (`target="_blank"`, `title`)
- Imagens com `<img src="" alt="">`
- Caminhos de arquivo (mesma pasta, subpastas, `../`)

**Exercícios práticos (escolha um):**
1. Criar página de receitas com: título, ingredientes (lista), modo de preparo (lista ordenada), link para outra receita e uma imagem ilustrativa
2. Criar uma página "Guia de Viagem" com pelo menos 3 destinos, cada um tendo: imagem, lista de pontos turísticos e link para mais informações
3. Montar uma página de "Carta de Apresentação" com link para seu LinkedIn e GitHub

**Recursos:**
- [MDN - Links](https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
- [MDN - Imagens](https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)

**Tarefas de casa (escolha uma ou mais):**
1. Criar uma página "Guia de Viagem" com pelo menos 3 destinos, cada um tendo: imagem, lista de pontos turísticos e link para mais informações
2. Montar uma página de "Carta de Apresentação" com link para seu LinkedIn e GitHub
3. Criar um "Glossário de Programação" com termos organizados em listas ordenadas por ordem alfabética
4. Fazer uma página que seja um "Menu de Restaurante" com categorias, listas de pratos e preços (fictícios)
5. Construir uma "Página de Tributo" para alguém que admira, com foto, biografia e fatos interessantes — todos como links para saber mais

**Tempo:** 4h (1h teoria + 2h prática + 1h correção coletiva)

---

### Aula 3 — CSS: Seletores e Box Model

**Conteúdo:**
- O que é CSS e por que separar estilo de conteúdo
- Inline CSS vs Internal CSS (`<style>`) vs External CSS (`<link>`)
- Seletores básicos: tag, classe (`.`), id (`#`)
- Propriedades essenciais: `color`, `font-size`, `background-color`
- Box Model: `content`, `padding`, `border`, `margin`
- Diferença entre `margin` e `padding`
- Centralizando elementos com `margin: auto`
- Flexbox básico (`display: flex`, `justify-content`, `align-items`)

**Exercícios práticos (escolha um):**
1. Estilizar a página "Sobre Mim" da Aula 1: fonte customizada, cores, cards com border-radius e shadow, layout centralizado com Flexbox
2. Criar cards de "Post de Blog" com: título, autor, data, conteúdo e "Leia mais" — todos estilizados com classes CSS
3. Fazer um "Card de Produto" para um e-commerce fictício com: imagem, nome, preço, botão de comprar e badge de "promoção"

**Recursos:**
- [MDN - Box Model](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/Building_blocks/The_box_model)
- [Flexbox Froggy](https://flexboxfroggy.com/) (joguinho interativo)
- [MDN - Flexbox](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Flexbox)

**Tarefas de casa (escolha uma ou mais):**
1. Recrear o visual de uma rede social famosa (perfil, posts, sidebar) usando apenas HTML e CSS (sem JavaScript)
2. Fazer um "Card de Produto" para um e-commerce fictício com: imagem, nome, preço, botão de comprar e badge de "promoção"
3. Criar um "Relógio Digital" usando CSS para os números e box model para o display
4. Desenvolver um "Menu de Navegação" horizontal com logo à esquerda e links à direita usando Flexbox
5. Criar cards estilizados para os personagens de um jogo ou anime favorito

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio extra)

---

### Aula 4 — CSS Grid e Responsividade

**Conteúdo:**
- CSS Grid: `grid-template-columns`, `grid-template-rows`, `gap`
- Grid vs Flexbox (quando usar cada um)
- `fr` units e `repeat()`
- Responsividade com `@media queries`
- Mobile-first: `min-width` vs `max-width`
- Breakpoints comuns (480px, 768px, 1024px)
- Boas práticas de organização CSS

**Exercícios práticos (escolha um):**
1. Criar um layout de cards de portfólio que funcione em desktop (3 colunas), tablet (2 colunas) e mobile (1 coluna)
2. Criar um "Dashboard de Finanças Pessoais" com cards de: Renda, Despesas, Investimentos e Metas — responsivo com Grid
3. Desenvolver uma "Landing Page" de produto com: hero banner, features em grid, pricing table e CTA final

**Desafio extra (para rápidos):**
1. Implementar menu hamburger com CSS puro para mobile

**Recursos:**
- [CSS Grid Garden](https://cssgridgarden.com/) (joguinho interativo)
- [MDN - CSS Grid](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Grids)
- [MDN - Media Queries](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Media_Queries/Responsive_design)

**Tarefas de casa (escolha uma ou mais):**
1. Criar um "Dashboard de Finanças Pessoais" com cards de: Renda, Despesas, Investimentos e Metas — responsivo com Grid
2. Desenvolver uma "Galeria de Fotos" com Grid que mude de 4 colunas (desktop) para 2 colunas (mobile)
3. Construir um "Layout de Revista Digital" com header, sidebar, conteúdo principal e footer — responsivo
4. Fazer uma "Landing Page" de produto com: hero banner, features em grid, pricing table e CTA final
5. Criar um "Cardápio Digital" responsivo para restaurante com categorias organizadas em Grid

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto integrador)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Portfólio pessoal simples com pelo menos 2 páginas
2. Uso correto de tags semânticas (header, main, footer)
3. Layout responsivo (Grid ou Flexbox)
4. CSS externo organizado (sem inline styles)

---

## Próximo módulo

→ [Javascript 1](modulos/javascript-1.md)

---

#modulo #html #css #fullstack
