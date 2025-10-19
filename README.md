# Sprint 13 – Predição de Rotatividade de Clientes da Model Fitness

## Descrição do Projeto

Neste projeto, meu objetivo foi analisar os dados de clientes da rede de academias **Model Fitness** e desenvolver estratégias para **prever a rotatividade** e reduzir perdas de clientes.  

Com base nos dados de perfis, frequência de visitas e histórico de compras, realizei uma **análise exploratória**, construí **modelos de previsão** e segmentei clientes em **agrupamentos** para identificar padrões de comportamento.

---

## Dados Utilizados

Arquivo principal: `gym_churn_us.csv`  

Campos incluídos:

- **Churn** — indica se o cliente saiu no mês seguinte.  
- **Dados do mês anterior:** `gender`, `Near_Location`, `Partner`, `Promo_friends`, `Phone`, `age`, `Lifetime`.  
- **Dados de frequência, compras e status atual:** `Contract_period`, `Month_to_end_contract`, `Group_visits`, `Avg_class_frequency_total`, `Avg_class_frequency_current_month`, `Avg_additional_charges_total`.  

---

## Passos do Projeto

### Passo 1: Baixar e Preparar os Dados
- Carreguei o arquivo `gym_churn_us.csv`.  
- Verifiquei tipos de dados, valores ausentes e consistência das colunas.  

### Passo 2: Análise Exploratória de Dados (AED)
- Explorei estatísticas básicas (`describe()`) e identifiquei valores ausentes.  
- Comparei características médias entre clientes que ficaram e clientes que saíram.  
- Criei histogramas, distribuições e matriz de correlação para identificar padrões nos dados.  

### Passo 3: Construção de Modelos de Predição
- Defini a variável alvo como `Churn`.  
- Dividi os dados em conjuntos de **treinamento** e **validação** usando `train_test_split()`.  
- Treinei dois modelos de classificação binária:
  1. **Regressão logística**
  2. **Floresta aleatória (Random Forest)**  
- Avaliei **acurácia, precisão e sensibilidade** dos modelos e comparei seus resultados.  
- Identifiquei o modelo mais eficiente para prever rotatividade de clientes.  

### Passo 4: Agrupamento de Clientes
- Padronizei os dados e construí um dendrograma usando `linkage()` para estimar o número de agrupamentos.  
- Apliquei **K-means** com `n=5` para segmentar os clientes.  
- Analisei características médias de cada agrupamento e distribuições de atributos.  
- Calculei a **taxa de rotatividade** por grupo, identificando quais clusters são mais propensos a sair e quais são leais.  

### Passo 5: Conclusões e Recomendações
- Baseado nos resultados, identifiquei **grupos-alvo prioritários** para retenção.  
- Sugeri medidas práticas para diminuir a rotatividade, como:
  - Promoções personalizadas para grupos com alto risco de churn.  
  - Incentivos para participação em sessões em grupo ou atividades específicas.  
  - Contato ativo e acompanhamento de clientes que não frequentam a academia regularmente.  
- Apresentei padrões gerais sobre comportamento de clientes e insights para melhorar a interação e fidelização.  

---

## Avaliação

Meu projeto será avaliado com base em:

- Qualidade da análise exploratória e entendimento dos dados.  
- Construção e avaliação dos modelos preditivos.  
- Clareza na criação dos agrupamentos e interpretação das características.  
- Capacidade de tirar conclusões e fornecer recomendações acionáveis.  
- Organização do código, comentários claros e formatação de notebook.  

