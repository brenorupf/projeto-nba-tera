# 🏀 Análise NBA – O que o Sacramento Kings precisa fazer para voltar aos Playoffs?

---

Este projeto foi desenvolvido durante o curso de **Data Science & Machine Learning da Tera** (2º semestre de 2022) em conjunto com os colegas Caio Rodrigues, Miguel Rocha e Vitor Soier. 

---

## 🎯 Objetivos do Projeto

 Treinar e simular todo o ciclo de um projeto na vida real:

- Definir a estrutura (contexto, problema de negócio, impacto e desenho da solução);
- Trabalhar com os dados (fazer web scraping, análise exploratória e modelagem);
- Criar a interface;
- Pensar os próximos passos;
- Apresentar para os experts da Tera, alunos e facilitadores no Demoday.

---

## 📊 Contexto

O Sacramento Kings é uma das 30 franquias associadas à NBA, situada na cidade de Sacramento, na Califórnia, e pertence à conferência oeste. Seu último (e único) título foi em 1951 (das equipes campeãs da NBA, é a que possui o maior jejum). Na época em que fizemos o projeto, dentre todas as equipes, é a que **estava há mais tempo fora da disputa dos playoffs** (desde a temporada 2005/2006, ou seja, havia 16 anos). Sendo até então, o maior período de uma franquia fora dos playoffs em toda a história da NBA, superando o Los Angeles Clippers que ficou de fora dos playoffs entre as temporadas 1977 a 1991 (14 anos).

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

