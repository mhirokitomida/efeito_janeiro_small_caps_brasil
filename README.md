# 📊 Efeito Janeiro no Brasil: Small vs Large Caps por Liquidez

👉 **[🔗 Acesse o Dashboard Interativo (GitHub Pages)](https://mhirokitomida.github.io/efeito_janeiro_small_caps_brasil/)**

---

## 📌 Sobre o projeto

Este projeto investiga a existência do **efeito janeiro** no mercado acionário brasileiro, analisando se ações de **menor liquidez** tendem a apresentar desempenho superior às de maior liquidez na janela entre **meados de dezembro e o final de janeiro**.

Como proxy para tamanho das empresas, foi utilizada a **liquidez média de negociação**, permitindo classificar os ativos em grupos comparáveis mesmo na ausência de market cap histórico completo.

---

## 🎯 Objetivo

Avaliar, de forma quantitativa e estatística, se existe evidência de que:

- 📌 Ações de menor liquidez (small caps proxy)  
- 📌 Superam ações de maior liquidez (large caps proxy)  

na janela clássica associada ao **efeito janeiro**.

Além disso, o projeto busca verificar se esse comportamento é **específico de janeiro** ou também aparece em outras janelas do ano.

---

## 🧠 Metodologia

A análise foi construída em quatro etapas principais:

---

### 1. Construção da base

- Dados históricos de preços ajustados (**close_adj**)  
- Volume financeiro (**volume_fin**)  
- Padronização temporal e limpeza de dados  
- Criação de colunas auxiliares (ano, mês, etc.)

---

### 2. Proxy de tamanho via liquidez

- Cálculo da **liquidez média de novembro** para cada ativo  
- Classificação anual dos ativos:
  - Bottom 30% → **Small caps proxy**
  - Top 30% → **Large caps proxy**
  - 40% intermediários → excluídos

---

### 3. Definição das janelas

#### 📌 Janela principal:
- Entrada: primeiro pregão após **15 de dezembro**
- Saída: último pregão de **janeiro**

#### 📌 Janelas de controle:
- Março → Abril  
- Abril → Maio  
- Julho → Agosto  
- Agosto → Setembro  

---

### 4. Cálculo de retornos e testes

Para cada janela e ano:

- 📈 Retorno por ativo  
- 📊 Retorno médio das carteiras (equal-weight)  
- 📉 Spread: **Small – Large**

Testes aplicados:

- 📊 **Teste t unilateral** (spread > 0)  
- 🔁 **Teste de permutação** (robustez empírica)  
- 📈 Estatísticas descritivas (média, mediana, dispersão, consistência)

---

## 📈 Principais Resultados

- A janela **dezembro→janeiro apresentou o maior spread médio** entre todas as janelas analisadas  
- O efeito é **economicamente relevante**, com small caps superando large caps  
- A evidência estatística é **moderada**, com p-valores próximos de 5%  
- Outras janelas também apresentaram spreads positivos, mas **menos consistentes e menos significativos**

👉 Isso sugere que:

> Existe um padrão econômico consistente, mas não uma evidência estatística forte o suficiente para afirmar que o efeito é totalmente robusto ao longo do tempo.

---

## 📊 Visualizações

O projeto inclui um relatório HTML interativo com:

- Comparação de retornos por janela  
- Distribuição do spread (boxplot)  
- Evolução temporal do spread  
- Histograma do efeito em janeiro  
- Tabelas interativas com filtros e ordenação  

---

## 🌐 Visualização do projeto

👉 https://mhirokitomida.github.io/efeito_janeiro_small_caps_brasil/

---

## ⚠️ Observações importantes

- A análise utiliza **liquidez como proxy de tamanho**, e não market cap  
- Os resultados são **sensíveis a valores extremos**, especialmente o ano de 2020  
- A janela de 2020 corresponde a **dez/2019 → jan/2020**, anterior ao período mais crítico da pandemia  
- O estudo identifica **associação estatística, não causalidade**  
- A amostra, embora relevante, ainda é relativamente limitada em termos históricos  

---

## 🧠 Principais Aprendizados

- Existe **diferença econômica consistente** entre ações de menor e maior liquidez  
- O efeito janeiro apresentou o **maior spread médio** entre as janelas analisadas  
- A evidência estatística é **moderada**, próxima ao limite de significância  
- O resultado é **sensível a outliers**, especialmente o ano de 2020  
- Outras janelas apresentam efeitos positivos, mas **menos robustos**  
- A liquidez se mostrou uma **proxy prática e funcional** para segmentação  

---

## 🏁 Conclusão

O estudo reforça uma ideia importante:

> Ações menos líquidas podem, sim, apresentar desempenho superior no início do ano —  
> **mas esse comportamento não é totalmente estável nem estatisticamente robusto em todos os períodos.**
