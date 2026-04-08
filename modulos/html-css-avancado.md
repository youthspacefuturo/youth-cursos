# HTML & CSS Avançado — Módulo 4

> Layouts profissionais com CSS Grid, animações e responsividade.

## Informações do Módulo

- **Aulas:** 4 (de 4h cada)
- **Carga horária:** 16h
- **Posição na trilha:** [Fullstack 12 Meses#fase 1 Fundamentos Linear](cursos/fullstack-12-meses#fase-1--fundamentos-linear.md)

---
## Aulas
### Aula 1 — CSS Grid Avançado

**Conteúdo:**
- Revisão rápida: Grid básico e Flexbox
- Grid template areas (`grid-template-areas`)
- `grid-column` e `grid-row` (span e posicionamento explícito)
- `minmax()` e `auto-fill` / `auto-fit`
- Grids aninhados (nested grids)
- Alinhamento dentro do grid: `align-items`, `justify-items`, `place-items`
- Grid vs Flexbox: quando usar cada um e quando combinar
- Construindo layouts complexos (header, sidebar, main, footer)

**Exercícios práticos (escolha um):**
1. Construir o layout de um blog completo: header com nav, sidebar com widgets, área principal de posts em grid e footer — responsivo
2. Criar um layout de dashboard administrativo: navbar lateral, header, área de conteúdo com cards em grid 2x2
3. Montar um layout de e-commerce: header, grid de produtos (4 colunas → 2 → 1), sidebar de filtros, footer

**Recursos:**
- [MDN - Grid Template Areas](https://developer.mozilla.org/pt-BR/docs/Web/CSS/grid-template-areas)
- [Grid by Example](https://gridbyexample.com/) — galeria de exemplos de layout
- [CSS Grid Garden](https://cssgridgarden.com/) (revisão)

**Tarefas de casa (escolha uma ou mais):**
1. Criar um layout de revista digital com hero, artigos em destaque (grid 3 colunas), artigos secundários e rodapé
2. Recriar o layout do YouTube (sidebar + área de vídeos em grid) com HTML e CSS puro
3. Criar um painel de controle com layout em grid: KPIs no topo, gráfico (placeholder) no centro, tabela na base
4. Construir a página de perfil de uma rede social com: capa, avatar, informações e posts em grid
5. Montar um portfólio com grid assimétrico (alguns cards maiores que outros usando `grid-column: span 2`)

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Responsividade Avançada e Mobile-First

**Conteúdo:**
- Mobile-first: por que começar pelo mobile
- Breakpoints estratégicos e semânticos (não só por tamanho de dispositivo)
- `@media queries` avançadas: `orientation`, `prefers-color-scheme`, `prefers-reduced-motion`
- `clamp()`, `min()`, `max()` para tipografia fluida
- Unidades relativas: `rem`, `em`, `vw`, `vh`, `%` — quando usar cada
- Imagens responsivas: `srcset` e `<picture>`
- Container queries (introdução)
- Testando responsividade no DevTools

**Exercícios práticos (escolha um):**
1. Refatorar um layout existente (da aula 1) para ser verdadeiramente mobile-first, aplicando `clamp()` na tipografia
2. Criar uma landing page completa que funcione perfeitamente em mobile (320px) e desktop (1440px)
3. Construir um cardápio digital responsivo com tipografia fluida e imagens adaptativas

**Recursos:**
- [MDN - Responsive Design](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Responsive_Design)
- [MDN - clamp()](https://developer.mozilla.org/pt-BR/docs/Web/CSS/clamp)
- [MDN - srcset](https://developer.mozilla.org/pt-BR/docs/Web/API/HTMLImageElement/srcset)
- [Responsively App](https://responsively.app/) — ferramenta de teste responsivo

**Tarefas de casa (escolha uma ou mais):**
1. Transformar a página "Sobre Mim" do módulo 1 em uma página responsiva profissional com tipografia fluida
2. Criar uma galeria de fotos responsiva com srcset para imagens otimizadas por tamanho de tela
3. Construir um site de restaurante mobile-first com menu, horários e localização
4. Criar uma página que adapte o layout com base em `prefers-color-scheme` (modo claro/escuro automático)
5. Montar um portfólio responsivo completo que funcione de 320px a 2560px sem quebrar layout

**Tempo:** 4h (1h teoria + 2h prática + 1h revisão coletiva)

---

### Aula 3 — Variáveis CSS e Animações

**Conteúdo:**
- Variáveis CSS: `--nome: valor` e `var(--nome)`
- Criando sistemas de design com variáveis (cores, espaçamento, tipografia)
- Transitions: `transition-property`, `duration`, `timing-function`, `delay`
- Animações com `@keyframes`: `from/to` e percentagens
- Propriedades animáveis (e o que evitar por performance)
- `animation-fill-mode`, `iteration-count`, `direction`
- Pseudo-classes de estado: `:hover`, `:focus`, `:active`
- Pseudo-elementos: `::before`, `::after`
- Performance de animações: `transform` e `opacity` vs `top/left`

**Exercícios práticos (escolha um):**
1. Criar um sistema de design com variáveis CSS: definir paleta de cores, escala de tipografia e espaçamento, aplicar em uma página existente
2. Construir um conjunto de botões animados: hover com efeito ripple, loading spinner, botão com ícone que desliza
3. Criar uma página de landing com: hero animado (texto entrando da esquerda), cards com hover suave, scroll reveal com CSS

**Recursos:**
- [MDN - CSS Custom Properties](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Using_CSS_custom_properties)
- [MDN - Using CSS Animations](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- [Animista](https://animista.net/) — gerador visual de animações CSS
- [CSS Tricks - Transition](https://css-tricks.com/almanac/properties/t/transition/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar um loading screen animado para uma aplicação fictícia
2. Construir um card de produto com animação de flip 3D ao hover (frente: imagem + nome, verso: descrição + botão)
3. Fazer um menu de navegação animado: links com underline que cresce do centro ao hover
4. Criar um skeleton screen (loading placeholder) com animação shimmer para simular carregamento de conteúdo
5. Construir um banner hero com texto animado (efeito de digitação com CSS) e imagem de fundo com parallax

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 4 — Boas Práticas, BEM e Projeto Final

**Conteúdo:**
- Metodologia BEM (Block, Element, Modifier): `.card`, `.card__title`, `.card--featured`
- Organização de arquivos CSS: por componente, por página
- Especificidade CSS e como evitar conflitos
- CSS resets e normalize.css
- Acessibilidade: `aria-label`, `role`, foco visível, contraste
- Performance CSS: o que evita reflows e repaints
- Inspecionando CSS com DevTools avançado
- Revisão dos conceitos do módulo
- Apresentação do projeto final do módulo

**Exercícios práticos (escolha um):**
1. Refatorar um CSS existente aplicando BEM e variáveis CSS, sem quebrar o visual
2. Criar um componente Card reutilizável com BEM: com e sem imagem, com e sem badge, variante destacada
3. Fazer uma auditoria de acessibilidade em uma página criada no módulo e corrigir os problemas encontrados

**Recursos:**
- [BEM Methodology](https://getbem.com/introduction/)
- [MDN - Accessibility](https://developer.mozilla.org/pt-BR/docs/Web/Accessibility)
- [WebAIM - Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [CSS Tricks - BEM](https://css-tricks.com/bem-101/)

**Tarefas de casa (escolha uma ou mais):**
1. Reescrever toda a CSS de um projeto anterior usando BEM e variáveis CSS
2. Criar uma biblioteca de componentes CSS: botões, badges, cards, inputs, alertas — todos com BEM e variáveis
3. Construir uma landing page completa: mobile-first, BEM, variáveis CSS, animações, acessível
4. Auditar e corrigir a acessibilidade de uma página existente (usar Lighthouse do DevTools)
5. Criar uma styleguide visual: página que mostra todas as cores, tipografias, espaçamentos e componentes do projeto

**Tempo:** 4h (1h teoria + 2h prática + 1h apresentações)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Landing page ou portfólio completo e responsivo
2. CSS organizado com BEM e variáveis CSS
3. Pelo menos 2 animações (hover + uma via keyframes)
4. Layout com Grid e Flexbox combinados
5. Aprovado no teste de contraste de cores (WCAG AA)

---

## Próximo módulo

→ [Nodejs Git Github](modulos/nodejs-git-github.md)

---

#modulo #css #avancado #grid #responsivo #animacoes #bem #fullstack
