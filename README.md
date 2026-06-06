# Projeto SaaS Analytics - Churn, Receita e Retenção

## Objetivo

Desenvolver um projeto completo de análise de dados utilizando SQL Server para analisar métricas de um negócio SaaS.

## Tecnologias

- SQL Server
- SSMS
- Git
- GitHub

## Estrutura do Projeto

### Dimensões

- dim_clientes
- dim_planos

### Fatos

- fato_assinaturas
- fato_pagamentos

### Métricas Analisadas

- Churn Rate
- MRR (Monthly Recurring Revenue)
- Receita por Plano
- Receita por Canal de Aquisição
- Retenção de Clientes
- Inadimplência

### Modelo de Dados

<img width="1322" height="613" alt="star_schema" src="https://github.com/user-attachments/assets/a8aa5844-2a64-4ad6-b1ec-6c8e0d9131a4" />

## Etapas do Projeto

### Etapa 1
Criação do banco de dados.

### Etapa 2
Modelagem dimensional.

### Etapa 3
Geração de clientes.
<img width="1005" height="700" alt="Criaçao de dbo dim_clientes" src="https://github.com/user-attachments/assets/94d6e6c7-4c84-4421-89b0-46ef326a0189" />
<img width="1272" height="737" alt="inserindo dados" src="https://github.com/user-attachments/assets/1699ec3a-8078-49b2-87c2-fd54dada878f" />

### Etapa 4
Geração de assinaturas.
<img width="998" height="552" alt="criação fato assinaturas" src="https://github.com/user-attachments/assets/64063e12-016f-4cb4-8348-577ff5278fb7" />
<img width="996" height="637" alt="iNSERINDO ASSINATURAS" src="https://github.com/user-attachments/assets/aa7ff600-dd8b-48ad-91b1-08eaccef7d5a" />

### Etapa 5
Geração de pagamentos.
<img width="1005" height="593" alt="criação tabela fato_pagamentos" src="https://github.com/user-attachments/assets/921c4548-c245-454b-a3e0-f20ede6f507f" />
<img width="756" height="748" alt="criando dados de pagamentos" src="https://github.com/user-attachments/assets/4d3103a5-7c28-4b70-bfda-a5ed260d11a6" />

###  6
Análises SQL.

- Receita Total 
<img width="1005" height="452" alt="01 - Receita_Total" src="https://github.com/user-attachments/assets/80263771-2e7c-419a-a460-5d80778313eb" />

- Quantidade por status de pagamento
<img width="1021" height="536" alt="02 - Qtde status de pagamento" src="https://github.com/user-attachments/assets/bacf9274-aa8e-42ba-be2b-e1fc640c14d5" />

- Receita por plano
<img width="625" height="637" alt="04 - Receita por plano" src="https://github.com/user-attachments/assets/e8f53bd1-6da9-4a9c-b1d2-9ae5cba53b3b" />

- Churn rate
<img width="533" height="503" alt="churn_rate" src="https://github.com/user-attachments/assets/380b8f49-b258-4a76-8df1-f58e02cbbabd" />

### Resultado

- Clientes ativos: 74
- Clientes cancelados: 26
- Churn Rate: 26%

 * Insight *

A análise revelou um churn rate de 26%, indicando que aproximadamente um quarto dos clientes cancelou sua assinatura durante o período analisado.
Em um cenário real de SaaS, essa métrica seria acompanhada continuamente para identificar oportunidades de retenção e redução da perda de receita recorrente.



