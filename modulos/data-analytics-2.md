# Data Analytics 2 — Módulo 6

> Machine Learning aplicado e storytelling com dados.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Posição na trilha:** [Data Science#fase 2 Especializacao Circular](cursos/data-science#fase-2--especializacao-circular.md)

---
## Aulas
### Aula 1 — Introdução ao Machine Learning

**Conteúdo:**
- O que é Machine Learning e como funciona
- Tipos de aprendizado: supervisionado, não supervisionado, por reforço
- Terminologia: features, target, training set, test set
- Overfitting e underfitting: bias-variance tradeoff
- Scikit-learn: o ecossistema
- Pipeline de ML: problema → dados → modelo → avaliação → deploy
- Train/test split: `train_test_split()`
- Pré-processamento: `StandardScaler`, `MinMaxScaler`
- Cross-validation: `cross_val_score()`
- Conceito de hiperparâmetros

**Exercícios práticos (escolha um):**
1. Primeiro modelo: prever preço de imóvel com regressão linear, avaliar com MSE e R²
2. Classificar emails como spam/não-spam com dados fictícios, calcular accuracy e confusion matrix
3. Pipeline completo: carregar dataset sklearn (iris), split, treinar, avaliar, visualizar

**Recursos:**
- [Scikit-learn Docs](https://scikit-learn.org/stable/user_guide.html)
- [Kaggle - ML Intro](https://www.kaggle.com/learn/intro-to-machine-learning)
- [Hands-On ML - Livro](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)

**Tarefas de casa (escolha uma ou mais):**
1. Treinar e avaliar 3 modelos diferentes no mesmo dataset, comparar métricas
2. Pesquisar e documentar os 10 algoritmos de ML mais usados no mercado
3. Criar notebook explorando o efeito de diferentes tamanhos de treino/teste
4. Implementar cross-validation em 3 modelos e comparar com simples train/test split
5. Ler artigo sobre bias-variance tradeoff e criar visualização explicando o conceito

**Tempo:** 4h (1h teoria + 2h prática + 1h discussão)

---

### Aula 2 — Regressão

**Conteúdo:**
- Regressão Linear Simples e Múltipla
- Interpretação dos coeficientes
- Métricas de regressão: MAE, MSE, RMSE, R²
- Regressão Polinomial: capturando não-linearidades
- Regularização: Ridge (L2) e Lasso (L1)
- ElasticNet: combinando Ridge e Lasso
- Feature importance: quais variáveis mais importam
- Visualizando residuals: diagnóstico do modelo
- Predição em novos dados
- Quando regressão é adequada

**Exercícios práticos (escolha um):**
1. Prever salário baseado em anos de experiência e nível de educação
2. Prever vendas de produto baseado em investimento em publicidade por canal
3. Prever consumo de energia de imóvel baseado em características (área, ocupantes, estação)

**Recursos:**
- [Scikit-learn - Regression](https://scikit-learn.org/stable/supervised_learning.html#regression)
- [StatQuest - Linear Regression](https://www.youtube.com/@statquest)

**Tarefas de casa (escolha uma ou mais):**
1. Análise de regressão de preços de imóveis: todas as etapas com interpretação dos coeficientes
2. Comparar Ridge vs Lasso vs ElasticNet no mesmo dataset: qual regularização funciona melhor?
3. Criar visualização de learning curve: modelo melhor com mais dados?
4. Implementar regressão polinomial e visualizar overfitting com graus altos
5. Prever preço de ações do dia seguinte com regressão linear (avaliar limitações)

**Tempo:** 4h (1h teoria + 2h prática + 1h interpretação)

---

### Aula 3 — Classificação

**Conteúdo:**
- Regressão Logística: classificação binária
- Métricas de classificação: accuracy, precision, recall, F1-score
- Confusion matrix: interpretando
- ROC curve e AUC
- Quando usar precision vs recall
- Árvore de Decisão: visual e interpretável
- Random Forest: ensemble de árvores
- Gradient Boosting: XGBoost, LightGBM
- Problemas de classes desbalanceadas: SMOTE, class_weight
- Seleção de modelo: `GridSearchCV`

**Exercícios práticos (escolha um):**
1. Classificar clientes como churners ou não com Random Forest, otimizar threshold
2. Detector de fraude: dataset desbalanceado, usar SMOTE e avaliar com F1
3. Diagnóstico médico: classificar pacientes com ou sem doença, minimizar falsos negativos

**Recursos:**
- [Scikit-learn - Classification](https://scikit-learn.org/stable/supervised_learning.html)
- [Imbalanced-learn Docs](https://imbalanced-learn.org/)
- [XGBoost Docs](https://xgboost.readthedocs.io/)

**Tarefas de casa (escolha uma ou mais):**
1. Comparar 5 algoritmos de classificação no mesmo dataset de churn: qual performa melhor?
2. Tuning de hiperparâmetros com GridSearchCV + RandomizedSearchCV no Random Forest
3. Análise de feature importance: quais variáveis mais influenciam a classificação?
4. Criar visualização comparativa de ROC curves de múltiplos modelos
5. Implementar Early Stopping no XGBoost e analisar número ideal de estimadores

**Tempo:** 4h (1h teoria + 2h prática + 1h comparação de modelos)

---

### Aula 4 — Clusterização e Aprendizado Não Supervisionado

**Conteúdo:**
- O que é aprendizado não supervisionado
- K-Means: algoritmo e limitações
- Escolhendo K: Elbow Method e Silhouette Score
- DBSCAN: clusters de forma arbitrária
- Hierarchical clustering: dendrograma
- PCA (Principal Component Analysis): redução de dimensionalidade
- t-SNE e UMAP: visualização de dados de alta dimensão
- Aplicações: segmentação de clientes, anomaly detection, compressão
- Avaliação de clusters (sem labels)
- Interpretação dos clusters

**Exercícios práticos (escolha um):**
1. Segmentação de clientes por RFM com K-Means: identificar perfis e nomear grupos
2. Detectar anomalias em transações financeiras com Isolation Forest
3. Visualizar dataset de alta dimensão com PCA e t-SNE, colorir por cluster

**Recursos:**
- [Scikit-learn - Clustering](https://scikit-learn.org/stable/modules/clustering.html)
- [Visualizing DBSCAN](https://www.naftaliharris.com/blog/visualizing-dbscan-clustering/)

**Tarefas de casa (escolha uma ou mais):**
1. Segmentação de países por indicadores socioeconômicos: identificar e nomear grupos
2. Detectar outliers em dataset de manufatura (sensores de equipamentos)
3. Aplicar PCA para reduzir dimensionalidade de dataset de texto (bag of words)
4. Comparar K-Means vs DBSCAN no mesmo dataset: qual faz mais sentido de negócio?
5. Criar personas de produto: usar clustering em dados de comportamento de usuários

**Tempo:** 4h (1h teoria + 2h prática + 1h interpretação)

---

### Aula 5 — Processamento de Linguagem Natural (NLP) Básico

**Conteúdo:**
- O que é NLP e aplicações
- Pré-processamento de texto: lowercasing, remoção de stopwords, pontuação
- Tokenização
- Stemming vs Lemmatização
- Bag of Words: `CountVectorizer`
- TF-IDF: `TfidfVectorizer`
- Análise de sentimentos: regras vs ML
- VADER: análise de sentimentos em inglês e português
- Classificação de textos com ML
- Word embeddings: introdução ao Word2Vec/BERT (conceitual)

**Exercícios práticos (escolha um):**
1. Análise de sentimentos de reviews de produtos: positivo/negativo/neutro com VADER
2. Classificador de spam via NLP: bag of words + Naive Bayes
3. Topic modeling básico: identificar tópicos em corpus de notícias com LDA

**Recursos:**
- [NLTK Docs](https://www.nltk.org/)
- [spaCy Docs](https://spacy.io/)
- [Hugging Face](https://huggingface.co/)

**Tarefas de casa (escolha uma ou mais):**
1. Analisar sentimentos de tweets sobre tema de interesse com VADER
2. Criar classificador de notícias por categoria com TF-IDF + Logistic Regression
3. Construir extrator de entidades: identificar pessoas, lugares e organizações em texto
4. Analisar feedback de clientes: identificar temas recorrentes com topic modeling
5. Explorar modelos do Hugging Face: usar modelo pré-treinado para classificação de texto

**Tempo:** 4h (1h teoria + 2h prática + 1h exploração)

---

### Aula 6 — Pipelines e MLflow

**Conteúdo:**
- Scikit-learn Pipeline: encadeando transformações e modelos
- `ColumnTransformer`: transformações por tipo de coluna
- `FeatureUnion`: combinando features
- Serialização de modelos: `joblib` e `pickle`
- MLflow: rastreamento de experimentos
- Logging de parâmetros, métricas e artefatos
- MLflow UI: comparando experimentos
- Model Registry: versionando modelos
- Reprodutibilidade: seeds, requirements, data versioning
- Boas práticas de MLOps

**Exercícios práticos (escolha um):**
1. Criar pipeline scikit-learn completo: pré-processamento + modelo + avaliação, serializar e carregar
2. Usar MLflow para comparar 3 algoritmos no mesmo dataset: logar métricas e visualizar na UI
3. Criar Model Registry: versionar modelo em produção e staging

**Recursos:**
- [MLflow Docs](https://mlflow.org/docs/latest/)
- [Scikit-learn Pipeline](https://scikit-learn.org/stable/modules/pipeline.html)

**Tarefas de casa (escolha uma ou mais):**
1. Refatorar projeto ML anterior usando Pipeline e MLflow para rastreamento
2. Criar experimento MLflow com 10+ runs variando hiperparâmetros, identificar melhor
3. Configurar MLflow no Render ou servidor AWS
4. Implementar automated ML básico: testar múltiplos algoritmos e selecionar melhor automaticamente
5. Criar script de retraining: retreinar modelo com novos dados e registrar no MLflow

**Tempo:** 4h (1h teoria + 2h prática + 1h MLOps)

---

### Aula 7 — Deploy de Modelos de ML

**Conteúdo:**
- Por que e como colocar modelo em produção
- Flask/FastAPI: criando API de predição
- Input validation: garantindo dados corretos
- Batch prediction vs Real-time prediction
- Docker: containerizando modelo
- Deploy na AWS: Lambda (serverless) ou EC2
- AWS SageMaker Endpoints (introdução)
- Monitoramento de modelo em produção: data drift, performance
- A/B testing de modelos
- Documentando API de ML com Swagger

**Exercícios práticos (escolha um):**
1. API FastAPI de predição: receber features via JSON, retornar predição e probabilidade
2. Dockerizar modelo e API, fazer deploy na EC2, testar com Postman
3. Criar Lambda de predição: modelo serializado em Layer, endpoint via API Gateway

**Recursos:**
- [FastAPI Docs](https://fastapi.tiangolo.com/)
- [BentoML - Deploy ML](https://www.bentoml.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Fazer deploy completo de modelo no Render: API FastAPI + modelo serializado
2. Criar sistema de monitoramento: logar predições em banco, detectar drift de distribuição
3. Implementar A/B test de modelos: 50% das requisições vão para modelo A, 50% para B
4. Documentar API de ML no Swagger: tipos de input, output, exemplos, erros
5. Criar script de batch prediction: processar CSV de novos dados e salvar predições

**Tempo:** 4h (1h teoria + 2h prática + 1h deploy ao vivo)

---

### Aula 8 — Projeto Final: Modelo de ML em Produção

**Conteúdo:**
- Revisão de todos os conceitos
- Definindo problema de negócio
- EDA focado no problema
- Feature engineering
- Seleção e treinamento de modelos
- Avaliação e interpretação
- Deploy e apresentação

**Exercício prático:**
1. Pipeline completo end-to-end: problema de negócio → dados → EDA → modelo → avaliação → API deployada

**Sugestões de projeto:**
1. Previsão de churn: qual cliente vai cancelar? (classificação)
2. Preço de imóveis: quanto vale este imóvel? (regressão)
3. Detecção de fraude em transações (classificação desbalanceada)
4. Recomendação de filmes/produtos (sistema de recomendação)
5. Previsão de demanda de produto (séries temporais)
6. Análise de sentimentos de reviews de empresa (NLP)

**Desafio extra:**
1. Criar explicabilidade do modelo com SHAP
2. Implementar monitoramento de data drift em produção
3. Criar interface web simples com Streamlit para o modelo

**Tarefas de casa (escolha uma ou mais):**
1. Publicar projeto no GitHub com README profissional e link da API
2. Criar apresentação de 5 slides: problema → solução → métricas → impacto → próximos passos
3. Escrever artigo sobre o projeto no LinkedIn ou Medium
4. Publicar notebook no Kaggle e receber feedback da comunidade
5. Criar dashboard no Power BI com predições do modelo em tempo real

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Notebook com EDA + modelagem documentados
2. Pipeline scikit-learn serializado
3. API de predição deployada
4. Métricas de avaliação interpretadas
5. MLflow ou equivalente para rastreamento
6. README com problema, solução e resultados

---

## Próximo módulo

→ [Projeto Final Data](modulos/projeto-final-data.md)

---

#modulo #machinelearning #ml #sklearn #nlp #deploy #mlops #datascience
