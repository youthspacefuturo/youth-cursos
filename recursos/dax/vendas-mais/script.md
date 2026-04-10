# Script — Geração de Dados da VendaMais

> Script Python que gera os CSVs fictícios para os exercícios de DAX.

## Como usar

1. Abra o terminal na pasta onde quer gerar os dados
2. Copie o código abaixo ou use o arquivo `.py` diretamente
3. Execute: `python script.py`
4. Os CSVs serão gerados na subpasta `generated/`

## Código

```python
import pandas as pd
import random
from datetime import datetime, timedelta

# CONFIG
NUM_CLIENTES = 500
NUM_PRODUTOS = 100
NUM_VENDEDORES = 20
NUM_VENDAS = 20000

# LISTAS BASE
cidades = ["Natal", "Recife", "Fortaleza", "Salvador", "João Pessoa", "Maceió"]
segmentos = ["Varejo", "Atacado", "E-commerce"]
categorias = ["Vestuário", "Calçados", "Eletrônicos", "Acessórios"]
primeiros_nomes = [
    "Ana", "Bruno", "Carla", "Diego", "Elisa", "Fernando", "Gabriela", "Hugo",
    "Isabela", "João", "Larissa", "Mateus", "Natália", "Otávio", "Paula", "Rafael",
    "Sabrina", "Thiago", "Valentina", "Yuri"
]
sobrenomes = [
    "Silva", "Souza", "Oliveira", "Santos", "Lima", "Pereira", "Costa", "Almeida",
    "Gomes", "Ribeiro", "Martins", "Araúlo", "Fernandes", "Carvalho", "Barbosa"
]

produtos_por_categoria = {
    "Vestuário": ["Camiseta Básica", "Calça Jeans", "Jaqueta Corta-Vento", "Camisa Social", "Vestido Midi"],
    "Calçados": ["Tênis Casual", "Tênis de Corrida", "Sandália Conforto", "Sapato Social", "Bota Cano Curto"],
    "Eletrônicos": ["Fone Bluetooth", "Smartwatch", "Caixa de Som", "Mouse Sem Fio", "Teclado Mecânico"],
    "Acessórios": ["Mochila Executiva", "Carteira de Couro", "Cinto Ajustável", "Óculos de Sol", "Boné Aba Curva"]
}
linhas_produto = ["Essencial", "Plus", "Premium", "Pro", "Max"]


def gerar_nome_completo():
    nome = f"{random.choice(primeiros_nomes)} {random.choice(sobrenomes)}"
    if random.random() < 0.35:
        nome += f" {random.choice(sobrenomes)}"
    return nome


def gerar_nome_produto(categoria):
    base = random.choice(produtos_por_categoria[categoria])
    linha = random.choice(linhas_produto)
    return f"{base} {linha}"


# CLIENTES
clientes = []
for i in range(1, NUM_CLIENTES + 1):
    clientes.append({
        "id_cliente": i,
        "nome": gerar_nome_completo(),
        "cidade": random.choice(cidades),
        "segmento": random.choice(segmentos)
    })

df_clientes = pd.DataFrame(clientes)

# PRODUTOS
produtos = []
for i in range(1, NUM_PRODUTOS + 1):
    categoria = random.choice(categorias)
    preco = random.randint(20, 500)
    margem = random.uniform(0.3, 0.6)
    custo = round(preco * (1 - margem), 2)
    produtos.append({
        "id_produto": i,
        "nome_produto": gerar_nome_produto(categoria),
        "categoria": categoria,
        "preco_unitario": preco,
        "custo_unitario": custo
    })

df_produtos = pd.DataFrame(produtos)

# VENDEDORES
vendedores = []
for i in range(1, NUM_VENDEDORES + 1):
    vendedores.append({
        "id_vendedor": i,
        "nome_vendedor": gerar_nome_completo(),
        "regiao": random.choice(cidades)
    })

df_vendedores = pd.DataFrame(vendedores)

# CALENDÁRIO — datas dinâmicas de 2023-01-01 até hoje
start_date = datetime(2023, 1, 1)
today = datetime.now()
total_days = (today - start_date).days

dates = []
for i in range(0, total_days + 1):
    d = start_date + timedelta(days=i)
    dates.append({
        "data": d.date(),
    })

df_calendario = pd.DataFrame(dates)

# VENDAS (FATO)
vendas = []
for i in range(1, NUM_VENDAS + 1):
    produto = random.choice(produtos)
    qtd = random.randint(1, 5)
    desconto = random.choice([0, 0, 0, 0.1, 0.2])  # maioria sem desconto
    status = random.choices(
        ["Concluída", "Cancelada", "Devolvida"],
        weights=[0.85, 0.10, 0.05]
    )[0]

    vendas.append({
        "id_venda": i,
        "id_cliente": random.randint(1, NUM_CLIENTES),
        "id_produto": produto["id_produto"],
        "id_vendedor": random.randint(1, NUM_VENDEDORES),
        "data": (start_date + timedelta(days=random.randint(0, total_days - 1))).date(),
        "qtd": qtd,
        "desconto": desconto,
        "status_venda": status
    })

df_vendas = pd.DataFrame(vendas)

# SALVAR CSVs na subpasta generated/
df_clientes.to_csv("generated/clientes.csv", index=False)
df_produtos.to_csv("generated/produtos.csv", index=False)
df_vendedores.to_csv("generated/vendedores.csv", index=False)
df_calendario.to_csv("generated/calendario.csv", index=False)
df_vendas.to_csv("generated/vendas.csv", index=False)

print("✅ Base de dados gerada com sucesso!")
```

## Saída

Gera os seguintes arquivos na subpasta `generated/`:

- `generated/clientes.csv` — 500 registros
- `generated/produtos.csv` — 100 registros
- `generated/vendedores.csv` — 20 registros
- `generated/calendario.csv` — de 2023-01-01 até hoje (~2 anos)
- `generated/vendas.csv` — 20.000 registros

> O período de dados é **dinâmico**: sempre que o script é executado, o calendário se estende até a data atual, mantendo ~2 anos de dados históricos.

## Requisitos

```bash
pip install pandas
```
