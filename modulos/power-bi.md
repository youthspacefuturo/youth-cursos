# Power BI — Módulo 5

> Visualização de dados e dashboards business intelligence.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Cursos que utilizam este módulo:** [Fullstack Python](../cursos/fullstack-python.md) · [Data Science](../cursos/data-science.md)

---
## Aulas
### Aula 1 — Introdução ao Power BI e Power Query

**Conteúdo:**
- O que é Business Intelligence e para que serve
- Power BI Desktop: interface e componentes
- Importando dados: CSV, Excel, JSON, banco de dados
- Power Query Editor: transformando dados antes de carregar
- Removendo colunas, renomeando, alterando tipos
- Filtros e substituições no Power Query
- Append e Merge de consultas
- Carregando dados no modelo
- Diferença entre Power Query e DAX
- Salvando e publicando no Power BI Service

**Exercícios práticos (escolha um):**
1. Importar CSV de vendas, limpar dados com Power Query (remover nulos, corrigir tipos), carregar e visualizar
2. Combinar duas tabelas (clientes + pedidos) com Merge, criar tabela única de análise
3. Importar dados de múltiplos arquivos CSV (um por mês) e combiná-los com Append

**Recursos:**
- [Power BI Documentation](https://learn.microsoft.com/pt-br/power-bi/)
- [Datasets para praticar - Kaggle](https://www.kaggle.com/datasets)
- [Power BI Desktop - Download](https://powerbi.microsoft.com/pt-br/desktop/)

**Tarefas de casa (escolha uma ou mais):**
1. Baixar dataset do Kaggle, importar e limpar no Power Query
2. Importar dados de uma planilha Excel com múltiplas abas e criar modelo
3. Criar relatório de vendas simples com dados de 3 meses
4. Importar dados de uma API pública e visualizar no Power BI
5. Documentar em Word/Notion todos os passos de limpeza de dados de um dataset

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Modelagem de Dados e Relacionamentos

**Conteúdo:**
- O que é modelagem de dados no Power BI
- Star Schema vs Snowflake Schema
- Tabelas fato e tabelas dimensão
- Criando relacionamentos no Power BI
- Cardinalidade: 1:N, N:N, 1:1
- Direção do filtro: unidirecional vs bidirecional
- Tabela de datas (Date Table): por que criar e como
- Boas práticas de modelagem para performance
- Ocultando colunas desnecessárias no modelo
- Verificando relações com a visão de modelo

**Exercícios práticos (escolha um):**
1. Criar star schema com: fato_vendas, dim_produto, dim_cliente, dim_data, dim_vendedor — relacionar tudo
2. Modelar dados de um e-commerce: pedidos, itens, produtos, clientes, categorias
3. Criar tabela de datas customizada com Python script dentro do Power Query

**Recursos:**
- [SQLBI - Star Schema](https://www.sqlbi.com/articles/from-flat-to-star/)
- [Microsoft - Create Date Table](https://learn.microsoft.com/pt-br/power-bi/guidance/model-date-tables)

**Tarefas de casa (escolha uma ou mais):**
1. Modelar dados de uma escola: turmas, alunos, disciplinas, notas, professores
2. Criar modelagem de um hospital: pacientes, médicos, consultas, exames
3. Comparar Star Schema vs Snowflake com exemplos reais, documentar prós e contras
4. Criar Tabela de Datas completa com ano, mês, trimestre, semana, dia da semana
5. Otimizar um modelo existente: identificar e corrigir relações problemáticas

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 3 — DAX Básico

**Conteúdo:**
- O que é DAX (Data Analysis Expressions)
- Colunas calculadas vs Medidas: diferenças e quando usar
- Medidas simples: `SUM()`, `COUNT()`, `AVERAGE()`, `MIN()`, `MAX()`
- `COUNTROWS()` e `DISTINCTCOUNT()`
- Medidas com condição: `CALCULATE()` básico
- `FILTER()` dentro do CALCULATE
- Contexto de linha vs contexto de filtro
- Variáveis DAX: `VAR` e `RETURN`
- Formatando medidas: moeda, percentual, inteiro
- Tabela de medidas: organização

**Exercícios práticos (escolha um):**
1. Criar medidas de vendas: Total Vendas, Ticket Médio, Total Pedidos, Clientes Únicos
2. Medidas de estoque: Total Produtos, Produtos Abaixo do Mínimo, Valor Total em Estoque
3. Medidas de RH: Total Funcionários, Média Salarial, Custo Mensal por Departamento

**Recursos:**
- [DAX Guide](https://dax.guide/)
- [SQLBI - DAX Patterns](https://www.daxpatterns.com/)
- [Microsoft Learn - DAX](https://learn.microsoft.com/pt-br/dax/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar 10 medidas para o dataset trabalhado em aula, com variáveis DAX
2. Calcular participação percentual de cada produto no total de vendas
3. Criar medida de meta vs realizado com variação percentual
4. Calcular ticket médio por segmento de cliente
5. Pesquisar e implementar 3 medidas do site daxpatterns.com no projeto

**Tempo:** 4h (1h teoria + 2h prática + 1h revisão)

---

### Aula 4 — DAX Intermediário: Time Intelligence

**Conteúdo:**
- Time Intelligence: análise ao longo do tempo
- Funções de data: `DATEADD()`, `DATESYTD()`, `DATESMTD()`
- Período anterior: `PREVIOUSMONTH()`, `PREVIOUSYEAR()`
- Acumulado do ano (YTD): `TOTALYTD()`
- Crescimento vs período anterior: variação absoluta e percentual
- `SAMEPERIODLASTYEAR()`
- Rolling Average (média móvel)
- `RANKX()`: ranqueando elementos
- `TOPN()`: top N resultados
- `SWITCH()`: lógica condicional em DAX

**Exercícios práticos (escolha um):**
1. Análise temporal de vendas: Total, MoM (mês a mês), YoY (ano a ano), YTD, crescimento %
2. Dashboard de performance: ranking de vendedores, top 5 produtos, evolução trimestral
3. Análise de cohort básica: clientes novos vs recorrentes por mês

**Recursos:**
- [SQLBI - Time Intelligence](https://www.sqlbi.com/articles/time-intelligence-in-power-bi-desktop/)
- [DAX Patterns - Time Intelligence](https://www.daxpatterns.com/time-patterns/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar dashboard de evolução mensal com variação MoM e YoY
2. Implementar média móvel de 3 meses nas vendas
3. Criar ranking dinâmico top 10 que muda conforme filtros aplicados
4. Calcular dias desde a última compra por cliente (DAX + Date Table)
5. Criar análise de sazonalidade: comparar o mesmo mês em diferentes anos

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 5 — Visualizações e Design de Relatórios

**Conteúdo:**
- Tipos de gráficos e quando usar cada um
- Gráficos básicos: barras, colunas, linhas, pizza, rosca
- Gráficos avançados: treemap, funil, gauge, waterfall
- Mapas: preenchido, bolhas, Azure Maps
- Tabelas e matrizes
- KPI cards e indicadores
- Configurações de formatação: cores, fontes, bordas
- Temas personalizados (JSON)
- Layout e composição: hierarquia visual
- Slicers: filtros visuais para o usuário
- Drill-down e drill-through

**Exercícios práticos (escolha um):**
1. Dashboard de vendas completo: KPIs no topo, gráfico de linha temporal, mapa, tabela top produtos
2. Relatório executivo: design limpo com paleta de cores da empresa, apenas gráficos essenciais
3. Dashboard de RH: headcount por departamento, pirâmide etária, turnover, mapa de distribuição

**Recursos:**
- [Power BI Themes Generator](https://themes.powerbi.tips/)
- [Inspiration - NovyPro](https://www.novypro.com/)
- [DataViz Catalogue](https://datavizcatalogue.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar dashboard com tema personalizado (JSON) usando as cores de uma empresa real
2. Replicar um dashboard de referência do NovyPro
3. Criar relatório de análise de redes sociais com dados fictícios
4. Desenvolver dashboard de monitoramento de projetos (status, prazo, custo)
5. Criar relatório financeiro: DRE simplificado com variação vs orçamento

**Tempo:** 4h (1h teoria + 2h prática + 1h peer review de designs)

---

### Aula 6 — Power BI Service e Compartilhamento

**Conteúdo:**
- Power BI Service vs Power BI Desktop
- Publicando relatórios no Power BI Service
- Workspaces: organizando relatórios por área
- Dashboards vs Reports (diferença no Service)
- Compartilhando relatórios: links, incorporação, apps
- Atualização automática de dados (Gateway)
- Row-Level Security (RLS): segurança por linha
- Mobile layout: otimizando para celular
- Power BI Embedded (introdução)
- Alertas e subscriptions

**Exercícios práticos (escolha um):**
1. Publicar relatório criado em aula, criar dashboard com pins, compartilhar com colega
2. Configurar RLS: criar roles para cada vendedor ver apenas seus próprios dados
3. Criar versão mobile de um relatório existente com layout otimizado

**Recursos:**
- [Power BI Service Docs](https://learn.microsoft.com/pt-br/power-bi/consumer/end-user-service-overview)
- [Power BI Mobile](https://learn.microsoft.com/pt-br/power-bi/consumer/mobile/)

**Tarefas de casa (escolha uma ou mais):**
1. Publicar todos os relatórios do módulo no Power BI Service
2. Configurar gateway local e atualização automática de dataset
3. Criar App do Power BI com múltiplos relatórios organizados
4. Configurar RLS para cenário multi-empresa
5. Testar relatório no aplicativo mobile e ajustar layout

**Tempo:** 4h (1h teoria + 2h prática + 1h tour do Service)

---

### Aula 7 — Power BI + Python

**Conteúdo:**
- Usando Python no Power BI (script visual e transformação)
- Configurando Python no Power BI Desktop
- Python como fonte de dados
- Scripts Python no Power Query
- Visuais Python: Matplotlib, Seaborn, Plotly
- Quando usar Python vs DAX nativo
- Casos de uso: forecasting, clustering, análise de texto
- Limitações e considerações de performance
- Bibliotecas suportadas: pandas, numpy, sklearn, matplotlib

**Exercícios práticos (escolha um):**
1. Criar visual Python com Seaborn no Power BI: heatmap de correlação entre variáveis
2. Usar Python no Power Query para limpar dados com pandas (remover outliers, normalizar)
3. Script Python como fonte de dados: gerar dados sintéticos e visualizar no Power BI

**Recursos:**
- [Microsoft - Python in Power BI](https://learn.microsoft.com/pt-br/power-bi/connect-data/desktop-python-scripts)
- [Real Python - Data Visualization](https://realpython.com/python-matplotlib-guide/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar visual de wordcloud com Python mostrando palavras mais frequentes em texto
2. Implementar forecast simples com sklearn no Power BI
3. Criar análise de clustering com KMeans e visualizar resultado no Power BI
4. Usar Python para importar dados de API e carregar no Power BI
5. Comparar o mesmo gráfico feito com DAX nativo vs Python — documentar prós e contras

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 8 — Projeto: Dashboard Completo

**Conteúdo:**
- Revisão dos conceitos do módulo
- Planejamento do dashboard: definir KPIs e perguntas de negócio
- Escolha e preparação do dataset
- Modelagem de dados
- Medidas DAX necessárias
- Design do relatório
- Publicação e apresentação

**Exercício prático:**
1. Dashboard completo do zero: dataset real, modelagem, DAX com Time Intelligence, design profissional, publicado no Service

**Sugestões de tema:**
1. Dashboard de vendas de e-commerce (dados do Olist no Kaggle)
2. Análise de streaming (Netflix, Spotify — dados públicos)
3. Dashboard financeiro de empresa fictícia
4. Análise de dados educacionais (notas, aprovação, evasão)
5. Dashboard de RH (headcount, turnover, custo de pessoal)

**Desafio extra:**
1. Criar storytelling: relatório narrativo que guia o usuário pela análise
2. Implementar botões de navegação entre páginas
3. Criar capa com sumário e links para cada seção

**Tarefas de casa (escolha uma ou mais):**
1. Publicar dashboard no Power BI Service com compartilhamento público
2. Criar apresentação de 5 slides sobre os insights encontrados
3. Escrever LinkedIn post sobre a análise realizada (prática de comunicação)
4. Adicionar página de metodologia ao relatório (fontes, transformações, limitações)
5. Receber feedback de um colega e aplicar melhorias

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentações)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Dashboard publicado no Power BI Service
2. Dataset real com modelagem Star Schema
3. Mínimo 5 medidas DAX (incluindo Time Intelligence)
4. Design profissional com tema customizado
5. Relatório com pelo menos 3 páginas
6. Apresentação de 5 minutos dos insights

---

## Materiais do Professor

- [Python X Banco com Streamlit.pptx](https://drive.google.com/file/d/1X2yU2HUwSi91VWhZ3bj_5QXGfssdPx-7/view)

---

## Recursos Complementares

- [Info](../recursos/dax/vendas-mais/info.md)
- [Exercicios](../recursos/dax/vendas-mais/exercicios.md)
- [Resolucoes](../recursos/dax/vendas-mais/resolucoes.md)

---

## Próximo módulo

→ [Aws](../modulos/aws.md) ou [Aws Git Data](../modulos/aws-git-data.md)

---

#modulo #powerbi #bi #dados #dashboards #dax #python
