# IA & Sensores — Machine Learning aplicado a dados de sensores

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![LACOP-UFF](https://img.shields.io/badge/LACOP--UFF-blue?style=flat-square)](https://www.uff.br/)

Repositório desenvolvido no contexto do **Workshop de Inteligência Artificial e Sensores**, realizado pelo LACOP — Universidade Federal Fluminense.

O projeto explora a aplicação de **Machine Learning a dados provenientes de sensores**, passando por preparação de dados, seleção de variáveis, treinamento de modelos, avaliação de desempenho e interpretação dos resultados.

## Projetos

### 01 — Previsão da Temperatura da Sala em 1 Hora

Modelo de regressão para prever a temperatura futura de um ambiente a partir de dados de sensores e características da sala.

**Modelo:** Random Forest Regressor
**Métrica:** MAE
**Resultado:** redução do erro de aproximadamente **61%** em relação ao baseline.

→ [`01-temperatura-umidade`](01-temperatura-umidade)

---

### 02 — Previsão do Consumo de Energia

Modelo de regressão para estimar o consumo horário de energia a partir de informações temporais, ambientais e de ocupação.

**Modelo:** Random Forest Regressor
**Métrica:** MAE
**Resultado:** redução do erro de aproximadamente **87%** em relação ao baseline.

→ [`02-consumo-energia`](02-consumo-energia)

---

### 03 — Reconhecimento de Atividade Humana

Classificação de atividades humanas utilizando dados de acelerômetros posicionados na região da lombar e da coxa.

**Modelo:** Random Forest Classifier
**Features:** seis eixos de aceleração (`back_x/y/z` e `thigh_x/y/z`)
**Experimentos:** participante individual e grupo de participantes.

O experimento com grupo de participantes apresentou **97,2% de acurácia**, enquanto o experimento individual com S022 apresentou **95,8%**.
→ [`03-reconhecimento-atividade`](03-reconhecimento-atividade)

> **Nota:** os resultados do projeto de reconhecimento de atividade ainda passam por uma etapa de validação do mapeamento dos rótulos do dataset antes de serem considerados resultados definitivos.

## Visão geral dos resultados

| Projeto          | Problema      | Modelo        |              Resultado |
| ---------------- | ------------- | ------------- | ---------------------: |
| Temperatura      | Regressão     | Random Forest |     **61% menos erro** |
| Energia          | Regressão     | Random Forest |     **87% menos erro** |
| Atividade humana | Classificação | Random Forest | **97,2% de acurácia*** |

* Resultado do experimento com grupo de participantes; sujeito à validação final do mapeamento dos rótulos.

## Tecnologias

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Jupyter Notebook / Google Colab**
* Machine Learning supervisionado
* Análise e visualização de dados

## Competências demonstradas

Este repositório reúne experiências práticas com:

* Preparação e exploração de dados;
* Dados provenientes de sensores;
* Regressão e classificação supervisionadas;
* Engenharia e seleção de features;
* Treinamento e avaliação de modelos;
* Comparação com modelos baseline;
* Interpretação de métricas e matriz de confusão;
* Análise crítica das limitações dos experimentos.

## Contexto

O trabalho foi iniciado em **25 de setembro de 2026** como parte do Workshop de Inteligência Artificial e Sensores do LACOP/UFF.

Além do desenvolvimento dos modelos, o projeto envolve a análise e discussão dos resultados com os demais participantes. Está prevista uma atividade presencial no **LACOP, no campus da UFF, em 16 de outubro de 2026**, para apresentação e discussão dos resultados obtidos.

## Estrutura do repositório

```text
├── README.md
├── requirements.txt
│
├── projetos/
│   ├── 01-temperatura-e-umidade/
│   ├── 02-consumo-de-energia/
│   └── 03-reconhecimento-de-atividade/
│
├── dados/
│   └── amostras/
│
├── documentos/
```

Os READMEs de cada projeto apresentam os objetivos, metodologia, resultados e limitações específicas de cada experimento.

## Observações

Os experimentos foram desenvolvidos com finalidade acadêmica e exploratória. Os resultados apresentados não devem ser interpretados como modelos prontos para produção.

## Sobre o projeto

**Workshop de Inteligência Artificial e Sensores**
**LACOP — Universidade Federal Fluminense**
**Início:** 25/09/2026
