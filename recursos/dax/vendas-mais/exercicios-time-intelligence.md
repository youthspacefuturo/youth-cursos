# Exercícios DAX — Inteligência de Tempo

## Contexto

Após a primeira versão do dashboard, o gerente Ricardo pediu uma segunda análise: **comparar os resultados do período atual com períodos anteriores**. Ele quer saber se o time está crescendo, estagnado ou em queda — e em qual ritmo isso acontece.

Para isso, você vai criar medidas que comparam dados entre períodos diferentes usando funções de Inteligência de Tempo do DAX.

---

## Modelo de Dados

As tabelas e relacionamentos são os mesmos da aula anterior:

- `vendas[id_cliente]` → `clientes[id_cliente]`
- `vendas[id_produto]` → `produtos[id_produto]`
- `vendas[id_vendedor]` → `vendedores[id_vendedor]`
- `vendas[data]` → `calendario[data]`

Colunas já criadas na tabela `calendario`: `Ano`, `Mes`, `Nome do Mes`, `Trimestre`, `Dia`, `Dia da Semana`, `Semana do Ano`, `Fim de Semana`

Colunas já criadas na tabela `vendas`: `Valor Original`, `Valor Final`, `Custo Total`, `Lucro`

Medidas já criadas: `Total de Vendas`, `Total de Custo`, `Lucro Bruto`, `Margem %`, `Quantidade Vendida`, `Numero de Vendas`, `Ticket Medio`, `Clientes Unicos`, `Produtos Vendidos`, `Vendas Canceladas %`, `Vendas YTD`, `Vendas SPLY`, `Crescimento YoY %`, `Vendas MTD`, `Vendas Ultimos 30 Dias`

---

## Parte 1 — Crescimento Periódico

### 1. Vendas no Mês Anterior (PM)
Retorne o **Total de Vendas do mês anterior** ao contexto de filtro atual.
> Dica: use `CALCULATE` com `PREVIOUSMONTH(calendario[data])`.

### 2. Crescimento Mensal (MoM %)
Calcule a **variação percentual** entre o Total de Vendas atual e o valor do mês anterior.
> Dica: `(Total de Vendas - PM) / PM`

### 3. Vendas no Trimestre Anterior (PQ)
Retorne o **Total de Vendas do trimestre anterior**.
> Dica: use `PREVIOUSQUARTER`.

### 4. Crescimento Trimestral (QoQ %)
Calcule a **variação percentual** entre o trimestre atual e o anterior.

### 5. Vendas no Mesmo Mês do Ano Anterior (SPLY) — via DATESBETWEEN
Reconstrua a lógica do SPLY, mas agora usando `DATESBETWEEN` e `DATEADD` em vez de `SAMEPERIODLASTYEAR`. O resultado deve ser o mesmo: Total de Vendas do mesmo período no ano anterior.
> Dica: use `DATESBETWEEN` com `DATEADD(calendario[data], -1, YEAR)`.

### 6. Crescimento no Mês Corrente vs. Mês Anterior do Ano Anterior
Imagine que hoje é junho de 2024. Compare o total de vendas de **junho de 2024** com o total de vendas de **maio de 2023** (mês anterior ao SPLY). Chame essa medida de `Vendas Mes Anterior Ano Anterior`.
> Dica: combine `PREVIOUSMONTH` com `SAMEPERIODLASTYEAR`.

---

## Parte 2 — Acumulados e Médias Móveis

### 7. Vendas Acumuladas no Trimestre (QTD)
Calcule o total de vendas **acumulado desde o início do trimestre** até a data atual do filtro.
> Dica: use `TOTALQTD`.

### 8. QTD do Ano Anterior
Retorne o valor de **QTD do mesmo trimestre do ano anterior**.
> Dica: combine `TOTALQTD` com `SAMEPERIODLASTYEAR`.

### 9. Crescimento do QTD (QoQ do Acumulado)
Calcule a variação percentual entre o QTD atual e o QTD do ano anterior.

### 10. Média Móvel de 3 Meses (3M MA)
Calcule a **média do Total de Vendas dos últimos 3 meses**, incluindo o mês atual.
> Dica: use `CALCULATE` com `DATESINPERIOD` e `AVERAGEX`.

### 11. Média Móvel de 6 Meses (6M MA)
Calcule a **média do Total de Vendas dos últimos 6 meses**, incluindo o mês atual.

### 12. Vendas do Último Trimestre Fechado
Retorne o Total de Vendas do **trimestre anterior completo** (sem incluir o trimestre atual em andamento).
> Dica: use `PREVIOUSQUARTER` com `TOTALQTD`.

---

## Parte 3 — Períodos Paralelos

### 13. Vendas de 2 Períodos Atrás (2 Meses Antes)
Retorne o Total de Vendas de **2 meses atrás** em relação ao contexto atual.
> Dica: use `PARALLELPERIOD` ou `DATEADD` com `-2` meses.

### 14. Vendas do Mesmo Trimestre Há 2 Anos
Retorne o Total de Vendas do **mesmo trimestre, 2 anos atrás**.
> Dica: use `PARALLELPERIOD` com `-2` anos.

### 15. Crescimento em 12 Meses (vs. Mesmo Mês 2 Anos Antes)
Calcule a variação percentual entre o Total de Vendas atual e o Total de Vendas de **2 anos atrás no mesmo mês**.
> Dica: combine `PARALLELPERIOD` com `SAMEPERIODLASTYEAR` duas vezes.

---

## Parte 4 — Cenários Completos

### 16. Dashboard Resumo de Crescimento
Construa as seguintes medidas para um **cartão de resumo de crescimento**:

| Medida | O que calcula |
|---|---|
| `Crescimento MoM %` | Variação vs. mês anterior |
| `Crescimento QoQ %` | Variação vs. trimestre anterior |
| `Crescimento YoY %` | Variação vs. mesmo período do ano anterior |
| `Crescimento YoY 2 Anos %` | Variação vs. 2 anos atrás |

Use `DIVIDE` em todas para evitar divisão por zero. Formate como **percentual**.

### 17. Tabela de Análise Período a Período
Usando uma matriz no Power BI com:
- **Linhas:** `calendario[Trimestre]`
- **Colunas:** `calendario[Ano]`
- **Valores:** as medidas abaixo

| Medida | O que calcula |
|---|---|
| `Total de Vendas` | Faturamento do período |
| `Vendas SPLY` | Faturamento do mesmo período no ano anterior |
| `Crescimento YoY %` | Variação percentual |
| `Crescimento QoQ %` | Variação vs. trimestre anterior |
| `Vendas QTD` | Acumulado no trimestre |
| `Vendas QTD Ano Anterior` | Acumulado no mesmo trimestre do ano anterior |

> Note que o QoQ % só faz sentido ao comparar linhas de **trimestres diferentes do mesmo ano**. QoQ não compara anos diferentes.

### 18. Vendas por Semana com Média Móvel
Em um gráfico de linhas com `calendario[Semana do Ano]` como eixo:
- Linha 1: `Total de Vendas` por semana
- Linha 2: `3M MA` (média móvel de 3 meses adaptada para semanas)

> Dica: para média móvel semanal, use `DATESINPERIOD` com `-21` dias (aproximadamente 3 meses em dias) dentro de `AVERAGEX`.

### 19. Classificação de Crescimento
Crie uma coluna calculada na tabela `_Medidas` (ou uma medida isolada) que classifique o crescimento YoY:

| Crescimento YoY % | Classificação |
|---|---|
| > 10% | "Crescimento Forte" |
| 0% a 10% | "Leve Crescimento" |
| -10% a 0% | "Leve Queda" |
| < -10% | "Queda Significativa" |

> Dica: use `SWITCH` com `TRUE()` para condições de range.
> Observação: se não houver crescimento no período (primeiro ano), exiba "Sem Histórico".

### 20. Receita Mensal com Destaque de Crescimento
Crie uma medida chamada `Destaque Crescimento` que retorne:
- `"↑ Alta"` se `Crescimento YoY % > 0`
- `"↓ Baixa"` se `Crescimento YoY % < 0`
- `"→ Estável"` se `Crescimento YoY % = 0`

Use essa medida em um visual de **tabela** ao lado do faturamento mensal para facilitar a leitura visual.
> Dica: use `IF` encadeado ou `SWITCH` com `TRUE()`.

---

## Parte 5 — Desafio Final

### 21. Análise Completa de Desempenho por Trimestre
Crie um relatório com os seguintes elementos:

**Visual 1 — Matriz Trimestral**
- Linhas: `calendario[Trimestre]`
- Colunas: `calendario[Ano]`
- Valores:
  - `Total de Vendas`
  - `Vendas SPLY`
  - `Crescimento YoY %` (formatado em %)
  - `Vendas QTD`
  - `QTD Ano Anterior`

**Visual 2 — Gráfico de Linhas Mensal**
- Eixo X: `calendario[Mes]`
- Linha 1: `Total de Vendas` de 2024
- Linha 2: `Vendas SPLY` (2023)
- Linha 3: `3M MA`

**Visual 3 — Cartões de Resumo (por Trimestre filtrado)**
- `Total de Vendas` do trimestre atual
- `Vendas SPLY` do mesmo trimestre do ano anterior
- `Crescimento YoY %`
- `Crescimento QoQ %`

**Visual 4 — Tabela de Crescimento por Categoria**
- Linhas: `produtos[categoria]`
- Colunas: cada uma das medidas de crescimento (MoM, QoQ, YoY, 3M MA)
- Destaque com `Destaque Crescimento`

> Este exercício combina tudo que foi aprendido nesta aula. Tente montar sem consultar as resoluções primeiro!
