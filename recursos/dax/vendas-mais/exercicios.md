# Exercícios DAX

## Contexto

A **VendaMais Distribuidora** é uma empresa de distribuição de produtos que opera em todo o Brasil. Após anos usando planilhas para acompanhar os resultados, o time comercial decidiu investir em um dashboard no Power BI para ter uma visão mais clara do desempenho das vendas.

O gerente comercial, **Ricardo**, trouxe os seguintes pedidos para a primeira versão do dashboard:

---

### O que a VendaMais quer ver?

**Página 1 — Visão Geral**
- Cartões com os KPIs principais: **Faturamento Total**, **Lucro Bruto**, **Margem %** e **Ticket Médio**
- Gráfico de linhas mostrando a **evolução mensal do faturamento** comparado ao **ano anterior (SPLY)**
- Gráfico de barras com o **faturamento acumulado no ano (YTD)** mês a mês

**Página 2 — Produtos**
- Tabela com o **ranking de produtos** por faturamento
- Gráfico de barras horizontais com os **Top 10 produtos mais vendidos** (por quantidade)
- Cartão com o número de **produtos distintos vendidos**

**Página 3 — Clientes e Vendedores**
- Cartão com o número de **clientes únicos**
- Gráfico de barras com **faturamento por vendedor**
- Gráfico de rosca com o **percentual de vendas canceladas vs. concluídas**

**Página 4 — Análise Temporal**
- Gráfico de linhas com **vendas MTD** (acumulado no mês)
- Gráfico de barras comparando **faturamento por dia da semana** (para entender se fins de semana performam diferente)
- Segmentação por **trimestre** e **ano**

---

> Para construir esses visuais, você vai precisar criar colunas calculadas e medidas DAX. Siga os exercícios abaixo na ordem — as medidas dependem das colunas.

---

## Modelo de Dados

Antes de começar, conecte os CSVs no Power BI e crie os relacionamentos:

- `vendas[id_cliente]` → `clientes[id_cliente]`
- `vendas[id_produto]` → `produtos[id_produto]`
- `vendas[id_vendedor]` → `vendedores[id_vendedor]`
- `vendas[data]` → `calendario[data]`

---

## Colunas Calculadas

### Calendário

> Todas as colunas abaixo devem ser criadas na tabela `calendario`, a partir da coluna `data`.

**1. Ano**
Extraia o ano da data.

**2. Mês (número)**
Extraia o número do mês (1 a 12).

**3. Nome do Mês**
Exiba o nome do mês em português (ex: "Janeiro").
> Dica: use `FORMAT` com a função `SWITCH` ou uma lista de valores.

**4. Trimestre**
Crie uma coluna no formato "Q1", "Q2", "Q3" ou "Q4".

**5. Dia**
Extraia o dia do mês.

**6. Dia da Semana (nome)**
Exiba o nome do dia da semana em português (ex: "Segunda").

**7. Semana do Ano**
Retorne o número da semana no ano (1 a 53).

**8. É Fim de Semana?**
Crie uma coluna booleana que indica se a data cai em sábado ou domingo.

---

### Vendas

> As colunas abaixo devem ser criadas na tabela `vendas`. Use `RELATED` para acessar dados de outras tabelas.

**9. Valor Original**
Calcule o valor bruto da venda antes do desconto: `qtd × preco_unitario`.

**10. Valor Final**
Calcule o valor líquido após o desconto: `valor_original × (1 − desconto)`.

**11. Custo Total**
Calcule o custo total da venda: `qtd × custo_unitario`.

**12. Lucro**
Calcule o lucro da venda: `valor_final − custo_total`.

---

## Medidas

> Crie as medidas abaixo em uma tabela separada chamada `_Medidas`.

### Básicas

**1. Total de Vendas**
Some o `valor_final` apenas das vendas com `status_venda = "Concluída"`.

**2. Total de Custo**
Some o `custo_total` apenas das vendas concluídas.

**3. Lucro Bruto**
Calcule a diferença entre o Total de Vendas e o Total de Custo.

**4. Margem %**
Calcule o percentual de margem sobre o Total de Vendas. Use `DIVIDE(coluna1, coluna2)` para evitar erro de divisão por zero.

**5. Quantidade Vendida**
Some a quantidade de itens em vendas concluídas.

**6. Número de Vendas**
Conte o número de transações concluídas.

**7. Ticket Médio**
Calcule o valor médio por venda concluída.

---

### Clientes e Produtos

**8. Clientes Únicos**
Conte o número de clientes distintos que realizaron ao menos uma compra concluída.

**9. Produtos Vendidos**
Conte o número de produtos distintos presentes em vendas concluídas.

**10. Vendas Canceladas %**
Calcule o percentual de vendas canceladas em relação ao total de transações.

**11. Ranking de Produtos**
Classifique os produtos pelo Total de Vendas usando `RANKX`.

---

### Inteligência de Tempo

> Para os exercícios abaixo, certifique-se de que a tabela `calendario` está marcada como **Tabela de Datas** no Power BI.

**12. Vendas Acumuladas no Ano (YTD)**
Calcule o total de vendas acumulado desde o início do ano até a data selecionada.
> Dica: use `TOTALYTD`.

**13. Vendas no Mesmo Período do Ano Anterior (SPLY)**
Retorne o Total de Vendas do mesmo período no ano anterior.
> Dica: use `SAMEPERIODLASTYEAR`.

**14. Crescimento Ano a Ano (%)**
Calcule a variação percentual entre o Total de Vendas atual e o SPLY.

**15. Vendas Acumuladas no Mês (MTD)**
Calcule o total de vendas acumulado desde o início do mês.

**16. Vendas nos Últimos 30 Dias**
Retorne o Total de Vendas dos últimos 30 dias a partir da data máxima disponível.
> Dica: use `DATESINPERIOD` e `MAX(calendario[data])`.
