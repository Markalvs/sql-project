# Projetos Desenvolvidos

## Projeto 1 — Dashboard de Acompanhamento de Vendas

Projeto desenvolvido para criação de indicadores de desempenho comercial utilizando SQL aplicado à análise de negócios.

### Objetivos

Construir um dashboard analítico contendo métricas de vendas, conversão e comportamento dos clientes.

### Indicadores desenvolvidos

- Leads gerados por período
- Quantidade de vendas
- Receita total
- Taxa de conversão
- Ticket médio
- Estados com maior volume de vendas
- Marcas mais vendidas
- Lojas com maior desempenho
- Dias da semana com maior volume de visitas

### Consultas realizadas

#### Receita, Leads, Conversão e Ticket Médio

Indicadores calculados mensalmente:

- Leads (#)
- Vendas (#)
- Receita
- Conversão (%)
- Ticket médio

```sql
WITH leads AS (

SELECT

DATE_TRUNC('month',visit_page_date) AS mes,

COUNT(*) AS leads

FROM sales.funnel

GROUP BY mes

)

SELECT *

FROM leads;
```

---

#### Estados com maior volume de vendas

```sql
SELECT

estado,

COUNT(*) AS vendas

FROM sales.customers

GROUP BY estado

ORDER BY vendas DESC;
```

---

#### Marcas que mais venderam

```sql
SELECT

brand,

COUNT(*)

FROM sales.products

GROUP BY brand

ORDER BY COUNT(*) DESC;
```

---

#### Lojas com maior desempenho

```sql
SELECT

store_name,

COUNT(*)

FROM sales.stores

GROUP BY store_name;
```

---

#### Dias da semana com mais visitas

```sql
SELECT

EXTRACT(DOW FROM visit_page_date),

COUNT(*)

FROM sales.funnel

GROUP BY 1;
```

---

### Competências Aplicadas

- Business Intelligence
- Indicadores Comerciais
- Funções agregadas
- JOINs
- Subqueries
- Conversão de métricas
- KPIs
- Análise temporal
- SQL Analítico

---
