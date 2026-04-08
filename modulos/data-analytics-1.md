# Data Analytics 1 — Módulo 5

> Análise exploratória e visualização de dados com Python.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Data Science#fase 2 Especializacao Circular](cursos/data-science#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — Ambiente e Pandas Básico

**Conteúdo:**
- Jupyter Notebook: células, execução, markdown
- JupyterLab vs Jupyter Notebook vs VS Code
- Anaconda / virtualenv: ambientes isolados
- Instalando bibliotecas: pandas, numpy, matplotlib
- Pandas: o que é e por que usar
- Series e DataFrame: estruturas fundamentais
- Criando DataFrame de lista, dicionário e CSV
- `.head()`, `.tail()`, `.info()`, `.describe()`
- Acessando dados: `.loc[]`, `.iloc[]`, colunas por nome
- Seleção com condições booleanas

**Exercícios práticos (escolha um):**
1. Explorar dataset de vendas: carregar CSV, inspecionar shape, tipos de dados, ver primeiras linhas, calcular estatísticas básicas
2. Análise de dataset de filmes: carregar, filtrar por gênero e ano, listar os 10 mais bem avaliados
3. Dataset de alunos: criar DataFrame manual, adicionar colunas calculadas, filtrar aprovados

**Recursos:**
- [Pandas Docs](https://pandas.pydata.org/docs/)
- [Kaggle Datasets](https://www.kaggle.com/datasets) — datasets gratuitos
- [10 Minutes to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)

**Tarefas de casa (escolha uma ou mais):**
1. Explorar dataset público do IBGE (população, economia) no Jupyter
2. Analisar dataset de games (metacritic scores, vendas) — filtros, ranking, comparações
3. Criar análise de dados pessoais: gastos mensais em planilha → DataFrame → insights
4. Explorar 3 datasets diferentes do Kaggle, documentar estrutura e possíveis análises
5. Comparar `.loc` vs `.iloc` com exemplos práticos em notebook

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Limpeza e Preparação de Dados

**Conteúdo:**
- Valores nulos: `.isnull()`, `.dropna()`, `.fillna()`
- Estratégias de imputação: média, mediana, moda, forward fill
- Tipos de dados: convertendo com `.astype()`
- Dados duplicados: `.duplicated()`, `.drop_duplicates()`
- Renomeando colunas: `.rename()`
- Strings em colunas: `.str.lower()`, `.str.strip()`, `.str.replace()`
- Criando colunas derivadas
- Lidando com outliers: IQR method
- Encoding de variáveis categóricas: `.map()`, `pd.get_dummies()`
- Data Quality: o que verificar antes de analisar

**Exercícios práticos (escolha um):**
1. Limpar dataset sujo: remover duplicatas, tratar nulos com estratégia adequada, corrigir tipos
2. Processar dataset de e-commerce com problemas: preços como string com "R$", datas erradas, categorias inconsistentes
3. Pipeline de limpeza: função que recebe DataFrame bruto e retorna DataFrame limpo e documentado

**Recursos:**
- [Pandas - Missing Data](https://pandas.pydata.org/docs/user_guide/missing_data.html)
- [Real Python - Data Cleaning](https://realpython.com/python-data-cleaning-numpy-pandas/)

**Tarefas de casa (escolha uma ou mais):**
1. Baixar dataset com problemas no Kaggle e documentar cada decisão de limpeza
2. Criar função de limpeza genérica: recebe DataFrame + regras → retorna limpo + relatório de mudanças
3. Tratar dataset de textos: normalizar nomes, remover caracteres especiais, padronizar emails
4. Implementar detecção e tratamento de outliers em dataset de preços
5. Criar data quality report: estatísticas de nulos, duplicatas, outliers por coluna

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 3 — Pandas Avançado: GroupBy e Agregações

**Conteúdo:**
- `.groupby()`: agrupando e agregando
- Múltiplas funções de agregação: `.agg()`
- Pivot tables com `pd.pivot_table()`
- `.crosstab()`: tabelas de frequência
- `.merge()`: combinando DataFrames (como SQL JOIN)
- `.concat()`: empilhando DataFrames
- Window functions: `.rolling()`, `.expanding()`
- Ranking: `.rank()`
- Percentis e quantis
- Applymap e transform

**Exercícios práticos (escolha um):**
1. Análise de vendas por categoria/região/período com GroupBy e pivot table
2. Combinar dados de múltiplas fontes com merge: vendas + clientes + produtos
3. Análise de série temporal simples: média móvel de vendas com rolling window

**Recursos:**
- [Pandas - GroupBy](https://pandas.pydata.org/docs/user_guide/groupby.html)
- [Pandas - Merge](https://pandas.pydata.org/docs/user_guide/merging.html)

**Tarefas de casa (escolha uma ou mais):**
1. Análise completa de dataset do Olist: faturamento por estado, categoria mais vendida, ticket médio por mês
2. Criar relatório automático: GroupBy + formatação → exportar para Excel formatado com pandas
3. Implementar cohort analysis: clientes por mês de primeira compra × retenção mensal
4. Análise de RFM (Recência, Frequência, Monetário) para segmentar clientes
5. Criar ranking dinâmico: top 10 produtos por mês com variação vs mês anterior

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 4 — Visualização com Matplotlib e Seaborn

**Conteúdo:**
- Matplotlib: estrutura de figuras, axes, plots
- Gráficos básicos: line, bar, scatter, histogram, pie
- Customizando: títulos, labels, cores, fontes, legendas
- Subplots: múltiplos gráficos em uma figura
- Seaborn: visualizações estatísticas simplificadas
- `sns.histplot()`, `sns.boxplot()`, `sns.violinplot()`
- `sns.heatmap()`: matriz de correlação
- `sns.pairplot()`: relações entre variáveis
- `sns.scatterplot()` com hue e size
- Paletas de cores e acessibilidade

**Exercícios práticos (escolha um):**
1. Dashboard analítico com matplotlib: 4 gráficos em subplot (distribuição, temporal, comparativo, correlação)
2. Análise exploratória visual de dataset de saúde: distribuições, outliers, correlações com Seaborn
3. Série temporal de vendas com tendência e sazonalidade destacadas

**Recursos:**
- [Matplotlib Docs](https://matplotlib.org/stable/tutorials/)
- [Seaborn Docs](https://seaborn.pydata.org/)
- [Python Graph Gallery](https://python-graph-gallery.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar infográfico completo de análise: 6+ visualizações contando uma história coerente
2. Replicar um gráfico profissional do Financial Times ou The Economist usando Matplotlib
3. Criar galeria de gráficos: 10 tipos diferentes com o mesmo dataset
4. Criar visualização de heatmap de correlação interpretada (explicar cada correlação forte)
5. Fazer estudo de acessibilidade: refazer gráficos com paletas amigáveis a daltônicos

**Tempo:** 4h (1h teoria + 2h prática + 1h peer review)

---

### Aula 5 — Visualização Interativa com Plotly

**Conteúdo:**
- Plotly Express: gráficos interativos com uma linha
- Gráficos básicos: `px.line()`, `px.bar()`, `px.scatter()`
- Mapas com Plotly: `px.choropleth()`, `px.scatter_geo()`
- Plotly Graph Objects: controle fino
- Subplots com `make_subplots()`
- Exportando para HTML e imagem
- Dash: framework de dashboards em Python
- Layout básico do Dash: `app.layout`
- Callbacks: interatividade com `@app.callback`
- Deployando Dash no Render

**Exercícios práticos (escolha um):**
1. Dashboard Dash interativo de vendas: gráficos com filtros de período, região e categoria
2. Mapa coroplético do Brasil com dados por estado (PIB, população, IDH)
3. App Dash de análise de portfólio: input de ações, gráfico de evolução e comparativo

**Recursos:**
- [Plotly Docs](https://plotly.com/python/)
- [Dash Docs](https://dash.plotly.com/)
- [Plotly Express Tutorial](https://plotly.com/python/plotly-express/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar dashboard Dash completo e deployar no Render
2. Mapa interativo do Brasil: dados por município (saúde, educação, economia)
3. Dashboard de monitoramento em tempo real: usar callback com interval para atualizar dados
4. Criar app de comparação de países: input de país → gráficos de indicadores
5. Recriar um dashboard do Power BI usando Dash + Plotly

**Tempo:** 4h (1h teoria + 2h prática + 1h deploy)

---

### Aula 6 — Estatística para Data Science

**Conteúdo:**
- Estatística descritiva: média, mediana, moda, desvio padrão
- Distribuições: normal, binomial, Poisson
- Correlação: Pearson, Spearman
- Causalidade vs Correlação (cuidados)
- Hipóteses: nula e alternativa
- Teste t, ANOVA, qui-quadrado (introdução)
- p-value: como interpretar
- Intervalos de confiança
- A/B testing básico
- NumPy: arrays e operações vetorizadas

**Exercícios práticos (escolha um):**
1. Análise estatística completa de dataset: distribuições, outliers, correlações, testes de hipótese
2. Simulação de A/B test: dois grupos, comparar médias, calcular significância estatística
3. Comparar grupos com teste ANOVA: vendas de 4 regiões são estatisticamente diferentes?

**Recursos:**
- [scipy.stats Docs](https://docs.scipy.org/doc/scipy/reference/stats.html)
- [StatQuest - YouTube](https://www.youtube.com/@statquest)
- [Seeing Theory](https://seeing-theory.brown.edu/) — probabilidade visual

**Tarefas de casa (escolha uma ou mais):**
1. Analisar distribuição de preços de imóveis: verificar normalidade, outliers, correlações com características
2. Conduzir A/B test simulado: dois designs de landing page, determinar qual converte mais
3. Análise de correlação entre múltiplas variáveis econômicas de países com heatmap
4. Criar explicação visual de p-value com simulações Python
5. Aplicar teste qui-quadrado para verificar independência entre variáveis categóricas

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 7 — Análise de Séries Temporais

**Conteúdo:**
- O que é série temporal e características
- Componentes: tendência, sazonalidade, ciclicidade, ruído
- Decomposição com `seasonal_decompose`
- Resampling: `resample()` no pandas
- Autocorrelação: ACF e PACF plots
- Rolling statistics: média móvel, desvio padrão móvel
- Forecasting simples: média, naive, exponencial smoothing
- Prophet (Facebook): forecasting com sazonalidade múltipla
- Avaliação de forecast: MAE, RMSE, MAPE
- Aplicações: vendas, tráfego, demanda, preços

**Exercícios práticos (escolha um):**
1. Decompor série temporal de vendas: identificar tendência e sazonalidade, prever próximos 3 meses com Prophet
2. Análise de tráfego web: resampling semanal, médias móveis, forecast de acessos
3. Previsão de temperatura: dados históricos → forecast com Prophet → comparar com naive baseline

**Recursos:**
- [Prophet Docs](https://facebook.github.io/prophet/)
- [statsmodels Docs](https://www.statsmodels.org/)
- [Forecasting Principles](https://otexts.com/fpp3/)

**Tarefas de casa (escolha uma ou mais):**
1. Forecast de vendas mensais de produto real com Prophet (12 meses)
2. Detectar anomalias em série temporal: picos e quedas fora do padrão
3. Comparar modelos de forecast: média móvel vs exponencial smoothing vs Prophet
4. Analisar correlação cruzada entre duas séries temporais (ex: temperatura × consumo de energia)
5. Criar dashboard de monitoramento de série temporal com Plotly Dash

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 8 — Projeto: Análise Exploratória Completa

**Conteúdo:**
- Revisão de todos os conceitos
- Escolhendo e entendendo o dataset
- EDA sistemático: shape, tipos, nulos, distribuições, correlações
- Visualizações narrativas: contando uma história com dados
- Insights e recomendações
- Apresentação profissional do notebook
- Reprodutibilidade: requirements.txt, seeds aleatórias
- Exportando relatório como HTML ou PDF

**Exercício prático:**
1. EDA completo de dataset real: limpeza, análise estatística, visualizações, insights e recomendações

**Sugestões de dataset:**
1. Dados do ENEM (educação brasileira)
2. Dados do Olist (e-commerce brasileiro)
3. COVID-19 (Our World in Data)
4. Dados climáticos do INMET
5. Mercado imobiliário de uma cidade

**Desafio extra:**
1. Criar dashboard Dash interativo como complemento do EDA
2. Publicar notebook no Kaggle com write-up profissional
3. Fazer forecasting da principal métrica do dataset

**Tarefas de casa (escolha uma ou mais):**
1. Publicar análise no Kaggle ou GitHub com README detalhado
2. Escrever post no LinkedIn ou Medium com os principais insights
3. Criar slide deck de 5 slides com os achados para apresentar ao "cliente"
4. Receber feedback de colega e iterar no notebook
5. Transformar análise em relatório PDF profissional com nbconvert

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Notebook Jupyter com EDA completo
2. Limpeza de dados documentada
3. Mínimo 5 visualizações (matplotlib/seaborn/plotly)
4. Análise estatística com interpretações
5. Insights e recomendações
6. Repositório GitHub organizado
7. README com contexto e principais achados

---

## Próximo módulo

→ [Data Analytics 2](modulos/data-analytics-2.md)

---

#modulo #dataanalytics #pandas #numpy #matplotlib #seaborn #plotly #eda #datascience
