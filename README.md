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

### Etapa 6
## Análises SQL.

### Receita Total 
<img width="1005" height="452" alt="01 - Receita_Total" src="https://github.com/user-attachments/assets/80263771-2e7c-419a-a460-5d80778313eb" />

- Quantidade por status de pagamento
<img width="1021" height="536" alt="02 - Qtde status de pagamento" src="https://github.com/user-attachments/assets/bacf9274-aa8e-42ba-be2b-e1fc640c14d5" />

### Receita por plano
<img width="625" height="637" alt="04 - Receita por plano" src="https://github.com/user-attachments/assets/e8f53bd1-6da9-4a9c-b1d2-9ae5cba53b3b" />

 ### Churn rate
<img width="533" height="503" alt="churn_rate" src="https://github.com/user-attachments/assets/380b8f49-b258-4a76-8df1-f58e02cbbabd" />

### Resultado
- Clientes ativos: 74
- Clientes cancelados: 26
- Churn Rate: 26%

 Insight
 
A análise revelou um churn rate de 26%, indicando que aproximadamente um quarto dos clientes cancelou sua assinatura durante o período analisado.
Em um cenário real de SaaS, essa métrica seria acompanhada continuamente para identificar oportunidades de retenção e redução da perda de receita recorrente.

## Análise de MRR (Monthly Recurring Revenue)
A análise de receita recorrente mensal demonstrou crescimento consistente ao longo do período analisado.

<img width="495" height="861" alt="06 - mrr" src="https://github.com/user-attachments/assets/7913cfb8-66cc-4236-ae63-3c88d88ad0a2" />

### Principais Resultados
* Jan/2024: R$ 1.499,50
* Nov/2024: R$ 11.095,70 (maior valor observado)
* Jul/2025: R$ 10.445,80

### Insights
* Crescimento expressivo da receita recorrente ao longo do período.
* Estabilização do faturamento em 2025, indicando maturidade da base de clientes.
* Pequenas oscilações mensais que poderiam ser investigadas através de análises complementares de churn e inadimplência.

### Conclusão
O negócio apresentou evolução positiva da receita recorrente, alcançando estabilidade operacional ao longo de 2025.

## Análise de Receita por Canal de Aquisição

A análise comparou a receita gerada por clientes adquiridos através dos diferentes canais de marketing.

<img width="566" height="717" alt="07_receita_por_canal" src="https://github.com/user-attachments/assets/388c741e-1161-4986-b050-f41d03bf95f7" />

### Resultados

| Canal        | Clientes |      Receita |
| ------------ | -------: | -----------: |
| Google Ads   |       16 | R$ 77.074,70 |
| Instagram    |       20 | R$ 72.372,30 |
| Indicação    |       15 | R$ 51.977,40 |
| Facebook Ads |       19 | R$ 38.379,40 |
| LinkedIn     |       12 | R$ 27.137,70 |

### Principais Insights
* Google Ads apresentou a maior receita total.
* Instagram trouxe mais clientes, porém com menor geração de receita.
* Existe evidência de diferença no valor médio dos clientes entre os canais.
* O resultado sugere oportunidades para otimização dos investimentos de marketing focando canais com maior retorno financeiro.

## Análise de Ticket Médio

<img width="841" height="592" alt="08 - ticket_medio" src="https://github.com/user-attachments/assets/8fbab8f2-be68-49b0-8ac4-a425cb2846d3" />

| Métrica           |         Valor |
| ----------------- | ------------: |
| Clientes Pagantes |            82 |
| Receita Total     | R$ 266.941,50 |
| Ticket Médio      |   R$ 3.255,38 |

Em média, quanto cada cliente gerou de receita para a empresa?
R$ 3.255,38 por cliente

Lembrando que já descobrimos anteriormente que:
- Enterprise gera a maior parte da receita.
Portanto, existe uma forte chance de que o Ticket Médio esteja sendo puxado para cima pelos clientes Enterprise.

## Análise de Ticket Médio por Plano

<img width="832" height="610" alt="09 - ticket_medio_por_plano" src="https://github.com/user-attachments/assets/b9c61c7d-5046-4287-be9d-62e14d66aa97">

| Plano        | Clientes | Receita Total |    Ticket Médio |
| ------------ | -------: | ------------: | --------------: |
| Enterprise   |       21 | R$ 180.963,80 | **R$ 8.617,32** |
| Business     |       18 |  R$ 49.375,30 | **R$ 2.743,07** |
| Professional |       20 |  R$ 25.674,30 | **R$ 1.283,72** |
| Basic        |       23 |  R$ 10.928,10 |   **R$ 475,13** |

A empresa não depende da quantidade de clientes.
Ela depende da qualidade dos clientes.

O plano Enterprise representa:
apenas 25,6% dos clientes pagantes (21 de 82)
mas aproximadamente 67,8% da receita total

Cada cliente Enterprise vale em média:
R$ 8.617
Enquanto um cliente Basic vale:
R$ 475
Ou seja: 
Um cliente Enterprise vale aproximadamente 18 vezes mais
que um cliente Basic.

## Análise de LTV (LIFETIE VALUE)

<img width="845" height="567" alt="10 - ltv_medio" src="https://github.com/user-attachments/assets/ca7ecc46-00cc-4673-be36-778ee6041e1a" />

## Análise de Churn por Plano

<img width="576" height="615" alt="12 - churn_por_plano" src="https://github.com/user-attachments/assets/afd301dc-3e06-401d-8acf-dc5ae889eb74" />

Ao analisar a taxa de cancelamento por plano, identifiquei que o plano Professional apresentou retenção superior aos demais. 
Embora a distribuição dos dados fosse equilibrada, a análise sugere um possível melhor alinhamento entre preço e valor percebido pelos clientes desse plano.

## Análise de Receita por Estado

### São Paulo lidera a receita:

·	Maior base de clientes (21) 

·	Maior receita total (R$ 76,8 mil) 

Isso sugere que São Paulo é atualmente o principal mercado da empresa.

### Rio de Janeiro é surpreendente: 

Apesar de ter apenas 16 clientes, o RJ possui o maior valor gerado por cliente.

- Clientes mais qualificados
- 
- Maior adesão aos planos premium
- 
- Melhor retenção

### Paraná merece atenção:

·	Menor receita total

·	Menor receita por cliente

R$ 2.494 por cliente contra mais de R$ 3.600 no RJ

Possíveis hipóteses:

·	Maior concentração de clientes Basic 

·	Menor retenção 

·	Menor adoção de planos avançados 

### Insight Executivo
Se eu estivesse apresentando esse projeto para uma empresa SaaS, diria:
Embora São Paulo seja o principal mercado em volume de receita, o Rio de Janeiro apresenta o maior valor médio por cliente, 
indicando uma possível concentração de clientes mais rentáveis. Por outro lado, o Paraná apresenta menor monetização da base,
sugerindo oportunidade para estratégias de upsell e expansão de planos premium.

## Análise Top 10 Clientes por Receita

<img width="546" height="827" alt="14 - Top_10_clientes_por_Receita" src="https://github.com/user-attachments/assets/e4622aeb-5636-479d-ac1f-430993e7a466" />

### O Plano Enterprise domina completamente

Os 10 clientes mais valiosos pertencem ao plano Enterprise.

Isso confirma o que já havíamos identificado anteriormente:
- Enterprise gera mais receita
- Enterprise possui maior ticket médio
- Enterprise concentra os clientes de maior valor

### Forte concentração de receita

O cliente líder:
João Martins→ R$ 17.496,50
Enquanto vários outros clientes estão na faixa de:
·	R$ 9 mil 
·	R$ 10 mil 
·	R$ 11 mil 
Isso sugere que João Martins possui uma permanência maior ou maior volume de pagamentos realizados.
Em uma empresa real, esse cliente seria classificado como:
+ Cliente Estratégico

### Risco de concentração

Se os Top 10 representam uma parcela muito grande da receita total, a empresa pode estar exposta a riscos.
Exemplo:
·	Se João Martins cancelar amanhã... 
·	Quanto a receita mensal será impactada? 

## Análise por Segmento de Empresa

<img width="937" height="703" alt="15 - Receita_por_Segmento_de_Empresa" src="https://github.com/user-attachments/assets/cb73f767-93f1-46ac-9a61-906f818ca4d4" />

### Educação é o segmento mais valioso
Não apenas em receita total.
Mas também em receita por cliente.
Cada cliente do segmento Educação gera mais do que o dobro da receita de um cliente do segmento Tecnologia. 

### Insight Executivo
A análise por segmento revelou que empresas do setor de Educação representam o grupo mais rentável da base de clientes, 
apresentando a maior receita total (R$ 91.419,60) e o maior valor médio por cliente (R$ 4.353,31). 
Em contrapartida, empresas de Tecnologia apresentaram o menor valor médio gerado por cliente, indicando diferenças significativas de monetização entre segmentos. 

## Análise Churn por Segmento de Empresa

O segmento Educação representa atualmente o principal gerador de receita da empresa, porém também apresenta a maior taxa de cancelamento da base (40%),
indicando um risco relevante para a sustentabilidade do faturamento futuro. 

✅ Maior receita
❌ Maior churn (40%)

Marketing é o "Segmento dos Sonhos" 

Receita Total     R$ 58.278
Clientes          21
Churn             14,29%

Temos:
✅ Boa receita
✅ Boa base de clientes
✅ Menor churn do negócio

### Análise rápida

🟢 Alta Receita + Baixo Churn
* Marketing
Segmento ideal para crescimento

* Financeiro
Base saudável e estável.

🟡 Alta Receita + Alto Churn
* Educação
Gera muito dinheiro, mas precisa de ações de retenção.

* E-commerce
Possui potencial de crescimento.

🔴 Baixa Receita + Alto Churn
* Tecnologia
Possui menor valor gerado e alta taxa de cancelamento.
É o segmento mais problemático da base.


