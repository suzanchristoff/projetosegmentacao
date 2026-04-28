# Segmentação de Clientes — El Mercado

Projeto de análise e segmentação de clientes utilizando a técnica **RFM (Recency, Frequency, Monetary)**, desenvolvido para responder a questões estratégicas de negócio de uma empresa fictícia do setor de varejo.

---

## Contexto e Objetivo

A empresa **El Mercado** enfrentava desafios relacionados a:

- Mudanças nas preferências dos consumidores
- Dificuldades de fidelização de clientes
- Manutenção e crescimento da receita de vendas
- Necessidade de estratégias de marketing mais direcionadas

O projeto buscou responder a essas questões por meio de análise exploratória de dados e segmentação comportamental da base de clientes.

---

## Ferramentas e Tecnologias

| Ferramenta | Uso |
| --- | --- |
| Google Sheets (Spreadsheets) | Processamento, limpeza e análise dos dados |
| Looker Studio | Visualização e construção do dashboard |

---

## Etapas do Projeto

### 1. Processamento e Preparação da Base de Dados

- **Importação:** dados divididos em 3 tabelas distintas, importados via função `IMPORTRANGE`
- **Dados nulos:** identificados com `COUNTBLANK`; os 24 clientes sem informação de salário receberam o valor da mediana; 7 transações sem ID de cliente foram desconsideradas por irrelevância estatística
- **Duplicatas:** 9 IDs duplicadas na tabela de resumo de compras foram removidas
- **Outliers:** identificados em idade e salário; mantidos e agrupados em faixas de valores
- **União das tabelas:** realizada com `PROCV` e `QUERY`
- **Variáveis criadas:** `tem_filhos`, `total_compras`, `idade`, `faixa_etária`, `faixa_salarial`, `recency`, `frequency`, `monetary`, `segmentos`, `score_R`, `score_F`, `score_M`, `media_score_FM`

### 2. Análise Exploratória dos Dados

- Agrupamento por variáveis categóricas
- Visualização por gráficos exploratórios
- Cálculo de medidas descritivas (média e mediana)
- Cálculo de quintis para segmentação

### 3. Segmentação RFM

A técnica RFM avalia cada cliente em três dimensões:

| Dimensão | Descrição |
| --- | --- |
| **Recency (R)** | Há quantos dias foi a última compra |
| **Frequency (F)** | Quantas vezes o cliente realizou compras |
| **Monetary (M)** | Valor total investido nas compras |

Os clientes foram divididos em **5 grupos via quintis**, recebendo notas de 1 a 5 em cada dimensão. A combinação das notas definiu o segmento de cada cliente.

---

## Dashboard

O dashboard foi construído no **Looker Studio** com duas páginas:

**Página 1 — Visão Geral**

- Receita total do período
- Total de transações e de clientes
- Ticket médio por transação
- Participação de cada segmento no faturamento
- Produtos mais consumidos por segmento
- Novos clientes registrados por mês

**Página 2 — Perfil Socioeconômico**

- Exploração do perfil dos clientes por segmento

---

## Principais Resultados

- **Clientes campeões** representam **28%** do faturamento, seguidos de **clientes em risco (26%)** e **clientes fiéis (21%)** — juntos, mais de 70% da receita total
- **Vinho e carne** são os produtos mais consumidos em todos os segmentos
- Média de **93 novos clientes por mês**, com pouca variação
- **Queda no número de transações** nos últimos 6 meses analisados
- Clientes **sem filhos** têm ticket médio **2x maior** do que clientes com filhos
- **89% dos clientes** têm ensino superior ou pós-graduação
- Faixa etária predominante: **40 a 69 anos**
- Canal físico representa **58% das vendas**

---

## Recomendações

**Clientes Campeões e Fiéis**

> Recompensar com programas de fidelidade, descontos exclusivos e experiências personalizadas. Incentivar indicações e investigar os fatores que impulsionam sua lealdade à marca.
> 

**Clientes em Risco**

> Investir em pós-venda e pesquisas de satisfação para entender o afastamento. Oferecer produtos similares aos que consumiam anteriormente para reengajá-los.
> 

---

## Autora

**Suzan Christoff**

Analista de Dados | E-commerce & Varejo

Projeto desenvolvido individualmente
