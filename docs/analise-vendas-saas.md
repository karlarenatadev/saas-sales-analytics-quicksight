# Análise de Vendas SaaS e Detecção de Anomalias com Amazon QuickSight

## 1. Contexto do Projeto e Desafio

### Cenário
A AnyCompany Consulting recebeu um conjunto de dados de vendas no modelo SaaS (Software as a Service) de um cliente. O objetivo era transformar dados brutos armazenados em arquivos CSV em **insights acionáveis** capazes de orientar decisões estratégicas de vendas e marketing.

### Meu Papel
Analista de Dados / Desenvolvedor(a) BI responsável por estruturar a ingestão de dados, construir visualizações analíticas e investigar padrões de comportamento de compra.

### Desafio Analítico
Criar um dashboard interativo chamado **Sales Overview**, capaz de responder perguntas estratégicas como:

- Como as vendas evoluíram ao longo do tempo?  
- Quais setores geram maior receita?  
- Existe sazonalidade nas vendas?  
- Existem eventos atípicos (anomalias) no faturamento?

---

## 2. Ferramentas e Tecnologias Utilizadas

### Amazon QuickSight
Ferramenta de Business Intelligence utilizada para:

- Ingestão e modelagem do dataset  
- Construção de visualizações interativas  
- Publicação de dashboards analíticos  

Os dados foram carregados no motor analítico **SPICE (Super-fast Parallel In-memory Calculation Engine)**, responsável por otimizar o desempenho das consultas e permitir análises rápidas sobre grandes volumes de dados.

### QuickSight Q (Generative BI)
Utilizado para geração de visualizações complexas através de **linguagem natural**, permitindo explorar os dados de forma mais intuitiva.

### Estatística Descritiva
Aplicação do método **Z-score** para detecção de anomalias no volume de vendas.

---

## 3. Desenvolvimento e Metodologia

O projeto seguiu uma abordagem analítica em quatro etapas principais:

### 1. Ingestão e preparação de dados
O dataset `SaaS-Sales.csv`, contendo registros de vendas entre 2021 e 2024, foi importado para o QuickSight. Durante essa etapa foram realizadas:

- Validação da estrutura dos dados  
- Identificação de dimensões (ex: país, indústria, segmento)  
- Identificação de métricas (ex: valor de vendas)

### 2. Construção das visualizações analíticas
Foram desenvolvidos diferentes tipos de gráficos para explorar dimensões distintas do negócio:

- **Gráfico de linha**: utilizado para analisar a evolução das vendas ao longo do tempo e identificar possíveis tendências ou sazonalidades.  
- **Gráfico de rosca (donut chart)**: utilizado para visualizar a distribuição de receita entre diferentes setores da indústria.

### 3. Exploração com Generative BI
Com o recurso **QuickSight Q**, foi possível gerar visualizações avançadas utilizando linguagem natural. Entre elas:

- **Diagrama de Sankey**: revelando o fluxo de vendas entre segmentos de clientes e regiões.  
- **Mapa geográfico**: mostrando a distribuição global das vendas por país.

Essas visualizações ajudaram a identificar padrões estruturais na base de clientes.

### 4. Investigação estatística de anomalias
Durante a análise do gráfico de tendência mensal foi identificado um pico visual significativo no volume de vendas. Para validar se esse evento era realmente anômalo, foi aplicado um teste estatístico simples utilizando:

**Média ± 2 desvios padrão**

Esse método permite identificar valores que se desviam significativamente do comportamento médio da série temporal.

---

## 4. Principais Descobertas (Insights)

### Visão Geral do Negócio
O volume total de vendas no período analisado foi de aproximadamente **2.297,2K**, sendo o setor **Financeiro** o principal comprador das soluções SaaS. Entre os produtos, o **FinanceHub** se destacou como o principal gerador de receita da empresa.

### Crescimento Consistente
A análise temporal revelou um crescimento sólido ao longo do período analisado, com uma **expansão acumulada de +51,6% entre 2021 e 2024**. Esse comportamento indica aumento consistente na adoção das soluções oferecidas pela empresa.

### Sazonalidade nas vendas
Foi identificado um padrão sazonal claro:

- O **quarto trimestre (Q4)** apresenta desempenho médio **85,7% superior aos demais trimestres**, sugerindo forte influência de fatores como:
  - Fechamento de orçamento corporativo  
  - Renovações contratuais  
  - Decisões estratégicas de final de ano
- Por outro lado, os meses de **janeiro e fevereiro** apresentam historicamente o menor volume de vendas.

### Detecção de anomalia
A análise estatística revelou um evento fora do padrão:

- Em **novembro de 2024**, o faturamento atingiu **R$ 112.326**, representando:  
  - **135% acima da média mensal**  
  - Um **Z-score de +2,57**

Esse valor ultrapassa o limite estatístico de 2 desvios padrão, caracterizando um **outlier significativo na série temporal**.

---

## 5. Recomendações Estratégicas

### Investigar o pico de Novembro de 2024
O evento anômalo pode estar associado a fatores como:

- Campanhas comerciais agressivas  
- Fechamento de contratos enterprise  
- Lançamento de novas funcionalidades no produto FinanceHub

Compreender a causa desse pico pode permitir replicar esse sucesso em períodos futuros.

### Mitigar a baixa tração no início do ano
Como **janeiro e fevereiro** apresentam menor volume de vendas, a empresa poderia implementar estratégias como:

- Campanhas promocionais para renovação antecipada  
- Descontos para contratos anuais  
- Foco em clientes do setor financeiro, que já demonstram maior propensão de compra

### Otimização da estratégia comercial
A análise do **diagrama de Sankey** indica fluxos específicos entre segmentos de clientes e regiões. Isso sugere que a equipe comercial pode priorizar os caminhos de maior rentabilidade, alocando recursos de forma mais eficiente.

---

## 6. Limitações da Análise
Apesar dos insights relevantes, algumas limitações devem ser consideradas:

- O dataset analisado representa apenas um recorte das vendas e não inclui variáveis importantes, como:
  - Custo de aquisição de clientes (CAC)  
  - Churn de clientes  
  - Duração dos contratos  
  - Margens de lucro por produto  

A inclusão dessas métricas permitiria análises ainda mais profundas sobre **rentabilidade e retenção de clientes**.

---

## 7. Conclusão
Este projeto demonstrou como ferramentas modernas de Business Intelligence, como o **Amazon QuickSight**, podem transformar dados brutos em **insights estratégicos acionáveis**. A combinação de visualização de dados, exploração com Generative BI e validação estatística permitiu identificar:

- Padrões de crescimento  
- Sazonalidade nas vendas  
- Um evento anômalo relevante na série temporal

Esses resultados reforçam o papel da análise de dados como suporte fundamental para **tomada de decisão orientada por dados (data-driven decision making)**.