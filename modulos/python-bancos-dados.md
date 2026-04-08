# Python e Bancos de Dados — Módulo 2

> Manipulação de dados e persistência com Python e SQL.

## Informações do Módulo

- **Aulas:** 8 (de 4h cada)
- **Carga horária:** 32h
- **Cursos que utilizam este módulo:** [Fullstack Python](cursos/fullstack-python.md) · [Data Science](cursos/data-science.md)

---
## Aulas
### Aula 1 — Python Intermediário: Strings, Arquivos e Módulos

**Conteúdo:**
- Strings avançadas: slicing, métodos (`.upper()`, `.lower()`, `.strip()`, `.split()`, `.join()`, `.replace()`)
- f-strings: formatação moderna de texto
- Leitura e escrita de arquivos (`open()`, `read()`, `write()`, `with`)
- Modos de abertura: `r`, `w`, `a`, `rb`, `wb`
- Trabalhando com arquivos CSV (leitura manual)
- Módulos padrão: `os`, `sys`, `math`, `random`, `datetime`
- Importando módulos: `import`, `from ... import`, aliases
- `pip`: instalando pacotes externos

**Exercícios práticos (escolha um):**
1. Processador de texto: ler arquivo .txt, contar palavras, linhas e caracteres, salvar relatório
2. Gerador de CSV: criar arquivo CSV com dados de alunos (nome, nota, situação) a partir de inputs
3. Calendário mensal: usar `datetime` para exibir o mês atual com destaque no dia de hoje

**Recursos:**
- [Real Python - File I/O](https://realpython.com/read-write-files-python/)
- [Python Docs - datetime](https://docs.python.org/pt-br/3/library/datetime.html)
- [Python Docs - os](https://docs.python.org/pt-br/3/library/os.html)

**Tarefas de casa (escolha uma ou mais):**
1. Script de renomear arquivos: ler pasta, adicionar prefixo ou sufixo em todos os arquivos
2. Gerador de relatório de despesas: ler CSV de gastos, calcular total por categoria
3. Diário digital: salvar entradas com data/hora em arquivo .txt
4. Analisador de texto: contar frequência de cada palavra em um arquivo .txt
5. Agenda de tarefas: salvar e ler tarefas em arquivo .txt (CRUD básico)

**Tempo:** 4h (1h teoria + 2h prática + 1h correção)

---

### Aula 2 — Orientação a Objetos (OOP)

**Conteúdo:**
- O que é OOP e por que usar
- Classes e objetos: `class`, `__init__()`, `self`
- Atributos de instância e de classe
- Métodos: definindo comportamentos
- Encapsulamento: `_protegido` e `__privado`
- Herança: `class Filho(Pai)`
- `super()`: chamando método do pai
- Polimorfismo: sobrescrevendo métodos
- Método `__str__()` e `__repr__()`
- Dataclasses (introdução)

**Exercícios práticos (escolha um):**
1. Sistema bancário: classes `ContaBancaria` com métodos depositar, sacar, ver saldo; `ContaPoupança` herdando com rendimento
2. Catálogo de veículos: classe `Veiculo` com marca, modelo, ano; subclasses `Carro` e `Moto` com atributos extras
3. Sistema de alunos: classe `Aluno` com nome, notas (lista), método calcular_media(), aprovado()

**Recursos:**
- [Real Python - OOP](https://realpython.com/python3-object-oriented-programming/)
- [Python Docs - Classes](https://docs.python.org/pt-br/3/tutorial/classes.html)

**Tarefas de casa (escolha uma ou mais):**
1. Biblioteca de livros: classes `Livro`, `Autor`, `Biblioteca` com métodos de busca e empréstimo
2. RPG simples: classes `Personagem`, `Guerreiro`, `Mago` com atributos e métodos de combate
3. Loja virtual: classes `Produto`, `Carrinho`, `Pedido` com cálculo de total e desconto
4. Geometria: classes `Circulo`, `Retangulo`, `Triangulo` herdando de `Forma`, todos com área e perímetro
5. Sistema de RH: `Funcionario`, `Gerente` (com bônus), `Estagiario` (com carga horária)

**Tempo:** 4h (1h teoria + 2h prática + 1h desafio)

---

### Aula 3 — Tratamento de Exceções e Dicionários

**Conteúdo:**
- Erros comuns em Python: `TypeError`, `ValueError`, `KeyError`, `IndexError`
- `try`, `except`, `else`, `finally`
- Capturando exceções específicas
- Levantando exceções: `raise`
- Criando exceções customizadas
- Dicionários: criação, acesso, modificação
- Métodos de dicionário: `.keys()`, `.values()`, `.items()`, `.get()`, `.update()`
- Dict comprehension: `{k: v for k, v in ...}`
- Tuplas: imutabilidade e uso prático
- Sets: conjuntos e operações (união, interseção)

**Exercícios práticos (escolha um):**
1. Validador de dados: receber input do usuário e validar com try/except (idade entre 0-150, email com @, telefone só números)
2. Contador de frequência: receber lista de palavras, usar dicionário para contar quantas vezes cada uma aparece
3. Agenda com dicionário: CRUD de contatos usando dicionário como banco (nome → telefone)

**Recursos:**
- [Real Python - Exceptions](https://realpython.com/python-exceptions/)
- [Python Docs - Dicts](https://docs.python.org/pt-br/3/tutorial/datastructures.html#dictionaries)

**Tarefas de casa (escolha uma ou mais):**
1. Parser de notas: ler arquivo CSV de alunos, tratar erros de formatação, gerar relatório
2. Tradutor de palavras: dicionário PT→EN, interface de busca com tratamento de KeyError
3. Analisador de vendas: dicionário de vendas por produto, calcular mais vendido, menos vendido, total
4. Inventário de jogos: dicionário de jogos com quantidade, atualizar estoque com validação de erros
5. Organizador de contatos: ler arquivo .txt de contatos, parsear para dicionário, buscar e editar

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 4 — SQL Básico

**Conteúdo:**
- O que é um banco de dados relacional
- SQL vs NoSQL (quando usar cada)
- Tabelas, linhas e colunas
- Tipos de dados SQL: `INTEGER`, `TEXT`, `REAL`, `BOOLEAN`, `DATE`
- `CREATE TABLE` e `DROP TABLE`
- `INSERT INTO` — inserindo dados
- `SELECT` — consultando dados
- `WHERE` — filtrando resultados
- `ORDER BY` — ordenando
- `LIMIT` — limitando resultados
- Instalando e usando DB Browser for SQLite (ferramenta visual)

**Exercícios práticos (escolha um):**
1. Banco de alunos: criar tabela alunos (id, nome, email, nota), inserir 5 registros, consultar por situação
2. Catálogo de filmes: tabela com título, diretor, ano, gênero — inserir 10 filmes, filtrar por gênero e ordenar por ano
3. Inventário: tabela de produtos (id, nome, categoria, preço, quantidade), consultas de busca e ordenação

**Recursos:**
- [SQLite Tutorial](https://www.sqlitetutorial.net/)
- [DB Browser for SQLite](https://sqlitebrowser.org/)
- [W3Schools SQL](https://www.w3schools.com/sql/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar banco de dados de uma biblioteca: tabelas livros, autores, empréstimos
2. Sistema de RH: tabelas funcionários, departamentos, cargos com consultas de relatório
3. Playlist musical: tabelas músicas, artistas, álbuns — consultar músicas por artista
4. Banco de receitas: tabelas receitas, ingredientes, categorias — consultar por categoria
5. Agenda de eventos: tabelas eventos, participantes — filtrar por data e categoria

**Tempo:** 4h (1h teoria + 2h prática + 1h exercícios)

---

### Aula 5 — SQL Avançado: Joins e Agregações

**Conteúdo:**
- Relacionamentos: chave primária (`PRIMARY KEY`) e chave estrangeira (`FOREIGN KEY`)
- `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`
- `GROUP BY` e funções de agregação: `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`
- `HAVING`: filtrando grupos
- Subconsultas (subqueries)
- `UPDATE` — atualizando registros
- `DELETE` — deletando registros
- Índices: o que são e por que usar
- Modelagem básica: normalização

**Exercícios práticos (escolha um):**
1. Sistema de pedidos: tabelas clientes, produtos, pedidos, itens_pedido — relatório de total por cliente com JOIN
2. Escola: tabelas alunos, disciplinas, notas — média de cada aluno, disciplina com mais reprovações
3. E-commerce: tabelas produtos, categorias, vendas — faturamento por categoria, produto mais vendido

**Recursos:**
- [SQLBolt - Interactive SQL](https://sqlbolt.com/)
- [Mode SQL Tutorial](https://mode.com/sql-tutorial/)
- [Lucidchart - ER Diagram](https://www.lucidchart.com/)

**Tarefas de casa (escolha uma ou mais):**
1. Criar modelo ER de um sistema hospitalar (pacientes, médicos, consultas, exames)
2. Sistema de delivery: consultas de pedidos por status, tempo médio de entrega, entregador mais eficiente
3. Rede social simplificada: usuários, posts, curtidas — posts mais curtidos, usuários mais ativos
4. Estoque com movimentações: entrada/saída de produtos, saldo atual por produto, alertas de estoque baixo
5. Relatório de vendas: top 5 produtos, vendas por mês, ticket médio por categoria

**Tempo:** 4h (1h teoria + 2h prática + 1h modelagem)

---

### Aula 6 — SQLite com Python

**Conteúdo:**
- Módulo `sqlite3` do Python
- Conectando ao banco: `sqlite3.connect()`
- Criando cursor: `conn.cursor()`
- Executando SQL: `.execute()`, `.executemany()`
- Buscando resultados: `.fetchone()`, `.fetchall()`, `.fetchmany()`
- `commit()` e `rollback()`
- Parametrização de queries (evitando SQL Injection)
- Context managers: `with sqlite3.connect() as conn`
- Gerenciando banco como módulo Python
- Criando funções CRUD reutilizáveis

**Exercícios práticos (escolha um):**
1. CRUD de tarefas com SQLite: criar banco, inserir, listar, atualizar status, deletar — tudo em Python
2. Agenda de contatos com SQLite: nome, email, telefone — buscar por nome, editar, deletar
3. Gerenciador de estoque: produto, quantidade, preço — adicionar, remover, listar abaixo de X unidades

**Recursos:**
- [Python Docs - sqlite3](https://docs.python.org/pt-br/3/library/sqlite3.html)
- [Real Python - SQLite](https://realpython.com/python-sqlite-sqlalchemy/)

**Tarefas de casa (escolha uma ou mais):**
1. Biblioteca com SQLite: CRUD de livros, empréstimo/devolução, listar disponíveis
2. Controle financeiro: tabelas receitas e despesas, saldo, filtro por mês
3. Agenda escolar: cadastro de alunos, disciplinas e notas com consultas de relatório
4. CLI de gerenciamento de projetos: criar projeto, adicionar tarefas, marcar como concluído
5. Sistema de senhas (local): salvar site, usuário e senha criptografada (usar hashlib)

**Tempo:** 4h (1h teoria + 2h prática + 1h projeto)

---

### Aula 7 — SQLAlchemy (ORM)

**Conteúdo:**
- O que é ORM e por que usar
- Instalando SQLAlchemy: `pip install sqlalchemy`
- Engine e Session
- Declarative Base: definindo modelos como classes Python
- Criando tabelas com `Base.metadata.create_all()`
- CRUD com ORM: `session.add()`, `session.query()`, `session.delete()`
- Filtros: `.filter()`, `.filter_by()`, `.first()`, `.all()`
- Relacionamentos: `relationship()`, `ForeignKey`
- Migrações básicas com Alembic (introdução)
- Comparativo: SQLAlchemy vs sqlite3 puro

**Exercícios práticos (escolha um):**
1. Refatorar o CRUD de tarefas (aula 6) usando SQLAlchemy com modelos e relacionamentos
2. Sistema de blog: modelos `User`, `Post`, `Comment` com relacionamentos 1:N
3. E-commerce simples: modelos `Product`, `Category`, `Order`, `OrderItem` com relacionamentos

**Recursos:**
- [SQLAlchemy Docs](https://docs.sqlalchemy.org/)
- [Real Python - SQLAlchemy](https://realpython.com/python-sqlalchemy/)

**Tarefas de casa (escolha uma ou mais):**
1. Migrar um projeto SQLite puro para SQLAlchemy
2. Sistema de escola: modelos `Aluno`, `Disciplina`, `Nota` com relacionamento ManyToMany
3. Criar API script que usa SQLAlchemy para popular banco com dados de um CSV
4. Biblioteca ORM: modelos `Livro`, `Autor`, `Emprestimo` com todas as queries necessárias
5. Pesquisar sobre Alembic e criar primeira migração em um projeto existente

**Tempo:** 4h (1h teoria + 2h prática + 1h comparativo)

---

### Aula 8 — Projeto: Sistema CRUD Completo

**Conteúdo:**
- Revisão dos conceitos do módulo
- Planejamento: modelagem do banco de dados
- Estrutura do projeto Python
- Implementando CRUD completo com SQLAlchemy
- Interface CLI interativa com menus
- Validação de dados com try/except
- Testes básicos de funcionalidade
- Documentação e README

**Exercício prático:**
1. Construir sistema completo com CLI interativa: pelo menos 2 entidades relacionadas, CRUD completo, validação, persistência com SQLAlchemy

**Sugestões de projeto:**
1. Sistema de biblioteca (livros, autores, empréstimos)
2. Gerenciador de tarefas por projeto
3. Controle de despesas pessoais por categoria
4. Cadastro de alunos com notas e relatórios

**Desafio extra:**
1. Exportar relatórios para CSV
2. Adicionar seed script para popular banco com dados fictícios
3. Implementar busca com múltiplos filtros

**Recursos:**
- [Faker - Gerar dados fictícios](https://faker.readthedocs.io/en/master/)

**Tarefas de casa (escolha uma ou mais):**
1. Incrementar o projeto com nova funcionalidade não planejada
2. Criar seed script que popula o banco com 50+ registros usando Faker
3. Escrever README completo com diagrama ER e instruções de uso
4. Adicionar exportação para CSV dos dados cadastrados
5. Criar testes básicos para as funções CRUD

**Tempo:** 4h (30min revisão + 3h projeto + 30min apresentação)

---

## Projeto do Módulo

Ao final do módulo, o aluno entrega:

1. Sistema CRUD com pelo menos 2 tabelas relacionadas
2. Persistência com SQLAlchemy
3. Interface CLI com menus
4. Validação de dados
5. README com instruções e diagrama ER

---

## Próximo módulo

→ [Rest Api Git](modulos/rest-api-git.md)

---

#modulo #python #sql #sqlite #sqlalchemy #oop
