# Resoluções — Inteligência de Tempo

---

## Parte 1 — Crescimento Periódico

### 1. Vendas no Mês Anterior (PM)
```dax
Vendas PM =
CALCULATE(
    [Total de Vendas],
    PREVIOUSMONTH(calendario[data])
)
```

### 2. Crescimento Mensal (MoM %)
```dax
Crescimento MoM % =
DIVIDE(
    [Total de Vendas] - [Vendas PM],
    [Vendas PM]
)
```

### 3. Vendas no Trimestre Anterior (PQ)
```dax
Vendas PQ =
CALCULATE(
    [Total de Vendas],
    PREVIOUSQUARTER(calendario[data])
)
```

### 4. Crescimento Trimestral (QoQ %)
```dax
Crescimento QoQ % =
DIVIDE(
    [Total de Vendas] - [Vendas PQ],
    [Vendas PQ]
)
```

### 5. SPLY via DATESBETWEEN + DATEADD
```dax
Vendas SPLY (DATESBETWEEN) =
CALCULATE(
    [Total de Vendas],
    DATESBETWEEN(
        calendario[data],
        DATEADD(calendario[data], -1, YEAR),
        DATEADD(calendario[data], -1, YEAR)
    )
)
```
> A forma mais simples é `SAMEPERIODLASTYEAR`, mas `DATESBETWEEN + DATEADD` é útil para entender como construir lógicas mais flexíveis.

### 6. Vendas do Mês Anterior ao SPLY
```dax
Vendas Mes Anterior Ano Anterior =
CALCULATE(
    [Vendas PM],
    SAMEPERIODLASTYEAR(calendario[data])
)
```

---

## Parte 2 — Acumulados e Médias Móveis

### 7. Vendas Acumuladas no Trimestre (QTD)
```dax
Vendas QTD =
TOTALQTD(
    [Total de Vendas],
    calendario[data]
)
```

### 8. QTD do Ano Anterior
```dax
Vendas QTD Ano Anterior =
CALCULATE(
    [Vendas QTD],
    SAMEPERIODLASTYEAR(calendario[data])
)
```

### 9. Crescimento do QTD (QoQ do Acumulado)
```dax
Crescimento QTD % =
DIVIDE(
    [Vendas QTD] - [Vendas QTD Ano Anterior],
    [Vendas QTD Ano Anterior]
)
```

### 10. Média Móvel de 3 Meses (3M MA)
```dax
Media Movel 3M =
CALCULATE(
    AVERAGEX(
        DATESINPERIOD(
            calendario[data],
            MAX(calendario[data]),
            -3,
            MONTH
        ),
        [Total de Vendas]
    )
)
```

### 11. Média Móvel de 6 Meses (6M MA)
```dax
Media Movel 6M =
CALCULATE(
    AVERAGEX(
        DATESINPERIOD(
            calendario[data],
            MAX(calendario[data]),
            -6,
            MONTH
        ),
        [Total de Vendas]
    )
)
```

### 12. Último Trimestre Fechado
```dax
Vendas Ultimo Trimestre Fechado =
CALCULATE(
    [Vendas QTD],
    PREVIOUSQUARTER(calendario[data])
)
```

---

## Parte 3 — Períodos Paralelos

### 13. Vendas de 2 Meses Antes
```dax
Vendas 2 Meses Antes =
CALCULATE(
    [Total de Vendas],
    DATEADD(calendario[data], -2, MONTH)
)
```
> Ou com `PARALLELPERIOD`:
```dax
Vendas 2 Meses Antes =
CALCULATE(
    [Total de Vendas],
    PARALLELPERIOD(calendario[data], -2, MONTH)
)
```

### 14. Mesmo Trimestre Há 2 Anos
```dax
Vendas Trimestre 2 Anos Antes =
CALCULATE(
    [Total de Vendas],
    PARALLELPERIOD(calendario[data], -2, YEAR)
)
```

### 15. Crescimento vs. 2 Anos Antes
```dax
Crescimento vs 2 Anos Antes =
DIVIDE(
    [Total de Vendas] - [Vendas Trimestre 2 Anos Antes],
    [Vendas Trimestre 2 Anos Antes]
)
```

---

## Parte 4 — Cenários Completos

### 16. Dashboard Resumo de Crescimento

```dax
Crescimento MoM % =
DIVIDE(
    [Total de Vendas] - [Vendas PM],
    [Vendas PM]
)

Crescimento QoQ % =
DIVIDE(
    [Total de Vendas] - [Vendas PQ],
    [Vendas PQ]
)

Crescimento YoY % =
DIVIDE(
    [Total de Vendas] - [Vendas SPLY],
    [Vendas SPLY]
)

Crescimento vs 2 Anos % =
DIVIDE(
    [Total de Vendas] - [Vendas Trimestre 2 Anos Antes],
    [Vendas Trimestre 2 Anos Antes]
)
```

### 17. Tabela de Análise Período a Período

Todas as medidas já foram criadas nos exercícios anteriores. Para o relatório, arraste:
- `calendario[Trimestre]` → Linhas
- `calendario[Ano]` → Colunas
- `Total de Vendas`, `Vendas SPLY`, `Crescimento YoY %`, `Vendas QTD`, `Vendas QTD Ano Anterior` → Valores

Para QoQ % na matriz, note que o valor será `BLANK` quando comparado entre anos diferentes — isso é esperado, pois QoQ compara períodos dentro do mesmo ano. Para análise cross-year, use YoY.

### 18. Média Móvel Semanal

```dax
Media Movel 3M Semanal =
CALCULATE(
    AVERAGEX(
        DATESINPERIOD(
            calendario[data],
            MAX(calendario[data]),
            -21,
            DAY
        ),
        [Total de Vendas]
    )
)
```
> `-21` dias é aproximadamente 3 meses. Ajuste para `-28` dias (4 semanas) se quiser precisão semanal.

### 19. Classificação de Crescimento

```dax
Classificacao Crescimento =
IF(
    ISBLANK([Crescimento YoY %]),
    "Sem Histórico",
    SWITCH(
        TRUE(),
        [Crescimento YoY %] > 0.10, "Crescimento Forte",
        [Crescimento YoY %] > 0,    "Leve Crescimento",
        [Crescimento YoY %] > -0.10, "Leve Queda",
        "Queda Significativa"
    )
)
```

### 20. Destaque de Crescimento

```dax
Destaque Crescimento =
SWITCH(
    TRUE(),
    [Crescimento YoY %] > 0,  "↑ Alta",
    [Crescimento YoY %] < 0,  "↓ Baixa",
    "→ Estável"
)
```

---

## Parte 5 — Resumo de Todas as Medidas

```dax
-- Crescimento Periódico
Vendas PM = CALCULATE([Total de Vendas], PREVIOUSMONTH(calendario[data]))
Vendas PQ = CALCULATE([Total de Vendas], PREVIOUSQUARTER(calendario[data]))

Crescimento MoM % = DIVIDE([Total de Vendas] - [Vendas PM], [Vendas PM])
Crescimento QoQ % = DIVIDE([Total de Vendas] - [Vendas PQ], [Vendas PQ])

-- Acumulados
Vendas QTD = TOTALQTD([Total de Vendas], calendario[data])
Vendas QTD Ano Anterior = CALCULATE([Vendas QTD], SAMEPERIODLASTYEAR(calendario[data]))
Vendas Ultimo Trimestre Fechado = CALCULATE([Vendas QTD], PREVIOUSQUARTER(calendario[data]))

-- Médias Móveis
Media Movel 3M =
CALCULATE(
    AVERAGEX(
        DATESINPERIOD(calendario[data], MAX(calendario[data]), -3, MONTH),
        [Total de Vendas]
    )
)

Media Movel 6M =
CALCULATE(
    AVERAGEX(
        DATESINPERIOD(calendario[data], MAX(calendario[data]), -6, MONTH),
        [Total de Vendas]
    )
)

-- Períodos Paralelos
Vendas 2 Meses Antes = CALCULATE([Total de Vendas], DATEADD(calendario[data], -2, MONTH))
Vendas Trimestre 2 Anos Antes = CALCULATE([Total de Vendas], PARALLELPERIOD(calendario[data], -2, YEAR))
Crescimento vs 2 Anos % = DIVIDE([Total de Vendas] - [Vendas Trimestre 2 Anos Antes], [Vendas Trimestre 2 Anos Antes])

-- Classificação e Destaque
Classificacao Crescimento =
IF(
    ISBLANK([Crescimento YoY %]),
    "Sem Histórico",
    SWITCH(
        TRUE(),
        [Crescimento YoY %] > 0.10, "Crescimento Forte",
        [Crescimento YoY %] > 0,    "Leve Crescimento",
        [Crescimento YoY %] > -0.10, "Leve Queda",
        "Queda Significativa"
    )
)

Destaque Crescimento =
SWITCH(
    TRUE(),
    [Crescimento YoY %] > 0, "↑ Alta",
    [Crescimento YoY %] < 0, "↓ Baixa",
    "→ Estável"
)
```
