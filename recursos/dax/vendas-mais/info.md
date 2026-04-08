# VendaMais Distribuidora

> Contexto da empresa fictícia usada nos exercícios de DAX.

## Sobre a Empresa

A **VendaMais Distribuidora** é uma empresa de médio porte do Nordeste brasileiro, especializada na distribuição de produtos de vestuário, calçados, eletrônicos e acessórios para clientes dos segmentos Varejo, Atacado e E-commerce.

## Gestor

**Ricardo** — Gerente Comercial
- Responsável pela análise de resultados e tomada de decisão
- Utiliza o Power BI como ferramenta principal de trabalho
- Precisa monitorar vendas, desempenho de vendedores, comportamento de clientes e tendências de mercado

## Banco de Dados

A base é composta pelas seguintes tabelas:

| Tabela | Descrição |
|--------|-----------|
| `clientes` | Cadastro de clientes (500 registros) |
| `produtos` | Catálogo de produtos (100 registros) |
| `vendedores` | Equipe de vendas (20 registros) |
| `vendas` | Transações realizadas (20.000 registros) |
| `calendario` | Tabela calendário扩展 (2 anos) |

## Dados Gerados

O script [Script](script.md) gera CSVs fictícios com dados realistas:
- 500 clientes de 6 cidades do Nordeste
- 100 produtos em 4 categorias
- 20 vendedores por região
- 20.000 vendas ao longo de 2 anos (2023-2024)
- Status: 85% Concluídas, 10% Canceladas, 5% Devolvidas
