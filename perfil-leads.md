## Projeto 2 — Perfil dos Leads

Projeto focado em segmentação e análise exploratória do comportamento dos leads.

### Objetivos

Identificar características demográficas, profissionais e comportamentais dos usuários.

### Análises realizadas

- Distribuição por gênero
- Status profissional
- Faixa etária
- Faixa salarial
- Classificação dos veículos visitados
- Idade média dos veículos
- Modelos mais visitados
- Marcas mais acessadas

### Consultas desenvolvidas

#### Distribuição por gênero

```sql
SELECT

genero,

COUNT(*) AS leads

FROM clientes

GROUP BY genero;
```

---

#### Status profissional

```sql
SELECT

status_profissional,

COUNT(*) AS leads

FROM clientes

GROUP BY status_profissional;
```

---

#### Faixa etária

```sql
SELECT

faixa_etaria,

COUNT(*)

FROM clientes

GROUP BY faixa_etaria;
```

---

#### Faixa salarial

```sql
SELECT

faixa_salarial,

COUNT(*)

FROM clientes

GROUP BY faixa_salarial;
```

---

#### Classificação dos veículos

```sql
CASE

WHEN idade_veiculo <= 2
THEN 'Novo'

ELSE 'Seminovo'

END
```

---

#### Veículos mais visitados

```sql
SELECT

brand,

model,

COUNT(*) AS visitas

FROM sales.products

GROUP BY brand,model;
```

---

### Competências Aplicadas

- Segmentação de clientes
- Análise comportamental
- Regras de negócio
- Classificação de dados
- Tratamento de datas
- CTEs
- CASE WHEN
- SQL Analítico
- Data Analytics

---

## Tecnologias Utilizadas

- SQL
- PostgreSQL
- pgAdmin

---

## Conceitos Aplicados

- SQL para Negócios
- Business Intelligence
- Data Analytics
- KPIs
- Modelagem Analítica
- Tratamento de Dados
- Segmentação de Clientes
- Consultas Analíticas
- Dashboards
- Análise Exploratória
