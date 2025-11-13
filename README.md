# 🏀 Análise NBA – O que o Sacramento Kings precisa fazer para voltar aos Playoffs?

---

## 🧠 Descrição Geral

Este projeto foi desenvolvido como parte do curso **Data Science & Machine Learning (Tera)** e tem como objetivo aplicar técnicas de **análise de dados** e **machine learning** para entender o que a franquia **Sacramento Kings** precisa melhorar para voltar a disputar os **Playoffs da NBA**, após um longo período sem classificações.

O estudo combina **análise estatística**, **modelagem preditiva** e **storytelling esportivo**, unindo a paixão pelo basquete à ciência de dados.

---

## 🎯 Objetivos do Projeto

- Identificar os fatores técnicos de jogo que mais influenciam a classificação de uma equipe aos playoffs.  
- Aplicar modelos de machine learning para prever se uma equipe tem ou não perfil de playoffs.  
- Propor insights e recomendações práticas para o **Sacramento Kings**, com base em dados reais.  
- Criar uma aplicação interativa (via **Streamlit**) que permita simular resultados.

---

## 📊 Contexto

A **NBA (National Basketball Association)** é a principal liga de basquete do mundo, composta por 30 franquias (29 nos EUA e 1 no Canadá).  
A participação nos **playoffs** é não apenas um marco esportivo, mas também **financeiro**, pois aumenta receitas de ingressos, patrocínios e valorização de marca.

O **Sacramento Kings** é a franquia há mais tempo fora dos playoffs (desde 2006), e o desafio proposto foi descobrir **o que tecnicamente o time precisa melhorar** para quebrar esse jejum histórico.

---

## 🗂️ Dados e Fontes

Os dados foram obtidos via **web scraping do site oficial da NBA (nba.com)**, abrangendo as **últimas 10 temporadas regulares** da **Conferência Oeste**.

**Variáveis principais:**
- `W` — Vitórias  
- `L` — Derrotas  
- `WIN%` — Percentual de vitórias  
- `PTS` — Pontos  
- `FG%` — Aproveitamento de arremessos de quadra  
- `3P%`, `3PA`, `3PM` — Aproveitamento e volume de arremessos de 3 pontos  
- `DREB`, `REB` — Rebotes defensivos e totais  
- `BLK`, `BLKA` — Bloqueios realizados e sofridos  
- `Playoffs` — Variável target (1 = classificado, 0 = não classificado)

---

## 🔎 Metodologia e Etapas do Projeto

1. **Coleta de Dados** – Web scraping do site da NBA.  
2. **Análise Exploratória (EDA)** – Estudo de correlação entre variáveis e “Playoffs”.  
3. **Formulação de Hipóteses** – Criação de hipóteses baseadas em variáveis técnicas (ex: FG%, 3P%, DREB, BLK).  
4. **Comparativos** – Análise entre o Sacramento Kings e as médias dos sextos colocados das últimas 10 temporadas (posição limite para classificação direta).  
5. **Modelagem Preditiva** – Aplicação de técnicas de **Classificação (Regressão Logística, Árvore de Decisão e Random Forest)**.  
6. **Avaliação de Modelos** – Uso de métricas **Precision, Recall e F1 Score** para determinar o melhor modelo.  
7. **Simulações** – Testes com substituição de jogadores e projeção de impacto nas variáveis críticas.  
8. **Criação de Aplicação Streamlit** – Interface interativa para explorar resultados e simulações.

---

## 📈 Principais Insights

- As variáveis **FG%**, **3P%**, **3PA**, **3PM**, **DREB** e **BLKA** têm forte influência na classificação.  
- O **Sacramento Kings** tem aproveitamento similar aos sextos colocados em quase todas as métricas, **exceto em rebotes defensivos e volume de arremessos de 3 pontos**.  
- O problema do time **não é o aproveitamento**, mas **a baixa quantidade de tentativas de 3 pontos**.  
- Melhorar a performance em **rebotes e bolas de 3** pode aumentar significativamente a chance de classificação.

---

## 🤖 Modelagem

Modelos testados:
- **Regressão Logística**  
- **Árvore de Decisão**  
- **Random Forest**

Melhor desempenho obtido com:
- **Modelo:** Regressão Logística  
- **Variáveis:** `FG%`, `3P%`, `3PA`, `3PM`, `BLKA`, `DREB`  
- **Métricas:**  
  - Precision: **0.64**  
  - Recall: **0.70**  
  - F1 Score: **0.67**

> A exclusão da variável “Vitórias” evitou *overfitting*, priorizando fatores técnicos e não resultados já consequentes.

---

## 🧮 Conclusões

O modelo desenvolvido ajuda a:
- **Compreender os fatores técnicos** que levam um time aos playoffs.  
- **Simular cenários** para ajustar variáveis-chave.  
- **Apoiar decisões estratégicas** de reforço no elenco (ex: contratar jogadores com melhor aproveitamento em 3 pontos e rebotes).

Com o modelo, o Sacramento Kings pode **priorizar contratações mais assertivas** e **monitorar indicadores técnicos críticos** durante a temporada.

---

## 🚀 Aplicação Interativa

🔗 [Acesse o dashboard interativo no Streamlit](https://projeto-nba-tera.streamlit.app/)

A aplicação permite simular o desempenho da equipe ao alterar variáveis técnicas e observar o impacto na probabilidade de classificação aos playoffs.

---

## 🧰 Ferramentas e Tecnologias Utilizadas

- **Linguagem:** Python  
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- **Modelagem:** Regressão Logística, Árvore de Decisão, Random Forest  
- **Visualização:** Matplotlib / Seaborn  
- **Aplicação:** Streamlit  
- **Ambiente:** Google Colab  
- **Versionamento:** Git e GitHub  
- **Documentação:** Markdown

---

## 📁 Estrutura Recomendada do Repositório

