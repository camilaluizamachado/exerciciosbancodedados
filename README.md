# 🗄️ Exercícios Práticos de SQL — MySQL

> Coleção de listas de exercícios práticos de Banco de Dados utilizando **MySQL**, desenvolvida como material de apoio para a disciplina de Banco de Dados da graduação em Engenharia de Computação.

---

## 📋 Sobre o Repositório

Este repositório reúne exercícios práticos organizados por nível de dificuldade e tema, todos aplicados sobre o banco de dados `loja_virtual` — um sistema realista de e-commerce com tabelas de clientes, produtos, pedidos, fornecedores, estoque e pagamentos. O objetivo é desenvolver progressivamente as habilidades de consulta, manipulação e administração de dados com SQL.

---

## 🗂️ Estrutura

```
.
├── exercicios_sql_basico.html         # Lista 01 — SQL Básico (Q01–Q30)
├── exercicios_sql_intermediario.html  # Lista 02 — SQL Intermediário (Q01–Q25)
└── README.md
```

---

## 📚 Listas de Exercícios

### Lista 01 — SQL Básico

**30 questões** cobrindo os fundamentos de consulta e manipulação de dados.

| Seção | Tópicos |
|---|---|
| 01 — SELECT e Filtragem | `SELECT`, `WHERE`, `LIKE`, `BETWEEN`, `IN`, `IS NULL`, `DISTINCT` |
| 02 — Ordenação e Limitação | `ORDER BY`, `LIMIT`, `OFFSET` |
| 03 — Funções de Agregação | `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`, `GROUP BY`, `HAVING` |
| 04 — Junções (JOINs) | `INNER JOIN`, `LEFT JOIN`, colunas calculadas, subquery simples |
| 05 — Consultas de Revisão | `TOP N`, ticket médio, produtos nunca vendidos, faturamento mensal, `UNION` básico |

---

### Lista 02 — SQL Intermediário

**25 questões** aprofundando recursos avançados do MySQL.

| Seção | Tópicos |
|---|---|
| 01 — Subconsultas | Subconsultas correlacionadas, `EXISTS`, `NOT EXISTS`, `IN`, segundo maior valor |
| 02 — CASE WHEN e Funções | `CASE WHEN`, `TIMESTAMPDIFF`, `DAYOFWEEK`, `DATE_FORMAT`, `UPPER`, `LOWER`, `CONCAT`, `IFNULL` |
| 03 — UNION e Conjuntos | `UNION`, `UNION ALL`, simulação de `INTERSECT`, pivô condicional |
| 04 — Views | `CREATE VIEW`, views atualizáveis, `WITH CHECK OPTION` |
| 05 — Transações e Integridade | `START TRANSACTION`, `COMMIT`, `ROLLBACK`, `SAVEPOINT`, `LAST_INSERT_ID`, `UPDATE` em lote |
| 06 — Índices e Performance | `CREATE INDEX`, `CREATE UNIQUE INDEX`, `EXPLAIN`, análise de full table scan |

---

## 🏗️ Schema do Banco de Dados

O banco `loja_virtual` simula o back-end de um sistema de e-commerce. As principais tabelas são:

```
cliente          — dados cadastrais dos clientes
endereco         — endereços vinculados aos clientes
produto          — catálogo de produtos com estoque e preços
categoria        — categorias de produtos
fabricante       — fabricantes dos produtos
fornecedor       — fornecedores da loja
pedido_venda     — cabeçalho dos pedidos de clientes
item_pedido_venda — itens de cada pedido de venda
pedido_compra    — pedidos de compra junto a fornecedores
item_pedido_compra — itens de cada pedido de compra
forma_pagamento  — formas de pagamento disponíveis
cidade           — cidades para endereçamento
```

---

## 🚀 Como Usar

### Pré-requisitos

- **MySQL 8.0+** (ou MariaDB 10.5+)
- MySQL Workbench, DBeaver ou outro cliente de sua preferência

### Configuração

1. Clone ou baixe o repositório.
2. Crie e selecione o banco de dados:
   ```sql
   CREATE DATABASE loja_virtual;
   USE loja_virtual;
   ```
3. Execute o script de criação das tabelas (`schema.sql`) e, em seguida, o de dados de exemplo (`seed.sql`), se disponíveis.
4. Abra as listas de exercícios no navegador e pratique as queries no seu cliente MySQL.

---

## 🎯 Níveis de Dificuldade

Cada questão é classificada com uma das três etiquetas abaixo:

| Etiqueta | Descrição |
|---|---|
| 🟢 **Fácil** | Conceitos fundamentais — SELECT, filtragem simples, ordenação |
| 🟡 **Médio** | JOINs, agregações, subqueries, funções de data e string |
| 🔴 **Avançado** | Subconsultas correlacionadas, pivôs, transações com SAVEPOINT, views atualizáveis |

---

## 💡 Dicas de Estudo

- Leia o enunciado com atenção antes de escrever qualquer linha de SQL.
- Tente resolver sem olhar as dicas — elas estão lá para desbloquear, não para substituir o raciocínio.
- Para as questões de transação, sempre teste o `ROLLBACK` antes do `COMMIT`.
- Use `EXPLAIN` para analisar o plano de execução das suas queries e entender o impacto dos índices.

---

Material acadêmico para uso educacional. Distribuição livre para fins de estudo.
