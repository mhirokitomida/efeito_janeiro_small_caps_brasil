# 📊 Efeito Janeiro no Brasil: Small vs Large Caps por Liquidez

👉 **[🔗 Acesse o Dashboard Interativo (GitHub Pages)](https://mhirokitomida.github.io/efeito_janeiro_small_caps_brasil/)**

---

## 📌 Sobre o projeto

Este projeto investiga a existência do **efeito janeiro** no mercado acionário brasileiro, analisando se ações de **menor liquidez** tendem a apresentar desempenho superior às de **maior liquidez** na janela entre **meados de dezembro e o final de janeiro**.

Como a base histórica não utiliza market cap consolidado para todo o período, foi usada a **liquidez média de novembro** como **proxy de tamanho**, permitindo classificar os ativos em grupos comparáveis e testar se o comportamento da virada do ano se destaca em relação a outras janelas do calendário.

---

## 🎯 Objetivo

Avaliar, de forma quantitativa e estatística, se existe evidência de que:

- 📌 Ações de menor liquidez (**small caps proxy por liquidez**)  
- 📌 Superam ações de maior liquidez (**large caps proxy por liquidez**)  

na janela clássica associada ao **efeito janeiro**.

Além disso, o projeto busca responder uma pergunta mais forte:

- 📌 A janela **dezembro→janeiro** é apenas positiva por si só  
- ou ela é de fato **superior às janelas de controle** ao longo do ano?

---

## 🧠 Metodologia

A análise foi construída em etapas estruturadas:

---

### 1. Construção da base

- Dados históricos de preços ajustados (**close_adj**)  
- Volume financeiro (**volume_fin**)  
- Padronização temporal e limpeza de dados  
- Criação de colunas auxiliares (ano, mês etc.)

---

### 2. Proxy de tamanho via liquidez

Para cada ano da amostra:

- cálculo da **liquidez média de novembro** por ativo  
- classificação anual dos ativos em grupos extremos:
  - **Bottom 30%** → small caps proxy por liquidez  
  - **Top 30%** → large caps proxy por liquidez  
  - **40% centrais** → excluídos para aumentar o contraste

---

### 3. Definição das janelas

#### 📌 Janela principal
- Entrada: primeiro pregão após **15 de dezembro**
- Saída: último pregão útil de **janeiro**

#### 📌 Janelas de controle
- Março → Abril  
- Abril → Maio  
- Julho → Agosto  
- Agosto → Setembro  

---

### 4. Cálculo de retornos

Para cada janela e ano:

- 📈 Retorno por ativo  
- 📊 Retorno médio das carteiras (**equal-weight**)  
- 📉 Spread: **Small – Large**

---

### 5. Testes estatísticos

A análise estatística foi dividida em duas camadas:

#### 📌 Testes contra zero
- **Teste t unilateral**
- **Teste de permutação**
- objetivo: avaliar se o spread de cada janela é positivo

#### 📌 Teste central da hipótese
- **Wilcoxon pareado unilateral**
- **Permutação pareada**
- comparação de **dezembro→janeiro** com cada janela de controle, **ano a ano**
- aplicação de **ajuste de Holm** para múltiplas comparações

---

## 📈 Principais Resultados

- A janela **dezembro→janeiro apresentou o maior spread médio** entre todas as janelas analisadas  
- O spread da janela principal foi **positivo em cerca de dois terços dos anos da amostra**  
- Nos testes **contra zero**, a janela principal apresentou **evidência estatística favorável**  
- Na comparação direta com as janelas de controle, a evidência ficou **mais fraca**  
- A melhor comparação ocorreu contra **março→abril**, mas **sem robustez após ajuste de Holm**  

👉 Isso sugere que:

> Existe uma **evidência econômica plausível** de efeito janeiro no Brasil,  
> mas não uma evidência estatística forte o suficiente para afirmar que a janela dezembro→janeiro é de forma robusta superior às janelas de controle.

---

## 📊 Visualizações

O projeto inclui um relatório HTML interativo com:

- Comparação direta de retornos por janela (**Small vs Large**)  
- Distribuição do spread por janela (**boxplots**)  
- Evolução temporal do spread  
- Histograma do spread em **dezembro→janeiro**  
- Gráficos do **spread médio por janela**  
- Comparação pareada entre **dezembro→janeiro** e janelas de controle  
- Tabelas interativas com filtros, ordenação e scroll  

---

## 🌐 Visualização do projeto

👉 https://mhirokitomida.github.io/efeito_janeiro_small_caps_brasil/

---

## ⚠️ Observações importantes

- A análise utiliza **liquidez como proxy de tamanho**, e não market cap observado diretamente  
- O estudo identifica **associação empírica**, não causalidade  
- A amostra é relevante, mas ainda limitada em termos históricos  
- Parte da magnitude observada é sensível a episódios específicos da amostra  
- O ano de **2020** teve peso relevante no resultado agregado  
- A janela de 2020 corresponde a **dez/2019 → jan/2020**, anterior ao período mais crítico da pandemia  

---

## 🧠 Principais Aprendizados

- Existe uma **diferença econômica relevante** entre ações de menor e maior liquidez na virada do ano  
- A janela **dezembro→janeiro** apresentou o **maior spread médio** do estudo  
- O efeito possui suporte estatístico quando avaliado **contra zero**  
- A superioridade frente às janelas de controle **não ficou robusta**  
- O resultado é sensível a anos específicos, especialmente **2020**  
- A liquidez se mostrou uma **proxy prática e funcional** para segmentação, mas não equivale a market cap direto  

---

## 🏁 Conclusão

O estudo aponta para um padrão **economicamente interessante** e compatível com a hipótese do efeito janeiro no Brasil.

Ações de menor liquidez **podem, sim, apresentar desempenho superior** no início do ano, e a janela **dezembro→janeiro** foi a mais forte entre as janelas analisadas. No entanto, quando a análise exige uma comparação mais rigorosa com janelas de controle ao longo do ano, essa superioridade **não se mostra estatisticamente robusta** após ajuste para múltiplas comparações.

Em termos práticos, a leitura mais correta é:

> ações de menor liquidez **podem** superar ações de maior liquidez na virada do ano,  
> mas esse comportamento deve ser tratado como uma **evidência plausível com robustez estatística moderada**,  
> e não como uma regularidade definitiva do mercado brasileiro.
